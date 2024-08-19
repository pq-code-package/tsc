# 2024-08-15 :  TSC Minutes

## Agenda

* Welcome
* [Minutes/actions from previous meeting](../2024-07-18/minutes.md)
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
* Any other business

## Minutes/actions from previous meeting

### Updates from related communities

#### PQCA

* Continued discussion on project lifecycle document - to be sent to a vote shortly.
* [Tooling Working group](https://github.com/PQCA/TAC/issues/14) proposal - to include sonarqube plugin work, scanning for crypto usage.
* [Application working group](https://github.com/PQCA/TAC/issues/34). Discussion about whether in scope. One proposed project for telco core. Understand relationship to work in GSMA, ETSI etc.

#### OQS

* [Final release of NIST standards](https://www.nist.gov/news-events/news/2024/08/nist-releases-first-3-finalized-post-quantum-encryption-standards) for [ML-KEM](https://csrc.nist.gov/pubs/fips/203/final), [ML-DSA](https://csrc.nist.gov/pubs/fips/204/final), and [stateless hash-based signatures](https://csrc.nist.gov/pubs/fips/205/final).
* Expecting quite release of 0.11 in next 2-3 weeks.
* Follow-on release for ML-KEM etc in Sep/Oct hopefully.
* Needs good quality implementation from upstream sources.
* Ideally would come from PQ-CP (Nigel to follow up).

### Review of subprojects

#### mlkem-c-embedded

* PR for 32 bit RISC-V. Still testing, likely to merge soon.
* Optimization next step.
* Upcoming vacation/conferences - quiet for next week.

#### mlkem-c-aarch64

* Nothing significant in last 2 weeks.
* still need to pull in keccak & optimized entities.

#### mlkem-c-libjade

* no update

#### mlkem-c-libcrux

* not much progress in last 2 weeks, but close to being able to merge once some work on licensing done.
* Looking for more help to help move quicker.

### mlkem-c-generic

#### Open TSC issues

* Sync usersids
* [Should PQCP implementations ship randombytes()](https://github.com/pq-code-package/tsc/issues/86) - Please add more comments in issue
* [OpenSSF scorecard for member subprojects](https://github.com/pq-code-package/tsc/issues/14) - Nigel planning to review, may open issues on individual repos for any followup work.
* [Assurance - initial docs (PR)](https://github.com/pq-code-package/documentation/pull/8) - please review along with [Adopt a definition of assurance levels](https://github.com/pq-code-package/tsc/issues/3)
* [Access to AWS AArch64 runners](https://github.com/pq-code-package/tsc/issues/75) - making progress, discussion in discord

### Any other business

* Kenny introduced himself as program manager, replacing Naomi. LF since 2017. 

## Action items

### New

* [ ] Nigel to followup owith PQCrystals on onboarding generic ML-KEM implementation

## Recordings

* [Recordings are available on your Open Profile page](https://openprofile.dev/my-meetings) under Past Meetings.

## Upcoming TAC meetings

* Next TSC meeting in 2 weeks, 2024-08-29 1300 UTC

[Please check the calendar](https://pqca.org/calendar/)

## Attended by

### TSC voting members

* [ ] [Manuel Barbosa](https://github.com/mbbarbosa), University of Porto
* [ ] [Hanno Becker](https://github.com/hanno-becker), AWS
* [X] [Nigel Jones](https://github.com/planetf1), IBM
* [X] [Matthias J. Kannwischer](https://github.com/mkannwischer), Chelpis Quantum Tech
* [X] [Franziskus Kiefer](https://github.com/franziskuskiefer), Cryspen
* [ ] [Tiago Oliveira](https://github.com/tfaoliveira), Sandbox AQ
* [ ] [John Schanck](https://github.com/jschanck), Mozilla
* [X] [Douglas Stebila](https://github.com/dstebila), University of Waterloo

### Additional attendees

* Hugo Landau
* Kenny Paul, Linux Foundation
* Yarkin Doroz, NVIDIA
