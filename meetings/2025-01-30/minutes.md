# 2025-01-30 :  TSC Minutes

## Agenda

* Welcome

* [Minutes/actions from previous meeting](https://github.com/pq-code-package/tsc/pull/129)
  * [X] Open issue to discuss next steps on libcrux rust library. (Franziskus)
  * [X] Open issue on meeting times (Pravek)
  * [ ] Review/follow-up NIST clarification around deserialized parameters (Hanno/Matthias)

* Updates from related communities:
  * [PQCA](https://github.com/PQCA)
  * [Open Quantum Safe](https://github.com/open-quantum-safe)

* Review status of sub projects:

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
  * [meeting times](https://github.com/pq-code-package/tsc/issues/128)

## Welcome

## Minutes/actions from previous meeting

Minutes from last meeting open as PR
Will discuss actions from last meeting in later sections

### Updates from related communities

#### PQCA

* Tooling group still looking for additional members
* [Blog post (Linked in)](https://www.linkedin.com/pulse/post-quantum-cryptographic-alliancepqca-enabling-transition-njqyf/) published on PQC in 5G networks (now using mlkem-native)
* Tooling workgroup open to additional contributions - currently working on sonarqube scanning for PQC.
* Note that [AWS website](https://aws.amazon.com/security/post-quantum-cryptography/) now has reference to pq-code-package.

#### OQS

* No update - no attendees overlap this week
* Noted that [mlkem-native adoption into liboqs](https://github.com/open-quantum-safe/liboqs/pull/2041) is in progress

### Review of subprojects

#### mlkem-c-libjade

* No significant update

#### mlkem-rust-libcrux

* Hoping to get input on issue & discuss in next meeting
* New upstream release (more apis) expected soon (being picked up by Signal)

#### mlkem-native

* Focussing on liboqs integration.
  * A few minor stumbling blocks.
  * Biggest was some performance regression on x86 not seen in local benchmarks. Fixed and now within 10% of PQCrystals reference implementation.
  * Contributor is that not all the assembly is imported, only that deemed most important for performance, since it causes additional verification burden.
  * Additional verification for ntt/inverse ntt (from John Harrison) for aarch64 [readme](https://github.com/pq-code-package/mlkem-native/blob/main/README.md#formal-verification)
  * Integration now ready. Waiting for second approval.
  * Will tag mlkem-native code as beta
  * Work underway to avoid key expansion - will help with NIST API discussion, as well as in performance comparisons (for example as done with OpenSSL)
  * Some [CLA](https://github.com/pq-code-package/tsc/issues/113) discussion - continue in next meeting
  * Background experimentation with AWS-LC especially in relation to toolchain/structure

#### Open TSC issues

* [Changes to meeting times](https://github.com/pq-code-package/tsc/issues/128) are proposed - please review

### Any other business

* Max asked if anyone is looking at ML-DSA key expansion, as there's been a discussion at the [IETF](https://wiki.ietf.org/group/sec/PQCAgility).
  * Primary concern - interoperability.
  * Also finance industry is trying to build tests
  * Discussed Sophie Schmeg's presentation at the [PQCA in December - 20241204](https://zoom.us/rec/play/rD-iJ3VJ9q_vpKghYI6amBK1gGikKcnz4R7bspj7eWXXR0VQNRZjSmeQmJKL-QT0pzGASG3URi-hBYWM.S7uEigxVQLrkErQ-?canPlayFromShare=true&from=share_recording_detail&continueMode=true&componentName=rec-play&originRequestUrl=https%3A%2F%2Fzoom.us%2Frec%2Fshare%2FAbVOvv5zwjPWVM3kb3Jbi4rHSiw2uH2gcdvkTKA1K-u2wK0mUnspAqcn4gbbN2hR.ArSg7R7z9tlt_D6k)(starts 17 minutes in) & mlkem-native discussion on key formats.

## Action items

### New

### Outstanding

* [ ] Document our process/policy on OpenSSL CLA
* [ ] Review/followup NIST clarification around deserialized parameters (Hanno/Matthias)

### Completed

* [X] Open issue to discuss next steps on libcrux rust library. (Franziskus)
* [X] Open issue on meeting times (Pravek)

## Recordings

* [Recordings are available on your Open Profile page](https://openprofile.dev/my-meetings) under Past Meetings.

## Upcoming TAC meetings

* Next TSC meeting in 2 weeks, 2025-02-13 1300 UTC.

[Please check the calendar](https://pqca.org/calendar/)

## Attended by

### TSC voting members

* [X] [Manuel Barbosa](https://github.com/mbbarbosa), University of Porto
* [X] [Hanno Becker](https://github.com/hanno-becker), AWS
* [X] [Nigel Jones](https://github.com/planetf1), IBM
* [ ] [Matthias J. Kannwischer](https://github.com/mkannwischer), Chelpis Quantum Tech
* [X] [Franziskus Kiefer](https://github.com/franziskuskiefer), Cryspen
* [ ] [Tiago Oliveira](https://github.com/tfaoliveira), Sandbox AQ
* [ ] [John Schanck](https://github.com/jschanck), Mozilla
* [ ] [Pravek Sharma](https://github.com/praveksharma), University of Waterloo

### Additional attendees

* Massimiliano Pala