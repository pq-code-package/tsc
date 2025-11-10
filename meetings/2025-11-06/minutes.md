# 2025-11-06: TSC Minutes

## Agenda

* Welcome
* Approval of minutes from previous meeting: [2025-10-02](https://github.com/pq-code-package/tsc/pull/187)
* Updates from related communities (PQCA, OQS)
 * Volunteer to join TAC meetings? Wednesday, 15:00 UTC, every two weeks
* Review status of sub projects
  * [mlkem-native](https://github.com/pq-code-package/mlkem-native)
  * [mldsa-native](https://github.com/pq-code-package/mldsa-native)
  * [mlkem-libjade](https://github.com/pq-code-package/mlkem-libjade)
  * [rust-libcrux](https://github.com/pq-code-package/rust-libcrux)
  * [slhdsa-c](https://github.com/pq-code-package/slhdsa-c)
* Discussion items
  * [PQCP Growth Plan](https://github.com/pq-code-package/tsc/issues/188)
    - [X] mlkem-native
    - [X] mldsa-native
    - [X] mlkem-libjade
    - [ ] rust-libcrux
    - [ ] slhdsa-c
  * [Project Documentation Standards](https://github.com/pq-code-package/tsc/issues/151)
    - [X] Manuel Barbosa
    - [ ] Hanno Becker
    - [X] Matthias Kannwischer
    - [X] Franziskus Kiefer
    - [ ] Jake Massimo
    - [X] Tiago Oliveira
    - [ ] Pravek Sharma
    - [ ] Markku-Juhani Saarinen
  * Review of remaining open issues:
    - [Determine any cross-implementation API requirements](https://github.com/pq-code-package/tsc/issues/4)
    - [Adopt a definition of assurance levels](https://github.com/pq-code-package/tsc/issues/3)
* Any other business
* Next meeting: 2025-12-04 13:00 UTC

## Attendees
TSC members:
* [X] Manuel Barbosa
* [X] Hanno Becker
* [X] Matthias J. Kannwischer
* [ ] Franziskus Kiefer
* [ ] Jake Massimo
* [ ] Tiago Oliveira
* [ ] Pravek Sharma
* [ ] Markku-Juhani Saarinen

Other attendees:
* None

## Action Items
- Hanno: Take turns with Matthias attending TAC meetings (every 4 weeks each)
- Matthias: Contact Pravek about stepping down from TSC
- Matthias: Contact Franziskus for rust-libcrux growth plan contribution
- Matthias: Contact Markku for slhdsa-c growth plan contribution
- Matthias: Create issues in all project repositories for documentation standards

## Minutes

* **TAC Meeting Attendance**:
  - TAC meetings occur every two weeks at an inconvenient time for Matthias (11pm after daylight saving changes)
  - Hanno agreed to take turns attending TAC meetings with Matthias (every 4 weeks each)

* **PQCP Growth Plan**:
  - https://github.com/pq-code-package/tsc/issues/188
  - Matthias has written growth plans for mlkem-native and mldsa-native
  - Manuel has submitted growth plan for libjade
  - Still waiting for contributions from:
    - Libcrux (Franziskus)
    - SLHDSA (Markku)
  - **Action**: Matthias to follow up with Franziskus and Markku for growth plan contributions
  - Growth plan to be revisited in one year

* **Project Documentation Standards**:
  - Issue [#151](https://github.com/pq-code-package/tsc/issues/151) now has 5 approvals (sufficient for approval)
  - Hanno reviewed and approved the documentation standards during the meeting
  - **Decision**: Documentation standards approved
  - **Next steps**: Matthias will create issues in all project repositories to implement the standards

* **TSC Membership**:
  - Pravek Sharma is no longer working on LibOQS and should step down from TSC
  - Douglas hired a new person to take over Pravek's role, who was expected to join this meeting but did not attend
  - **Action**: Matthias to contact Pravek about formally stepping down

* **Sub-project updates**:
  - **mlkem-native** (Hanno Becker):
    - Successfully integrated into OpenTitan (zeroRISC's distribution - https://github.com/zerorisc/expo/pull/97). Integration leverages Keccak hardware acceleration. Added option to disable batching to enable use of hardware Keccak accelerator (accelerator can only handle one state at a time).
    - mlkem-native functional when using 16-bit compilers (AVR 8-bit microcontroller support tested in CI)
  - **mldsa-native** (Matthias Kannwischer):
    - Alpha release planned soon
  - **mlkem-libjade**: No updates
  - **rust-libcrux**: No updates
  - **slhdsa-c**:
    - No current development activity.
    - One student from Douglas's group attempted CBMC proofs but did not complete them
    - slhdsa-c is merged into LibOQS release candidate and will ship in a few weeks

* **Next meeting: 2025-12-04 13:00 UTC**
