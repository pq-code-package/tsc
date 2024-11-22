# 2024-10-24 :  TSC Minutes

## Agenda

* Welcome
* [Minutes/actions from previous meeting](../2024-10-10/minutes.md)
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
* Discussion
  * [mlkem-native #105](https://github.com/pq-code-package/tsc/issues/105)
  * [liboqs usage #103](https://github.com/pq-code-package/tsc/issues/103)
  * [randombytes() #86](https://github.com/pq-code-package/tsc/issues/86)
  * [serialized vs deserialized #4](https://github.com/pq-code-package/tsc/issues/4)
  * [open TSC issues](https://github.com/orgs/pq-code-package/projects/4/views/1)
* Any other business
  * liboqs representative
  * meeting schedule/duration

## Welcome

## Minutes/actions from previous meeting

Minutes have been merged. Please raise issue/PR for any corrections.

### Updates from related communities

#### PQCA

Meeting canceled for this week - no updates

#### OQS

* want to start pulling pqcp implementations that are ready. Discussing with Matthias & Hanno.
* Pravek Sharma (University of Waterloo) will be taking lead in liasing / integration - already been involved with libjade kyber in liboqs, alongside Basil (IBM)

### Review of subprojects

### mlkem-c-aarch64

* original plan of independent ML-KEM generic, aarch64 & perhaps AVX2 implementations could be an obstacle to adoption - similar, but different.
* aarch64 implementation has evolved to provide interface to more easily incorporate specific implementations ie AVX2 from Kyber ref repo. Stay close to reference, but enable this specialization.
* Function signatures same across implementations, but semantics differ - so have made these definitions common. Aim to verify C code with CBMC.
* (Manuel): can also use code from Jasmin : contracts on a per-function basis with bounds. like an AVX2 implementation. Will review interface.
* C code tries to remain close to reference implementation whilst addressing a few implementation defined behaviours. (FIPS 203 input validation is open as issue)
* targetted more at server/pc/mobile platforms (vs embedded which focusses more on memory usage/code size).
* Aiming for an alpha release to get awareness of internal interface & gather feedback.
* Naming change proposal - mlkem-native currently proposed. Agree in next meeting.
* Have asked for feedback from John Shanck / Peter Schwabe

### mlkem-c-embedded

No updates. (team working on above)

### mlkem-c-libjade

* getting close to completion for the avx2 super optimized implementation. A few more optimizations with proofs to do. 
* Target is IEEE S&P conference.
* Hope to fit into the API structure covered in the mlkem-c-aarch64 discussion.

#### Open TSC issues

No updates.

### Any other business

#### Releases

* Discussion on what's needed for an alpha release: (see mlkem-c-aarch64 discussion also)
  * minimum is security/licensing.
  * document/transparency.
  * explain objectives ie inviting feedback on apis.
  * milestone set up in mlkem-c-aarch64. Assigning [issues targetted for release](https://github.com/pq-code-package/mlkem-c-aarch64/issues?q=sort%3Aupdated-desc+is%3Aissue+is%3Aopen+milestone%3Aalpha-release) there. please review.

#### liboqs representative

* Douglas proposed that Pravek Sharma is best placed to liase between liboqs & pqcp on adopting implementations of algorithms as he'll be doing much of the work.
* Will check LF process/charter offline & start this process.

## Action items

### New

### Outstanding

### Completed

* [X] Contact John Schanck to see if interested in retiming TSC meetings.
  * closing given discussion on mlkem-c-aarch64

## Recordings

* [Recordings are available on your Open Profile page](https://openprofile.dev/my-meetings) under Past Meetings.

## Upcoming TAC meetings

* Next TSC meeting in 2 weeks, 2024-11-07 1300 UTC.

[Please check the calendar](https://pqca.org/calendar/)

## Attended by

### TSC voting members

* [X] [Manuel Barbosa](https://github.com/mbbarbosa), University of Porto
* [X] [Hanno Becker](https://github.com/hanno-becker), AWS
* [X] [Nigel Jones](https://github.com/planetf1), IBM
* [X] [Matthias J. Kannwischer](https://github.com/mkannwischer), Chelpis Quantum Tech
* [ ] [Franziskus Kiefer](https://github.com/franziskuskiefer), Cryspen
* [ ] [Tiago Oliveira](https://github.com/tfaoliveira), Sandbox AQ
* [ ] [John Schanck](https://github.com/jschanck), Mozilla
* [X] [Douglas Stebila](https://github.com/dstebila), University of Waterloo

### Additional attendees

* J P Lomas, QRL
* Yarkin Doroz (NVIDIA)






