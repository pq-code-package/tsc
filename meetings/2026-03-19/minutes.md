# 2026-03-19: TSC Minutes

## Agenda

* Welcome
* Updates from related communities (PQCA, OQS)
* Review status of sub projects
  * [mlkem-native](https://github.com/pq-code-package/mlkem-native)
  * [mldsa-native](https://github.com/pq-code-package/mldsa-native)
  * [mlkem-libjade](https://github.com/pq-code-package/mlkem-libjade)
  * [rust-libcrux](https://github.com/pq-code-package/rust-libcrux)
  * [slhdsa-c](https://github.com/pq-code-package/slhdsa-c)
* Discussion items
  * TSC chair elections
    - Matthias's term ends April 2026
    - Proposed schedule: nominations April 1-15, vote April 16-23 if needed
  * PQCA Mentorship Program
    - https://github.com/pq-code-package/tsc/issues/197
    - Call for proposals extended until mid-April
  * PQCP Inclusion Proposal: C++20 ML-KEM and ML-DSA
    - https://github.com/pq-code-package/tsc/issues/204
  * [Reconsider TSC meetings](https://github.com/pq-code-package/tsc/issues/193)
  * [PQCP Growth Plan](https://github.com/pq-code-package/tsc/issues/188) - Status update
    - [X] mlkem-native
    - [X] mldsa-native
    - [X] mlkem-libjade
    - [ ] rust-libcrux
    - [ ] slhdsa-c
  * [Project Documentation Standards](https://github.com/pq-code-package/tsc/issues/151) - Implementation status
    - [X] [mlkem-native](https://github.com/pq-code-package/mlkem-native/issues/1289)
    - [X] [mldsa-native](https://github.com/pq-code-package/mldsa-native/issues/634)
    - [X] [mlkem-libjade](https://github.com/pq-code-package/mlkem-libjade/issues/4)
    - [ ] [rust-libcrux](https://github.com/pq-code-package/rust-libcrux/issues/6)
    - [ ] [slhdsa-c](https://github.com/pq-code-package/slhdsa-c/issues/38)
  * Review of remaining open issues:
    - [Determine any cross-implementation API requirements](https://github.com/pq-code-package/tsc/issues/4)
    - [Adopt a definition of assurance levels](https://github.com/pq-code-package/tsc/issues/3)
* Any other business
* Next meeting: 2026-04-02 13:00 UTC

## Attendees
TSC members:
* [X] Manuel Barbosa
* [ ] Hanno Becker
* [X] Basil Hess
* [X] Matthias J. Kannwischer
* [ ] Franziskus Kiefer
* [ ] Jake Massimo
* [X] Tiago Oliveira
* [ ] Markku-Juhani Saarinen

Other attendees:
* Anjan Roy

## Action items

* Matthias: Open an issue to call for nominations for TSC chair (April 1 - April 15)
* All TSC members: Continue discussion and provide feedback on Anjan's project proposal ([#204](https://github.com/pq-code-package/tsc/issues/204)) on GitHub for one week
* Matthias: Call for a vote on Anjan's project proposal in one week via the LFX platform

## Minutes

**OQS update (Basil)**

Basil gave his first update as the new OQS representative on the TSC. OQS is preparing a new release (the last release was in November 2025). This will be the first release to include mldsa-native code, replacing the previous PQ Crystals upstream. It will also include the new mlkem-native v1.1 release. Other highlights: adding MQOM (NIST PQC on-ramp signature submission), an update to NTRUPrime (still used by OpenSSH), and improved testing including Wycheproof test vectors for ML-KEM and ML-DSA. Release candidate expected by end of March.

**PQCA/TAC update (Matthias)**

Mentorship program: The call for proposals has been extended until mid-April since no proposals were submitted during the initial period. TAC chair elections and general member representative elections are ongoing. Matthias nominated himself again for the technical community representative and got confirmed. The group also briefly discussed OpenSSF baseline and its potential relevance to PQCA projects.

**mlkem-libjade (Manuel)**

A lot of work was done leading up to RWC. Improvements to repository maintenance and CI. New releases of the Jasmin compiler and an upcoming release of the EasyCrypt prover. A new release of mlkem-libjade is expected soon. Work on ML-DSA full proof is ongoing, with the goal of finishing before the end of the year.

**mlkem-native (Matthias)**

New release v1.1 with a PR into OQS. The biggest milestone is the completion of all HOL Light proofs for the x86 backend: correctness proofs, constant-time proofs, and memory safety proofs for all assembly. Intrinsic implementations were replaced with assembly to enable HOL Light verification. A new document `SOUNDNESS.md` has been added describing the verification approach, gaps, risks, and mitigations. The RWC talk was well received and generated interest from potential consumers.

**mldsa-native (Matthias)**

Ongoing HOL Light proofs for the Arm and x86 backends, with many functions still to cover. The goal is to complete verification and create a stable release (currently alpha) well before end of year. The x86 and Aarch64 verification are progressing in parallel. The C code is production-ready despite the alpha label. There is a memory-optimized configuration flag for ML-DSA that reduces RAM usage from ~130KB to much less, which could be added to OQS, but some CBMC proofs are not yet complete for that configuration due to issues with unions.

Basil asked about a pending PowerPC64 backend pull request for mlkem-native. Matthias will respond after consulting with Hanno.

**TSC chair elections**

Matthias's term as TSC chair ends in April 2026. Proposed schedule:
- Nomination period: April 1 - April 15
- If 2 or more nominations are submitted, execute a rank-based vote
- Voting period: April 16 - April 23

The TSC approved this proposed schedule.

**PQCP inclusion proposal: C++20 ML-KEM and ML-DSA ([#204](https://github.com/pq-code-package/tsc/issues/204))**

Anjan Roy presented his proposal to include two C++20 libraries (ML-KEM and ML-DSA) in PQCP. The libraries are header-only, fully `constexpr`, use `std::span` instead of raw pointers, have zero dependencies, and are portable (no assembly). Performance is approximately 3x slower than mlkem-native/mldsa-native (compared against assembly backends), primarily due to lack of 4x SIMD parallel Keccak hashing. The libraries have extensive testing (property-based, mutation, fuzzing) and strict compiler/static analysis settings.

Discussion points:
- Basil asked about overlap with mlkem-native/mldsa-native. Anjan explained the codebases are very different due to C++20 `constexpr` features which are not available in C.
- Matthias asked about formal verification plans. Anjan expressed interest but noted uncertainty about C++20 tool support and a need for assistance.
- Tiago asked about performance benchmarks. Anjan confirmed ~3x gap vs assembly backends.
- Manuel asked about team size and long-term maintainability. Anjan has been the sole developer for 3.5 years and is looking for a second maintainer. Inclusion in PQCP would provide exposure and motivation.
- Basil asked about adoption. No confirmed production deployments; interest is inferred from GitHub stars (127 for ML-KEM) and forks.

The TSC agreed to continue the discussion on GitHub for one week, then Matthias will call for a vote via the LFX platform (rather than GitHub issues) to improve participation.

**Reconsider TSC meetings ([#193](https://github.com/pq-code-package/tsc/issues/193))**

The current approach of opening a GitHub issue before each meeting to check attendance and canceling if fewer than 4 people plan to attend is working well. The TSC agreed to continue this practice.

**Growth plan and documentation standards**

The growth plan ([#188](https://github.com/pq-code-package/tsc/issues/188)) and documentation standards ([#151](https://github.com/pq-code-package/tsc/issues/151)) have been completed by the sub-projects represented at the meeting (mlkem-native, mldsa-native, mlkem-libjade) but remain outstanding for rust-libcrux and slhdsa-c.

