# 2025-06-05 :  TSC Minutes

## Attendees
TSC members: 
* [ ] Manuel Barbosa
* [X] Hanno Becker
* [X] Matthias J. Kannwischer
* [ ] Franziskus Kiefer
* [X] Tiago Oliveira
* [X] Pravek Sharma
* [ ] Jake Massimo

Other attendees:
 * Hayden Parsons (University of Waterloo)

## Action items
- [ ] Everyone: Look at https://insights.linuxfoundation.org/
- [ ] Everyone: Propose blog posts for the PQCA website
- [X] Matthias: Reschedule meeting to monthly. Next meeting: 2025-07-03 13:00 UTC
- [X] Matthias: Proposing closing orphaned issues

## Minutes 

* Minutes/actions from previous meeting
 * Minutes available at https://github.com/pq-code-package/tsc/blob/main/meetings/2025-05-22/minutes.md

* Nigel Jones ending his term as TSC team lead
  - Matthias thanks Nigel for acting as TSC lead for the past year.

* John Schanck stepping down from the TSC
  - Thank you to John!

* Updates from related communities:
  * [PQCA](https://github.com/PQCA)
     
     * Matthias provided an update from the 2025-05-04 PQCA TAC meeting.

     * The PQCA is calling for additional blog posts and is asking projects within the PQCP to volunteer to write blog posts. Additionally, we may propose higher level blog posts (e.g., on PQC in general). Volunteers can contact the PQCA TAC or Matthias directly.
     
     * New LFX Insights platform soft-launched: https://insights.linuxfoundation.org/. It is fully functional and is going to be officially launched in the end of the month. It has insights into all LF projects including PQCP such as project health, security, etc. Please take a look. The LFX Insights team is asking for feedback on the platform.
       
  * [Open Quantum Safe](https://github.com/open-quantum-safe)
      * Pravek provides an update on OQS.

      * mlkem-native v1.0.0 has been integrated and merged.

      * Looking for maintained portable C implementation for SLH-DSA. Discussions on-going to start a project in the PQCP. Current plan is to base the implementation on [sloth](https://github.com/slh-dsa/sloth) by Markku-Juhani Saarinen. A meeting is scheduled for next week.

* Review status of sub projects:

  * [mlkem-native](https://github.com/pq-code-package/mlkem-native)

     * Hanno provides an update on mlkem-native.

     * mlkem-native v1.0.0 has been released this week. This marks the completion of the HOL-Light functional correctness proofs for all Arm64 assembly. CBMC proofs (type-safety, memory-safety) for all C code have been completed before.

     * Matthias adds that pull requests to liboqs and AWS-LC have been opened. Additionally, a pqm4 integration has been completed.
 
  * [mldsa-native](https://github.com/pq-code-package/mldsa-native)

    * Matthias provides an update on mldsa-native.

    * CBMC proofs are 75% done. Now proving the top-level functions. Expected to finish this in the next few weeks.

    * Arm64 and AVX2 backend have been started. Now gradually adding more assembly.

  * [mlkem-libjade](https://github.com/pq-code-package/mlkem-libjade)

    * Tiago provides an update on libjade.

    * There is currently work on-going on a ML-KEM-1024 implementation. Once that is completed, it will be considered to publish a new version in the PQCP.

  * [mlkem-rust-libcrux](https://github.com/pq-code-package/mlkem-rust-libcrux)

    * No representative of libcrux present to provide an update.

* Discussion (if not covered previously)

  * Changing meeting frequency to monthly: https://github.com/pq-code-package/tsc/issues/169

    * Matthias calls for a vote to reduce the frequency of the TSC meetings to monthly.
    
    * Franziskus agreed beforehand online. 

    * Hanno, Tiago, Pravek, and Matthias vote in favour.

    * The proposal passes with 5/7 votes.

    * The next meeting will be 2025-07-03 13:00 UTC.

    * The calendar invite has been updated.

  * Review of very old issues:

    * Matthias proposes to clean up old issues that no one is working on. He will tag everyone in the corresponding issues. If no one speaks up, they will be closed.

    * The first set of orphaned issues are
       - Establish an end-user advisory committee: https://github.com/pq-code-package/tsc/issues/2
       - Consider including process separation: https://github.com/pq-code-package/tsc/issues/5
       - Discuss issues around packaging project components for adoption: https://github.com/pq-code-package/tsc/issues/6
       - Adopt a component lifecycle document: https://github.com/pq-code-package/tsc/issues/7
       - Arrange next hackathon: https://github.com/pq-code-package/tsc/issues/31

* Any other business
    * No other business to discuss.
