---
title: Managing mailing lists
description: Information, tools, and resources for managing IETF working group mailing lists
published: true
date: 2025-11-25T00:58:39.905Z
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

To access a specific list, you can go through the main page above, or using a direct URL of the form: `https://mailman3.[DOMAIN]/mailman3/lists/[LISTADDRESS]/`

For example, for the list `admin-discuss@ietf.org`, this is: `https://mailman3.ietf.org/mailman3/lists/admin-discuss@ietf.org/`

General information on using the admin interface can be found on the [IETF Website](https://www.ietf.org/participate/lists/#managing).

## Accounts
To use Postorius you will need an account. You can create an account on any of the front pages (above) using the **Sign up** menu item.  Only one account is needed - it will automatically apply to the other domains above.

Currently, the account name you use for logging in to Postorius is independent of any other IETF system, so please use any account name that you wish. 

## Admin permissions
List admin permissions are linked to email addresses. To active your permissions, you will need to [link your email address(es)](https://www.ietf.org/participate/lists/#managing) to that account

If you have an account linked to your email address and do not have the permissions to a list that you expect, then please contact support@ietf.org.

* To see all the lists for which are an **owner**: `https://mailman3.[DOMAIN]/mailman3/lists/?role=owner`
* To see all the lists for which are a **moderator**: `https://mailman3.[DOMAIN]/mailman3/lists/?role=moderator`

## Integration with Datatracker
### Working group lists
The Datatracker page for a WG lists the **mailing lists for that WG** and the list archives. The general form of the Datatracker link is as follows, where `[WGNAME]` is the WG abbrevation: `https://datatracker.ietf.org/group/[WGNAME]/about/`

When a change is made in Datatracker, such as a WG Chair changing, there is currently a manual process that updates Mailman.

Additionally, addresses for group chairs, ADs and other expansions are provided at: `https://datatracker.ietf.org/group/[WGNAME]/email/`

### Non-WG lists
There is a single Datatracker page that lists all [non-WG lists](https://datatracker.ietf.org/list/nonwg) but this only links to the Mailman page for that list.

Datatracker does not record any other information about non-WG lists.

## Global allowlist and members vs non-members
The IETF mailing systems maintains a [global allowlist](/mailing-lists/first-time-subscription#global-allowlist) of addresses that are permitted to send to mailing lists. Any address on that list can send to any mailing list, whether or not it is subscribed to that list.

When a post is sent to a list from an address that it is not a member but this message is accepted because that address is on the global allowlist, that address is then automatically added as a **non-member** of the mailing list.  While non-members can post to a list (unless moderated), only members receive messages sent to the list. 

If you need to find a specific address to manage on your list then remember to check **both** the list of **members** and **non-members** for your list. 

# Common management tasks
## Handling of moderated messages
Messages can be held in moderaton for a number of reasons, not just because the address is set to moderation. The moderation queue for a specific list can be found under **Held messages** on the top menu:

![mailman3-moderation_options-new.png](/mailman3-moderation_options-new.png)

or using this direct URL: `https://mailman3.[DOMAIN]/mailman3/lists/[LISTADDRESS]/held_messages`

## Moderating / unmoderating
Before putting an address into moderation, please make sure you are following the guidance on [disruptive posting](/mailing-lists/disruptive-posting)

To put an address into moderation you first need to find the address, which may mean checking both the members and non-members lists and changing the **Moderation** setting to `Hold`.

To unmoderate, change the **Moderation** setting to `Default processing`. 

## Putting the whole list into moderation
From the **Settings** tab for your list, select the **Message Acceptance** sub-tab and on there:
1. Locate the section titled **Default action to take when a _member_ posts to the list** and from the dropdown menu, select `Hold for moderation` 
2. Additionally, locatye the section **Default action to take when a _non-member_ posts to the list** and from the dropdown menu select `Hold for moderation` 
3. Click the **Save changes** button at the bottom of the page to apply the new moderation settings.

## Spam control
Control of spam is centralised in the IETF mail system and while most spam is blocked, some may occasionally get through to a list. 

If you have a problematic spammer that you want to block and you are certain that they are only a spammer then:
1. (*optional*) Temporarily add them to the ban list (**Ban list** on the list admin menu) or put them into moderation.
2. Contact support@ietf.org to have them blocked at the mail server.
3. (*optional*) If spam messages have made it through to the mail archive and you want those messages not to be visible, then please contact support@ietf.org with links to the messages.

# Further information
* Guidance on managing [disruptive posting](/mailing-lists/disruptive-posting)
* Explanation of [First-time subscription](/mailing-lists/first-time-subscription) and the global allowlist.
* For information on where action may be required by law see the [IESG Statement on restricting access to IETF IT systems](https://datatracker.ietf.org/doc/statement-iesg-statement-on-restricting-access-to-ietf-it-systems-20221031/)