---
title: Formatting and Content of IETF Working Group Agendas and Minutes
description: This document provides suggestions about the form and content of Working Group agendas and minutes.
published: true
date: 2021-12-16T15:33:18.805Z
tags: 
editor: markdown
dateCreated: 2021-12-16T15:29:24.352Z
---

[RFC 2418](http://rfc-editor.org/rfc/rfc2418.html) outlines the procedures for IETF Session operation. However, it contains little information about post-IETF meeting working group chair responsibilities. In particular, it provides little guidance with respect to either form or submission deadlines for the artifacts of the meeting, namely, session minutes and presentation materials. This document addresses these issues and provides suggestions about the form and content of Working Group agendas and minutes. The use of the templates is not mandatory and the guidance herein may be safely ignored.

# Table of Contents

1.  Introduction
2.  Agendas
    2.1.  Agenda Content and Formatting Considerations
        2.1.1.  The Header
        2.1.2.  The Body
    2.2.  Submission Procedure and Deadlines
3.  The brief meeting report
4.  Minutes
    4.1.  The Purpose of Session Minutes
    4.2.  Minutes Content Considerations
    4.3.  Minutes Formatting Considerations
        4.3.1.  The Header
        4.3.2.  The Body
        4.3.3.  Length of Submitted Minutes
    4.4.  Encoding
    4.5.  Submission Procedure and Deadlines
    4.6.  Minutes Errata -- Correcting Mistakes
5.  Other meeting materials such as presentations
    5.1.  Encoding
    5.2.  Submission Procedure and Deadlines
    5.3.  Presentation Errata -- Correcting Mistakes
6.  Acknowledgments
7.  Security Considerations
8.  IANA Considerations
9.  References
    9.1.  Normative References
    9.2.  Informative References

Appendix A.  Templates
    A.1.  Agenda Template
    A.2.  Minutes Template
§  Authors' Addresses

# 1.  Introduction
Section 3.1 of RFC 2418 [RFC2418] (Bradner, S., "IETF Working Group Guidelines and Procedures," September 1998.) outlines the procedures for IETF Working Group operation. However, it contains little information about post-IETF meeting working group chair responsibilities. In particular, it gives little guidance with respect to either form or submission deadlines for the artifacts of the session, namely, working group minutes and presentation slides. This document provide that guidance together with a few templates that may assist the reader in constructing the artifacts. The use of the templates is not mandatory and the guidance herein may be safely ignored.

# 2.  Agendas

RFC 2418 section 3.1 defines a clear role for the agenda as part of the session planning. It states: 

> For coordinated, structured WG interactions, the Chair(s) MUST publish a draft agenda well in advance of the actual session. The agenda should contain at least:
> - The items for discussion;
> - The estimated time necessary per item; and
> - A clear indication of what documents the participants will need to read before the session in order to be well prepared.

This mandate serves a number of needs. It allows working group chairs to carefully optimize the meeting time. Presenters know well in advance how to tailor their presentations to the allocated time and participants know what material to read in order to come prepared. In addition, a good agenda can act as a checklist for the for the chairs during the meeting.

## 2.1.  Agenda Content and Formatting Considerations

There are a couple of considerations that can help one to produce an agenda that serves everybody's needs. One will always have to try to make trade-offs between the size of the formatted document and the amount of detail to add. This document suggests some content and some hints to present this content in a uniform way. According to ( "Submitting Meeting Materials for IETF Working Group and BOF Sessions," Jan 2006.), agendas can be submitted in HTML and TXT encoding. Since a clearly formatted agenda can be used as a template for the construction of the minutes one should clearly structure the source text. When submitting HTML you could consider ``<pre>`` tags to preserve the formatting.

### 2.1.1.  The Header
To unambiguously identify the agenda the header should at least contain the name of the working group and its acronym and the IETF meeting to which this meeting relates.

By adding some standard information to your header the agenda can be used as a 'one-stop-shop' for all information regarding the meeting. Consider adding the location and time of the meeting, pointers to the jabber room, pointers to audio- or web-cast and a pointer to the working groups web pages. This document provide that guidance together with a few templates that may assist the reader in constructing the artifacts. The use of the templates is not mandatory and the guidence herein may be neglected. Versioning the agenda is also a recommended practice. Finally, don't forget to add the contact information of the chairs.

Try to separate the header from the rest of the agenda with a "graphical" element such as a line of "="-signs when the agenda is encoded in TXT or the ``<hl>`` when the agenda is encoded in HTML.

Figure 1 (Agenda Section Header) provides an example Agenda Section Header.

     Formatting of IETF Workflow Documents Group (FIWD) AGENDA

     Meeting : IETF202, Monday 34 November 2032.
     Location: Fargo Hilton, Coens room, 12:30-14:00.
     Chairs  : Bert <bert@example.com>, Ernie <ernie@example.com>
     Jabber  : FIWD@jabber.ietf.org
     URL     : http://tools.ietf.org/wg/FIWD/

     Agenda  : version 1.4 (draft)

     ==============================================================
Figure 1: Agenda Section Header

### 2.1.2.  The Body

The body of the agenda presents the structure of the meeting. In our experience the meeting can usually be split in 'topics'. The meeting-administrivia is one 'topic', the administrivia concerning the working group documents is another 'topic'. By trying to structure the agenda by 'topic' a chair brings structure to the meeting. Stated from a meeting-centric point of view: The structure of a meeting should be represented in the agenda.

For each topic there will be a number of sub-topics. All subtopics have a title, and in the most common case, somebody to speak for them. If there is reading material such as an internet-draft a reference should be supplied. For each subtopic you should indicate how much time is allocated.

When refering to an internet-draft please use the full name inclucing the version number and extention e.g. draft-ietf-fiwd-pnum-centr-02.txt.

Note that it often happens that people want to be in the room for a particular topic. By also indicating the total time allocated to a topic one can allow participants to selectively join rooms.

Try to format topics and subtopics so that they can be clearly distinguished. Indentation and or 'section numbers' are handy formatting tools. Introducing a topic with one or two lines may help to identify what the intended goal of the discussion is.

We suggest that you always include "Meeting Administrivia" as a topic. By explicitly sub-topics like "Previous Minutes", "Scribe" and "Blue Sheets" a chair can be sure those topics are addressed.

When using HTML to encode the agenda we suggest you put in links to the document and use a short notation. When using text, consider that you have to trade off writing out complete URLs (in order to facilitate cutting and pasting) versus the conciseness of using only draft names. Figure 2 (Example Agenda Body) provides an example Agenda Body.


    A. Meeting Administrivia                 chairs        (total: 5 min)

        - Mailing list and URL
        - Minutes Scribe
        - Jabber Scribe
        - Blue Sheets
        - Previous Minutes

    B. Stalled Work                          chairs        (total:10 min)

       Documents that have not seen anything happen. Status update
       and proposed way forward.

        - draft-ietf-fiwd-handwritten-minutes-12.txt
        - draft-ietf-fiwd-agenda-over-sms-02.txt
        - discussion

    C. Page Numbers                                        (total:  30 min)

       Several proposals on page numbering have been put forward.

       We will have to make a choice based on requirements.

       (draft-ietf-fiwd-pnum-requirements-5.txt)

       - Page numbers at the center          Meyer         (10 min)
         draft-ietf-fiwd-pnum-centr-02.txt

       - Page numbers at the right           Kolkman       (10 min)
         draft-ietf-fiwd-pnum-right-06.txt

       - Page number strawman and chairs        (10 min)
         discussion

    D. Possible Work Items                                 (total: 15 min)

       D.1 XML based agendas and minutes.    Grover        (10 min)

           Work on development of a DTD for minutes
           and agendas.

          - draft-grover-fiwd-pnum-xml-workflow-docs-02.txt
          - Discussion                                     (5 min)

       D.2 (...)

    G. Working Group Administrivia                        (total: 10 min)

       G.1 Conclusion WGLC minutes translation   chairs  (3 min)

          - draft-ietf-fiwd-translation-05.txt

           Chair summarizes WGLC.
Figure 2: Example Agenda Body

## 2.2.  Submission Procedure and Deadlines

Submitting Meeting Materials for IETF Working Group and BOF Sessions is the authoritative source for the submission procedure and the deadlines. Note that submission of an agenda is mandatory.

# 3.  The brief meeting report

RFC 2418, section 6.1 instructs WG Chairs "to provide the Area Director with a very short report (approximately one paragraph on email) on the session". This information is used by the Area directors during the IETF week and is of most value when sent immediately after the session. The practice is not common for all areas so chairs should check with their ADs if they expect such report.

If the responsible AD for the WG requests them, then the chairs should consider to copy their working group on this report.

# 4.  Minutes

Section 3.1 of RFC 2418 mandates that "All working group sessions (including those held outside of the IETF meetings) shall be reported by making minutes available". And while there is a brief discussion of the desired content (note that this is not required content), including the session agenda, an account of the discussion including any decisions made, and the list of attendees, it gives little other guidance. Further, while the IETF secretariat maintains "instructions" web pages ([“Minutes for the IETF Proceedings,” 2005](https://www.ietf.org/chairs/wg-agendas-minutes-formatting-content/#MINUTES).), they provide only vague guidelines, and note that the format and content of the minutes is to be "is defined by the chair and minute-taker". As a result, IETF session minutes are of widely varying content and quality. In the following sections we suggest a format for IETF session minutes.

## 4.1.  The Purpose of Session Minutes

RFC 2418 states that "It is also good practice to note important decisions/consensus reached by email in the minutes of the next 'live' session, and to summarize briefly the decision-making history in the final documents the WG produces." Note that decisions reached during a face-to-face meeting about topics or issues which have not been discussed on the mailing list, or are significantly different from previously arrived mailing list consensus must be reviewed on the mailing list. This suggests the importance of the working group's minutes: while the working group minutes just reporting and critical record-keeping, there are times when a working group's minutes play an important role in signaling the subsequent confirmation process (post working group meeting) on the mailing list.

The suggestion here is that the purpose of the minutes is to summarize and document the history and activity (and in particular, any decision making activity) of the live meeting, both for those who could not attend, and for archival purposes. Thus timely submission of minutes, along with standardized format and quality, are essential to the operation of the IETF process.

The guiding principle behind the minutes, then, is that they must convey enough information to a non-attending reader to be able to review the meeting activity and understand the meeting outcome. In general, the minutes must be of sufficient detail and accuracy such that if an event cannot be understood to have happened from the minutes, then the event in question "did not happen" at the meeting.

## 4.2.  Minutes Content Considerations

In general, session minutes serve two main functions. First, they provide a record of the issues discussed during the meeting, and those participating in the discussions for those who weren't in attendance. Second, they provide a record that can be used to review decisions that were made (such as those items on which the WG has reached consensus, etc). As such, standardized format, as well as quality and completeness, are essential to the operation of the IETF process.

Note that it is important to record each draft which is discussed at the meeting, including its revision number, since the discussion needs to be placed in context. This includes drafts that have not yet been accepted as working group documents, and late revisions of working group documents. This is important as working group minutes are frequently used as a resource answering questions relating to prior art, as well questions about the state of the technical development of a protocol.

The main body of the Minutes section must be a prose description of the issues discussed at the meeting and any apparent conclusions reached in the room. Other material may be included as supporting documentation from the meeting -- for example, transcript-style notes ("A said," then "B said," then "C said"), or a detailed list of changes to a document. These should be included as attachments to, and not replacements for, the Minutes.

Finally, the minutes may include any other additional information that the working group chair deems appropriate as as appendices or attachments.

## 4.3.  Minutes Formatting Considerations

### 4.3.1.  The Header

In order to unambiguously identify the minutes they should, just like agendas, have a clear and unambiguous header. The content should at least contain the name of the working group, the IETF number, the date and time of the meeting and the name of the scribes. A version number is recommended. Figure 3 (Example Minutes Header) provides an example Minutes Header.

     Formatting of IETF Workflow Documents Group (FIWD) Minutes


     Meeting : IETF202, Monday 34 Noctember 2032.

     Location: Fargo Hilton, Coens room, 12:30-14:00.

     Chairs  : Bert <bert@example.com>, Ernie <ernie@example.com>

     Minutes : Elmo <elmo@example.net>

               Version 2

     ==============================================================
Figure 3: Example Minutes Header

### 4.3.2.  The Body

The minutes body should occur just below the minutes header. To improve readability, we suggest that details are skipped and only the main topics are listed. We suggest that the sub-topic structure is maintained in the minutes.

Try to format the text in such a way that topics and subtopics are clearly grouped. Start each (sub)topic with adding the names of document that have been discussed. A properly formatted agenda can easily be used as a template. Working group chairs could suggest minute takers to construct such a template from the agenda before the meeting.

Enumeration room consensus or actions for each topic is helpful.

Figure 4 (Example Minutes Body) contains an example of the formatting of a the body of a set of minutes for our imaginary working group. We try to present an example for a style that captures the gist of the meeting and a formatting that represents the structure of the meeting.

### 4.3.3.  Length of Submitted Minutes

Minutes should provide a thorough summary of the issues discussed during the working group/BOF sessions, and should be limited in size. As a guideline we suggest three pages of text per hour of meeting.

  =======================================================
  AGENDA
    A. Meeting Administrivia

    B. Stalled Work

    C. Page Numbers    D. Possible Work Items
       D.1 XML based agendas and minutes.
       D.2 (...)
    G. Working Group Administrivia
       G.1 Conclusion WGLC minute translation

  =======================================================

  MEETING Report
    A. Meeting Administrivia

       Elmo volunteered as scribe.
       Pino volunteered as jabber scribe.

       Minutes of the IETF201 where posted and finalized within 2
       weeks after IETF201. The minute takes is acknowledged.
       The room unanimously approved the minutes.

       There was one action item from IETF201, this is dealt with in
       item B of this meeting.

    B. Stalled Work
       Documents that have not seen anything happen. Status update
       and proposed way forward.
        - draft-ietf-fiwd-handwritten-minutes-12.txt
        - draft-ietf-fiwd-agenda-over-sms-02.txt

       The chairs explained that the document editors for these draft
       have changed their jobs and have requested to be resigned as
       editors. Volunteers have been called for on the list but nobody
       stepped forward. The chairs suggest that this work is dropped
       from the charter.

       Tarantino notes that this work has seen little activity except
       from the editors he wonders how this work ever made it on the
       charter. The discussion drifted into how handwriting can
       effectively be scanned. It was concluded by requesting the
       chairs to remove this work from the charter.

       Action on chairs: Have these drafts removed from the charter.

    C. Page Numbers
       Several proposals on page numbering have been put forward.
       We will have to make a choice based on requirements.
       (draft-ietf-fiwd-pnum-requirements-5.txt)

       - Page numbers at the center
         draft-ietf-fiwd-pnum-centr-02.txt

         Meyer presented his slides (see proceedings).

         During his presentation he stressed that that printing page
         numbers in the center of the page eases double sided
         printing.

       - Page numbers at the right
         draft-ietf-fiwd-pnum-right-06.txt

         Kolkman explained that during Meyers presentation that there
         are economic and environmental considerations in addition to
         the aesthetic principles on which the 'pnum-right' draft is
         based. The room hummed in consensus when the chairs suggested
         to document the economical issues in the 'pnum-centr' draft and
         the original requirements draft and then move to last call.

       - Page number strawman and discussion

         The strawman was not discussed. See above.

       Action on Meyer: update pnum-centr to document the economical
                        and environmental considerations of two-side
                        printing

    D. Possible Work Items                                 (total: 15 min)
     (...)
Figure 4: Example Minutes Body

## 4.4.  Encoding

(“Submitting Meeting Materials for IETF Working Group and BOF Sessions,” Jan 2006.) allows HTML encoded minutes. We suggest that TXT encoding is used except for those cases in which the working group chair wants to emphasize flow or other formatting.

In summary, the minutes for the IETF proceedings must be submitted in ASCII form, and formatted either in either plain text format or in HTML (where ``<pre>`` tags can be used to preserve formatting). That is, non-ASCII binary formats such as JPEG (“The JPEG Image Format,” 2005.) or executable code such as Java (“The JAVA Programming Language,” 2005.) must not be included in submitted minutes.

## 4.5.  Submission Procedure and Deadlines

(“Submitting Meeting Materials for IETF Working Group and BOF Sessions,” Jan 2006.) is the authoritative source for the submission procedure and the deadlines.

## 4.6.  Minutes Errata -- Correcting Mistakes

Corrections to minutes will be accepted until the Friday six weeks from the Friday of the meeting week. Such corrections should be sent to minutes@ietf.org. In general, the rule can be stated as follows:

The Working Group Chair can make changes to submitted minutes or presentation materials for six weeks from the Friday of meeting week; However, the chair must have submitted some form of the materials to the IETF Secretariat by the forth Friday following the meeting week.

# 5.  Other meeting materials such as presentations

The IETF secretariat webpages on the submission of meeting materials (“Submitting Meeting Materials for IETF Working Group and BOF Sessions,” Jan 2006.) also outlines acceptable encodings (outlined below), and layout guidelines for session presentation materials. However, these guidelines are (possibly necessarily) vague, and provide no procedures for working group chairs to ensure consistent cross-working group presentation quality. As a result, IETF session presentation materials are of widely varying content and quality. In the following sections we outline a standard format for IETF session materials, and a process for their submission.

In general, in order to have presentation materials included in the meeting proceedings, an on-line copy set of the slides in an approved format, must be submitted within two weeks following the meeting (see discussion of formats and deadlines below). Presentation slides covering information reported in the minutes need not be submitted.

## 5.1.  Encoding

(“Submitting Meeting Materials for IETF Working Group and BOF Sessions,” Jan 2006.) lays out the accepted presentation formats. In particular, the presentation materials must be provided one following encodings in order to be accepted for publication in the meeting proceedings:

File Name Encoding

=============================================
.TXT Plain text (Unix / Mac / Dos)

.DOC MS Word Document (v 95 - latest version)

.PDF Adobe Portable Document Format  Acrobat 3 - latest version)

.PPT MS PowerPoint (v 95 - latest version)

Many presenters are currently use MagicPoint (“MagicPoint,” 2005.) as a presentation tool, MagicPoint format documents must be converted to one of the above formats for submission to the secretariat.

## 5.2.  Submission Procedure and Deadlines

(“Submitting Meeting Materials for IETF Working Group and BOF Sessions,” Jan 2006.) is the authoritative source for the submission procedure and the deadlines.

While submission of minutes is mandatory, submission of slides is optional.

Presenters should provide presentation materials in one of the acceptable formats described above to the working group chair by before the meeting who can then upload the material to the IETF website. This provides remote participants to pull the slide materials from the website which provides the necessary context with an audio stream.

If a presenter fails to to provide the working group chair with presentation materials in a timely fashion or in standard format, the materials may not appear in the meeting proceedings.

The form on  (“Proceedings Submission Form,” 2005.) does not need to be used when material is uploaded via the IETF website. The form is only relevant in the context of interim meetings.

Hard copies must not be submitted, as they will not be used. Finally, slides should not be submitted for the proceedings if they contain information included in the minutes.

Note: The materials must be in electronic form, but the form is PDF (not amenable to editing, etc).

## 5.3.  Presentation Errata -- Correcting Mistakes

Corrections to minutes will be accepted until the Friday six weeks from the Friday of the meeting week. Such corrections should be sent to proceedings@ietf.org. In general, the rule can be stated as follows:

The Working Group Chair can make changes to submitted minutes or presentation materials for six weeks from the Friday of meeting week; However, the chair must have submitted some form of the materials to the IETF Secretariat by the forth Friday following the meeting week.

# 6.  Acknowledgments

Rebecca Bunch, Leslie Daigle and Allison Mankin made several helpful and clarifying comments on earlier versions of this document.

# 7.  Security Considerations

This document specifies neither a protocol nor an operational practice, and as such, it creates no new security considerations.

# 8.  IANA Considerations

This document creates a no new requirements on IANA namespaces[RFC2434] (Narten, T. and H. Alvestrand, “Guidelines for Writing an IANA Considerations Section in RFCs,” October 1998.).

## 9.  References

## 9.1. Normative References

[RFC2418]

Bradner, S., “IETF Working Group Guidelines and Procedures,” BCP 25, RFC 2418, September 1998 (TXT, HTML, XML)

[RFC2434]

Narten, T. and H. Alvestrand, “Guidelines for Writing an IANA Considerations Section in RFCs,” BCP 26, RFC 2434, October 1998 (TXT, HTML, XML).

## 9.2. Informative References

[MEETINGTOOL] “The IETF Meeting Materials Management Tool,” Web Page: http://www.ietf.org/instructions/meeting_materials_tool.html, 2005.

[MEETINGSUBMISSION] “Submitting Meeting Materials for IETF Working Group and BOF Sessions,” Web Page: http://www.ietf.org/instructions/meeting_materials.html, Jan 2006.

[MINUTES] “Minutes for the IETF Proceedings,” Web Page: http://www.ietf.org/instructions/minutes.html, 2005.

[PROCSUB] “Proceedings Submission Form,” Web Page: http://www.ietf.org/instructions/proxform.pdf, 2005.

[JAVA] “The JAVA Programming Language,” Web Page: http://java.sun.com, 2005.

[JPEG] “The JPEG Image Format,” Web Page: http://www.jpeg.org, 2005.

[MGP] “MagicPoint,” Web Page: http://member.wide.ad.jp/wg/mgp, 2005.

# Appendix A.  Templates

## A.1.  Agenda Template

<Working Group Name> (<working group abbreviation&gt); AGENDA
Meeting : IETF<Number>  <Scheduled Date of Meeting>Location: <Hotel and room information>, <timeslot>Chairs  : <chair name> <chair email address>          <co-chair1 name> <co-chair1 email address>Jabber  : <jabber room URL>URL     : <Working Group or URL>Agenda  : version: <Agenda Version>=========================================================
AGENDA

 o Administriva

   - Mailing list: <subscription info>

   - Scribe(s)?

   - Blue Sheets

 o Agenda Bashing
   <name>

 o Review and status of work items

   Active Drafts
   -------------
   <Draft Name>        <allocated time (minutes)>
   <draft file name>
   <author>
   ...
   <drafts>            <allocated time (minutes)>   Potential New Work
   ------------------
   + Work Item1
     <Draft Name>       <allocated time (minutes)>
     <draft file name>
     <author>
     <Discussion>       <allocated time (minutes)>

   + Work Item2
     <Draft Name>       <allocated time (minutes)>
     <draft file name>
     <author>
     <Discussion>       <allocated time (minutes)>

   Other
   -----
   <misc stuff>

### A.2.  Minutes Template

Instead of using this template it is probably easiest to use the published agenda to derive the actual minutes template

<Working Group Name> (<working group abbreviation>) MINUTES

Meeting : IETF<Number>  <Scheduled Date of Meeting>
Location: <Hotel and room information>, <timeslot>
Chairs  : <chair name> <chair email address>
          <co-chair1 name> <co-chair1 email address>
Minutes :  <minute taker name> <minute taker email address>
          version: <Agenda Version>
=========================================================
AGENDA
  A. Meeting Administrivia
  B.
  C.
  D.
     D.1
     D.2
==========================================================

Meeting Report
  A. Meeting Administrivia

      <Minute Scribe> volunteered as minutes scribe.
      <Jabber Scribe> volunteered as jabber scribe.      < status previous minutes >

   B. < topic title >
       * < draft-foo-discussed-draft-1 >
       * < draft-foo-discussed-draft-2 >
       * < draft-foo-discussed-draft-3 >

      < Meeting prose >

      < Action Items >

   C. < topic title >
       * < draft-foo-discussed-draft-1 >
       * < draft-foo-discussed-draft-2 >
       * < draft-foo-discussed-draft-3 >

      < Meeting prose >

      < Action Items >

## Authors' Addresses

David Meyer
University of Oregon/Cisco Systems
1225 Kincaid St.
Eugene OR 97403
USAEmail: dmm@1-4-5.net
URI: http://www.1-4-5.net/~dmm

Olaf M. Kolkman
NLnet Labs
Kruislaan 419
Amsterdam 1098 VA
The Netherlands
Email: olaf@nlnetlabs.nl
URI: http://www.nlnetlabs.nl