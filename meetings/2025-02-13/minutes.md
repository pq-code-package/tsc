# 2025-02-13 :  TSC Minutes

## Agenda

* Welcome

* [Minutes/actions from previous meeting](../2025-01-30/minutes.md)

* Membership changes

  * Douglas Stebila has now [resigned](https://github.com/pq-code-package/tsc/pull/134) from the TSC
  * Welcome the mldsa-native project (agreement via [github](https://github.com/pq-code-package/tsc/issues/135))
    * [Propose @jakemas as voting TSC member](https://github.com/pq-code-package/tsc/issues/139)

* [New meeting time proposal](https://github.com/pq-code-package/tsc/issues/128) - current proposal:
  * Europe/Asia meeting at 1000 CET
    * 0900 UK, 1700 Taiwan
  * Europe/USA meeting at 1700 CET
    * 0800 US West Coast
    * 1000 Toronto
    * 1100 US East Coast
  * Scheduled for 30 minutes in Central Europe time zone & will follow daylight savings.
  * Continue with Thursday. 2 weeks between meetings, so 4 weeks per slot.

* Updates from related communities:
  * [PQCA](https://github.com/PQCA)
  * [Open Quantum Safe](https://github.com/open-quantum-safe)

* Review status of sub projects:

  * [mlkem-native](https://github.com/pq-code-package/mldsa-native)
  * [mldsa-native](https://github.com/pq-code-package/mlkem-native)
  * [mlkem-libjade](https://github.com/pq-code-package/mlkem-libjade)
  * [mlkem-rust-libcrux](https://github.com/pq-code-package/mlkem-rust-libcrux)
    * [what do do with repo/docs](https://github.com/pq-code-package/tsc/issues/128)
  * [mlkem-native](https://github.com/pq-code-package/mlkem-c-embedded)
    * [liboqs integration](https://github.com/pq-code-package/mlkem-native/issues/653)
    * [NIST clarification](https://github.com/pq-code-package/tsc/issues/4)
    * [OpenSSL CLA](https://github.com/pq-code-package/tsc/issues/113)

* Discussion (if not covered previously)

  * [Other Open TSC issues](https://github.com/orgs/pq-code-package/projects/4/views/1)

* Any other business

## Welcome

Noted that Douglas has resigned as per agenda notice, and that ML-DSA native is welcomed as a new subproject

## Minutes/actions from previous meeting

### Updates from related communities

#### PQCA

* A blog post was published two weeks ago from Nvidia on accelerating PQC.
* A blog post is being prepared for the one-year anniversary of PQCA.
  * There will be a section in the blog post on PQCP.
  * A section on "what to expect in 2025" will be included.

#### OQS

* Two big changes were getting mlkem-native into OQS thanks to Basil Hess and the ML-KEM implementation from CUPQC from Nvidia.
* There have been loose conversations around API changes.
  * The feeling is that preserving the current three-function API is not a priority, and offering flexibility to users is preferred.
* Discussions are underway about whether PQCP should make its own ML-KEM provider.
  * A new issue will be created for discussion.
* An issue was recently opened on liboqs talking about adding checks for ML-KEM keys.
  * The specific check that it mentioned is called pairwise consistency checks.

### Review of subprojects

#### mlkem-native

* API changes are being discussed.
  * The API will be implemented in MLKEM-Native.
  * The NIST discussions did not go any further.
  * The API will be implemented in a backward, compatible way.
  * Additional functions will be added.
  * The NIST issue will be closed.
* The AWS-LC integration is in progress.
  * A pull request has been opened: https://github.com/aws/aws-lc/pull/2176
The OpenSSL CLA issue was discussed.
* The issue is whether to get the contributors to ML-KEM-Native to sign the CLA.
* This means not just the current contributors but also the previous contributors to the reference implementation.
* The feedback from Peter Schwabe was positive, but he has yet to reach out to the rest of the team.
* There are nine people in the AUTHORS file of the reference implementation.
* It is not very likely that OpenSSL will use the PQCP algorithm.
* The PQCP TSC needs to decide whether it is worth the time to get the CLA signed.
* The issue will be closed if it is not going anywhere.
* The PQCrystals team will be double-checked.
* If they have not signed the CLA, then the issue will be closed.  

#### Open TSC issues

It was noted we should review the backlog in a future meeting

### Any other business

* An offline vote will be held on whether to add Jake Massimo (@jakemas) to the TSC as a voting member.
* Agreed to reschedule future meetings as per notice in Agenda - PQCA Calendar will be updated

## Action items

### New

### Outstanding

### Completed

* [X] Document our process/policy on OpenSSL CLA
* [X] Review/followup NIST clarification around deserialized parameters (Hanno/Matthias)

## Recordings

* [Recordings are available on your Open Profile page](https://openprofile.dev/my-meetings) under Past Meetings.

## Upcoming TAC meetings

* Next TSC meeting in 2 weeks, 2025-02-27 0900 UTC.

[Please check the calendar](https://pqca.org/calendar/)

## Attended by

### TSC voting members

* [X] [Manuel Barbosa](https://github.com/mbbarbosa), University of Porto
* [ ] [Hanno Becker](https://github.com/hanno-becker), AWS
* [X] [Nigel Jones](https://github.com/planetf1), IBM
* [X] [Matthias J. Kannwischer](https://github.com/mkannwischer), Chelpis Quantum Tech
* [X] [Franziskus Kiefer](https://github.com/franziskuskiefer), Cryspen
* [ ] [Tiago Oliveira](https://github.com/tfaoliveira), Sandbox AQ
* [ ] [John Schanck](https://github.com/jschanck), Mozilla
* [X] [Pravek Sharma](https://github.com/praveksharma), University of Waterloo

### Additional attendees

* Jp Lomas, Die QRL Stiftung
* Justine Paul, Die QRL Stiftung
