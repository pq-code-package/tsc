# 2025-05-22 : TSC Minutes

## Agenda

* Welcome
* Minutes/actions from previous meeting
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

Nigel Jones welcomed attendees to the meeting, noting the return to the "normal" meeting time.

## Minutes/actions from previous meeting (2025-05-08)

* Nigel Jones mentioned that the AI-generated minutes from the last meeting (2025-05-08) were available in a pull request, noting a date error that needed correction. He encouraged review and comments.
* **Review of 2025-05-08 Action Items**:
    * **Google Calendar Link**: Nigel Jones reported that the issue with the incorrect Google Calendar link on the website (confusing "Add to Google Calendar" link) was raised with the Linux Foundation (LF) TAC representative, who confirmed a change would be made imminently.
    * **Meeting Time Change**: This was handled offline, and the current meeting reflects the reversion to the previous time slot.
    * **TSC Lead Nominations**: To be discussed under its agenda item.
    * **Manuel Barbosa (mlkem-libjade SHA3 consumable), Franziskus Kiefer (common README), Pravek Sharma (ICMC slide)**: Deferred as Pravek was not present and these were linked to his input or specific project updates.

## Updates from related communities

### PQCA

* Nigel Jones reported attending the latter half of the recent PQCA meeting.
* Much of the PQCA meeting discussed their own calendar entry confusions.
* A significant discussion point was the PQCA Marketing Outreach Committee, including issues around their meeting publicity. The committee aims to improve publicity for PQCA activities, including organizing blog posts. Members interested in contributing were advised to check the PQCA minutes.

### Open Quantum Safe (OQS)

* Nigel Jones noted the OQS release a couple of weeks prior, which included mlkem-native.
* No other specific OQS updates were discussed by the group.
* **SLH-DSA in OQS**: Nigel Jones mentioned a discussion from the PQCA call about a proposed SLH-DSA implementation for OQS ([liboqs issue #1894](https://github.com/open-quantum-safe/liboqs/issues/1894), shared by Franziskus Kiefer in chat). It appears a student in Waterloo (close to the OQS team and Douglas Stebila) might be looking into it. This raised questions about whether PQCP should be involved, the state of any upstream project, and potential consistency with PQCP implementations. Matthias Kannwischer commented that SLH-DSA with the existing Keccak (SHA3) work isn't too hard to implement.

## PQCP TSC Lead Election

* Nigel Jones, whose term was up, announced he would not be re-standing for the TSC Lead position.
* The issue for nominations had been open for three weeks with no nominations received.
* The meeting was technically not quorate (requiring 5 TSC members, 4 were present including Nigel).
* **Proposal**: To provisionally discuss and identify a potential lead, then confirm via GitHub issue or at the next quorate meeting. Nigel would also consult the Linux Foundation for advice on procedure.
* Matthias Kannwischer asked about the responsibilities of the TSC Lead. Nigel outlined them as:
    * Liaising with other PQCA groups.
    * Being a voting member on the PQCA Committee.
    * Ensuring a regular heartbeat of communication for PQCP (e.g., organizing regular meetings).
    * Potentially other project involvement.
* **Nominations**:
    * Matthias Kannwischer nominated himself, stating he would do it if no one else stepped up.
    * Franziskus Kiefer expressed similar sentiments but felt he wouldn't have enough time to do the role properly and deferred to Matthias.
    * Hanno Becker stated he did not have the bandwidth.
* **Outcome**: Matthias Kannwischer was the sole nominee.
* **Decision**: The group provisionally agreed to Matthias Kannwischer becoming the new TSC Lead.
* **Action**: Matthias nominated himself on the relevant GitHub issue during the meeting. Nigel Jones requested attendees to vote on the issue to formalize the election once the required number of votes is reached. Nigel will assist Matthias with the transition (e.g., meeting scheduling).

## Review status of sub-projects

### mlkem-native

* Hanno Becker provided updates:
    * **ARM64 Functional Correctness Proofs**: All ARM64 functional correctness proofs (using HOL Light) are now complete, including for rejection sampling. Credit was given to John Harrison for this work. This meets the technical bar for a v1.0 release.
    * **Relicensing**: The project is awaiting the final relicensing of the assembly code to the triple license (Apache-2.0 OR ISC OR MIT) to match the rest of the repository. Arm has agreed via email, but a formal commit on the repository (as recommended by Hart Montgomery from LF) is pending. Once this is complete, v1.0 will be released.
    * **Reason for Relicensing**: Hanno explained the relicensing (from just Apache-2.0 for the bulk and MIT for some Arm-originated assembly) was proactive to make consumption by other projects (like AWS-LC, which uses Apache/ISC dual-license) as smooth as possible by minimizing licensing discussions, rather than a response to a specific blocker.
    * **Verification Blog Post**: Nigel Jones suggested a blog post detailing the verification work (HOL Light, CBMC) as a key selling point for the implementation. Hanno agreed this would be worthwhile once v1.0 is out and suggested pinging the Linux Foundation to help promote it. Franziskus Kiefer noted this aligns with the original goals of PQCP to have a minimum bar of correctness proofs and should be highlighted in READMEs.

### mldsa-native

* Matthias Kannwischer reported:
    * Work is in progress.
    * CBMC proofs are almost done (expected in another week or two).
    * Work has started on adding ARM64 and AVX2 assembly, with some functions still left.
    * Many small things are still needed before integration into liboqs and other places, but progress is steady, benefiting from the work done on mlkem-native.

### mlkem-libjade

* No updates as Manuel Barbosa was not present.

### mlkem-rust-libcrux

* Franziskus Kiefer reported:
    * Work is now on their roadmap.
    * **README/Documentation**: A first version of a common README will be created for libcrux. This will serve as a basis for discussion on what information should be standard across PQCP projects (e.g., verification status labeling, performance comparison methods). This relates to the "assurance" and "initial docs" issues.
    * **Common APIs**: Work will be done to implement the common APIs discussed at HACS (as per the open GitHub issue), adapting them for Rust while maintaining naming and structural consistency with C implementations. This should also progress the "cross-implementation APIs" issue.
    * These two items are hoped to be done within the next two weeks.
    * Once the ML-KEM work is complete, they can look at ML-DSA (their implementation is done, proofs expected in ~2 weeks).

### mlkem-c-embedded

* Nigel Jones stated this should be removed from the agenda as it was previously decided to leave it for now.

## Discussion

### Other Open TSC Issues

* Nigel Jones suggested that some older, generic issues (e.g., "assurance initial docs") might be closable if they are not actionable or are being superseded by organic work within the projects. This could be a follow-up activity.
* Franziskus Kiefer noted his planned work on the libcrux README and APIs should address or move forward some of these existing general issues.
* **John VanDyke's TSC Membership**: Nigel Jones raised that John VanDyke is still listed as a TSC voting member but has not been able to attend meetings. To make achieving a quorum easier, it was suggested he be moved from a voting member role.
    * **Action**: Matthias Kannwischer to contact John VanDyke about this.

### Upcoming Conferences

* No specific upcoming conferences were discussed.

### Confirm date/time of next meeting

* The next meeting will be in two weeks at the current (reverted) time slot. (Thursday, June 5, 2025).

## Any other business

* Nigel Jones offered to share details with Matthias Kannwischer on meeting scheduling logistics.

## Action items

### New

* [ ] Nigel Jones to correct the date on the 2025-05-08 minutes PR.
* [ ] All TSC members to review and comment on the 2025-05-08 minutes PR.
* [ ] TSC members to vote on the GitHub issue for Matthias Kannwischer's TSC Lead nomination to formalize the election.
* [ ] Hanno Becker (and team) to consider a blog post on mlkem-native verification achievements post-v1.0 release and liaise with LF for promotion.
* [ ] Matthias Kannwischer (and team) to continue work on mldsa-native, focusing on CBMC proofs and assembly.
* [ ] Franziskus Kiefer (and team) to:
    * Create a draft common README structure for the mlkem-rust-libcrux repository.
    * Implement common APIs for mlkem-rust-libcrux.
* [ ] Matthias Kannwischer to contact John Schanck regarding his status as a voting TSC member.
* [ ] Nigel Jones to remove 'mlkem-c-embedded' from future meeting agendas.
* [ ] Nigel Jones to share meeting scheduling logistics with Matthias Kannwischer.
* [ ] TSC (led by Matthias Kannwischer) to review open TSC issues for potential closure or update.

### Outstanding (from 2025-05-08)

* [ ] Manuel Barbosa to investigate making the libjade SHA3 implementation externally consumable. (Deferred)
* [ ] Pravek Sharma to share his ICMC slide regarding consumer considerations for PQCP implementations when the documentation discussion is active. (Deferred)
* (From previous minutes) Document our process/policy on OpenSSL CLA - on hold.

## Attended by

### TSC voting members

* Nigel Jones (IBM) - Outgoing TSC Lead
* Matthias Kannwischer (Chelpis Quantum Tech) - Incoming TSC Lead
* Franziskus Kiefer (Cryspen)
* Hanno Becker (AWS)

### Additional attendees

* None.