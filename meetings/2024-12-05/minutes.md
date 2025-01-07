# 2024-11-21 :  TSC Minutes

## Agenda

* Welcome

* [Minutes/actions from previous meeting](../2024-11-21/minutes.md)

* Updates from related communities:
  * [PQCA](https://github.com/PQCA)
  * [Open Quantum Safe](https://github.com/open-quantum-safe)

* Review status of sub projects:

  * [mlkem-libjade](https://github.com/pq-code-package/mlkem-libjade)
  * [mlkem-rust-libcrux](https://github.com/pq-code-package/mlkem-rust-libcrux)
  * [mlkem-native](https://github.com/pq-code-package/mlkem-c-embedded)

* Discussion (if not covered previously)

  * mlkem-native alpha release / blog post
  * [FIP203 - 7 function api #4](https://github.com/pq-code-package/tsc/issues/4#issuecomment-2456391348)
  * [Working towards liboqs usage #103](https://github.com/pq-code-package/tsc/issues/103)
  * [Requiring OpenSSL CLA #113](https://github.com/pq-code-package/tsc/issues/113)
  * [Other Open TSC issues](https://github.com/orgs/pq-code-package/projects/4/views/1)
  * Meetings : Dec 19, Jan 2 - any changes/cancellations needed?

* Any other business.

## Welcome

Thanks to Matthias for running the meeting last week.
Apologies from Hanno.

## Minutes/actions from previous meeting

### Updates from related communities

#### PQCA

* Sophie Schmeig presented to the PQCA on her concerns around NIST & digital signature algorithms including ML-DSA, including specifically around the API. Can listen to PQCA meeting recordings ([approx 17 mins into this recording](https://zoom.us/rec/play/u-ZnNDvtgGsepLi--IoOEq-0DN7cGuLg3QAbegnl2RSY8f4YKAtWSh9LcHLsPK2F_OIKsIEu9LyBVHBI.KjyivmL72n7vVRIi?canPlayFromShare=true&from=share_recording_detail&continueMode=true&componentName=rec-play&originRequestUrl=https%3A%2F%2Fzoom.us%2Frec%2Fshare%2FAbVOvv5zwjPWVM3kb3Jbi4rHSiw2uH2gcdvkTKA1K-u2wK0mUnspAqcn4gbbN2hR.ArSg7R7z9tlt_D6k)), she's also happy to come to this meeting to discuss her thoughts including the API changes 6 months after NIST release.
* Tooling workgroup meetings have started - team eager to see additional contributions/participation
* We discussed the [proposed blog post](https://github.com/PQCA/TAC/issues/61) - we just need a few approval/reviews & then can publish, hopefully early next week.

#### OQS

* New release ~Friday with security patch.
* codepoint updates.


### Review of subprojects

#### mlkem-native

* Alpha release - stable code, cbmc proofs for core, ml-kem. Now need feedback
* Not incorporated anything based on API discussions, just 3 part API. Need to, but need agreement first. Have draft email to send to NIST.
* Discussion on anywhere else the [blog post](https://github.com/PQCA/TAC/issues/61) should be shared - just website for now.
* Discussed implementation with Basil/Pravek to start discussion on use within liboqs. They have looked at code. One review comment
required change. Work now is actually integrating

#### mlkem-c-libjade

* Old PR deleted
* preparing pull of code including benchmark testing, simple example, crypto artifact. Jasmine implementation completely verified.
* AVX2 x2 improvements being added.
* Tests - plan to test this implementation against native (mlkem-native is tested against official test vectors, Kyber repo test vectors, and test c/avx2/arm etc against each other).

#### Open TSC issues

* [#113](https://github.com/pq-code-package/tsc/issues/113) (OpenSSL SLA) - contributors need to sign OpenSSL CLA. OpenSSL may then be able to use any of our implementations. General consensus this is ok, and we should aim to do it for all subprojects, including new ones from the beginning. We should document our policy and procedures (action).
* [#4](https://github.com/pq-code-package/tsc/issues/4) (API Changes) - as above, email being drafted by Matthias for NIST.

### Any other business
  
## Action items

### New

- [ ] Document our process/policy on OpenSSL CLA

### Outstanding

### Completed

## Recordings

* [Recordings are available on your Open Profile page](https://openprofile.dev/my-meetings) under Past Meetings.

## Upcoming TAC meetings

* Next TSC meeting in 2 weeks, 2024-12-19 1300 UTC. Nigel, Tiago noted they would not be able to attend.

[Please check the calendar](https://pqca.org/calendar/)

## Attended by

### TSC voting members

* [ ] [Manuel Barbosa](https://github.com/mbbarbosa), University of Porto
* [ ] [Hanno Becker](https://github.com/hanno-becker), AWS
* [X] [Nigel Jones](https://github.com/planetf1), IBM
* [X] [Matthias J. Kannwischer](https://github.com/mkannwischer), Chelpis Quantum Tech
* [ ] [Franziskus Kiefer](https://github.com/franziskuskiefer), Cryspen
* [X] [Tiago Oliveira](https://github.com/tfaoliveira), Sandbox AQ
* [ ] [John Schanck](https://github.com/jschanck), Mozilla
* [X] [Pravek Sharma](https://github.com/praveksharma), University of Waterloo
* [ ] [Douglas Stebila](https://github.com/dstebila), University of Waterloo

### Additional attendees
