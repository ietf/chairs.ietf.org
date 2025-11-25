---
title: First-time subscription
description: Explanation of what happens when someone subscribes to an IETF mailing list for the first time
published: true
date: 2025-11-25T00:50:49.665Z
tags: 
editor: markdown
dateCreated: 2025-11-25T00:48:58.838Z
---

# First time sending to the IETF
All email sent to IETF mailing lists goes through the mail gatekeeper, postconfirm, which does the following:
* Challenge/response for first time subscribers
* Builds the global allowlist
* Manages DMARC processing

## Challenge response for first-time subscribers
When postconfirm sees an address for the first time, it sends the following challenge message:
```plaintext
Welcome to the Internet Engineering Task Force (IETF) and its companion organizations, 
the Internet Architecture Board (IAB) and Internet Research Task Force (IRTF).

We have received an email from your email address, "$sender", sent to "$recipient", 
with the subject
'$[msg["subject"]]'

As this is the first time we have received an email from "$sender", your email will not 
be delivered until you confirm that you sent it by replying to this message with the 
confirmation code in the subject line intact. You do not need to write anything in your 
reply.

Please note that by replying to this message, you agree to follow IETF processes and 
policies, a reminder of which is given in the IETF Note Well 
(https://www.ietf.org/about/note-well/), and in doing so you consent to the use of your 
information in accordance with the IETF/IRTF/IAB Privacy Statement 
(https://www.ietf.org/privacy-statement/).

If you did not send this message or do not want it delivered, you do not need to do 
anything.

If you have any questions, please forward this email to $[conf.admin_address] and we 
will be happy to assist.

-- 
The IETF (including the IAB, IRTF and RFC Editor)
https://www.ietf.org/

(For internal use only: $filename)
```

This serves the following purpose:
1. Explains who we are
2. Authenticates subscription by the sender email address
3. Explains where to find our policies
4. Records agreement to IETF Policies through an affirmative action
5. Provides a support path for problems/queries.

## Global allowlist
Once an address has responded to the postconfirm challenge, it is entered into a global allowlist of address that can send to IETF mailing lists. 

This feature is provided in order to meet this requirement from the [IESG Statement on Spam Control on IETF Mailing Lists](https://datatracker.ietf.org/doc/statement-iesg-iesg-statement-on-spam-control-on-ietf-mailing-lists-20080414/)

> IETF mailing lists MUST provide a mechanism for legitimate technical participants to bypass moderation, challenge-response, or other techniques that would interfere with a prompt technical debate on the mailing list without requiring such participants to receive list traffic. 

The global allowlist is automatically added to the configuration of every mailing list.  This MUST NOT be removed by list admins - if removal is detected then it will automatically be re-added.

# Mailman initial subscription
When someone subscribes to a mailing list, they receive the following message confirming their subscription (Note the IRTF version is longer as it uses the IRTF Note Well):

```plaintext
Welcome to the Internet Engineering Task Force (IETF), founded in 1986, the premier 
standards development organization for the Internet.

You are now subscribed to the "$display_name" mailing list at $domain, which is 
described as:

 —-
$info
 —-

For this list:
 - Send messages to the list at $listname
 - Manage your subscription at https://mailman3.$domain/mailman3/lists/$listname/ (may 
require you to create an account)
 - Archive at https://mailarchive.ietf.org/arch/browse/$short_listname/ 
 - Contact the owners at $owner_email

Please note:

By participating in the IETF you agree to follow IETF processes and policies 
[https://www.ietf.org/policies/]. This Note Well is a reminder of some of those 
policies.

* IETF participants are expected to behave in a professional manner and extend respect 
and courtesy to their colleagues at all times (see RFC 7154: IETF Guidelines for 
Conduct [https://www.rfc-editor.org/rfc/rfc7154.html] and IETF Anti-Harassment Policy 
[https://datatracker.ietf.org/doc/statement-iesg-ietf-anti-harassment-policy-
20131103/]). If you have any concerns about behavior, please contact the Ombudsteam 
[https://www.ietf.org/contact/ombudsteam/] who have a duty of confidentiality and 
extensive powers to act, as set out in RFC 7776: IETF Anti-Harassment Procedures 
[https://www.rfc-editor.org/rfc/rfc7776.html].

* If you are aware that any IETF contribution (as defined in RFC 5378: Rights 
Contributors Provide to the IETF Trust [https://www.rfc-editor.org/rfc/rfc5378.html]) 
is covered by patents or patent applications that are owned or controlled by you, your 
employer or your sponsor, you must disclose that fact, or not participate in the 
discussion (see RFC 8179: Intellectual Property Rights in IETF Technology 
[https://www.rfc-editor.org/rfc/rfc8179.html]).

* For detailed process information consult RFC 2026: Internet Standards Process 
[https://www.rfc-editor.org/rfc/rfc2026.html] and RFC 2418: IETF Working Group 
Guidelines and Procedures [https://www.rfc-editor.org/rfc/rfc2418.html] and updates to 
those.

* The IETF routinely makes public written, audio, video, and photographic records of 
IETF activities, including your personal information as set out in the IETF Privacy 
Statement [https://www.ietf.org/privacy-statement/]. 

For advice, please talk to Working Group chairs or Area Directors.

You can find out more about the IETF, IRTF and IAB at:

	www.ietf.org, www.irtf.org, www.iab.org

For all other questions, please contact us at support@ietf.org.
```

This serves the following purpose:
1. Explains the purpose of the list, using the long description
2. Explains how to use the list
3. Explains how to manage the subscription
4. Includes the full Note Well as a reminder of the policies
5. Provides a support path for problems/queries.
