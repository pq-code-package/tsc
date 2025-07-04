# 2025-07-03: TSC Minutes

## Agenda

* Welcome
* Approval of minutes from previous meeting (2025-06-05)
* [Nomination for new TSC voting member: Markku-Juhani Saarinen](https://github.com/pq-code-package/tsc/issues/176)
* [Project Lifecycle Stage Review](https://github.com/pq-code-package/tsc/issues/178)
    * PQCP is currently in Incubation stage
    * We need to decide if we want to move to the Growth Stage or stay in the Incubation Stage
* Updates from related communities:
    * [PQCA TAC](https://github.com/PQCA/TAC)
    * [Open Quantum Safe](https://github.com/open-quantum-safe)
* Review status of sub projects:
    * [mlkem-native](https://github.com/pq-code-package/mlkem-native)
    * [mldsa-native](https://github.com/pq-code-package/mldsa-native)
    * [mlkem-libjade](https://github.com/pq-code-package/mlkem-libjade)
    * [mlkem-rust-libcrux](https://github.com/pq-code-package/mlkem-rust-libcrux)
    * [slhdsa-c](https://github.com/pq-code-package/slhdsa-c)
* Discussion (if not covered previously)
    * Issues proposed for closure (Matthias commented to close around 2025-07-03):
        * [Add project dashboard](https://github.com/pq-code-package/tsc/issues/58)
        * [ML-KEM Test Vectors](https://github.com/pq-code-package/tsc/issues/29)
        * [Agree and document contribution guidelines & PR process](https://github.com/pq-code-package/tsc/issues/22)
        * [Decide how project results should be consumed & communicate this](https://github.com/pq-code-package/tsc/issues/15)
        * [OpenSSF scorecard for member subprojects](https://github.com/pq-code-package/tsc/issues/14)
        * [Adopt a code of conduct](https://github.com/pq-code-package/tsc/issues/9)
        * [Develop a security policy](https://github.com/pq-code-package/tsc/issues/8)
    * [Other Open TSC issues](https://github.com/orgs/pq-code-package/projects/4/views/1)
        * Remaining open issues for review:
            * [Project Documentation Standards](https://github.com/pq-code-package/tsc/issues/151)
            * [Add CONTRIBUTING.md to all repos](https://github.com/pq-code-package/tsc/issues/54)
            * [Determine any cross-implementation API requirements](https://github.com/pq-code-package/tsc/issues/4)
            * [Adopt a definition of assurance levels](https://github.com/pq-code-package/tsc/issues/3)
    * **Next meeting: 2025-08-07 13:00 UTC**
* Any other business

## Attendees
TSC members: 
* [X] Manuel Barbosa
* [X] Hanno Becker
* [X] Matthias J. Kannwischer
* [X] Franziskus Kiefer
* [ ] Jake Massimo
* [X] Markku-Juhani Saarinen
* [ ] Tiago Oliveira
* [X] Pravek Sharma

## Action Items
- Matthias: Add Markku-Juhani Saarinen to TSC membership
- Matthias: Recommend PQCP for Growth stage to TAC
- Franziskus: Finalize documentation standards proposal and comment on [#151](https://github.com/pq-code-package/tsc/issues/151)

## Minutes

* **Minutes from previous meeting (2025-06-05)**: Approved

* **TSC Membership**: 
  - Markku-Juhani Saarinen nomination approved with sufficient votes from TSC members
  - Welcome to Markku as new TSC voting member

* **Project Lifecycle Stage Review**:
  - **Decision**: TSC voted to recommend PQCP move from Incubation to Growth stage
  - Unanimous approval from 5 TSC members present
  - Matthias to submit recommendation to TAC

* **Updates from related communities**:
  - **PQCA TAC**: 
    - Mentorship program available - volunteers needed to mentor
    - Outreach committee focusing on marketing activities
    - New PQCA social media accounts on LinkedIn and X:
      - https://www.linkedin.com/company/post-quantum-cryptography-alliance/
      - https://x.com/PQCAorg
    - Seeking blog posts from community members (can be research-focused, not limited to PQCA projects)
    - Blog posts will be shared on social media channels
  - **OQS**: 
    - slhdsa-c integration work underway, expected completion in 2-3 weeks
    - Same project lifecycle review process as PQCP (not yet completed)

* **Sub-project updates**:
  - **mlkem-native**: 
    - Functional correctness proofs complete for all Arm assembly
    - AWS-LC integration ongoing with assembly backend
    - RISC-V support PR in review, looking good for merge
  - **mldsa-native**: 
    - Major CBMC performance improvements enable top-level function proofs
    - Assembly integration progressing but still gap to state-of-the-art performance
    - Expect to complete verification work soon
  - **mlkem-libjade**: 
    - ML-KEM proofs progressing, refactoring work ongoing
    - Potential new PQCP release with 2 parameter sets and full proofs planned
  - **mlkem-rust-libcrux**: 
    - README PR ready for review and merge
    - Considering unified rust repository structure for all algorithms
    - ML-DSA proofs nearly complete
  - **slhdsa-c**: 
    - Supports all 12 FIPS 205 parameter sets plus ~300 experimental parameter sets
    - Single binary supports multiple parameter sets (smaller firmware footprint)
    - OQS integration in progress, vectorized API changes planned for performance

* **Technical discussions**:
  - **ACVP key validation**: 
    - New NIST test vectors include secret key and public key validation tests
    - Requires new API functions returning 0/1 for validation
    - May need coordination with OQS on API
  - **Documentation standards** (https://github.com/pq-code-package/tsc/issues/151): 
    - Performance benchmarking: agreed to require instructions on how to benchmark rather than uniform fair benchmarks
    - Memory usage reporting discussed (stack usage, binary size) - more discussion required
    - Verification coverage: projects should clearly document what guarantees are provided and what code is covered
    - Table format proposed showing modules vs verification types (correctness, memory safety, etc.) - deemed as too detailed for some projects. Consensus was to leave that up to the sub-projects as long as guarantees are well defined and coverage is clear.
    - Franziskus will create a proposal and post it for comment.

* **Issues for closure**: Approved closing orphaned issues as proposed
* **Next meeting: 2025-08-07 13:00 UTC**