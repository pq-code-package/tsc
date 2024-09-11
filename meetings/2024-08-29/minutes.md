# 2024-08-29 :  TSC Minutes

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

We started with a few introductions to welcome some new participants:

* Pierre (Thalys) : Really interested in project. Mostly focussed on liboqs but monitoring what's going on in pqcp & other parts of pqca.
* Aditya (University of Delhi) :Interested in PQCA and working in this in telecoms - looking at solutions/proposals.
* Yarkin (Nvidia) :product manager. Crypto libraries. Current focus PQC
* Nigel : TSC lead

## Minutes/actions from previous meeting

No additional notes

### Updates from related communities

#### PQCA

* Aditya has [proposal](https://github.com/PQCA/TAC/issues/34) open for PQC in 5G networks as part of Application Working group proposal
* Project lifecycle vote passed - governs how new subprojects are admitted to pqca (for example, tooling)

#### OQS

* NIST standards finalized - work going on to incorporate in new release in next month or so.
* Request for help - review open issues across repos (including [liboqs](https://github.com/open-quantum-safe/liboqs/issues), [oqs-provider](https://github.com/open-quantum-safe/oqs-provider/issues)), discussions & participate

### Review of subprojects

### mlkem-c-generic

* Nigel has contacted Peter Schwabe to discuss including generic implementation within pqcp - work that John schanck had started. Originates in [PQ-Crystals/Kyber](https://github.com/pq-crystals/kyber)
* Some changes expected - for example use of volatile to reduce issues with non-constant time behaviour, validation of input parameters.
* Ongoing support, security issue reporting will happen in pqcp.
* plan to start bringing code ([PR](https://github.com/pq-code-package/mlkem-c-generic/pull/6)) in over next 1-2 weeks. Sort licenses, basic build.
* In future can start [consolidating APIs](https://github.com/pq-code-package/tsc/issues/4), statements about [assurance](https://github.com/pq-code-package/tsc/issues/3) etc across all our ML-KEM implementations.
* Longer term we expect oqs to source ML-KEM from this implementation.
* looking for additional volunteers.

#### Open TSC issues

Additional algorithms
* [ML-DSA](https://github.com/pq-code-package/tsc/issues/94), [SLH-HSA](https://github.com/pq-code-package/tsc/issues/95)
* (Yarkin) - there may be additional standards, for example LMS, XMSS - required by CNSA [ [wikipedia](https://en.wikipedia.org/wiki/Commercial_National_Security_Algorithm_Suite#:~:text=The%20Commercial%20National%20Security%20Algorithm,NSA%20Suite%20B%20Cryptography%20algorithms.) | [paper](https://media.defense.gov/2022/Sep/07/2003071836/-1/-1/0/CSI_CNSA_2.0_FAQ_.PDF)].

### Any other business

## Action items

### New

None

### Completed

* [X] Nigel to followup owith PQCrystals on onboarding generic ML-KEM implementation

## Recordings

* [Recordings are available on your Open Profile page](https://openprofile.dev/my-meetings) under Past Meetings.

## Upcoming TAC meetings

* Next TSC meeting in 2 weeks, 2024-09-12 1300 UTC

[Please check the calendar](https://pqca.org/calendar/)

## Attended by

### TSC voting members

* [ ] [Manuel Barbosa](https://github.com/mbbarbosa), University of Porto
* [ ] [Hanno Becker](https://github.com/hanno-becker), AWS
* [X] [Nigel Jones](https://github.com/planetf1), IBM
* [ ] [Matthias J. Kannwischer](https://github.com/mkannwischer), Chelpis Quantum Tech
* [ ] [Franziskus Kiefer](https://github.com/franziskuskiefer), Cryspen
* [ ] [Tiago Oliveira](https://github.com/tfaoliveira), Sandbox AQ
* [ ] [John Schanck](https://github.com/jschanck), Mozilla
* [ ] [Douglas Stebila](https://github.com/dstebila), University of Waterloo

### Additional attendees

* Aditya Koranga, University of Delhi
* Yarkin Doroz, NVIDIA
* Pierre-Elisée Flory (Thales)
