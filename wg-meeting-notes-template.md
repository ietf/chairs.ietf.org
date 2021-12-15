---
title: wg-meeting-notes-template
description: A template for wg meeting notes that works with IETF Datatracker
published: true
date: 2021-12-15T00:08:11.891Z
tags: 
editor: markdown
dateCreated: 2021-12-15T00:08:11.891Z
---

# WGNAME IETF 111 Session Agenda

> Notes about this template: 1. This template is offered as an example starting point only—there is no required format for IETF WG meeting agendas; 2. The source is availble at: This note should be removed 
{.is-warning}


# About WGNAME

## Materials, Charter, Documents
* [ADD WG General Info](https://datatracker.ietf.org/group/add/about/)
* [ADD GitHub Repositories](https://github.com/ietf-wg-add)
* [ADD Documents, Drafts and I-Ds](https://datatracker.ietf.org/group/add/documents/)

## ADD Chairs & Area Director
* AD:  Eric Vyncke
* Chairs: Glenn Deen, David Lawrence

## Session link, minutes, jabber
* [Meetecho Link](https://meetings.conf.meetecho.com/ietf111/?group=add) remote participation
* [Meeting Minutes](https://codimd.ietf.org/notes-ietf-111-add)
* [Meeting Chat](xmpp:add@jabber.ietf.org?join)

## IETF 111 ADD Session Times

Add has a single 2hr session: Friday July 30, 12:00-14:00 PDT (UTC-7)  1900-2100 UTC
___

# ADD Agenda 12:00-14:00 PDT Friday
___
## Welcome
* 5 minutes
* [NOTE WELL](https://www.ietf.org/about/note-well.html)
* Scribe selection
Hazel Smith, Tim Wicinski, Mark Andrews
* Agenda bashing
no changes
***
## Drafts

### Meeting Materials
* IETF 111 ADD Presentions [Link](https://datatracker.ietf.org/meeting/111/session/add)

### 1. Discovery of Designated Resolvers (DDR)
* [draft-ietf-add-ddr](https://datatracker.ietf.org/doc/draft-ietf-add-ddr/)
* 10 minutes + 10 minutes Q&A


Quick update on DDR
Published draft -02 version, 5 open issues (generally minor), 1 open PR for discussion later in session
Summary of recent changes:
    * Removed "equivalence", only talk about "designated"
    * Cleaned up use of SVCB and address hints
    * Clarified behaviour of \_dns.resolver.arpa
    * Updated and added examples and guidance so it's clearer how this works - should be a lot clearer and easier to understand

#### "resolver.arpa use" Issue #21
    * Concern is use of resolver.arpa instead of X.X.X.X.in-addr.arpa
    * Current rationale is to mimic ipv4only.arpa
        * Querying specific resolver information
        * Doesn't require a record per resolver address

Alexander Mayrhofer(AM): Favor of the change


Daniel Migault(DM):
    * Notes that it breaks the security model of DNSSEC, says that it is a sufficiently large problem.
    * Question to previous person: what sort of harm do we expect it to [ something like fix? missed word ] in the public DNS


Benjamin Schwartz(BS)(Google):
    * Supports Resolver.arpa
    * If you want to use DNSSEC, your resolver has to be identified by a DNS name - if you use an IP address, then DNSSEC does not apply


Alexander Mayrhofer(AM):
    * Unsuspecting sysadmins will put it into the public DNS, or will desperately try to get in-addr.arpa delegations for RFC1918 space.
    * resolver.arpa makes it clear that information does not belong into the public DNS.


Ralf Weber(RW): Would not work in the home network

Mark Andrews(MA): RFC 1918 space implicitly delegated to everyone


Glenn Deen: This is explicitly captured in the GitHub as issue 21, and if you want to  leave a comment post there or onto the mailing list


#### Issue #18 "Authenticated, Opportunistic, and More?"
Brief summary from slides:
    * "Authenticated discovery allows trusted redirection to a designated resolver"
    * "Opportunistic discovery allows use of an encrypted protocol on the same IP address as the known Do53 resolver"
        * List discussion about the value of this; what do we think?
            * Ben Schwartz(??): Noting that this question about will be discussed in more detail later in the meeting
    * "A complete mismatch between the provisioned IP address and the designated resolver is currently disallowed"
        * "This is the local CPE -> ISP resolver case" - DDR currently considers authenticatiing this case out of scope, but the unauthenticated hint exists
        * PR #11 is an attempt to solve this with a different security model and weaker identity guarantees.
        * Another approach here is to simply disallow automatic use, but allow systyem policy or user approval to allow this


Eric Rescorla(ER): ? sounds terrifying - Modal dialog "User, would you like to techtechtech??"


Tommy Pauly(TP): Maybe a prompt if you have a list of already trusted (TRRs?) resolvers, "Do you want to use [foo]?" Opinion that ? is not solveable at a protocol level.


Glenn Deen(GD): Good discussion, but DDR is a discovery mechanism, it's not the whole solution. Yuo have good points, but we're drifting off a little into the usability side of things, this is low level technical gorp that will be made use of [ sth like "further up the stack"]


Tommy Pauly(TP): DDR is a mechanism, at some point the mechanism will run out of things it can do. All the discussion of the various things that can be done with these various hints in a CPE situiation, but that it is largely out of scope


GD: notes that it it also out of scope for our current charter

ER: [ something about not designing a thing that isn't of any use to anyone? ] interface between the ? and the decision maker?


TP: believe what we are saying is that DDR gives you a hint, and can give you an authenticated version, .... all three of these use cases are valid and usefui to different people, but that is where this mechanism ends


### 2. Analysis of DNS Forwarder Scenario Relative to DDR and DNR
* [draft-stark-add-dns-forwarder-analysis](https://datatracker.ietf.org/doc/draft-stark-add-dns-forwarder-analysis/)
* 10 minutes + 20 minutes Q&A

#### Presentation from Barbara Stark

_What this draft is_
Common scenario with CPE with DNS Proxy/DNS Forwarder functionality in it. How does this scenario play out?
"Analyzes the behaviours that residential end users and home network owners (e.g. parents of young children) might experience when OSs and applications support DDR and/or DNR, and the CE router of the home network offers itself as the Do53 resolver"

 _Why home network CE routers do DNS forwarding_
* Local name resolution: Often times these devices provide local name resolution, and have their own little domain, so they can tell people "if you ever need to access your router, just type in this domain name"
* Captive portal: don't know whether the current proposals would break captive portal
* Caching: [ possibly a comment here about whether caching would break this? unsure, need to check recording later ]

_Assumptions_
"Common OSs support both DNR and DDR, some applications (e.g. browsers) support DDR, No CA will sign a certificate with a private IP address in a SAN"

So we know that certificate authorities cannot be used to provide a chain of trust for any

_Scenario 1: CE Router not updated_
Result: The OS/app will not discover a local Encrypted Resolver. OS/app may subsequently use some non-standard mechanism to select an Encrypted Resolver (we really have no idea what they'll do).

"Pretty clear that DDR and DNR do not currently satisfy the requirement R4.2 that it shoudl not require any changes to DNS forwarders on non-upgradeable legacy network devices, or that they should not forward queries for resolver.arpa upstream"


Tommy Pauly(TP): DDR says you shouldn't forward these upstream, but does explain that for a bilnd forwarder it may do that when it knows that it is not the end resolver that will be offering encrypted DNS. I believe that the intent is that when you have


BS: that is what you have today


TP:... the client device will still get the hint as to what encrypted resolver it can use. [[ HS note: but will it actually be usable, as the cert won't include the IP of the CPE's DNS forwarding resolver?? so it won't be authenticated ]]

_Scenario 2: Updated CE router provides DNR_


BS:In the DHCP replies. But not tryign to offer DoH locally in the CPE. [...] Some OSes might use this information if they feel like it, but some might not. Applications that use the resolver.arpa will not use the encrytped resolver. Our local name resolution is now broken? Legacy captive portal is now broken? Filtering in the CE router (i.e. as enabled by the owner of the home network) is now broken? Filtering in the core network resolver continues to operate. No local caching.


Ben Schwartz(Ben S): ... of the form "I would suggest that you use this resolver instead". If the device is telling the network "don't use me" then it's no surprise that the services that it provides are no longer present in the .... . but this is its own decision. ... DNR in which case there is no problem. You're describing essentially a buggy deployment, the answer is essentially "don't do that"


BS: Would Agree. To be able to come to a conclusion like that using paper rather than code. So I agree.

_Scenario 3: Updated CE router supports opportunistic encryption to sits DNS forwareder and provides its info in DNR and DDR_

OSes that feel like supporting it will support it, and those that don't wont. Talking to my friends that do router development, this isn't a very likely thing to happen in the context of such uncertainty. Whilst this could certainly provide .... whilst a possibility, this is appearing to be an unlikely possibility.

_Is the analysis accurate?_


BS: What I'm seeing is ... what I'm going to see in CE routers, either the proxy is on or the proxy is off. If we assume that even advertising the DHCP address of the upstream doens't make snese, then those really are the options. And if those are the options, and we were serious about wanting to support this use case, and maybe not breaking some things that users can currently do in the process, what is the path that we should take?

_If the ... what are next steps?_

Do we create implementation best practices? Ben has said it's out of scope, but recharters _can_ happen...

Just like we can't necessarily expect OSes to do DNR or DDR, we can't expect OSes to follow best practices... but we can at least express them

GD: In  scope... we can say "do not do [thing]" - guidance on avoiding doing stupid stuff, totally in scope.


BS: If we are not allowed to ever consider that users be given options, then I think that this is dead in the water. I don't think that it is really possible to say that users have control but wer are not going to allow users to have control. That we are not going to ever recommend that users have control of this?


GD: What we are not charted to do is to work on the UI or the browser logic portion of this, we are chartered ... architectural decisions re CPE deviceswould be in scope ... whilst staying away from the UI and client [ of end-user devices? ]


BS: That is going to result in us giving up on this use case/ This use case isn't supported, it's going to be broken, because we'Re not even considering giving recommendations on how users are treated.



#### Q&A

Tommy Jensen (TJ): First just to ... syaing that we are going to [...] doesn't mean we are goign to abandon it. As someone pointed out, DDR stops at "we are going to validate this hint", it's still there even if we can't authenticate it ... but we can't standardise it,

Most of the things discussed here are time bound... eventually ? and ? and ? will eventually address this issues. Am I missing something?


BS: The DNS caching hit can probably be accepted, "the latency probably isn't that bad", ...  capive portal, need to support local domain names, some kind of split horizon - CE router can't reasonably be expected to support DoH, some way to say "don't use DoH for [local domains]"?


Eric Nygren(EN): Might be worth calling out is what is and isn't possible on the boundaries, expecially on the parental controls stuff (a hot topic), you could have two different resolver IPs you could hand out, [] or you could have a DoH policy URI that embeds some of the policy information, ... become harder and not as easy to do the fine grained parental controls you can do on the router itself


BS: if you do it at the server level, you can no longer specify it in the household on a per device basis? [parental controls is] A bit more of a concern to my co-author across the pond.


EN: [ some devices do MAC based decisions] You need to put it up a level, and give the user a different IP address that doesn't do parental controls


BS: It's not seeing the MAC addresses [ if it's being done by a server outside of the home network ]


Tommy Pauly(TP): Want to reiterate for the group that a number of cases that work for both DDR and DNR. Comcast, quad 75, going to work just fine with DDR/DNR. I don't think we want to accept breakage .... scenario 2.... skipping local filtering rules, skipping local name resolution, are both more complex things, are not equivalent... mechanisms in DDR are necessary to allow clients to solve this, but are not sufficient in this specific scenario to solve this. A device cannot make the decision for someone as to whether they want to use the filering on their local CE or not. ... shake out long term ... policy ... beyond what we can do in this working group.


BS: Talk about what we could do with ... settings, without discussing what the UI should be like. We have often been able to have configuration around protocols.


Eric Rescorla(ER): Seems to me this presentation ... the point of DDR is to allow you to upgrade to an encrypted connection without touching the local router, ... what you're asking for is to *not* upgrade without touching the local router... ??? ... Firefox detects local filtering, and turns off DoH, if it can't resolve something it falls back... if you're not going to touch the router, ... if a local router wishes to stay in the game, it should have to make some positive action? but the purpose of this group is biasing towards encryption, it seems like ... leaning towards encryption,... agree it's not ideal to break those use cases, but... we know we don't get it right all the time, but ...


BS: I'm just kind of concerned, people were kind of hoping that homenet would be able to cause the home routers to be able to do some ? ... kind of a realist, worked with them for about 20 years, if local routers do change it will be a long long time. we should ack our expectations around this particular use case, and not pretend otherwise


ER: I don't think I'm prettending otherwise, I just don't know how to solve this particular problem.


BS: Okay


Eric Vyncke(EV): [AD Hat] It is within the charter to put ... recommendation ... but not deciding policy like "you should do this and this and this"


Andrew Campling(AC): Thank you to Barbara and Chris for writing this up, important that we xcdocument the real world. Imperative that wer find solutions for 1 and 3. Particularly 1 when we ack that shelf life for routers is 10+ years. Can't say that users should just upgrade them because [sth lile "that's not reality."]"


### 3. DHCP and Router Advertisement Options for the Discovery of Network-designated Resolvers (DNR)
* [draft-ietf-add-dnr](https://datatracker.ietf.org/doc/draft-ietf-add-dnr/)
* 5 minutes + 5 minutes Q&A

#### Summary
"Dan Wing (presenting), et al.""

* Changes since previous IETF
        * Got review from DHC, design rationale, incorportated Michael's suggestion from section 3
        *
    * Nedt stpes: Request WGLC
    *

#### Q&A


Benjamin Schwartz(BZ): I think this draft is great, in the sense it's ready for last call, but I also kind of worry that if we move forward now we preempt some important discussions - it should remain in line with DDR. I.... we really need to be clear on what the authentication rules are, what names you need to have in your certificates are. Still a topic of debate, we should try to reach similar/matching solutions for DDR and DNR.


Chris Box(CB):  Agree its a little early to do a group last call. In terms of content, was to incorporate what SVCB says as "it's the same as DDR" except it's not the same as DDR... have to take out the address hints as. ... wonder if we lose what we were trying to achieve which was to keep them the same



BZ: Don't view that as a serious misalignment, but also, we should revisit the IP hint recommendations in DDR.

### 4. Split-Horizon DNS Configuration
* [draft-reddy-add-enterprise-split-dns](https://datatracker.ietf.org/doc/draft-reddy-add-enterprise-split-dns/)
* 5 minutes + 5 minutes Q&A

#### Summary/talk
Dan Wing (presenting), and T. Reddy

Agenda
    * Draft updates from 02 and o4

Quick recap
Discover local names, similar to pslit DNS configuration in IKEv2 for RFC 8598... public but diff ver

Update to scope
Dplit-DNS configuration is applicable to any network, e.g. enterprise, isp m,movile network etc. provisioning domain key to ... _, RFC ???

_Proof of Authority_
Go out and make sure that the private domain is not known to the public DNS. A query to a public DNS server is necessary to do that.

Alternatively, querying to a local reoslver and getting a DNSSEC protected answer. Just querying to a local resolver and getting a non-DNSSEC protected answer doesn't acutally prove anything.

If RRSet matches or is a subdomain of and ADN, if that fails the network is not authoritative and we don't use that claim of authority of a private domain.

Client doesn't need to perform those for some special purpose domains, like ".home.arpa". Question about a registry of these going forward? IETF-sanctioned ones plus non-sanctioned ones like .local may need ot be handled in the same way.

_Discovery of Network block policy_

Policy expression (not "policy prescription")

(Expecting Comments)

Client might do all kinds of interesting and curious routings around those blockings.

Shortcut

What the network is trying to do is block things, trying to keep the device ... because it wants to do filtering, whatever it wants to do. The client can ignore this, can do whatever it wants. Purpose is to give information to the user, they can see when they go to join the network, I can only use the local DNS for what the policy is, maybe the user goes "I don't want to use this network"


#### Q&A


Eric Rescorla(ER): I don't think this is necessarily a bad idea/ The way I would say, I guess, in the contect of DNR "here is the thing I want you to use, and I don't want you to use anything else" ... I know Vixie had talked about, ... tri-state, " ... ", I really wish you would" and "If you do I'll try to block you"? Trying to think about what the useful characteristics ate. Tommy you may have some thoughts?


Tommy Pauly(TP): Thanks Dan for presenting this. ? split the split DNS stuff out from the filtering/policy stuff? To Marcus earlier point, it's a useful ... local networks often missing whern compared to a VPN. ... sentiment ... would prefer to see it not be in this document. I think there could be more done here. I think there are different scenarios ... "do not use anything other than me, we need to see everything for policy reasons" ... "... poluicy JSON ..." ... here is other information.... something but doesn't track your IP... here's a safe browsing thing.... Important, good to discuss, thanks.


Benjamin Schwartz(BS): THink this tpics have to be split, they seem unrelated. They both seem pretty meaty, it's pretty
I have some real concertns here... people in the world join networks and don't have a liot of choice about the networks they join. We need to be careful about what we help enable networks to impose. How is this going to be limited to enterprise networks, and is that going to be a firm restriction that we can rely on?


Andrew Campling(AC): First ... important. Specificatlly for split horizon, being able to have this policy expression is important as well, whether included here or ref here it doesn't matter either way, but it is a necc adjunct to split horiz. ... needs to be dev sep and referenced or dev here. Both parts important to the split horiz use case.

### 5. Discovery of Encrypted DNS Resolvers: Deployment Considerations
* [draft-boucadair-add-deployment-considerations](https://datatracker.ietf.org/doc/draft-boucadair-add-deployment-considerations/)
* 5 minutes + 10 minutes Q&A

#### Summary/Presentation

_reminder_
Pulled out of DNR and into its own spec because it was felt to be better.

Most text same, a couple pf tuneups. Managed and unmanaged home routers. Managed by the ISP vs managed by the consumer.

Legacy CPE are discussed in here as well as managed and unmanaged DV provisioned certificates and how to get those.

Taking us down the steps of trying to work out how to solve some of the problems Barbara mentioned in her talk.

Next steps?

Is there interest to mainain this effort? If so, should we adopt as Informational?

Not seen a lot of discussion on this... do we need to turn the crank, or get a +1, or...?

#### Q&A


Glenn Deen(GD)(as Chair): Line item to develop informational docs. Would fit very well within charter _if we wnated to_, as you suggest.


Ben Shwartz(BS): Thius kind of document could be useful, but it seems wfully early to provide impl guidance for standard not yet impl or deployed. We'll do a much better job with this if we have some actualy deploy experience on which to base our reccs.


Eliot Lear(EL): That's an argument not to push the doc hrough aLAst Call, but not an excuse to not progress it. Would be cool to have a doc like this that "tracks" this implementaton effort as we get experience.


Alexander Mayrhofer(AM): I think ... connect operational experience.... the last time that we actually finished, I wouldn't be sure ... i think we do need a spot to ... discuss operationsal considerations. ... easily lost in the mailing list. It's useful.


GD: What I'm hearing is that we might consider doing an "Adoption call" in the WG... is that what I'm picking up? ... > general nods from p ... Good to know.

## Other Discussion Topics

### 6. Private IPs, DDR, and PR#11

* Slides: See [PR11 ADD DNS and Forwarders](https://datatracker.ietf.org/meeting/111/materials/slides-111-add-ddr-and-forwarders-aka-pr-11-00) slides by Ben Schwartz & Tommy Jensen
* DDR Pull Request [PR11](https://github.com/ietf-wg-add/draft-ietf-add-ddr/pull/11)
* See [ADD list Thread](https://mailarchive.ietf.org/arch/msg/add/NYik5dhJyTS7QeTJxVQACyCWOWo/) for background discussion
* 10 minutes + 15 minutes discussion

#### Presentation: DDR and Forwarders, Ben Schwartz (Google)

Back to first topic, tlaking about this scenario, forwarder

... resolver it is pointing at actually _does_ suppot DoT, can the client get DoT in this scenario.

As Barbara has pointed out, it is actually in our Requirements [ that we support this?].


BS: DDR says that this information is useless, and you shouldn't use it ... DDR and its reqs do not form a consistent body of text right now.


Tommy Pauly: Agreed. We should change the text to say what ... said.


BS: Just to be clear, we are talking about legacy. Reluctant forwarders, that are in place for some operational reaons. Needing to bring up DHCP on the local network before confiugration has been totally figured out, so you can tell local clients something before WAN link is up.


Out of scope: forwarders that implement DDR, DNR, upsteam foesn't offer enc DNS, forwarders with updateable filtering. They can and should add resolver.arpa to their filters?


Question: You've sent a query for this special name, ...


DDR draft-o2 says no upgrade for you... No Private IPs in cers -> Val fails -> No upgrade.


Doesn't seem ideal. BS been working on pull req #11 that tries to change this behaviour. What is asys is if the cllient doesn't have secure identity... it should use it for no more than 5 minutes. A little unusual, we don't normally have sec reqs phrased like this... why? This changes the security posture, you are no longer vuln to passive monitoring, you can upgrade to enc connection... but vuln to active adversary is slightly diff... that adv can prevent you doing DDR, with this change, it's not that the active adv has to be present, it is that they have to be present the last time you refreshed this. Which is why refresh, so that a transiently present active adv cannot "stick around" after faking repsonse once.


Implications for forensics... logs must contain a specific secquence rather than a random sampling


Intetnonal forwarders: ...


Paths forward:


PR #11 is what you need to do as a cient if you want DDR in a upgrade scenario. Question is whether you want to include that in scope? I'll let Tommy ...


Tommy Jensen: good job walking through PR. ... I don't think this PR belongs in DDR, not because it isn't worthy of being addressed, but because it should be ... separately. Tradeoffs that Ben just walked us through... in DDR if the validation fails, it could be an active attacker... a client ism aking a "seucirty vs functionality" kind of tradeoff... as Ben said, a nuance there... adding some security against passive ... ? doesn't make sense to impl if client unwilling to do [ refreshing thing? ]. We can say "if you 're unwilling to do ... do mechanism X"...  some clients may want to do ... some may want to alkways verify the ident of resolv.


TJ: A lot fo good work. I think it deserves its own space.


Eric Orth(EO): Support for this. One of the most important things for this to reoslve. Previously .... . Don't have strong opiniobn if should be in DDR or eslsewhere. Shoudl eb up to client whether it supports DDR or DDR+[this additional mechanism]. I think this does a sufficient job of ... turning a transient attack into a ... PR solves this ... doesn't completely solve user-intent scenario, everything Barbara Stark was talking about, if we bypass the ... we might skip the filtering, client doesn't know if this is something the client wanted to do. As long as we make the client aware that the user may want to do that. Maybe the client only uses this in a config UI where the user says "yes I wanna do the upgrade". Maybe in a couple years time, we don't need to do that anymore once all the CPE know to filter out "resolver.arpa" as the ecosystem has evolved and prevents the filtering being bypassed. Whether part of DDR or a sep doc, this sounds like a great way to go.

Tommy Pauly(TP): Don't really know if this is a blind forwarder, or a pihole, ... because you don't know that, this is not safe to do automatically full stop,... you need more understanding of the user intent... until you have ... this *cannot* be part of DDR, I don't think that's appropriate at all.


Not great to remain unencrypted. You're still going to be downgradeable if chekcing every 5 mins, which isn't any worse

in the active adv case it is ... waiting a 5 miniute period you can send the client anywhere

You can continue to do lookups w/o responses.  Leave to option E at the end.  Much more nuanced.


BS: Curious about active attacker scenario


TP: 2 case:  Own cert that is compromised you can be attacked.


BS: needs control of address


TP: in PR #11 only 1 packet needed to redirect. In current DDR you need active control.


BS: length of contol of IP is the destinction.


Tommy Jenson: DDR falls back to plain DNS is not the only response, if you have fallback encryt resolver.


BS: all distinctions are w/in the roll of client behaviour. What are the bounds of client behaviour


TJ: the ecosystem is interested in a signal even if not authenticated.




#### Q&A





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


GD: BS submitted draft about service B


BS: new draft out - July 26


GD: Good discussion this week.  Interim - mid Sep? Op -> Chairs


EV: Thanks.


Tommy Jensen: is there a clear consenus of #11


DL: Will folowup


BS: thinks this should not be in doc.


Poll: Should DR #11 be made a seperate doc. 29/1/30
Poll results: 29 raised hands showing support, 1 not raised showing non-support, many non-participating hands.


We are done.

### As Time Permits
___
