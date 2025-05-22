# 2025-05-08 : TSC Minutes

## Agenda

* Welcome
* Minutes/actions from previous meeting
    * review meeting times
* Updates from related communities:
    * [PQCA](https://github.com/PQCA)
    * [Open Quantum Safe](https://github.com/open-quantum-safe)
* PQCP TSC Lead election.
* Review status of sub projects:
    * [mlkem-native](https://github.com/pq-code-package/mlkem-native)
    * [mldsa-native](https://github.com/pq-code-package/mldsa-native)
    * [mlkem-libjade](https://github.com/pq-code-package/mlkem-libjade)
    * [mlkem-rust-libcrux](https://github.com/pq-code-package/mlkem-rust-libcrux)
    * [mlkem-c-embedded](https://github.com/pq-code-package/mlkem-c-embedded)
* Discussion (if not covered previously)
    * [Other Open TSC issues](https://github.com/orgs/pq-code-package/projects/4/views/1)
        * can we close any of these issues?
    * Upcoming conferences
    * Confirm date/time of next meeting
* Any other business

## Welcome

Nigel Jones welcomed attendees to the meeting.

## Minutes/actions from previous meeting

### Review Meeting Times

* The group discussed the trial of split meeting times, which aimed to increase attendance by accommodating different time zones.
* It was noted that attendance had been low in recent meetings.
* Pravek Sharma commented that the previous single meeting time was carefully chosen to balance the needs of members in North America and Taiwan and suggested reverting to it.
* Franziskus Kiefer mentioned that travel and issues with the Google Calendar link (still pointing to an old calendar) had affected his attendance. He also noted that the current alternative time was mainly for US West Coast attendees, and if they weren't joining, it might not be necessary.
* Nigel Jones acknowledged the calendar link issue and the difficulty of split times with a small group.
* **Decision**: Members were asked to comment on [issue #157](https://github.com/pq-code-package/tsc/issues/157) regarding reverting to the original single meeting time.

## Updates from related communities

### PQCA

* Nigel Jones was unable to attend the previous day's PQCA meeting but had provided them with an update on PQCP, including the meeting time discussion and progress on ML-DSA and ML-KEM. No updates were available from the PQCA meeting itself.

### Open Quantum Safe (OQS)

* Pravek Sharma reported that he and Spencer presented at ICMC, discussing PQCA, PQCP, and OQS.
* They released their first user survey, which yielded some responses, including interest in cryptographic agility.
* OQS released a new version three weeks prior, which was the first to include mlkem-native.
* Pravek is looking into the integration code needed for mldsa-native.

## PQCP TSC Lead Election

* Nigel Jones proposed extending the nomination period for the TSC Lead by one week from the previous day (May 7th, 2025), as over half the TSC members had only recently agreed to the election process.
* If multiple nominations are received, a vote will be held in a week's time.
* Members were encouraged to nominate themselves or others.

## Review status of sub-projects

### mlkem-native & mldsa-native

* Nigel Jones mentioned ongoing discussions around relicensing mlkem-native and mldsa-native to a triple license (Apache 2.0, MIT, ISC) and seeking contributor agreement. Pravek Sharma confirmed awareness and his agreement.
* The previous discussion about requiring OpenSSL CLAs was on hold until more interest from OpenSSL was shown.
* There is an ongoing stream of fixes, formal verifications, and proofs, particularly for mldsa-native, including new benchmarking.

### mlkem-libjade

* Manuel Barbosa reported interactions with industrial partners who are moving towards adopting the code.
* Tweaks are being made to the ML-KEM code to meet partner requirements, with a plan to freeze implementations and push them to the PQCoding repository before the summer.
* Pravek Sharma inquired about the common code (e.g., SHA3) used in libjade and the possibility of a separate repository for this formally verified common code, which could then be used by liboqs or other implementations.
* Manuel Barbosa confirmed they can make their SHA3 implementation externally consumable and will look into it.

### mlkem-rust-libcrux

* Franziskus Kiefer stated his plan is to not have the code directly in the PQCP repository but rather a document linking to it and describing the implementation.
* He emphasized the need for a common README layout across PQCP projects to present information like API, verification status, and benchmarks consistently. He plans to create a first version for the libcrux repository.
* Pravek Sharma noted that platform choice (e.g., Windows support) is another important factor for consumers and offered to share a slide he created for ICMC on this topic.

### mlkem-c-embedded

* No specific updates mentioned in the transcript.

## Discussion

### Other Open TSC Issues

* The main open issues discussed were the meeting schedule ([issue #157](https://github.com/pq-code-package/tsc/issues/157)), the request for TSC Lead nominations, the long-running discussion on API changes, and meeting times.

### Upcoming Conferences

* ICMC was mentioned where Pravek and Spencer presented.

### Confirm date/time of next meeting

* To be decided based on feedback on [issue #157](https://github.com/pq-code-package/tsc/issues/157) regarding meeting times. Nigel Jones will update the calendar accordingly.

## Any other business

* No other business was discussed.

## Action items

### New

* [ ] Nigel Jones to follow up again on the incorrect Google Calendar link on the website.
* [ ] All TSC members to comment on [issue #157](https://github.com/pq-code-package/tsc/issues/157) regarding reverting to the original single meeting time.
* [ ] TSC members to submit nominations for TSC Lead.
* [ ] Manuel Barbosa to investigate making the libjade SHA3 implementation externally consumable.
* [ ] Franziskus Kiefer to create a proposal for a common README/documentation structure for PQCP projects, starting with the libcrux repository.
* [ ] Pravek Sharma to share his ICMC slide regarding consumer considerations for PQCP implementations (e.g., platform choice) when the documentation discussion is active.

### Outstanding

* (From previous minutes) Document our process/policy on OpenSSL CLA - on hold.

## Attended by

### TSC voting members

* Nigel Jones (IBM)
* Manuel Barbosa (University of Porto)
* Franziskus Kiefer (Cryspen)
* Pravek Sharma (University of Waterloo)

### Regrets

* Hanno Becker (AWS)
* Matthias J. Kannwischer (Chelpis Quantum Tech)

### Additional attendees

* None.