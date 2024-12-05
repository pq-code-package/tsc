# 2024-11-21 :  TSC Minutes

## Agenda

* Welcome

* [Minutes/actions from previous meeting](../2024-11-07/minutes.md)

* Updates from related communities:
  * [PQCA](https://github.com/PQCA)
  * [Open Quantum Safe](https://github.com/open-quantum-safe)

* Review status of sub projects:

  * [mlkem-libjade](https://github.com/pq-code-package/mlkem-libjade)
  * [mlkem-rust-libcrux](https://github.com/pq-code-package/mlkem-rust-libcrux)
  * [mlkem-native](https://github.com/pq-code-package/mlkem-c-embedded)

* Discussion (if not covered previously)

  * [Renaming of mlkem-native #105](https://github.com/pq-code-package/tsc/issues/105)
  * [FIP203 - 7 function api #4](https://github.com/pq-code-package/tsc/issues/4#issuecomment-2456391348)
  * [Working towards liboqs usage #103](https://github.com/pq-code-package/tsc/issues/103)
  * [Do we supply randombytes() #86](https://github.com/pq-code-package/tsc/issues/86) - NO/test-only / close ?
  * [Requiring OpenSSL CLA #113](https://github.com/pq-code-package/tsc/issues/113)
  * [Other Open TSC issues](https://github.com/orgs/pq-code-package/projects/4/views/1)

* Any other business

## Welcome

* Matthias welcomed everyone to the meeting. Nigel unable to join today

## Minutes/actions from previous meeting

### Updates from related communities

#### PQCA

None of today's attendees were at the PQCA meeting, so no update.

#### OQS

* Working on next OQS release including ML-DSA & a security advisory.
* Some discussions/issue around additional APIs, such as public key derivation from secret key. To be discussed as TSC, and community wants clarity from NIST before moving ahead.

### Review of subprojects

#### mlkem-c-libjade

* Additional proofs finished on AVX rejection sampling code
* Tiago working on pushing things up from upstream to pqcp.
* Close to having a AVX2 implementation ready to go out.
* Will need to add new APIs as that general discussion continues.
* After this want to do arm verified implementations, & dilithium. Cortex-M4 to start, more powerful in future, also vectorization.

### mlkem-native (was mlkem-c-aarch64)

* Finished CBMC proofs for everything except SHA-3 (C code -> top level API).
  * Absence of undefined behaviour, memory safety / no overflow.
  * CBMC is pragmatic choice - assumed/guaranteed bounds of input/output.
* Release in next 2-3 weeks hopefully.

#### Open TSC issues

* [#105](https://github.com/pq-code-package/tsc/issues/105) Renaming - done
* [#4](https://github.com/pq-code-package/tsc/issues/4) API discussion ongoing. Gaining Consensus (maybe secret key->public key to be added). Plan to draft email for NIST (pqc forum/list) in issue with summary of discussion.
* [#103](https://github.com/pq-code-package/tsc/issues/103) No specific work on integration into OQS yet. (Pravek/Basil). After alpha.
* [#86](https://github.com/pq-code-package/tsc/issues/86) Random bytes - we should not have implementation / should close.
* [#113](https://github.com/pq-code-package/tsc/issues/113) OpenSSL - need individual and employer document. Relevant for mlkem-native, and for mlkem-c-libjade. Good time to do it comment in issue

### Any other business

* Releases / structure
  * libjade
    * will be AVX2 (perhaps x86) assembly + source code (single Jasmin file) + header for C + docs.
    * in future will expand as compiler adds new backends.
    * user provides randombytes().
    * next year make it possible to reuse parts of implementations, not all of it.
    * liboqs will be consuming from pqcp in future.
  * mlkem-native
    * source code only initially. considering a library.
    * aarch64 has many Keccak implementations... may need to determine at runtime in future.
  * generally... more discussion on APIs and modularity.
  
## Action items

### New

### Outstanding

### Completed

## Recordings

* [Recordings are available on your Open Profile page](https://openprofile.dev/my-meetings) under Past Meetings.

## Upcoming TAC meetings

* Next TSC meeting in 2 weeks, 2024-12-05 1300 UTC.

[Please check the calendar](https://pqca.org/calendar/)

## Attended by

### TSC voting members

* [X] [Manuel Barbosa](https://github.com/mbbarbosa), University of Porto
* [X] [Hanno Becker](https://github.com/hanno-becker), AWS
* [ ] [Nigel Jones](https://github.com/planetf1), IBM
* [X] [Matthias J. Kannwischer](https://github.com/mkannwischer), Chelpis Quantum Tech
* [ ] [Franziskus Kiefer](https://github.com/franziskuskiefer), Cryspen
* [ ] [Tiago Oliveira](https://github.com/tfaoliveira), Sandbox AQ
* [ ] [John Schanck](https://github.com/jschanck), Mozilla
* [X] [Pravek Sharma](https://github.com/praveksharma), University of Waterloo
* [ ] [Douglas Stebila](https://github.com/dstebila), University of Waterloo

### Additional attendees
