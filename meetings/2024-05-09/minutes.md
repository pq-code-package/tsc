---
layout: default
title: 2024-05-09 TSC Meeting Record
parent: Meeting Minutes
grand_parent: PQCP TSC
nav_exclude: true
---

# 2024-05-09 TSC Meeting Minutes

## Agenda

* Welcome
* Reminder of [TSC Charter](charter/charter-2024-01-29.pdf)
* Agree TSC membership
* Establishing a voting procedure
* Election of a TSC chair
* Identify a representative from the PQCP TSC to the [PQCA Technical Advisory Committee](https://pqca.org/about/technical-advisory-council/)
* Agree meeting frequency and appropriate days/times
* Discuss & identify initial priorities for the TSC
* Review relevant PQCA activities
* Review status of sub projects
  
  * [mlkem-c-generic](https://github.com/pq-code-package/mlkem-c-generic)
  * [mlkem-c-embedded](https://github.com/pq-code-package/mlkem-c-embedded)
  * [mlkem-c-aarch64](https://github.com/pq-code-package/mlkem-c-aarch64)
  * [mkkem-libjade](https://github.com/pq-code-package/mlkem-libjade)
  * [mlkem-rust-libcrux](https://github.com/pq-code-package/mlkem-rust-libcrux)
  * test vectors?
  * [documentation](https://github.com/pq-code-package/documentation)

* Any other business

## Announcements

## Presentation

None

## Decision

* [x] Initial list of TSC voting members confirmed.

## Discussion

### TSC Charter

Key elements from charter were highlighted - we agreed this was accurate:

_PQ Code Package Project, which will build high-assurance production-ready software implementations of forthcoming post-quantum cryptography standards, starting with the ML-KEM algorithm_

Alex noted the charter stats a **CONTRIBUTING.md** file should be present in each repo. We don't have this. [Issue 54](https://github.com/pq-code-package/tsc/issues/54)

### TSC _Voting_ Membership

It was noted by Naomi this should be referred to as Voting members. We have an open community to which everyone is invited. Here we are only voting on those elegible to vote in future TSC discussions.

Discussed composition of TSC - typically starts as maintainer from each of the contributing subjects. Each member proposed in the initial list explained their role. A vote was taken which agreed with the initial voting members of the TSC. These voting members are listed in the attendance section below.

### Voting Procedure / Election of a TSC Chair / PQCA TAC Rep

We agreed that an offline vote was the best way to elect a TSC Chair. Naomi will arrange a vote via github. Ry noted candidates should self-nominate.

Naomi also pointed out that the TSC Chair will be the PQCA TAC Rep.

### Meeting frequency/times

Some consensus of a monthly frequency longer term, but we agreed to have the next meeting in 2 weeks time as we're getting started. The current time (Thu 1300 UTC) seems ok. Naomi will send out a 1-off invite, and we'll review at the next TSC meeting.

### Discuss initial priorities


#### Common APIs

See [
](https://github.com/pq-code-package/tsc/issues/4)

Agreed useful to have common APIs between implementations, especially where they are in the same language (and similar where it makes sense, if not).

We should ask users about APIs (including John in Mozilla where it's used in [NSS](https://wiki.mozilla.org/NSS)). [Open Quantum Safe](https://openquantumsafe.org/) is also a consumer.

Tiago noted that sometimes randomization needs to come from outside, so needed an API change for NSS.

Hanno pointed out a consistent internal structure is useful too ie common functions in C implementations, as is common packaging. Doug mentioned it could be useful for a consumer to pull in several different implementations (ie generic, x86 etc).

Agreed a good starting point would be for 1 or 2 projects to present on their APIs and design decisions for the rest of the group. We could start with Tiago & then Matthias.

#### Lifecycle / Projects / Assurance

How do we describe assurance levels?

Franziskus mentioned this should be a high priority as it's on our charter.

Can we have a single definition? Noted aspects can vary (ie threading model, whether algo is constant-time checked...). Agreed each project could explain what their interpretation is & share. We can then derive a common definition. Nigel pointed out we need to be able to explain to a consumer what to expect - how do I choose which implementation to use?

What do we expect from a reference implementation? Is this production ready? Agreed important to have reference implementation.

What is production code? What are it's characteristics? Nigel noted that the PQCA has a [project lifecycle proposal](https://docs.google.com/document/d/1NV-0vNgXWdc81oqT0jv0C-9Funb8dySS06u90ghF-X4/edit), and some discussion is [delegated to the open quantum safe team](https://github.com/open-quantum-safe/tsc/issues/1) - so probably makes sense to consolidate the discussion there.

Security vulnerability reporting also important.

Nigel suggested that Production could mean getting to a point where an org could take it & incorporate into their systems with some level of confidence, or perhaps goes into a distribution like Fedora.

#### Test vectors

Norman would like to propose a [common testing harness](https://github.com/pq-code-package/tsc/issues/29) within PQCP. Common API would help. We could use the [NIST acvts test server](https://csrc.nist.gov/projects/cryptographic-algorithm-validation-program/how-to-access-acvts). Need to supply credentials including cert. Ry will help out with the cert.

#### Hackathons

It may make sense for future hackathons to be more targetted?
## Review PQCA activities

Nigel briefly mentioned the following calls for workgroups at the PQCA:

* [Security and Governance](https://github.com/PQCA/TAC/issues/2)
* [CBOMs and SBOMs](https://github.com/PQCA/TAC/issues/14)
* [Algorithms](https://github.com/PQCA/TAC/issues/7)

## Review subprojects

Matthias mentioned they now have stack optimized code. Not very fast yet. Working through some cleanup including cc0 licensing. Currently no issues to discuss at tsc. For aarch64 have defined what to achieve - Hanno is new maintainer for this.

Nigel briefly mentioned our initial docs site at https://docs.pqcodepackage.org .

We ran out of time to do justice to this discussion. Continue in next session.

## Action items

Action items

### Done (from previous minutes)

### Old

### New

* [ ] Nigel to share links on project lifecycle discussions
* [ ] Nigel to contact John Schanck about API needs
* [ ] Tiago, Matthias to Present API design/approach for embedded/arch64 (see [Issue 4](https://github.com/pq-code-package/tsc/issues/29))
* [ ] All - what does high assurance mean for the embedded/arch64 subproject
* [ ] Naomi to arrange TSC chair vote
* [ ] Naomi to schedule next meeting / send out invites

## Recordings

* [Recordings are available on your Open Profile page](https://openprofile.dev/my-meetings) under Past Meetings

## Upcoming TAC meetings

[Please check the calendar](https://pqca.org/calendar/)

## Attended by

### TSC voting members

* [x] [Manuel Barbosa](https://github.com/mbbarbosa), University of Porto
* [x] [Hanno Becker](https://github.com/hanno-becker), AWS
* [x] [Nigel Jones](https://github.com/planetf1), IBM
* [x] [Matthias J. Kannwischer](https://github.com/mkannwischer), CHelpis Quantum Tech
* [x] [Franziskus Kiefer](https://github.com/franziskuskiefer), Cryspen
* [x] [Tiago Oliveira](https://github.com/tfaoliveira), Sandbox AQ
* [ ] [John Schanck](https://github.com/jschanck), Mozilla
* [x] [Douglas Stebila](https://github.com/dstebila), University of Waterloo

### Additional attendees

* Alex Bozarth, IBM
* Norman Ashley, Cisco
* Naomi Washington, Linux Foundation
* Ry Jones, Linux Foundation
* Yarkin Doroz, NVIDIA
* Duc Tri Nguyen, Cryptography Engineering Research Group @ GMU
