---
layout: default
title: 2024-05-23 TSC Meeting Record
parent: Meeting Minutes
grand_parent: PQCP TSC
nav_exclude: true
---

# 2024-05-23 TSC Meeting Minutes

## Agenda

 Welcome
* Approval of [2024-05-09 minutes](https://github.com/pq-code-package/tsc/pull/53)
* Update on [TSC chair vote](https://github.com/pq-code-package/tsc/issues/52)
* Funding for [AWS ECS](https://github.com/pq-code-package/mlkem-c-aarch64/issues/34) / [Github arm runners](https://github.com/pq-code-package/tsc/issues/55)
* Security - PQCA workgroup / SECURITY.md & lists / [Github reporting](https://github.com/PQCA/wg-security/issues/2)
* Updates and observations from related communities:
  * [PQCA](https://github.com/PQCA)
  * [Open Quantum Safe](https://github.com/open-quantum-safe)
* Discussion - [What does 'assured' mean?](https://github.com/pq-code-package/tsc/issues/3)
* [Hackathons](https://github.com/pq-code-package/tsc/issues/31)
* Review status of sub projects:
  * [mlkem-c-generic](https://github.com/pq-code-package/mlkem-c-generic)
  * [mlkem-c-embedded](https://github.com/pq-code-package/mlkem-c-embedded)
  * [mlkem-c-aarch64](https://github.com/pq-code-package/mlkem-c-aarch64)
  * [mkkem-libjade](https://github.com/pq-code-package/mlkem-libjade)
  * [mlkem-rust-libcrux](https://github.com/pq-code-package/mlkem-rust-libcrux)
  * [documentation](https://github.com/pq-code-package/documentation)
* Review  [open TSC issues](https://github.com/pq-code-package/tsc/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc):

  * any noteable progress
  * topics for next meeting
* Any other business
* Next meeting / ongoing schedule

## Introductions

Rod Chapman introduced himself as a colleague of Hano's at AWS Cryptography Group with a particular interest in formal verification of PQC. He has previously build a formally verified implementation of Kyber.

## Decisions

## Discussion

### Approval of 2024-05-09 minutes

Nigel thanked everyone who'd reviewed the minutes. Naomi pointed out that a formal vote is not needed. We agreed to approve minutes via github in future.

### Update on TSC votes

Nigel confirmed that he was elected TSC Chair following the vote.

### Funding for ARM jobs

Matthias summarized that his team want to benchmark, which is where real ARM processors are needed. This should be automated so that we can  compare over time. For regular testing emulation remains an option.

hano noted that we need to know exactly what hardware we are running on. Git runners may be an option if we can find this out. Benchmarking will also be done on specific hardware boards. Graviton is an interesting target.

We agreed bare metal instances were not needed - experience indicates using the virtualized environments are good enough - and a lot cheaper.

Ry updated us that a board vote to allocate money for this (and requests from oqs) did not pass due to not reaching quorum, but those present were in favour. It's expected to pass. BuildJet is also an option & are easy to integrate. For Amazon the master services agreement needs to be used to arrange access. The intent is to have a budget of $10k to use across all options for PQCA so we don't need to keep going back with updated requests. Ry can also work with team to integrate dedicated hardware with github actions.

Hanno noted this work isn't time critical, and also that in future there was a possibility of wanting to delve deeper with some super optimized code - discussion for another day.

The team agreed to continue discussion via issues as this has been progressing well.

### Security

Nigel noted that liboqs recently enabled private vulnarability reporting in their github repositories and proposed we do the same in pqcp (including creation of a SECURITY.md). We agreed this was reasonable to do.

### PQCA update

Max gave an update on PQCA. He reminded the team of the current workgroups include security and CBOM which are both looking for anyone interested to join. For CBOMs we may be able to start cataloguing important projects.

This week's PQCA TAC included a presentation from Dana Wang, OpenSSF on open-source security, scorecards etc. In the future we hope we can influence these scorecards to capture if a project is pq ready/compliant/has CBOM.

There's also activity to get funding for mentorship, and support students doing masters/PhD to make contributions. Doug mentioned this was part of the original formation discussions to bring new talent in.

Finally there is currently a vote for vice-chair open.

Nigel mentioned scorecard work had started in OQS, and whilst we have scorecards in pqcp, there is action to act on the findings.

The potential of needing funding for formal audits was also brought up, but Matthias felt there is a fair way off yet. Ry pointed out that Trail Bits has recently joined PQCA. Doug mentioned OQS had a call with TrailBits recently, and hopefully they'll be looking at some oqs code pro-bono.

### Open Quantum Safe

In addition to mentoring, audits (above) Doug pointed out that acting on scorecard findings takes engineering resources.

Release 0.11 is being worked towards over the next month. Two likely inclusions will be stateful hash-based signatures, the Mayo signature scheme, and a formally verified Kyber implementation from libjade.

A security issue was also reported which now has a patch.

Ry pointed out that OQS has a [dashboard](https://openquantumsafe.org/dashboard) which can include links to openssf reports. Nigel mentioned if we benchmark this could be useful info to add. Max pointed out we need to ensure the content is actionable, ie we use it.

 
 ### What does assured mean

 _to be written_

 ### Hackathons

 _to be written_

 ### Review of subprojects

 _to be written_

### Any other business

 _to be written_

### Next meeting / ongoing schedule

 _to be written_

## Action items

Action items

### Done (from previous minutes)

* [X] Naomi to arrange TSC chair vote (this was completed)
* [X] Naomi to schedule next meeting / send out invites (this was completed)
* [X] All - what does high assurance mean for the embedded/arch64 subproject (discussion was arranged, will track via issues above)
* [X] Nigel to share links on project lifecycle discussions (this was added to previous minutes)

### Old

* [ ] Nigel to contact John Schanck about API needs
* [ ] Tiago, Matthias to Present API design/approach for embedded/arch64 (see [Issue 4](https://github.com/pq-code-package/tsc/issues/29))

### New

## Recordings

* [Recordings are available on your Open Profile page](https://openprofile.dev/my-meetings) under Past Meetings

## Upcoming TAC meetings

The next meeting will be scheduled in 2 weeks time - 1300 UTC on 2024-06-06

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
* Yarkin Doroz, Worcester Polytechnic Institute
* Duc Tri Nguyen, Cryptography Engineering Research Group @ GMU
* Rod Chapman, Amazon Web Services
