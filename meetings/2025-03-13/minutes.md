# 2025-03-13 :  TSC Minutes

## Agenda

* Welcome

* [Minutes/actions from previous meeting](../2025-02-27/minutes.md)

* Updates from related communities:
  * [PQCA](https://github.com/PQCA)
  * [Open Quantum Safe](https://github.com/open-quantum-safe)

* Review status of sub projects:

  * [mlkem-native](https://github.com/pq-code-package/mlkem-native)
  * [mldsa-native](https://github.com/pq-code-package/mldsa-native)
  * [mlkem-libjade](https://github.com/pq-code-package/mlkem-libjade)
  * [mlkem-rust-libcrux](https://github.com/pq-code-package/mlkem-rust-libcrux)
  * [mlkem-c-embedded](https://github.com/pq-code-package/mlkem-c-embedded)

* Discussion (if not covered previously)

  * [PQCA Blog Post](https://github.com/PQCA/TAC/issues/65)
  * [Other Open TSC issues](https://github.com/orgs/pq-code-package/projects/4/views/1)

* Any other business

## Welcome


## Minutes/actions from previous meeting

Minutes have been merged. Thanks to reviewers for corrections.

### Updates from related communities

#### PQCA

* Main topic at PQCA this week was the [PQCA Blog Post](https://github.com/PQCA/TAC/issues/65) - see below for our discussion on content
* Elections are underway for:
  * PQCA TAC lead.
  * PQCA community rep - only open to those working for companies not represented on PQCA board.

#### OQS

* liboqs release candidate for 0.13.0 planned, including deterministic keygen API for ML-KEM and updates from mlkem-native.
* Initial plan to include mlkem-native API in this release, but moving ahead without those changes.

### Review of subprojects

#### mlkem-native

* Further progress on formal byte-level verification of assembly with John Harrison using [Hol Light](https://hol-light.github.io/).
  * includes core routines - NTT, inverse NTT, and Keccak variants (including complex neon/scalar hybrids).
  * C code is verified with CBMC. memory, safety, overflow should cover many potential bugs - compiler output is not being verified with HOL-Light.
  * Need to match CBMC contract to hol-light
  * Formal verification of AArch64 assembly nearing completion.
  * One remaining area is rejection sampling - complex.
  * AVX2 next.
* Release of OQS with mlkem-native expected soon.
* PR to AWS-LC in progress, with one approval.  

### mlkem-c-embedded

* currently on hold pending more interest.
* noted one discord post mentioning embedded.

#### mlkem-c-libjade

* ARM implementation of ML-KEM AVX2 version is very close to completion, stable.
* Some final documentation to be completed.  
* formal verification of AVX2 implementation to be covered at [IEEE Symposium on Security and Privacy](https://sp2025.ieee-security.org/)

#### mlkem-rust-libcrux

No update.

#### mldsa-native

No update.

#### Open TSC issues

* PQCA Blog Post

  * spirit of bringing together multiple implementations and highlighting different guarantees and properties.
  * PQCP as a place to find implementations.
  * adoption of ML-KEM in Open Quantum Safe and AWS-LC.
  * real-world impact via deployments to attract contributors.
  * What's next including ML-DSA and encouraging contributors.
  * Will discuss further on [discord](https://discord.com/invite/xyVnwzfg5R) tomorrow to complete first draft.


### Any other business

* Noted the need to review attendance and revisit meeting times if needed.

## Action items

### New

### Outstanding

### Completed

## Recordings

* [Recordings are available on your Open Profile page](https://openprofile.dev/my-meetings) under Past Meetings.

## Upcoming TSC meetings

* Next TSC meeting in 2 weeks, 2025-03-27 1000 Central European Time (UTC+1).

[Please check the calendar](https://pqca.org/calendar/)

## Attended by

### TSC voting members

* [X] [Manuel Barbosa](https://github.com/mbbarbosa), University of Porto
* [X] [Hanno Becker](https://github.com/hanno-becker), AWS
* [X] [Nigel Jones](https://github.com/planetf1), IBM
* [ ] [Matthias J. Kannwischer](https://github.com/mkannwischer), Chelpis Quantum Tech
* [ ] [Franziskus Kiefer](https://github.com/franziskuskiefer), Cryspen
* [ ] [Tiago Oliveira](https://github.com/tfaoliveira), Sandbox AQ
* [ ] [John Schanck](https://github.com/jschanck), Mozilla
* [X] [Pravek Sharma](https://github.com/praveksharma), University of Waterloo

### Additional attendees

None.
