---
title: GitHub Use for Working Groups
description: This page provides a summary of the ways working groups (WGs) may set up and use GitHub Organizations and GitHub Repositories, as detailed In RFC 8874 and RFC 8875.
published: true
date: 2021-12-20T17:43:20.313Z
tags: 
editor: markdown
dateCreated: 2021-12-20T17:43:20.313Z
---

If a WG Chair wishes to create a new GitHub Organization or Repository for their working group themselves, [RFC 8875](https://www.rfc-editor.org/rfc/rfc8875.html) specifies:

- Name the GitHub Organization: ietf-wg-[WGACRONYM]
- Add the IETF Secretariat as owner (IETF Secretariat GitHub user ID: @ietf-secretariat)
- Add all WG Chairs and the WG Secretary (if applicable) as owners
- Add the WG Area Directors as owners
- Add the URL for the GitHub Organization to the IETF Datatracker About Page under "Additional Resources"
- Initialize a GitHub Organization Administrative Team made up of WG Chairs and WG Secretary (if applicable). It should be named "WGACRONYM-chairs" (for example: dnsop-chairs)

If you’d like assistance in setting up your GitHub organization, please send email to support@ietf.org with the subject line "GitHub Organization Request for WGACRONYM." Please include the GitHub user IDs for all WG Chairs, Secretaries and Area Directors when making your request.

The Secretariat will create the GitHub organization (with designated owners) and will add the GitHub Organization URL to the "Additional Resources" area of the IETF Datatracker About page for the working group.

Once the GitHub Organization for the WG is set up the WG Chairs would be able to do any (or all) of these actions to facilitate the work of the WG:

- Create a new repository for an individual draft (at the discretion of the WG chair)
  - The repository should be the draft filename
  - Document authors and editors should be identified as collaborators
- Create a new repository for an already adopted working group draft
  - The repository should be the draft filename
  - Document authors and editors should be identified as collaborators
- Migrate an existing document repository into the WG GitHub organization
- Create a new repository that contains multiple drafts.

[RFC 8874](https://www.rfc-editor.org/rfc/rfc8875.html) details a set of guidelines for working groups that choose to use GitHub for their work.