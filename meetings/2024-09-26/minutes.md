# 2024-09-26 :  TSC Minutes

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

* Any other business

Lomas, QRL## Welcome

## Minutes/actions from previous meeting

Minutes have been merged. Please raise issue/PR for any corrections.

### Updates from related communities

#### PQCA

* Following up on open issues around project lifecycle document.
* Tooling workgroup started, including CBOM generation tool - discussions underway as to whether actual code moves under PQCA.
* PQC for 5G - presenting to pqca board + feedback session planned with some of Nigel's colleagues invovled in 3GPP/GSMA.

#### OQS

* 0.11 including ML-KEM final (C from PQCrystals) out, probably Friday.
* Hoping future releases will start incorporating algorithms from PQ Code Package - advise when suitable to try and pull in, or include in release.
* Hope to get final ML-DSA in next release.

### Review of subprojects

### mlkem-c-aarch64

* Ry reported CI moved to paid Github runners to avoid wait-time before builds start as this had been causing multi-hour backlogs. This option could be taken on other PQCA repos if required. [cost report](https://app.octolense.com/accounts/PQCA)

### mlkem-c-libjade

* Hope to get implementation in soonish with stable ML-KEM for avx2 and reference implementation coming from Jasmine.
* finishing off changes following publishing of ML-KEM final version & refactorings.

### mlkem-c-libcrux

* PR open. About to merge back proofs. Hopefully done next week.
* Currently has 2 versions (proven & yet to be proven) - to be consolidated in future version.
* Sorting out how to manage concurrent with ongoing development on libcrux repo - workflow. Expect to 'release' to pqcp
* Libcrux currently [exporting C Code](https://github.com/cryspen/libcrux/tree/main/libcrux-ml-kem/cg) (header only version being integrated into BoringSSL). Open SSH picked up portable version. Also google. firefox nss has portable code. Can extract various versions. Doug will share with liboqs.


### mlkem-c-generic

* PR and issues open for review. Have asked Basil for feedback. No further progress.
* Looking for volunteers to help.
* Plan to merge then get back with Pete Schwabe.

#### Open TSC issues

* Various issues open to add additional algorithms. Douglas pointed out we should be careful not to spread too thinly without additional contributors.
* Ongoing discussion on random bytes implementation.
* Deserialized API - sounds useful, but not clear it's a high priority right now.
* Comments on algo characteristics welcome.

### Any other business

* Douglas: Discussion underway with OpenSSL about where they get their algorithms from. ML-KEM is most important, but others include ML-DSA and stateless hashes too. Will discuss pqcp as a potential source. Currently talking through licensing issues (CLA) with help of LF.
* Nigel: The call time is still awkward for Americas, particularly West. We may be missing out on increased involvement. If anyone additional is keen to join (particularly new contributors) but finds the time awkward we could consider meetings with the time varying to accommodate. Doug: may affect John Schanck? Nigel to check.

## Action items

### New

* [ ] Contact John Schanck to see if interested in retiming TSC meetings.

### Completed

## Recordings

* [Recordings are available on your Open Profile page](https://openprofile.dev/my-meetings) under Past Meetings.

## Upcoming TAC meetings

* Next TSC meeting in 2 weeks, 2024-10-10 1300 UTC.

[Please check the calendar](https://pqca.org/calendar/)

## Attended by

### TSC voting members

* [X] [Manuel Barbosa](https://github.com/mbbarbosa), University of Porto
* [ ] [Hanno Becker](https://github.com/hanno-becker), AWS
* [X] [Nigel Jones](https://github.com/planetf1), IBM
* [ ] [Matthias J. Kannwischer](https://github.com/mkannwischer), Chelpis Quantum Tech
* [X] [Franziskus Kiefer](https://github.com/franziskuskiefer), Cryspen
* [ ] [Tiago Oliveira](https://github.com/tfaoliveira), Sandbox AQ
* [ ] [John Schanck](https://github.com/jschanck), Mozilla
* [X] [Douglas Stebila](https://github.com/dstebila), University of Waterloo

### Additional attendees

* Ry Jones, Linux Foundation
* J P 

# Links
https://app.octolense.com/accounts/pq-code-package
