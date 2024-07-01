---
layout: default
title: 2024-06-06 TSC Meeting Record
parent: Meeting Minutes
grand_parent: PQCP TSC
nav_exclude: true
---

# 2024-06-06 TSC Meeting Minutes

## Agenda

* Welcome
* [Minutes/actions from previous meeting](https://github.com/pq-code-package/tsc/pull/59/files)
* [Agree ongoing meeting schedule](https://github.com/pq-code-package/tsc/issues/60)
* Updates from related communities:
  * [PQCA](https://github.com/PQCA)
  * [Open Quantum Safe](https://github.com/open-quantum-safe)
* Discussion - [What does 'assured' mean?](https://github.com/pq-code-package/tsc/issues/3)
* Discussion - [Common API](https://github.com/pq-code-package/tsc/issues/4)
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

## Introductions / Welcome

Apologies noted from Douglas, Matthias and Franziskus.

JP Lomas introduced himself as a developer with QRL Foundation.
Jonas Schneider-Bensch introduced himself as a developer from Cryspen, and providing cover for Franziskus who can't make it today.


## Decisions

no formal votes

## Discussion

### Minutes/actions from previous meeting

Outstanding issues: Will close API discussion action as we started that discussion.
Minutes were approved via github.

### Agree ongoing meeting schedule

We agreed not enough of the voting members were present, so we will continue on the existing schedule for now. (every two weeks, same time)

### Updates from related communities

Ongoing discussions at PQCA

* Security workgroup
* CBOM workgroup

 OQS

* new release coming out
* some vulnarabilities reported ie compiler optimization bug. Yarkin mentioned there was also an outstanding discussion in oqs about row-hammer attach on ML-KEM, and whether such attached featured in the threat model. Ry mentioned that if anyone wanted to see the draft advisories, they should contact him for access.

### What does assured mean

* See [pq-code-package/documentation#8](https://github.com/pq-code-package/documentation/pull/8) for initial draft of docs
* Hanno: need more refinement about formal proof. Add more links ie to aarch64 repo. Long term strive for functional correctness of the assembly. For example assembley level guarantees, constant time, trusted computing base assumptions.
* Tiego - will look into discussion and see how he can contribute from the jasmine side, along with Manuel.

### Common API

* Tiago/ Hanno- general agreement with proposal. Funcion names should be namespaced (same signature) as multiple parts of code package could be used together
* Should _derand functions be exposed to user? Diedre said that NIST explicitly stated redrand should not be part of full public api
* need to find out what level of hiding is sufficient for fips
* Discovery APIs are not usual in crypto libraries at runtime - mostly at runtime just protocol negotiation

### Review of subprojects

* aarch 64 is progressing (Hanno):
  * CI has developed. 2 arm runners - one macOS, one Linux
  * working with Rod on integrating cbmc (macOS). Some code changes. evaluating cbmc findings. Annotating code, trying not to diverge too much.
  * Ry pointed out that to get cbmc for the arm runners we'd need to build and cache (pcp team need to do build. Ry can help with caching) - but agreed we don't need this currently

* libjade (Tiago)
  * formally verifying Kyber episode 5 - security and correctness proof down to assembly. Updated for ML-KEM. Artifact contains a docker image/file to make replication of proofs easier as dependencies can be tricky to get together
  * Norm asked if this approach could be extended to other implementations
  * Nigel suggested that when complete, presenting this at a future meeting would be useful

* libcrux (Jonas)
  * Hope to have a version in repo by end of month.

### Any other business

No other topics.

### Next meeting / ongoing schedule

* Continue discussion on common API & Assurance
* open TSC issue on other suggestions
* Tiago will not be able to attend next meeting

## Action items

## New Action items

No new action items

### Done (from previous minutes)

* [X] Nigel to open issue to agree long-term meeting schedule
* [X] Tiago, Matthias to Present API design/approach for embedded/arch64 (see [Issue 4](https://github.com/pq-code-package/tsc/issues/29))

### Old

* [ ] Nigel to contact John Schanck about API needs
* [X] Tiago, Matthias to Present API design/approach for embedded/arch64 (see [Issue 4](https://github.com/pq-code-package/tsc/issues/29))

### New

## Recordings

* [Recordings are available on your Open Profile page](https://openprofile.dev/my-meetings) under Past Meetings

## Upcoming TAC meetings

The next meeting will be scheduled in 2 weeks time - 1300 UTC on 2024-06-20

[Please check the calendar](https://pqca.org/calendar/)

## Attended by

### TSC voting members

* [ ] [Manuel Barbosa](https://github.com/mbbarbosa), University of Porto
* [X] [Hanno Becker](https://github.com/hanno-becker), AWS
* [X] [Nigel Jones](https://github.com/planetf1), IBM
* [ ] [Matthias J. Kannwischer](https://github.com/mkannwischer), CHelpis Quantum Tech
* [ ] [Franziskus Kiefer](https://github.com/franziskuskiefer), Cryspen
* [X] [Tiago Oliveira](https://github.com/tfaoliveira), Sandbox AQ
* [ ] [John Schanck](https://github.com/jschanck), Mozilla
* [ ] [Douglas Stebila](https://github.com/dstebila), University of Waterloo

### Additional attendees

* Ry Jones, Linux Foundation
* Jonas Schneider-Bensch, Cryspen
* Yarkin Doroz, NVIDIA
* Normal Ashley, Cisco Systems
* Deirdre Connolly, SandboxAQ
