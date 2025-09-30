# 2025-10-02: TSC Minutes

## Agenda

* Welcome
* PQCP Growth Plan
* Updates from related communities (PQCA, OQS)
* Review status of sub projects
  * [mlkem-native](https://github.com/pq-code-package/mlkem-native)
  * [mldsa-native](https://github.com/pq-code-package/mldsa-native)
  * [mlkem-libjade](https://github.com/pq-code-package/mlkem-libjade)
  * [mlkem-rust-libcrux](https://github.com/pq-code-package/mlkem-rust-libcrux)
  * [slhdsa-c](https://github.com/pq-code-package/slhdsa-c)
* Discussion items
  * [Rust libcrux repository re-org](https://github.com/pq-code-package/tsc/issues/181) - Vote on renaming proposal
  * [Project Documentation Standards](https://github.com/pq-code-package/tsc/issues/151)
  * Review of remaining open issues:
    - [Determine any cross-implementation API requirements](https://github.com/pq-code-package/tsc/issues/4)
    - [Adopt a definition of assurance levels](https://github.com/pq-code-package/tsc/issues/3)
* Any other business
* Next meeting: 2025-11-06 13:00 UTC

## Attendees
TSC members:
* [ ] Manuel Barbosa
* [X] Hanno Becker
* [X] Matthias J. Kannwischer
* [X] Franziskus Kiefer
* [ ] Jake Massimo
* [X] Tiago Oliveira
* [ ] Pravek Sharma
* [ ] Markku-Juhani Saarinen

Other attendees:
* Hart Montgomery (Linux Foundation, PQCA)

## Action Items
- All projects: Consider growth strategies from Hart's presentation and discuss on GitHub or in next meeting
- Matthias: Create growth plan document for TAC presentation
- Matthias: Open issues in all project repositories with documentation standards requirements
- Hanno & Tiago: Review and agree on documentation standards list
- Hart: Check on PQCA blog post reach/effectiveness metrics

## Minutes

* **PQCP Growth Plan**:
  - **LFDT Playbook**: Hart shared [LFDT Growth Playbook](https://docs.google.com/presentation/d/1r4wljummNbfwRHxH4zYAenSvNIx2EcpChmMgpa5lazM/edit?usp=sharing)
  - **Focus**: Primary goal for PQCP is awareness and user base growth (not necessarily contributors at this stage)
  - **Growth Strategies Ideas** (presented by Hard, primarily from LFDT playbook):
    - **Blog Posts & Media**:
      - Currently posting on PQCA blog
      - Also consider LFDT, OpenSSF, and CNCF blogs
    - **Meetups**:
      - LFDT offers virtual and in-person meetups (45-min presentations, recordable)
      - How-to guides particularly effective
      - Recommended having beginner-friendly sessions
    - **Public Calls**:
      - Already have public TSC calls on calendar
      - Less intimidating than GitHub for newcomers
    - **Communication Channels**:
      - Discord active with good response times (critical for attracting users)
      - PQCA has LinkedIn and Twitter accounts available
    - **Good First Issues**:
      - Challenging for PQCP due to technical nature of cryptography
    - **Workshops**:
      - Virtual and in-person how-to workshops, recorded for online consumption
      - Consider 6-month cadence with new versions
    - **Mentorships**:
      - PQCP had strong applicant pool
      - Budget available for more mentorships (flexible timing, not just summer)
      - Available globally
    - **Case Studies**:
      - Multiple case studies create critical mass and drive adoption
      - AWS Crypto Library (AWSLC) using mlkem-native - opportunity for case study
    - **Newsletter**:
      - LFDT has newsletter capability
      - Would feature releases, milestones, conferences, workshops
      - PQCP is considering a newsletter
    - **Ecosystem Mapping**:
      - Who is using PQCP already?
      - Already documenting consumers in README files
    - **Collaboration Opportunities**:
      - OpenSSF - post-quantum conversation upcoming
      - Post-quantum Kubernetes
      - CNCF could be interesting partner
  - **Action**: Each project to think about growth strategies, discuss on GitHub or next meeting, create document for TAC

* **Updates from related communities**:
  - **PQCA**:
    - LinkedIn and Twitter accounts active
    - Blog posts being published
    - Planning paper repository
    - Mentorship programs available
  - **OQS**: No representative attended

* **Sub-project updates**:
  - **mlkem-native** (Hanno Becker):
    - Starting AVX2 HOL-Light proof development (progress expected over next month)
    - Two new backend contributions:
      - RISC-V 64 backend from Markku (under review, expected to merge this month)
      - ppc64 backend from IBM (first review done, needs work, confident it will merge)
    - Total backend count will reach 4
  - **mldsa-native** (Matthias Kannwischer):
    - Exceeded performance of AArch64 MLDSA implementation in PQClean (met alpha release performance bar)
    - AVX2 work ongoing - small gap vs Dilithium team implementation for signing, expect to close in 2 weeks
    - First integration into LibOQS completed (not merged yet but works, identified all needed changes)
    - **Alpha release expected in 4-6 weeks**
  - **mlkem-libjade** (Tiago Oliveira):
    - Full-time engineer working on project until December, focused on CI
    - Focusing on ML-KEM 1024 completeness
    - CI checks include: safety, performance, and proofs
    - **Target: Release by end of December**
    - Planning blog post about accomplishments
    - Implementation correctness proofs take 2.5 hours with 8 cores (goal: optimize to <10 minutes)
    - Matthias offered CI assistance based on his experience
  - **mlkem-rust-libcrux** (Franziskus Kiefer):
    - Common PQCP APIs merged into ML-KEM
    - **Release planned within next 1-2 weeks** with common APIs
    - Feature flag enables C APIs for easy drop-in replacement
    - Once renaming complete, will add MLDSA to repository
    - MLDSA code exists, most proofs done, some cleanup remaining
  - **slhdsa-c**: No updates

* **Technical discussions**:
  - **Rust libcrux repository re-org** (https://github.com/pq-code-package/tsc/issues/181):
    - Resolved
  - **Project Documentation Standards** (https://github.com/pq-code-package/tsc/issues/151):
    - Existing list of agreed-upon documentation standards shared
    - Action plan:
      1. Hanno and Tiago to review standards list
      2. All agree to standards
      3. Matthias opens issues in all project repositories
      4. Projects implement standards and close issues
      5. Finally close old documentation standards issue
  - **Cross-implementation API requirements** (https://github.com/pq-code-package/tsc/issues/4):
  - **Assurance levels** (https://github.com/pq-code-package/tsc/issues/3):

* **Other business**:
  - Meeting time discussion: Tiago and Manuel have teaching duties on Thursdays going forward
  - May need to discuss new meeting time in future

* **Next meeting: 2025-11-06 13:00 UTC**
