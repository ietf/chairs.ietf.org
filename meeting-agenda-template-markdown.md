---
title: WG meeting agenda template
description: WG meeting agenda template in markdown
published: true
date: 2021-12-14T00:02:22.012Z
tags: 
editor: markdown
dateCreated: 2021-12-14T00:02:20.229Z
---

> Notes about using this template
The following values provdie some placeholders:
"NNN" = IETF meeting number
"NAME" = Full working group name
"WGNAME" = WG Acronym
  
{.is-highlight}
 
# WG Meeting agenda : Markdown template
(IETFNNN or "Interim") WGNAME WG Session Agenda

# About the Working Group NAME (WGNAME)

## Materials, Charter, Documents
* [WG General Info](https://datatracker.ietf.org/group/WGNAME/about/)
* [WG GitHub Repositories](https://github.com/[WG Github path])
* [ADD Documents, Drafts and I-Ds](https://datatracker.ietf.org/group/WGNAME/documents/)

## WGNAME Chairs & Area Director
* AD:  (AD name)
* Chairs: (Chair 1 name), (Chair 2 name)

## Session link, minutes, jabber
* [Meetecho Link](https://meetings.conf.meetecho.com/ietfNNN/?group=WGNAME remote participation
* [Meeting Minutes](https://codimd.ietf.org/notes-ietf-NNN-WGNAME
* [Meeting Chat](xmpp:add@jabber.ietf.org?join)

## IETF NNN WGNAME Session Times

Add has a single 2hr session: Friday July 30, 12:00-14:00 PDT (UTC-7)  1900-2100 UTC
___

# ADD Agenda (Start time)-(End time) (TZ) (Day)
___
## Welcome
* 5 minutes
* [NOTE WELL](https://www.ietf.org/about/note-well/)
* Scribe selection
* Agenda bashing
***
## Drafts

### Meeting Materials
* IETF NNN WGNAME Presentions [Link](https://datatracker.ietf.org/meeting/NNN/session/WGNAME)

### 1. ITEM 1
* [DRAFT 1](https://datatracker.ietf.org/doc/DRAFT 1/)
* 10 minutes + 10 minutes Q&A

### 2. ITEM 2
* [DRAFT 2](https://datatracker.ietf.org/doc/DRAFT 2/)
* 10 minutes + 20 minutes Q&A

### 3. ITEM 3
* [draft-ietf-add-dnr](https://datatracker.ietf.org/doc/draft-ietf-add-dnr/)
* 5 minutes + 5 minutes Q&A

### 4. Split-Horizon DNS Configuration
* [draft-reddy-add-enterprise-split-dns](https://datatracker.ietf.org/doc/draft-reddy-add-enterprise-split-dns/)
* 5 minutes + 5 minutes Q&A

### 5. Discovery of Encrypted DNS Resolvers: Deployment Considerations
* [draft-boucadair-add-deployment-considerations](https://datatracker.ietf.org/doc/draft-boucadair-add-deployment-considerations/)
* 5 minutes + 10 minutes Q&A




## Other Discussion Topics

### 6. Private IPs, DDR, and PR#11  

* Slides: See [PR11 ADD DNS and Forwarders](https://datatracker.ietf.org/meeting/111/materials/slides-111-add-ddr-and-forwarders-aka-pr-11-00) slides by Ben Schwartz & Tommy Jensen
* DDR Pull Request [PR11](https://github.com/ietf-wg-add/draft-ietf-add-ddr/pull/11)
* See [ADD list Thread](https://mailarchive.ietf.org/arch/msg/add/NYik5dhJyTS7QeTJxVQACyCWOWo/) for background discussion
* 10 minutes + 15 minutes discussion
#### Question posed by EKR for discussion:

> The general assumption for the DDR threat model so far is that:
>
> 1. (presumably because DHCP is secure in some way). If that's not true,
> then I think we can agree that DDR does not provide much additional
> security benefit because the attacker can just substitute their own
> resolver [0].
>
> 2. Either the home network or the ISP network is insecure, otherwise
> you don't need DoX.
>
> OPPORTUNISTIC MODE
> So, first, its not entirely clear to me what the Opportunistic mode of
> S 4.2 provides. In this scenario, presumably the client will be doing
> TLS to the CPE (because otherwise the IP address would be the
> resolver's public address), which means that we are concerned with the
> attacker controlling the home network. So, in this scenario, we are
> only getting value if you have a network in which:
>
> 1. The attacker can *see* traffic not destined for their IP address
>   (otherwise there's not much point in encrypting).
> 2. The attacker cannot forge traffic from another IP address>
>   (otherwise they can just impersonate the CPE because there
>   is no certificate).
>
> Are there an appreciable number of networks with these properties? If
> so, can we write down where that happens and put it in Security
> Considerations? If not, we should consider removing this mode.

---

### Planning & Wrap up

* 5 min - Wrap up + Future Planning

### As Time Permits
___
