# 2024-11-07 :  TSC Minutes

## Agenda

* Welcome

* [Minutes/actions from previous meeting](../2024-10-24/minutes.md)
  * Proposal/vote on Pravek Sharma joining TSC.
  * Note that the generic repo is now archived.

* Updates from related communities:
  * [PQCA](https://github.com/PQCA)
  * [Open Quantum Safe](https://github.com/open-quantum-safe)

* Review status of sub projects:

  * [mkkem-libjade](https://github.com/pq-code-package/mlkem-libjade)
  * [mlkem-rust-libcrux](https://github.com/pq-code-package/mlkem-rust-libcrux)
  * [mlkem-c-embedded](https://github.com/pq-code-package/mlkem-c-embedded)
  * [mlkem-c-aarch64](https://github.com/pq-code-package/mlkem-c-aarch64)

* Discussion (if not covered previously)

  * [Renaming of mlkem-native #105](https://github.com/pq-code-package/tsc/issues/105)
  * [FIP203 - 7 function api #4](https://github.com/pq-code-package/tsc/issues/4#issuecomment-2456391348)
  * [Working towards liboqs usage #103](https://github.com/pq-code-package/tsc/issues/103)
  * [Do we supply randombytes() #86](https://github.com/pq-code-package/tsc/issues/86) - NO/test-only / close ?
  * [Requiring OpenSSL CLA #113](https://github.com/pq-code-package/tsc/issues/113)
  * [Other Open TSC issues](https://github.com/orgs/pq-code-package/projects/4/views/1)

* Any other business
  * meeting time (1300 UTC) after summer->winter time

 ## Welcome

* We welcomed 
  * Peter Schwabe (Max Planck Institute) - involved in PQCA/PQCP kickoff. 
  * Guncha Malik (IBM) - from IBM Cloud.

## Minutes/actions from previous meeting

* Pravek Sharma has been voted in (offline) as a PQCP TSC Voting member. As a member of the OQS TSC he will be particularly focussed on ensuring good communication between the projects, as Douglas Steibla did previously.

### Updates from related communities

#### PQCA

No update. Nigel was unable to attend the PQCA this week.

#### OQS

* Bringing in updates for the latest ML-DSA FIPS spec, including update the context string. 
* Talks underway on SLH-DSA.
* oqs provider - Code points updated, composite strings update, update in next week.
* Demos - contributor bring in profiling based on Locust - could be useful in filling in current profiling gaps in oqs.
* Pravek also asked if there was specific information the pqcp tsc would find useful
* some discussions to integrate mlkem-native, maybe rust/crux. OQS falling behind in IETF hackathon, so needs to get the standard algorithms implementations in first. Once done can integrate other upstreams.

### Review of subprojects

No updates on libjade, libcrux, or embedded.

### mlkem-native (was mlkem-c-aarch64)

* Main focus is becoming a generic implementation.
* Agreed renaming to mlkem-native.
* Peter introduced discussion on API changes:
  * NIST competition was based on 3 function API - as done in prior competitions.
  * Input validation is required, yet not covered by API - meaning in machine readable terms?
  * Explicit API already implemented by BoringSSL & others
  * 7 function API can address validation, efficiently
  * _Listen to the recording for the full, detailed discussion on specific issues, performance, solutions_
  * Important we consult with NIST & ultimately get some public clarity.
  * OQS also looking at additional APIs. Pravek will discuss with Douglas.
  * See [issue #4](https://github.com/pq-code-package/tsc/issues/4)
  * would want to adopt a similar approach in implementations like libjade, libcrux - get input from Franziskus.
  * Initial release
    * mlkem-native will working on alpha release soon to get feedback on library usability, platform specific issues, API.
    * API changes will not gain consensus in 2 weeks - so not included.
    * Lots of progress on formal verification with CBMC & assembly, but no specific targets for alpha release.
    * Should think about how much we need to publicize/target - blog?

#### Open TSC issues

* [#86](https://github.com/pq-code-package/tsc/issues/86) - agreed to close
* [[#113](https://github.com/pq-code-package/tsc/issues/113)] - proposal that all previous, current, future contributors need to agree to OpenSSL CLA, so that they can consider usage of pqcp. Nigel will add link to CLA. Please review

### Any other business

* Meeting time: difficult for west-coast US. Agreed to stick with current time. Any discussion can happen in forums.
* Pairwise consistency check - seems unnecessary. Not an issue for static keys, but a lot of current usage is ephemeral. Could adopt key caching. Standard indicates check is every time. Peter will probe NIST prior to public discussion. Matthias offered to write public post at a future appropriate time.

#### Releases

#### liboqs representative

## Action items

### New

### Outstanding

### Completed

## Recordings

* [Recordings are available on your Open Profile page](https://openprofile.dev/my-meetings) under Past Meetings.

## Upcoming TAC meetings

* Next TSC meeting in 2 weeks, 2024-11-21 1300 UTC.

[Please check the calendar](https://pqca.org/calendar/)

## Attended by

### TSC voting members

* [ ] [Manuel Barbosa](https://github.com/mbbarbosa), University of Porto
* [X] [Hanno Becker](https://github.com/hanno-becker), AWS
* [X] [Nigel Jones](https://github.com/planetf1), IBM
* [X] [Matthias J. Kannwischer](https://github.com/mkannwischer), Chelpis Quantum Tech
* [ ] [Franziskus Kiefer](https://github.com/franziskuskiefer), Cryspen
* [ ] [Tiago Oliveira](https://github.com/tfaoliveira), Sandbox AQ
* [ ] [John Schanck](https://github.com/jschanck), Mozilla
* [X] [Pravek Sharma](https://github.com/praveksharma), University of Waterloo
* [ ] [Douglas Stebila](https://github.com/dstebila), University of Waterloo

### Additional attendees

* Peter Schwabe, Max Planck Institute
* Guncha Malik,IBM
