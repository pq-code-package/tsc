---
layout: default
title: 2024-06-20 TSC Meeting Record
parent: Meeting Minutes
grand_parent: PQCP TSC
nav_exclude: true
---

# 2024-06-20 TSC Meeting Minutes

## Agenda

* Welcome
* [Minutes/actions from previous meeting](../2024-06-06/minutes.md)
* Updates from related communities:
  * [PQCA](https://github.com/PQCA)
  * [Open Quantum Safe](https://github.com/open-quantum-safe)
* Review status of sub projects:
  * [mlkem-c-generic](https://github.com/pq-code-package/mlkem-c-generic)
  * [mlkem-c-embedded](https://github.com/pq-code-package/mlkem-c-embedded)
  * [mlkem-c-aarch64](https://github.com/pq-code-package/mlkem-c-aarch64)
  * [mkkem-libjade](https://github.com/pq-code-package/mlkem-libjade)
  * [mlkem-rust-libcrux](https://github.com/pq-code-package/mlkem-rust-libcrux)
  * [documentation](https://github.com/pq-code-package/documentation)
* [open TSC issues](https://github.com/orgs/pq-code-package/projects/4/views/1):  
  * [What does 'assured' mean?](https://github.com/pq-code-package/tsc/issues/3) : continued
  * [Common API](https://github.com/pq-code-package/tsc/issues/4) : continued
  * [First Release](https://github.com/pq-code-package/tsc/issues/74)
* Any other business


## Minutes/actions from previous meeting

### Welcome

Apologies from Matthias and Tiago.

No additional notes on previous minutes

### Updates from related communities

#### PQCA

* Next call on 3 July includes a presentation on CBOM tooling by one of Nigel/Max's IBM colleagues. See [PQCA calendar](https://pqca.org/calendar/). Thinking about how to get more CBOMs out there - make it easy, can we have a catalogue, what other initiatives are going on?
* Project lifecycle proposal continuing in [issue](https://github.com/PQCA/TAC/issues/24) (includes link to doc).

#### OQS

* A few recent security vulnerability reports led to point releases, and the OQS team using the Github reporting/advisory mechanism.
* Working towards 0.11 which includes the long-awaited stateful hash based signature support, in addition to the libjade version of Kyber. Prelude to pulling the formally verified versions from pq-code-package (direct for now). Likely release early July.
* updates to scorecard, hope to merge soon. Will raise more issues to implement & mitigate reports within pq-code-package also.
* Discussion getting started on more updates/revisions of oqs demo repo. Contact Alex for more info.

### Review of subprojects

#### mlkem-c-generic

* Generic implementation not yet in place. liboqs uses the PQ Crystals implementation that Peter Schwabe looks after. So exists in community, but needs someone to work to bring it into pq-code-package. In itself not an issue at the moment, however Hanno noted that it would be useful to have fairly soon to help in looking at sharing some C code between the repositories i.e. to make more testable (but also taking care not to change unnecessarily).

#### mlkem-c-aarch64

* Hanno reported that good progress is being made on aarch64:
  * CI - Now have 3 minds of runners. MacOS arm, Linux arm, Linux x86 (emulated). Also have hardware boards hooked into CI to do initial benchmarking.
  * CBMC - working with Rod to use cbmc to demonstrate absence of undefined behaviour. Not trying to prove functional correctness, but will rule out a class of bugs. Rod added the team is Gaining experience with cbmc, making it easier, learning how to make code more testable, so we can make it a push button activity in CI, and roll out more broadly.

#### mlkem-libjade

* Stabilizing upstream libjade repo first. In pqcp we'll expose the parts that make sense to use.
* finishing off a proof of thx AVX version - looking competitive/fast. Pushing through June/July to get ready before August break.
* Documentation being worked on.
* Received some requests as to whether parts of the implementation could be used - for example reusing the avx2 matrix expansion code within another C implementation - will need to work through how to do this, and understand the relationship with other repos.

#### documentation

Nigel reminded the team that we have a documentation repo where we can start building docs.

#### Open TSC issues

* Project board [here](https://github.com/orgs/pq-code-package/projects/4)
* Reviewed open issues and updated accordingly
* Arm runners - now in place for CI. But still need benchmarking. Ry suggested to close [ARM Runners #55](https://github.com/pq-code-package/tsc/issues/55) and open a new issue specifically on benchmarking. Will work with Hanno ie on Graviton.
* [Assurance Levels #8](https://github.com/pq-code-package/tsc/issues/3) - [docs pr](https://github.com/pq-code-package/documentation/pull/8) - needs to be more fine grained (Hanno). Rod will take a look.
* [API #4](https://github.com/pq-code-package/tsc/issues/4) - reminder to continue discussion ie Exposure of derand functions.
* [Release #74](https://github.com/pq-code-package/tsc/issues/74) - release likely to be per-repository as consumers likely to not need all, and to avoid slowing progress

### Any other business

No other topics.

## Action items

No updates

## Recordings

* [Recordings are available on your Open Profile page](https://openprofile.dev/my-meetings) under Past Meetings

## Upcoming TAC meetings

The next meeting will be scheduled in 2 weeks time - 1300 UTC on 2024-07-04

[Please check the calendar](https://pqca.org/calendar/)

## Attended by

### TSC voting members

* [X] [Manuel Barbosa](https://github.com/mbbarbosa), University of Porto
* [X] [Hanno Becker](https://github.com/hanno-becker), AWS
* [X] [Nigel Jones](https://github.com/planetf1), IBM
* [ ] [Matthias J. Kannwischer](https://github.com/mkannwischer), CHelpis Quantum Tech
* [ ] [Franziskus Kiefer](https://github.com/franziskuskiefer), Cryspen
* [ ] [Tiago Oliveira](https://github.com/tfaoliveira), Sandbox AQ
* [ ] [John Schanck](https://github.com/jschanck), Mozilla
* [X] [Douglas Stebila](https://github.com/dstebila), University of Waterloo

### Additional attendees

* Alex Bozarth, IBM
* Rod Chapman, Amazon Web Services
* Ry Jones, Linux Foundation
* Hart Montgomery, Linux Foundation
