# 2024-10-10 :  TSC Minutes

## Agenda

* Welcome
* [Minutes/actions from previous meeting](../2024-09-26/minutes.md)
* Updates from related communities:
  * [PQCA](https://github.com/PQCA)
  * [Open Quantum Safe](https://github.com/open-quantum-safe)
* Review status of sub projects:
  * [mlkem-c-generic](https://github.com/pq-code-package/mlkem-c-generic)
    * [initial code setup](https://github.com/pq-code-package/mlkem-c-generic/issues/4)
  * [mlkem-c-embedded](https://github.com/pq-code-package/mlkem-c-embedded)
  * [mlkem-c-aarch64](https://github.com/pq-code-package/mlkem-c-aarch64)
  * [mkkem-libjade](https://github.com/pq-code-package/mlkem-libjade)
  * [mlkem-rust-libcrux](https://github.com/pq-code-package/mlkem-rust-libcrux)
  * [documentation](https://github.com/pq-code-package/documentation)
* [open TSC issues](https://github.com/orgs/pq-code-package/projects/4/views/1)
* Any other business

## Welcome

## Minutes/actions from previous meeting

Minutes have been merged. Please raise issue/PR for any corrections.

### Updates from related communities

#### PQCA

* Working on closing project lifecycle followups
* Discussions around how to stimulate interest and activity in some quiet workgroups such as Documentation.
* qsc in 5G project presented to board, and feedback session held with some telco/gsma/3gpp experts.

#### OQS

* 0.11 release of liboqs completed. Working through updating downstream projects include liboqs-provider
* Using ML-KEM etc from PQCrystals, but goal remains to pull from pqcp.
* Franziskus has been in touch about exported C implementations from libcrux - will discuss. 

### Review of subprojects

### mlkem-c-aarch64

_Hanno was unable to make the meeting byt provided the following via discord_

* MLKEM-C-AArch64 has been progressing well, we're now -- from all I know -- the fastest AArch64 implementation out there. The current goal is to work through the AVX2 code from the reference implementation and fit it into a common C<-Native interface suiting both AArch64 and AVX2.

### mlkem-c-libjade

* Extracted single file implementation from formosa ml-kem repo.
* Developments on proofs for fully optimized version - ideally want this first. Looking at timeline. If it takes too long will push earlier implementation from crypto this year.
* Hoping to have discussion with Matrhias on benchmarks.

### mlkem-c-libcrux

* [PR](https://github.com/pq-code-package/mlkem-rust-libcrux/pull/3) open for initial implementation. Reviews invited.
* need to work on process for updates. Currently has a bash script.
* Looking for volunteers to help

### mlkem-c-generic

No progress on reference implementation. Proposal to discuss next time around using the aarch64 implementation for Intel ie generic.

#### Open TSC issues

No updates.

### Any other business

* Ry. Suggest we have a logo. Have created AI generated logo - will post in discord - [link](https://discord.com/channels/1202723482224295936/1233337574668501033/1291745533299527765)

## Action items

### New

### Outstanding

* [ ] Contact John Schanck to see if interested in retiming TSC meetings.
  - _will wait until after discussion on generic implementations_

### Completed

## Recordings

* [Recordings are available on your Open Profile page](https://openprofile.dev/my-meetings) under Past Meetings.

## Upcoming TAC meetings

* Next TSC meeting in 2 weeks, 2024-10-10 1300 UTC.

[Please check the calendar](https://pqca.org/calendar/)

## Attended by

### TSC voting members

* [ ] [Manuel Barbosa](https://github.com/mbbarbosa), University of Porto
* [ ] [Hanno Becker](https://github.com/hanno-becker), AWS
* [X] [Nigel Jones](https://github.com/planetf1), IBM
* [ ] [Matthias J. Kannwischer](https://github.com/mkannwischer), Chelpis Quantum Tech
* [X] [Franziskus Kiefer](https://github.com/franziskuskiefer), Cryspen
* [X] [Tiago Oliveira](https://github.com/tfaoliveira), Sandbox AQ
* [ ] [John Schanck](https://github.com/jschanck), Mozilla
* [X] [Douglas Stebila](https://github.com/dstebila), University of Waterloo

### Additional attendees

* Ry Jones, Linux Foundation
* Yarkin Doroz, NVIDIA
