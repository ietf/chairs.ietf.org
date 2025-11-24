---
title: Managing mailing lists
description: Information, tools, and resources for managing IETF working group mailing lists
published: true
date: 2025-11-24T22:58:14.949Z
tags: 
editor: markdown
dateCreated: 2021-12-14T18:14:00.690Z
---

# Key background information for list admins
## Mailman admin interface - Postorius
IETF mailing lists are operated using Mailman 3, which provides its own admin interface called **Postorius**.  Mailing list admins need to use Postorius to manage their lists. 

The IETF organizes list management into three domains:
* https://mailman3.ietf.org/ for IETF lists
* https://mailman3.irtf.org/ for IRTF lists
* https://mailman3.rfc-editor.org/ for RFC Editor lists

To access a specific list, you can go through the main page above, or using a direct URL of the form:

`https://mailman3.[DOMAIN]/mailman3/lists/[LISTADDRESS]/`

For example, for the list `admin-discuss@ietf.org`, this is:

`https://mailman3.ietf.org/mailman3/lists/admin-discuss@ietf.org/`

General information on using the admin interface can be found on the [IETF Website](https://www.ietf.org/participate/lists/#managing).

## Accounts
To use Postorius you will need an account. You can create an account on any of the front pages (above) using the **Sign up** menu item.  Only one account is needed - it will automatically apply to the other domains above.

Currently, the account name you use for logging in to Postorius is independent of any other IETF system, so please use any account name that you wish. 

## Admin permissions
List admin permissions are linked to email addresses. To active your permissions, you will need to [link your email address(es)](https://www.ietf.org/participate/lists/#managing) to that account

If you have an account linked to your email address and do not have the permissions to a list that you expect, then please contact support@ietf.org.

* To see all the lists for which are an **owner**:  `https://mailman3.[DOMAIN]/mailman3/lists/?role=owner`
* To see all the lists for which are a **moderator**:  `https://mailman3.[DOMAIN]/mailman3/lists/?role=moderator`

## Integration with Datatracker
### Working group lists
The Datatracker page for a WG lists the **mailing lists for that WG** and the list archives. The general form of the Datatracker link is as follows, where `[WGNAME]` is the WG abbrevation:

`https://datatracker.ietf.org/group/[WGNAME]/about/`

When a change is made in Datatracker, such as a WG Chair changing, there is currently a manual process that updates Mailman.

Additionally, addresses for group chairs, ADs and other expansions are provided at:

`https://datatracker.ietf.org/group/[WGNAME]/email/`

### Non-WG lists
There is a single Datatracker page that lists all [non-WG lists](https://datatracker.ietf.org/list/nonwg) but this only links to the Mailman page for that list.

Datatracker does not record any other information about non-WG lists.

## Members vs non-members
If you need to find a specific address to manage on your list then remember to check **both** the list of **members** and **non-members** for your list. 

The reason that non-members exist is due to interactions with the [global allowlist](/postconfirm-dmarc-global-allowlist). When a post is sent to a list from an address that it is not a member but this message is accepted because that address is on the global allowlist, that address is then automatically added as a non-member of the mailing list.

Both members and non-members can post to a list (unless moderated) but only members receive messages sent to the list.

# Common management tasks
## Spam control
Control of spam is centralised in the IETF mail system and while most spam is blocked, some may occasionally get through to a list. 

If you have a problematic spammer that you want to block and you are certain that they are only a spammer then:
1. (*optional*) Temporarily add them to the ban list (**Ban list** on the list admin menu) or put them into moderation.
2. Contact support@ietf.org to have them blocked at the mail server.
3. (*optional*) If spam messages have made it through to the mail archive and you want those messages not to be visible, then please contact support@ietf.org with links to the messages.

## Handling of moderated messages
Messages can be held in moderaton for a number of reasons, not just because the address is set to moderation. The moderation queue for a specific list can be found under **Held messages** on the top menu:

![mailman3-moderation_options-new.png](/mailman3-moderation_options-new.png)

or using this direct URL:

`https://mailman3.[DOMAIN]/mailman3/lists/[LISTADDRESS]/held_messages`





IETF mailing lists are the primary discussion forums for IETF Working Groups (WGs). While groups may also use in-person or online meetings—as well as platforms such as GitHub—to raise, suggest or discuss issues initially, these should be brought to the WG mailing list so that a group position can be determined.

IETF Working Group lists are generally open to anyone with an email address.


### Email expansions




## Uses of WG mailing lists
Beyond discussion of relevant topics and documents relevant to a particular working group, Working Group email lists are also used to:
- Announce WG interim meetings
- Announce WG sessions at IETF meetings
- Share meeting notes

When actions on documents such as calls for adoption of an I-D by a WG and WG Last Calls, are are noted using the IETF Datatracker, it sends messages automatically to the WG email list.



## Dealing with disruptive posting
Regrettably, managing mailing lists sometimes includes handling disruption postings by participants. It is your responsibility as chair to ensure the mailing list discussions serve the purposes of the Working Group, make forward progress, and adhere to the IETF Guidelines for Conduct ([BCP 54](https://www.rfc-editor.org/info/bcp54)). (Refer to [RFC 2418 section 6.1](https://www.rfc-editor.org/rfc/rfc2418.html#section-6.1) for details on the chair role.) You have several tools at your disposal to keep Working Group mailing list discussions on track:

- [RFC 3934](https://www.rfc-editor.org/rfc/rfc3934) describes a method for giving warnings and, in the face of continued disruptive posts, suspending the participants posting privileges on the Working Group mailing list. You may also consult with your Area Director for other possible methods to address disruptions on the mailing list.

- [BCP 83](https://www.rfc-editor.org/info/bcp83) allows posting rights to be indefinitely revoked from the any IETF mailing list using a Posting Rights Action. If a disruptive participant on your Working Group mailing list is subject to a BCP 83 Posting Rights Action on another IETF mailing list, as chair you may simply remove their posting privileges on your Working Group's list.

The IESG has provided [guidance on moderating IETF WG mailing lists](https://www.ietf.org/about/groups/iesg/statements/mailing-lists-moderation/) to control excessive spam, persistent off-topic postings, persistent personal attacks, etc. on mailing lists.

The above actions are meant to deal with generally disruptive behavior on Working Group mailing lists. Independent of any action you take as a chair to manage your Working Group mailing list, if a particular disruption on the mailing list also constitutes harassment, per the [IETF Anti-Harassment Policy](https://datatracker.ietf.org/doc/statement-iesg-ietf-anti-harassment-policy-20131103/), then you can decide to confidentially make a report of harassment (as can any IETF participant) and the IETF Ombudsteam will investigate the report as such. You can also confidentially contact the Ombudsteam for advice about how to handle a situation without a formal investigation being undertaken.


## Managing your list subscriptions
Details about how to manage your own subscriptions to ietf.org, irtf.org, and rfc-editor.org email lists can be found on the [www.ietf.org Mailing list page  ](https://www.ietf.org/participate/lists/#managing).


