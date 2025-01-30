# 2025-01-16 :  TSC Minutes

## Agenda

* Welcome

* [Minutes/actions from previous meeting](2024-12-05/minutes.md)
  * noted issue about OpenSSL - added to agenda later

* Updates from related communities:
  * [PQCA](https://github.com/PQCA)
  * [Open Quantum Safe](https://github.com/open-quantum-safe)

* Review status of sub projects:

  * [mlkem-libjade](https://github.com/pq-code-package/mlkem-libjade)
  * [mlkem-rust-libcrux](https://github.com/pq-code-package/mlkem-rust-libcrux)
  * [mlkem-native](https://github.com/pq-code-package/mlkem-c-embedded)
    * [liboqs integration](https://github.com/open-quantum-safe/liboqs/pull/2041) also [TSC issue](https://github.com/pq-code-package/tsc/issues/103)
      * Draft PR from Basil. Some code structure discussions. Consider blog after release?
    * Feedback/next steps from [blog post](https://pqca.org/blog/2024/pqca-announces-alpha-release-of-mlkem-native/)?  & [llm summary](https://docs.google.com/document/d/1VVP01fdHh7IVWG2Y-Njd3GIyTa8cZI50L-zJWr3Zaz4/edit?tab=t.0)
  
* Discussion (if not covered previously)

  * [FIP203 - 7 function api #4](https://github.com/pq-code-package/tsc/issues/4#issuecomment-2456391348)
  * [Requiring OpenSSL CLA #113](https://github.com/pq-code-package/tsc/issues/113)
    * Correction in [minutes](https://github.com/pq-code-package/tsc/pull/124) - suggest voting
  * [Other Open TSC issues](https://github.com/orgs/pq-code-package/projects/4/views/1)
  * Reminder: PQCP TSC vote in May - current term ends 2025-05-22

* Any other business

## Welcome

## Minutes/actions from previous meeting

Correction noted from previous meeting minutes (openSSL CLA). Will update.

### Updates from related communities

#### PQCA

* First meeting yesterday.
* Pointed out mlkem-native progress & blog post.
* Tooling workgroup open to additional contributions - currently working on sonarqube scanning for PQC.

#### OQS

* mlkem-native integration (more detail later)
* new release at end of year

### Review of subprojects

#### mlkem-c-libjade

* Progress on arm implementations of mlkem. Non vectorized, running on embedded platform. Proof finished for avx2. Release soon.

#### mlkem-c-libcrux

* rust library already installable from upstream source via cargo. Less likely people would just go to github to use. No additional engagement from other contributors. No value-add in having code duplication, so proposing to focus on documentation, findability.
* there is one other serious rust implementation (rust crypto) - but not formal verification.
* Discussion - need to consider what/how to document/point to library. Open an issue to address.
* question about whether it's worth having tests here - but who would maintain?

#### mlkem-native

* Main technical work complete.
* CBMC proofs complete for C.
* Now focussing on ease of use, platform compatibility, documentation.
* Integration work with liboqs underway. PR passes CI. Docs to do ie constant-time tests. Currently needs patch - but not a blocker. will make integrated version a v1 beta.
* Final version - outstanding question of whether to expose API using internal key format to improve performance
* Looking at integration with AWS-LC - challenges include big differences in build approach.
* considering how to handle all integration cases with different needs on structure.
* No feedback from blog post.
* Could consider another blog post when part of liboqs release
* Matthias needs to reach out on NIST lists about [API changes](https://github.com/pq-code-package/tsc/issues/4) to expose deserialized keys. Think currently in draft. Not having these can hurt performance comparisons, for example with openSSL. Other implementations also have this including libcrux, boringSSL. Hanno will followup including review.

#### Open TSC issues

* [Open SSL CLA #113](https://github.com/pq-code-package/tsc/issues/113)
  * OpenSSL currently integrating from boringSSL.
  * mlkem-native briefly mentioned in [openssl discussion thread](https://github.com/openssl/openssl/issues/26006).
  * Franziskus noted that they (cryspen) are currently replacing boringSSL with mlkem-native.
  * openSSL had a performance comparison - boringSSL C faster (see above comment on deserialized parameters).
  * Concerned about needing C90 -- so mlkem-native is now updated for this.
  * They seem to be looking at performance improvements now. less likely to change direction?
  * For mlkem-native, cla doesn't seem to be a problem - but they'd want the reference contributors to sign too. Matthias had initial conversation with Peter Schwabe.
  * Noted that if we do it, easier to do sooner not later.
  * will continue discussion in next meeting.

* Additional algorithms
  * PQCP was setup as a source of production-ready algorithms.
  * No additional teams/people for other algorithms yet.
  * Franziskus noted that have ml-dsa in rust, started verifying. Portable and avx2. Maybe neon
  * Manuel - also in libjade, ml-dsa in x86 avx + ref, scalar, and arm (not vectorized). neither verified yet - will be starting that.

### Any other business

* Current TSC lead term ends 22 May - similar in PQCA. Leads will be up for election.
* Pravel noted we'd discussed meeting times in December - will open issue to see if there's a desire to change times to accomodate more people/location.

## Action items

### New

* [ ] Open issue to discuss next steps on libcrux rust library. (Franziskus)
* [ ] Open issue on meeting times (Pravek)
* [ ] Review/followup NIST clarification around deserialized parameters (Hanno/Matthias)

### Outstanding

* [ ] Document our process/policy on OpenSSL CLA

### Completed

## Recordings

* [Recordings are available on your Open Profile page](https://openprofile.dev/my-meetings) under Past Meetings.

## Upcoming TAC meetings

* Next TSC meeting in 2 weeks, 2025-01-30 1300 UTC.

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
* [X] [Pravek Sharma](https://github.com/praveksharma), University of Waterloo
* [ ] [Douglas Stebila](https://github.com/dstebila), University of Waterloo

### Additional attendees

* J P Lomas, QRL