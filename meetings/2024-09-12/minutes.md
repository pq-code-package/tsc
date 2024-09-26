# 2024-09-12 :  TSC Minutes

## Agenda

* Welcome
* [Minutes/actions from previous meeting](../2024-08-15/minutes.md)
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
  * [ML-DSA](https://github.com/pq-code-package/tsc/issues/94) and [SLH-DSA](https://github.com/pq-code-package/tsc/issues/95)
* Any other business

## Welcome

No new faces today.

## Minutes/actions from previous meeting

No additional notes

### Updates from related communities

#### PQCA

* PQC/5G proposal - will be presenting to board. Feedback for that team from some industry experts involved in GSMA, 3GPP etc.
* Tooling working group - voting underway. Initial project is sonarqube plugin
* Following up on open issues around project lifecycle document

#### OQS

* Finalizing next release of liboqs - 0.11, including ML-KEM (from PQCrystals - in future hope to get from pqcp)
* Release candidate expected by end of week
* Also includes libjade versino of Kyber (with Tiago's help especially around packaging/licensing)
* Additional NISTsignature on-ramp algorithms
* ML-DSA not in this release (will be from PQCrystals, again hope to see this from pqcp)

### Review of subprojects

### mlkem-c-aarch64

* Hanno working with Ry on getting the ec2 benchmarking setup - now working. Can select/run benchmarks/tests & in CI regularly running on Graviton 2 (free) + 3 (paid). Fiddly but flexible/easy to use.
* NTT Assembly - starting with clean, then will use super optimized version.
* Discussion on benchmarking framework and results - useful for other projects. See workflow files in github
* Douglas will mention to spencer / pravek who have been looking at overhauling existing system.
  * [Example charts](https://pq-code-package.github.io/mlkem-c-aarch64/dev/bench/)

### mlkem-c-libjade

* Had been an ambitious plan to try and get initial version in by the summer holidays
* now expecting to have final implementation of super optimized avx mlkem ready in next few months.
* Proof not yet complete - like this completed before pushing.

### mlkem-c-generic

* PR and issues open for review
* Will reach out to Basil for feedback & then Peter once initial load done.
* Need to get a point of being a viable upstream for liboqs (and meet their expectations around testing etc.)
* Welcome comments, feedback, and participation ie for maintainers. Peter Schwabe has offered advice and help
* Code is reference only, from *standard* branch. Not includin AVX
* Tiago pointed out that the standards branch is now merged into PQCrystals main

#### Open TSC issues

* Issues open on ML-DSA and some other algorithms - if anyone is having discussions with the implementors of these and want to open up discussion on pqcp that would be helpful.
  * Nigel is asking IBM colleagues involved in ML-DSA
* Norman pointed out there's some debate over stateful signatures and whether it belongs in a library when it's mostly used in HSMs (NIST has some guidance)
* Manuel points out that stateful hash based signatures will be coming into libjade. Will reach out to Andreas Hülsing. State needs to be kept tamper proof, but may be variety of options like usb keys.
* Ongoing discussion on random bytes - Tiago thinks could be somewhat out of scope, need to be careful - though ok for testing. Look for thoughts from Matthias when back. Also we need to agree on API - jasmine implementation requires specific function to be defined. Can then document.

### Any other business

## Action items

### New

### Completed

## Recordings

* [Recordings are available on your Open Profile page](https://openprofile.dev/my-meetings) under Past Meetings.

## Upcoming TAC meetings

* Next TSC meeting in 2 weeks, 2024-09-26 1300 UTC

[Please check the calendar](https://pqca.org/calendar/)

## Attended by

### TSC voting members

* [X] [Manuel Barbosa](https://github.com/mbbarbosa), University of Porto
* [X] [Hanno Becker](https://github.com/hanno-becker), AWS
* [X] [Nigel Jones](https://github.com/planetf1), IBM
* [ ] [Matthias J. Kannwischer](https://github.com/mkannwischer), Chelpis Quantum Tech
* [ ] [Franziskus Kiefer](https://github.com/franziskuskiefer), Cryspen
* [X] [Tiago Oliveira](https://github.com/tfaoliveira), Sandbox AQ
* [ ] [John Schanck](https://github.com/jschanck), Mozilla
* [X] [Douglas Stebila](https://github.com/dstebila), University of Waterloo

### Additional attendees

* Ry Jones, Linux Foundation
* Norman Ashley, Cisco
