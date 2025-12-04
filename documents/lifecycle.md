---
title: Document lifecycle
description: An extended description of the working group document lifecycle provides an overview of the various stages of a document, how a document progresses from one stage to another, and the roles different individuals and groups play at each stage.
published: true
date: 2025-12-04T21:38:49.482Z
tags: 
editor: markdown
dateCreated: 2022-05-10T14:46:37.419Z
---

# Introduction

RFC 4858 talks about "Document Shepherding from Working Group Last Call to Publication". There's a significant part of a document's life that happens before Working Group Last Call, starting, really, at the time that a working group begins discussing a version of the idea that's been posted as an individual Internet-Draft (I-D). It seems reasonable and helpful in many situations to begin shepherding when there's a call for adoption as a working group document. 

This document extends RFC 4858, describing how that extended shepherding function might work and what tasks might be involved throughout the document's lifecycle, and suggesting how Working Group Chairs might choose to implement extended shepherding.

It is very common to see documents progress far too slowly, sometimes languishing for many months and even for years due to neglect. Sometimes a working group will intentionally set a document aside, put it on a back burner while it works on more pressing things. But it's often not intentional: the document sits around because of lack of follow-through, waking up occasionally when someone realizes that the last version has expired and an IETF meeting is coming up soon.

We would really prefer to process documents efficiently, ensuring that whatever happens is intentional: that documents are set aside only when it makes sense to do so, and that active documents move forward in the process, with someone responsible for making sure that happens.

This document suggests specific tasks a Working Group Chair should be doing or delegating in order to maintain forward progress, accountability, and quality control on a working group document. It adds to what's in RFC 4858, intending to extend it, not replace it. Major extensions involve assigning a Shepherd and defining specific tasks earlier in a document's life, and possibly delegating Document Shepherd tasks to a Shepherd who is neither a Chair nor the Working Group Secretary (consistent with the [IESG Statement on Document Shepherds](https://datatracker.ietf.org/doc/statement-iesg-iesg-statement-on-document-shepherds-20101011/)).

The summaries in each section of the tasks expected at that stage in the document's lifecycle can make this an easy reference and checklist for Working Group Chairs and Document Shepherds.

The specific mechanism suggested here will not be suitable for all working groups, all management models, and all situations. While it's a good idea to have the stages laid out and the tasks at each stage identified, not all working groups will benefit from having a single document shepherd designated at the start. Indeed, when a document is legitimately years in the making, personnel may come and go and changes will be necessary. A particular working group might be working only on one document at a time, with all tasks shared between the chairs.

> For these and other reasons, the suggestions herein are meant to be adapted to specific situations to retain the underlying objective of maintaining progress through active involvement.

## Notational Conventions

It is important to note that this document makes no formal process changes and there is no normative language here.

Initial Capitals are used in some terms, such as "Document Shepherd", to indicate that those terms represent specific roles in the management model that is described.

# The Document Shepherd as a "Function"

This document looks at the Document Shepherd as a "function", rather than as a single person. The Document Shepherd Function has a set of tasks that need to be performed, but the tasks do not all have to be performed by one individual.

While, ultimately, it is the responsibility of the Working Group Chairs to ensure that the shepherding tasks get done, the Chairs do not have to do all those tasks by themselves. From Section 6.1 of the "Working Group Guidelines and Procedures" (RFC 2418):

> The Working Group Chair is concerned with making forward progress through a fair and open process, and has wide discretion in the conduct of WG business. The Chair must ensure that a number of tasks are performed, either directly or by others assigned to the tasks.

This document proposes an extended set of Document Shepherd tasks, well beyond those covered in RFC 4858. In many cases it will be reasonable to assign the entire Document Shepherd Function to one person (to a Chair or to a non-chair delegate), but in many other cases the Chairs will likely choose to delegate parts of that function and keep other parts for themselves. In any case, the Chairs remain responsible for the management of the working group; they are whom the Area Director (AD) will come to if something goes wrong or things fail to make progress.

As we talk, then, about what the "Document Shepherd" does, understand that the individual doing each particular task will be the one assigned that task as the work on a particular document is laid out. When we say that the Shepherd should do a task in consultation with the Chairs, that's automatically true when it's already a Chair who's doing it.

And this bears repeating: Nothing in this document is suggesting that the Working Group Chairs abdicate any responsibility. They have the final responsibility for managing each document's progress and for managing the working group in general. Any Chair who chooses to delegate some of this responsibility must still ensure that it's carried out properly. And any Chair who does not feel comfortable delegating any of this should not do so. Of course, either way, the Chair has to answer to the working group and the responsible Area Director if the work lags.

# Stages in a Document's Lifecycle

From the time a working group is asked to take on a document as one of its work items, the document will go through a number of stages, most of which correspond closely to working group document states (RFC 6174) or IESG document states in the datatracker (see [the mapping table below](#lifecycle-stages-and-corresponding-document-states)):

1. Call for Adoption
2. Working Group Document
3. Working Group Last Call
4. Shepherd Writeup Underway
5. AD Evaluation
6. IETF Last Call
7. Waiting for AD Go-Ahead
8. IESG Evaluation
9. Approved by the IESG  
10. In RFC Editor Queue
12. AUTH48
13. Published

Through most of those stages steps will have to be taken, tasks will need to be performed, to make sure the document moves forward, that consensus is reached, that the right reviews are done, that updates are made, that consensus still holds after significant changes, and so on. The Document Shepherd Function comprises that set of tasks, and the document shepherd works with the Chairs as needed, and to have the datatracker state changes recorded.

The following sections will discuss some of the tasks needed at each stage, and will suggest how Working Group Chairs might handle those tasks and their delegation -- how the Document Shepherd Function might work. The details will vary, depending upon how each working group is managed, but what follows should be a good example, and will provide a basis for adaptation. And see also RFC 4858, Section 3.

## Preparing for Adoption and Shepherding

At the point that the working group begins considering adoption of a document, the Working Group Chairs have some decisions to make, beginning with confirming that the document is within the scope of the working group's charter. This is the time to choose a Responsible Chair for the document, much as it will eventually have a Responsible Area Director later in its life. The Responsible Chair will be the one who oversees the Document Shepherd Function and has primary responsibility for making sure that everything gets done.

The Responsible Chair should then (perhaps in consultation with the other Chair(s), depending upon the Chairs' agreement about division of work) decide how much of the Document Shepherd Function to handle herself, and which pieces, if any, to delegate. Examples might be as follows:
* The Responsible Chair will be the sole Document Shepherd.
* The Responsible Chair will be the Document Shepherd through the end of the Working Group Document stage, and will appoint a non-chair Shepherd during that stage to handle subsequent shepherding tasks (similar to what's set out in RFC 4858).
* The Responsible Chair will appoint a non-chair Shepherd to handle the early shepherding tasks, and the Responsible Chair will take over the Document Shepherd tasks for Working Group Last Call and beyond (the converse of the previous example).
* The Responsible Chair will appoint a non-chair Shepherd to handle all shepherding tasks from start to end.  The delegate will work closely with the Responsible Chair, heavily supervised (perhaps this is a training situation).
* The Responsible Chair will appoint a non-chair Shepherd to handle all shepherding tasks from start to end.  The delegate will report to the Responsible Chair, and will be supervised at certain key points.
* The Responsible Chair will appoint a non-chair Shepherd to handle all shepherding tasks autonomously (perhaps for a very experienced Shepherd, well trusted by the Chairs).

And so on... there may be many combinations, many levels of supervision vs. autonomy, many ways to divide the work. It's also possible to delegate to more than one non-chair Shepherd at different stages. The Chairs need to judge the extent to which continuity and centralized responsibility are important for the document in question and the management style of the chairs, and whether making it one other person (supervised by one Responsible Chair) is best.

In choosing Shepherds, the Chairs should be alert to real and perceived conflicts of interest, and should make the appointment of Shepherds and the work they do as open a process as is reasonable within the management of the working group. Chairs need to be comfortable with the Shepherds they appoint; at the same time, appointing the same shepherds for every document might not be the best choice. Consider balance, and use this as an opportunity to distribute responsibility.

Some Chairs may prefer to handle all tasks themselves, because, after all, they remain formally responsible for their successful completion. Yet there can be a lot gained by delegating much of the work. Delegating work and giving a degree of responsibility to relatively more junior participants gets people more closely engaged with the working group and with the IETF. Giving significant responsibility can be an excellent training exercise, preparing participants to take on future roles as Working Group Chairs. And in a busy working group, offloading work from the Chairs to senior, experienced people can prevent the Chairs from being overcommitted, enabling the work to move forward much more efficiently.

This document will often talk about the Shepherd making certain decisions and judgments, such as judging consensus. It's important to keep in mind that when the Shepherd is not one of the Chairs (when the function is delegated), these judgments take the form of advice to the Chairs, and that the Chairs have the formal responsibility for making process-related decisions and for judging consensus. Any appeals will always be made with respect to decisions by the Chairs.

And, of course, a non-chair Shepherd can and should consult with the Responsible Chair whenever she feels the need, and certainly whenever issues arise of which the Chairs should be aware, or about which the Shepherd needs advice or other help.

Communication with the Shepherd is often dependent upon having the correct email address in the datatracker. It would be good, especially if the Shepherd is not a Chair, to check that the Shepherd's email address in the datatracker is correct and current.

Tasks that need to be taken in preparation might be as follows:
1. Chairs: Confirm that the document falls within the working group's charter.
1. Chairs: Select a Responsible Chair to handle the document.
1. Responsible Chair: Decide on a work/delegation plan.
1. Responsible Chair: Possibly appoint a non-chair Shepherd; else the Responsible Chair becomes the Shepherd.
1. Check that the Shepherd's email address in the datatracker is correct.

## Stage: Call for Adoption

Once it is determined who will handle the Document Shepherd tasks, the Shepherd needs to do the actual adoption process. The details will vary based on how the particular working group is run, but a typical process will start with posting a call for adoption to the working group mailing list, pointing to the individual draft that's being considered. There'll be a comment period for adoption discussion, after which the Shepherd will, based on working group discussion, give a recommended judgment to the Chairs.

Often, working groups are chartered with a startup document list, and specific calls for adoption are not needed. In those cases, the Shepherd will not need to handle a call and comment period, and can begin with the next paragraph.

Assuming that the document was adopted, the Chairs will appoint one or more Editors for the working group version of the document (these are often, but not always, the same people who wrote the individual version, and the Chairs should put some thought into who the right Editors should be), and will handle the datatracker updates (for which Chair access is required). The Chairs should not forget to record the name and email address of the Document Shepherd in the tracker -- this will ensure that the Shepherd is copied on necessary email later.

In summary, the tasks at the Call for Adoption stage might be as follows:

1. Shepherd: Make the call for adoption; set deadlines and schedule.
1. Shepherd: Communicate the result to the Chairs;
1. Chairs: Announce the result and appoint Document Editor(s) for the WG document.
1. Chairs: Update the datatracker; approve -00 version submission.

## Stage: Working Group Document

Once a -00 version is posted, the Shepherd's primary task is to keep the document moving forward: keeping discussion going, making sure issues are tracked and document updates are posted, and helping things toward consensus. Let's not downplay the importance of active management here: this is where things so often fall short, what causes documents to take **years** to complete. The Shepherd should not rush discussions that are useful, but the Shepherd should make sure that things don't get lost in the forest either.

The Chairs will decide how the working group should be managed, and any non-chair Shepherd should be working with the Chairs at this stage, communicating any difficulties and getting help with issue resolution when needed. Tools such as the issue tracker and the working group wiki, which are available to every working group, may be helpful here -- particularly if many issues come up, if issues are often taking a long time to be resolved, or if the same issues tend to come up repeatedly.

The issue tracker can be used to record not just the issues themselves, but significant parts of the discussion on both sides, helping to make it clearer what the resolution was and why, and whether a particular request to re-open a closed issue really involves new points or is just a re-hash. This is also a good time to record implementation and interoperability information in the working group wiki, along with any other information that will be helpful to the community and the IESG when the document comes out of the working group.

When implementations are proceeding in parallel with document development, it is sometimes useful to get early allocation of protocol parameters and code points (RFC 7120). The Shepherd should watch for those situations and raise the issue with the working group, bringing the request to the Chairs and responsible AD if it's decided that early allocation is needed.

Discussions need to be steered, with a goal of avoiding unproductive, circular discussions, re-hashing of old arguments, and tangential discussions that go "off into the weeds". Discussions also often need to be prodded. Lulls can be fine, but when it looks like nothing is happening for a while, remind the participants of open issues, ask for reviews of updated document versions or of recent changes that don't seem to have been discussed. It's often useful to make specific requests of participants off list, not just relying on sending "please review" messages to the list. The goal here is to ensure that rough consensus is reached on the document, covering as much of the document as possible, and certainly covering the key points. See RFC 7282 for a detailed discussion of rough consensus in the IETF.

Document Editors need to be prodded as well. We're all volunteers, and many of us are working on a lot of things. A particular document can fall off to the side for a long while. It's best to avoid the trap of getting updates only before each IETF meeting, just in time to beat the submission cutoff. If updates aren't posted fairly promptly after a set of issues is resolved, ask the Editors when they'll be able to get changes rolled into a new document version. Check that the Editors are following working group consensus as they make their updates.

Even with plenty of prodding and reminding and steering, it sometimes happens that a document simply can't be finished and abandoning it needs to be considered. Perhaps there's no longer the interest there was at adoption. Perhaps the document has been overtaken by other events. Or perhaps there's too much controversy over it, and rough consensus just isn't going to happen. The Shepherd should consult with the Chairs to decide whether the working group should stop work on the document.

The Shepherd will know when the document is moving from this stage into the next, and when she needs to shift the focus into preparation for last call and for getting the document to the AD.

In summary, the tasks for the Shepherd at the Working Group Document stage might be as follows:

1.  Work with the Chairs to understand the desired mechanism for managing discussions.
1.  Watch the discussions as they unfold; call out and record specific issues that come up.
1.  Steer the discussion when necessary.
1.  Prod the discussions when necessary.
1.  Prod the Document Editors when necessary.
1.  Use appropriate tools, such as issue trackers and wikis.
1.  Consider early IANA allocation and bring it up for discussion if appropriate.
1.  Determine when it's time to start wrapping things up and moving to Working Group Last Call, and advise the chairs.
1.  Alternatively, determine that it's not possible to move the document forward, and the Chairs need to consider abandoning it.

## Stage: Working Group Last Call

When any contentious issues have been resolved and the document has had a good level of review, the Shepherd should start looking at when it's time to wrap things up, have a last call within the working group, and get the document ready to send to the Responsible AD. What needs to be done now is largely the same as in the Working Group Document stage, but with a particular aim of getting remaining issues closed and making sure that discussions are tightly focused. Where veering off to explore things that might be added to the document was a fine thing to do in the earlier stages, this is the time to say that the document is "feature complete", and to keep discussions reined in.

Working Group Last Call is a recommended step, though not a required one (it is not part of the formal process), and most working groups do issue a formal "last call" before sending the document to the Responsible AD. The Shepherd, in consultation with the chairs, can take the responsibility of issuing that message and of analyzing comments to determine whether things are ready to go ahead.

This is also the time to make sure that important reviews are done. Ask for reviews from key working group contributors, and check whether any external reviews are needed. External reviews might include expert reviews for IANA registrations (some registrations require early review on specific mailing lists), reviews of formal specifications such as MIBs, XML, and ABNF, and reviews from experts in other areas (does the document need to be checked by a web services expert, a security expert, a DNS expert?). Some of this will happen automatically later -- there will be a Security Directorate review at some point, for example, and IANA will formally kick off expert review during Last Call -- but it's easier on the Document Editors and the working group if you know something is particularly necessary and arrange for it sooner. The IANA folks are willing to do an early review of the IANA actions at this stage, so consider asking for that if the document has a large or unusually involved set of IANA actions.

The [shepherd writeup](http://www.ietf.org/iesg/template/doc-writeup.html), which can be found in the IESG section of the IETF web site, is a good reference for the Shepherd for making sure the necessary bits are being covered, so this is also a good time to start the writeup. It will be finished later, when the document is ready to be sent to the Responsible AD, but getting a start now can be helpful, and will serve as a reminder to ask the questions and request the reviews that will later be needed.

The tasks for the Shepherd at the Working Group Last Call stage might be
as follows:

1. Issue an official "Working Group Last Call" message on the list, with a reasonable deadline given.
1. Closely watch the reviews and discussions at this stage, and make sure they are focused on closing final issues and giving the document final review.
1. Specifically ask (perhaps off list) for key reviews.
1.  Begin preparing the shepherd writeup, and request any external reviews that will be needed.
1.  Analyze the results of Working Group Last Call and get final updates from the Document Editors.

## Stage: Shepherd Writeup Underway

Working Group Last Call is over, and the Shepherd and Chairs have determined that any issues that came out of that have been adequately resolved. It's time to finish up the shepherd writeup, dotting the last of the "i"s and crossing the final "t"s.

Remember that the shepherd writeup serves two major purposes:

1.  It ensures that some key items have been double checked.
2.  It provides information to the IESG, which is useful during IESG Evaluation.

For the first purpose, "yes" and "no" are reasonable answers to some of the writeup questions. In particular, a number of the questions ask if something has been checked, or it some abnormal situation exists. "Yes" to confirm that the check has been made, or "no" to state that the abnormal situation does not exist are fine responses. Of course, if the answer to the first is "no" or to the second is "yes", further explanation is necessary. In other words, "yes" could be a reasonable answer by itself, but "no" would require more by way of explanation... or vice versa.

But for the second purpose, providing useful information to the IESG, yes/no responses are often of little or no use. Questions about the working group process and discussions are especially looking for some sort of narrative information. Don't just say that there was much discussion that eventually reached consensus, or that there were a number of controversial points that were resolved -- say something about the discussion, talk a bit about the controversies. If there were particular points that simply did not get any discussion but probably should have, say that.

When the Shepherd has the writeup done, a non-chair Shepherd should consult with the Chairs to make sure they're happy with it and agree with what's in it. The Chairs will then need to make some datatracker updates that only they have authorization for: they will upload the writeup to the tracker and change the document state.

When the Shepherd has the writeup done, a non-chair Shepherd should consult with the Chairs to make sure they're happy with it and agree with what's in it. The Chairs will then need to make some datatracker updates that only they have authorization for: they will upload the writeup to the tracker and change the document state.

Changing the document's working group state to "Submitted to IESG for Publication" will trigger the necessary email messages and IESG state changes, and will get the document into IESG "Publication Requested" state, from which the Responsible AD will begin her processing of the document. And as RFC 4858 says, the Shepherd should also email the writeup to the working group's mailing list, so the working group is aware of it. The writeup will be public anyway, because it will be in the datatracker, so it can only help the open process to make it more visible to the working group whose work it reflects.

See also RFC 4858), Section 3.1, but note that the writeup template has changed significantly since the version in that document. The [current writeup](http://www.ietf.org/iesg/template/doc-writeup.html) is in the IESG section of the IETF web site.

The tasks at the Shepherd Writeup Underway stage might be as follows:

1. Shepherd: Complete the shepherd writeup and send it to the Chairs for approval.
1. Chairs: Work with the Shepherd to finalize the writeup.
1. Chairs: Put the writeup into the datatracker, and change the tracker document state to the appropriate one for requesting publication.
1. Shepherd: Send the writeup to the working group mailing list and inform the working group that publication has been requested.

## Stage: Area Director Evaluation

The next stage in the process is up to the Responsible Area Director, and the Document Shepherd has but one easy task: help make this stage as short as possible. The Responsible AD or the IESG Secretary will do some document state changes in the datatracker (to Publication Requested and then to AD Evaluation), and the AD will review the document and either request IETF Last Call or respond to the authors (and, we hope, to the Shepherd as well; here's where it was useful to have put the Shepherd's email address in the tracker) with review comments and suggestedchanges. In the latter case, the document's state might change to "AD Evaluation, Revised I-D Needed".

The Shepherd needs to watch for the key state changes and the AD's review. If the review doesn't happen in a reasonable time -- allowing for a busy AD's schedule and remembering that the document you're shepherding isn't the only one on the AD's docket -- send a reminder...perhaps as a question, "How is the review on !draft-ietf-frobozz-xyzzy coming?" Use your judgment to decide how long to wait, but most ADs will appreciate a reminder here and there as long as it's not at the level of
"pestering".

Once the review comes in, make sure the Document Editors are on top of it and respond in a timely manner. Make sure that the working group is consulted on issues brought up in the review that are significant enough to require the working group's engagement in the response. Editorial tweaks can arguably be handled by the editors alone at this point, and changes to the protocol clearly need to go back to the working group,
but many issues fall in between, and good judgment is important. The Chairs should be involved in deciding where the line is drawn.

Many documents spend \*months\* in AD Evaluation state, largely because of lack of good shepherding. It may look like there's only one major task here, but it's an important one. Please don't give it short shrift.

See also RFC 4858, Section 3.2.

The tasks for the Shepherd at the AD Evaluation stage might be as follows:

1.  Make sure the AD reviews the document in a timely manner, and send occasional reminders as needed.
1.  Make sure the Document Editors respond to the review in a timely manner, and poke them as well, as needed.`  
1.  Keep the dialogue going between the Responsible AD and the editors until all issues have been dealt with and the document is ready for the next stage.
1.  See to it that issues are brought back before the working group if they are significant enough to require it.

## Stage: IETF Last Call

Once the Responsible AD is satisfied that the document is ready to move ahead, she will put it in Last Call Requested state. That prompts the IESG Secretary to send out the Last Call announcement and to put the document into "In Last Call".

The Shepherd's job in the IETF Last Call stage is very similar to what's needed in AD Evaluation. Start by watching for last-call comments, including various special reviews. Reviews will come in from the Security Directorate and the General Area Review Team (GenART), and some may also come from other review teams and directorates. Reviews might also be coming in at this stage, if they haven't already, that were specifically requested by the Shepherd (see the Working Group Last Call stage in Section 3.4).

The Shepherd needs to make sure all of those reviews are addressed by the document editors, and that the specifically requested reviews get done. "Addressed" doesn't mean that every change asked for in every last-call comment needs to be made. Sometimes, a reasonable response is to say that the working group discussed the point, and the document correctly reflects its consensus -- that is, the working group disagrees with the last-call comment. At other times, it's reasonable to disagree with the reviewer and look for any other support for the reviewer's position. Rough consensus can be a tricky thing (RFC 7282), but the bottom line is that all comments need at least be considered. Directorate and review-team reviews, in particular, require acknowledgment and response (though they, too, can be disagreed with).

Throughout the IETF Last Call stage, as well as in the upcoming IESG Evaluation, it is important that the working group be kept aware of the changes that are being made to their document. Continued use of the issue tracker is a useful way to do that. For especially significant changes, explicitly calling the working group's attention to them on the mailing list is a good idea. It's very important to continue transparency into these later stages of the process.

During Last Call, IANA will review the document's IANA Considerations, will respond with their summary of what they think needs to be done by IANA after the document is approved, and will ask any questions they have. The Shepherd should watch for this review and make sure that the actions IANA proposes are correct and that any questions they have are answered. At this point, IANA will also contact any Designated Experts required to formally approve any registrations, so it will help if the shepherd has done the necessary preparatory work (see Section 3.4). See also RFC 4858, Section 4.

Different Responsible ADs will have different preferences for whether documents in IETF Last Call should be updated while they're still in that state. The Shepherd should check with the AD and advise the Document Editors. Sometimes it's best to keep a stable version throughout last-call review; other times it's better to get changes posted quickly, so the same issues aren't brought up by multiple reviewers. Work with the AD and the editors to handle this.

The tasks for the Shepherd at the IETF Last Call stage might be as follows:

1.  Monitor the last-call comments, and make sure that specifically  requested reviews arrive.  
2.  Make sure the Document Editors respond to all reviews and  comments in a timely manner.  
3.  Keep the dialogue going between the community and the editors  until all issues have been dealt with.
4.  See to it that issues are brought back before the working group if they are significant enough to require it.

## Stage: Waiting for AD Go-Ahead

When Last Call completes, the tracker state for the document will automatically go to "Waiting for AD Go-Ahead". This is the Shepherd's signal to re-check the comments from last call, to make sure an updated I-D is posted that is ready for IESG Evaluation, and to let the Responsible AD know when everything is set. The AD will be watching for this as well, but, as in the other stages, it's the Shepherd's responsibility to keep an eye on things and make sure what's needed gets done.

This is also a good time to remember that the document shepherd writeup is not static. If significant time has elapsed, significant discussion has happened, or significant changes have been made, it's a good idea to work with the Chairs to update the shepherd writeup in the datatracker, making sure that delays, discussions, and major changes are outlined inthe writeup for the IESG.

The Responsible AD has some manual work to do here: she must record the IETF consensus in the datatracker, move the document into IESG Evaluation, issue an IESG ballot for the document, and schedule the document on an IESG telechat agenda. The Shepherd should watch for this and make sure the Responsible AD is on top of it.

The tasks for the Shepherd at the Waiting for AD Go-Ahead stage might be as follows:

1.  Make sure a new I-D is posted with the latest changes, and inform the Responsible AD that all changes have been incorporated and that the document is ready for IESG Evaluation, or...
2.  ...inform the Responsible AD that no changes are required and that the document is ready for IESG Evaluation.
1.  Update the Shepherd writeup if anything has come up during Last Call that the IESG should know about.  The Chairs will update the writeup in the datatracker.
1.  Follow up with the Responsible AD if necessary, to make sure she takes the necessary steps to enter IESG Evaluation.

## Stage: IESG Evaluation

As the ADs do their reviews they will record ballot positions on the document. Ballot positions can be one of "Yes", "No Objection", "Discuss", and "Abstain" (there's also "Recuse" for cases when the AD has a conflict of interest with the document, if, for example, the AD is one of the authors/editors). Any of these ballot positions can be accompanied by non-blocking review comments, and "Discuss" also comes with blocking comments in addition—these must be resolved to the satisfaction of the Discussing AD before the document can be approved by by the IESG. The document will be scheduled for a bi-weekly "telechat" (at the time of this writing they're on Thursdays), and it will be approved then or left in one of several follow-up states.

The IESG Evaluation period is normally somewhere between one and three weeks, though it can be as little as a few days in unusual circumstances. Be aware, though, that there's usually a burst of review activity in the final few days before the telechat, and expect most reviews to come in then.

The IESG Evaluation comments and DISCUSS positions will be copied to the Document Shepherd (again, it was important to have put the Shepherd's email address in the tracker), and the Shepherd should be watching for them and making sure that the Document Editors respond promptly -- at this stage, quick turnaround is most important. Sometimes the Shepherd or Chairs might respond to AD questions and comments themselves, and sometimes they might leave it to the editors. The process works best when everyone engages, with the goal of resolving the issues brought up by the ADs as efficiently as possible.

A word about DISCUSS positions: Many Document Editors treat these as adversarial situations created by aggressive ADs, but that's generally not the intent. First, many DISCUSSes are resolved quickly and easily by a round of email with the Discussing AD, and that's as it should be: the point is that the AD has something to "discuss" with those responsible for the document before she can agree to the document's approval.

Second, many DISCUSSes that do take more effort, often significant back and forth with the Discussing AD and other IESG members, result in a better document, having cleared up some significant confusion or having closed a hole in the specification that was missed at earlier stages.

Please try to treat the situation as one in which everyone is looking to make the document better.

Most often, ADs who record DISCUSS positions (and review comments) are quite responsive, and will work with the Editors and Shepherd to get everything resolved. Sometimes, though, a busy AD can find herself lacking the time to respond. The Shepherd should keep the ADs honest, pushing for quick responses. In earlier stages, too- frequent reminders might be considered unreasonable, but at this stage discussion should be fairly brisk, and a delay of more than a couple of days should be unusual, on either side.

Non-blocking IESG Evaluation comments should be treated as IETF Last Call comments are: the Document Editors should respond to them and do their best to address them, but failure to come to agreement on them will not block the document's progress.

And, as at other stages, the Shepherd should work with the Chairs to ensure that any changes of significance are brought back to the working group for their review before the final approval notice goes out.

The IESG web site has more details about [IESG ballot positions](http://www.ietf.org/iesg/voting-procedures.html) and about [IESG DISCUSS ballots](http://www.ietf.org/iesg/statement/discuss-criteria.html) in particular. And see also RFC 4858, Section 3.3.

The tasks for the Shepherd at the IESG Evaluation stage might be as follows:

1.  Keep track of the DISCUSS positions and review comments by the IESG.
1.  Make sure all comments are addressed, and help the discussions of DISCUSS positions reach closure.
1.  Keep both the Document Editors and the Discussing AD engaged in the resolution of the issues.`  
1.  See to it that issues are brought back before the working group if they are significant enough to require it.

## Stage: Approved by the IESG

Once the document has been on a telechat, any necessary revised versions have been posted, and all DISCUSS positions are "cleared", the Responsible AD (or the IESG Secretary) will put the document into the "Approved, Announcement to be Sent" state. If there's any follow-up that needs to be done, it will be held with a sub-state (usually "Point Raised, Writeup Needed"), and the Shepherd should make sure that whatever final checks are needed get done, and that the Responsible AD clears the sub-state and informs the IESG Secretary.

At this stage, it's usually a matter of making sure that the latest version of the document adequately addresses the non-blocking comments by the ADs. Final adjustments to the document will be made either by an updated draft (submitted by the editors) or by RFC Editor notes (entered by the Responsible AD, and not directly visible). The Shepherd should work with the Responsible AD to understand what still needs to be done and to make sure it happens, and to check on RFC Editor notes and make sure they're correct and that the working group is aware of them.

The tasks for the Shepherd at the Approved by the IESG stage might be as follows:

1. Work with the Responsible AD to understand what still needs to be addressed.
1. Double-check the IANA actions and ask the AD about any RFC Editor notes; follow up on any errors or omissions.
1. Make sure the Document Editors and the Responsible AD move the document to the final Approved state.

## Stage: In RFC Editor Queue

Shortly after the approval announcement is sent out, the document will go into the RFC Editor queue, and the Shepherd will start seeing it pass through a number of RFC Editor states. For most of this, the Shepherd need do nothing, and is just waiting for the AUTH48 state. This will usually take between a few weeks and a few months, depending upon many factors, but it can be held up indefinitely by normative references to documents that are not yet ready for publication. Be aware of what the document is waiting for, and otherwise just wait. If anything looks odd, ask the Responsible AD to check.

Watch particularly for states that indicate that IANA is waiting for something, and be aware of likely timing on missing references (RFC Editor "MISSREF" states). For the former, make sure that IANA gets the responses they need. For the latter, consider alternatives in cases where missing references are likely to cause significant delays that might be avoided by using different references. Consult with the Chairs and Responsible AD if it seems that some action would be useful.

Also watch for questions from the RFC Editor, which occasionally come during their editing process, before AUTH48. Make sure the authors give timely responses, and keep the working group informed about anything that seems substantive.

The tasks for the Shepherd at the In RFC Editor Queue stage might be as follows:

1.  Sip tea or drink beer or wine, and wait for AUTH48.
1.  Talk to the Responsible AD if something doesn't look right.
1.  Watch for questions from the RFC Editor, and track the responses.

## Stage: AUTH48

AUTH48 is an RFC Editor state that occurs when the RFC Editors have done their final edits on the document before publication. It's meant to represent a 48-hour period in which the AUTHors can review what the RFC Editor has changed, have a final look at the document, and make sure it's ready to go.

AUTH48 is a critical document state; do not downplay its importance. At this stage, the Shepherd should re-review the document, paying special attention to recent changes. The Document Editors must do the same, and a response from every Author/Editor listed at the top of the document is required before the RFC Editor will finish the publication process. The Document Shepherd needs to make sure that the Editors all respond, and should take the lead in prompting them early and frequently. Remember that "AUTH48" is meant to refer to 48 hours, not 48 days. Don't let this drag on.

The RFC Editor will often have questions that the Authors/Editors need to answer. The Document Editors often have minor changes to insert at this point. The Shepherd should consider those answers, those changes, and the changes the RFC Editor has made leading into AUTH48, and assess, in consultation with the Chairs and the Responsible AD, whether any changes need to be passed back to the working group—remember that the document has been approved by rough consensus of the working group, and then of the IETF as a whole, and the final, published version must continue to reflect that consensus.

It's unusual for there to be significant controversy at this stage, but it's been known to happen. Sometimes a change or a question by the RFC Editor will raise a question with the Document Editors that had not come up before. Sometimes, the right answer to one of those questions will be more than just editorial, and sometimes it will involve a significant technical decision. Decisions of that nature should not be made by the Document Editors alone, and the Shepherd should arrange with the Chairs to have those issues discussed by the working group.

If there are changes the RFC Editor thinks the responsible AD needs to approve, they will flag those changes and ask the AD for approval. It's easy for ADs to miss those—they expect this stage to be pretty routine—so it's important to make sure the AD is aware that a response is needed. Watch for such items and remind the AD if there's no response within a few days.

Most of the time, though, this stage will run smoothly, the Document Editors will respond to the AUTH48 messages with a minimum of prodding, and the RFC Editor will announce their happiness and proceed with the publication process.

See also Section 5 of RFC 4858.

The tasks for the Shepherd at the AUTH48 stage might be as follows:

1. Monitor the AUTH48 process and make sure all questions are answered and all Authors/Editors respond as needed.
2. Assess whether any issues that come up are significant enough to  need review by the working group.

## Stage: Published

We're done. The RFC Editor has published the document, and the RFC announcement has been made. Many thanks to the Shepherd for having seen it through and for helping to assure a high quality document.

# Some Final Notes

We have outlined a Document Shepherding Function, above, in a lot of detail, so let's put the executive summary back here:

What it all boils down to is setting up one person who takes responsibility for following the progress of a document from Call for Adoption through Publication, staying actively involved with managing the discussion and issue resolution at every stage, and making sure the necessary participants are responsive and that things don't languish from inattention.

And again, Working Group Chairs may delegate all or part of this function to a non-chair participant, or retain all responsibility for it themselves. In the latter case, what is described here is nothing different to what should be happening already. Setting it out as clear tasks and a set of stages in the document's lifecycle will make it easier to recognize what needs to be done when, and to handle delegation when the Chairs choose to delegate.

# Acknowledgments

The first version of this was written by Barry Leiba. Many thanks to Murray Kucherawy and Allison Mankin for early review and many particularly helpful comments.

# References

Bradner, S., ["IETF Working Group Guidelines and Procedures", BCP 25, RFC 2418](https://datatracker.ietf.org/doc/rfc2418/), September 1998

Levkowetz, H., Meyer, D., Eggert, L. and A. Mankin, ["Document Shepherding from Working Group Last Call to Publication", RFC 4858](https://datatracker.ietf.org/doc/rfc4858/), May 2007

Juskevicius, E., ["Definition of IETF Working Group Document States", RFC 6174](https://datatracker.ietf.org/doc/rfc6174/), March 2011

Cotton, M., ["Early IANA Allocation of Standards Track Code Points", BCP 100, RFC 7120](https://datatracker.ietf.org/doc/rfc7120/), January 2014

Resnick, P., ["On Consensus and Humming in the IETF", RFC 7282](https://datatracker.ietf.org/doc/rfc7282/), June 2014

IESG, ["IESG Ballot Procedures", May 2009](http://www.ietf.org/iesg/voting-procedures.html)

IESG Statement, ["DISCUSS Criteria in IESG Review", July 2007](http://www.ietf.org/iesg/statement/discuss-criteria.html)

IESG Statement, ["IESG Statement on Document Shepherds", October 2010](http://www.ietf.org/iesg/statement/document-shepherds.html)

IESG, ["Working Group Submission Writeup", February 2014](http://www.ietf.org/iesg/template/doc-writeup.html)

# Lifecycle Stages and Corresponding Document States

| Lifecycle stage | Document state | State owner | 
| --- | --- | --- | 
| Call for Adoption | Call for Adoption by WG Issued | WG |
|Working Group Document | WG Document | WG | 
| Working Group Last Call | In WG Last Call | WG | 
| Shepherd Writeup Underway | WG Consensus: Waiting for Writeup | WG |
| AD Evaluation | AD Evaluation | IESG | 
| IETF Last Call | In Last Call | IESG | 
| Waiting for AD Go-Ahead | Waiting for AD Go-Ahead | IESG | 
| IESG Evaluation | IESG Evaluation | IESG | 
| Approved by the IESG | Approved-announcement to be sent | IESG | 
| In RFC Editor Queue | RFC Ed Queue | IESG | 
| AUTH48 | AUTH48 | RFC Editor | 
| Published | RFC Published | RFC Editor |