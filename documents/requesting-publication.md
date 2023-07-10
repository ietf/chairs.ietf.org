---
title: Quick Guide: Requesting publication of a WG I-D
description: How to requests publication of a Working Group Internet-Draft
published: true
date: 2023-07-10T19:33:55.868Z
tags: 
editor: markdown
dateCreated: 2023-07-10T19:24:55.289Z
---

This quick guide was created by [Mirja Kühlewind](https://datatracker.ietf.org/person/mirja.kuehlewind@ericsson.com)

Before following this guide, login into IETF Datatracker and navigate to the main page for the Internet-Draft (I-D) to be submitted. If you are chair for the WG in which the document is being considered, you should see the views shown below. Much of the information will already be automatically entered in the IETF Datatracker, but you will need to double check some of the details:

0. Check that the “Intended RFC status” is set to the intended status as agreed by the working group and indicated in the document header

1. Assign a [document shepherd](https://chairs.ietf.org/en/documents/document-shepherding) if one isn't already set.
> Note: this can be done any time after the working group has adopted a document, so a shepherd may already be assigned),
{.is-info}
- Click on edit next to “Document shepherd”
- Enter one email address of the Datatracker account of the shepherd, select the right address, and click save (the shepherd needs to have a datatracker account)

2. Set the WG state to: "In WG Last Call":
- Click on edit next to “WG state”
- Click on “In WG Last Call” button
- Optionally enter “weeks in this state” or comments
- Click "Submit": this will send an email to the I-D authors, WG chairs, and the responsible Area Director

3. Send (manually) an email to the working group mailing list indicating the start of the Working Group Last Call period, which is usually 2 weeks (see [RFC2418](https://www.rfc-editor.org/rfc/rfc2418.html)). If any Intellectual Property Rights (IPRs) are disclosed for this I-D, consider noting it in the WG last call.

4. Wait until the Working Group Last Call (WGLC) deadline expires.

5. When the WGLC deadline expires, review all comments received and send an email that a) closes the WGLC and b) announces the outcome of the WGLC. E.g. the document is:
- ready to be submitted to the IESG with a request for publication, 
- will be ready with specific revisions, or 
- is not ready for certain reasons.

If the working group decided to not go ahead, (re-)set the “WG State” to “WG Document”. You may consider adding a tag, if you think it’s useful for your group.

6. If a revised version of the I-D is needed after WGLC, you may put the document into “Waiting for WG chairs to go ahead” with the tag “Revised I-D Needed - Issue raised by WGLC”-> This will trigger an email to the authors, shepherd, chairs, and AD.

7. Change the “WG State” to “WG Consensus: Waiting for Write-Up” -> This will trigger an email to the authors, shepherd, chairs, and AD.

8. When the final version of the I-D is submitted, ask document shepherds (usually by email) to prepare and upload the write-up. Shepherds can do that by clicking the edit button next to “Shepherd write-up”; the following form already contains the write-up template.

9. When the Write-up is uploaded in the Datatracker by the shepherd, review the write-up and request publication
- Push the “Submit to IESG for publication“ button at the bottom on the far right 

Review all information on the next page and click “send”
-> This will trigger a mail to the AD, chairs, secretariat, shepherd, as well as WG mailing list

10. If you have a milestone that indicates submission of this document to the IESG, mark the milestone as done. On the working group page, click on “Edit milestones”
- Click on the milestone you want to change and tick the “Resolved” box, then click “Review changes”
- On the next page you can review your changes again before you save them. Don’t forget to click the save button! -> This will trigger a mail to the chairs, AD, and WGmailing list.

And in only 10 steps (which may take multiple weeks) you have submitted your WG I-D to the IESG for publication! Read this IESG statement to understand what happens as the IESG considers the document.: 



1. Click the "Request review" button.
![screenshot_2023-03-07_at_17.25.34.png](/screenshot_2023-03-07_at_17.25.34.png)
1. Select the Early review type and the team(s) you would like to request review from. 
1. Specify a deadline and add any additional comments that might be of use to the reviewing team.
![screenshot_2023-03-07_at_17.23.19.png](/screenshot_2023-03-07_at_17.23.19.png)