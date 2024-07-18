# 2024-07-04 :  TSC Meeting

## Agenda

* Welcome
* [Minutes/actions from previous meeting](https://github.com/pq-code-package/tsc/pull/78/files)
* Updates from related communities:
  * [PQCA](https://github.com/PQCA)
  * [Open Quantum Safe](https://github.com/open-quantum-safe)
* Review status of sub projects:
  * [mlkem-c-generic](https://github.com/pq-code-package/mlkem-c-generic)
  * [mlkem-c-embedded](https://github.com/pq-code-package/mlkem-c-embedded)
  * [mlkem-c-aarch64](https://github.com/pq-code-package/mlkem-c-aarch64)
  * [mkkem-libjade](https://github.com/pq-code-package/mlkem-libjade)
  * [mlkem-rust-libcrux](https://github.com/pq-code-package/mlkem-rust-libcrux)
  * [documentation](https://github.com/pq-code-package/documentation)
* [open TSC issues](https://github.com/orgs/pq-code-package/projects/4/views/1):  
* Any other business

### Welcome

It was noted that today is a public holiday in the USA.

## Minutes/actions from previous meeting

No additional notes.

### Updates from related communities

#### PQCA

* Presentation/demo on PQ crytographic code scanning plugin for sonarqube. Project currently under [IBM/sonar-cryptography](https://github.com/IBM/sonar-cryptography). Front end web UI not yet in open source, but expected soon. Supports Java/Python currently, contributions welcome for other languages.
* Continued discussion on [Project Lifecycle](https://docs.google.com/document/d/1NV-0vNgXWdc81oqT0jv0C-9Funb8dySS06u90ghF-X4).

#### OQS

* Working towards next release 0.11. WIll include libjade implementation. Will be a prelude to sourcing implementations from pq-code-package. Tiago synchronizing with team next week. Expect main branch will move to Apache 2.0.
* Alex [proposing updates](https://github.com/open-quantum-safe/oqs-demos/issues/286) for the demos project.

### Review of subprojects

#### mlkem-c-aarch64

* Mostly working on automated benchmarking on different boards (self-hosted). Results [here](https://pq-code-package.github.io/mlkem-c-aarch64/dev/bench/).
* intent is to get a baseline before further improvements added.
* Triggered on merge, but can be triggered in PR via label (non org members need approval) - looking at improvements so any regressions can be spotted before merge.
* Working with Ry on [Graviton access](https://github.com/pq-code-package/tsc/issues/75)
* Douglas pointed out OQS has a mac m1 mini - a current gap for aarch64 testing. Will require some thought to [harden github runner](https://docs.github.com/en/actions/security-guides/security-hardening-for-github-actions#hardening-for-self-hosted-runners) & allow access.
* Douglas noted that OQS has a goal to revisit benchmarking. Spencer will be working on this and may contact Matthias for advice.

#### mlkem-rust-libcrux

* Franziskus has been working on separating out the code upstream ie into different crates. Working through policies such as when code is pushed, issue tracking, which crate is where, dependencies (small number). We noted that rust crates contain source only - so not a binary distribution.

#### Open TSC issues

* [[#3](https://github.com/pq-code-package/tsc/issues/3) : Franziskus noted that for libcrux they have some crude labels, and consolidation on the descriptions would be useful.

### Any other business

No other topics.

## Action items

No updates.

## Recordings

* [Recordings are available on your Open Profile page](https://openprofile.dev/my-meetings) under Past Meetings

## Upcoming TAC meetings

The next meeting will be scheduled in 2 weeks time - 1300 UTC on 2024-07-18.

[Please check the calendar](https://pqca.org/calendar/)

## Attended by

### TSC voting members

* [ ] [Manuel Barbosa](https://github.com/mbbarbosa), University of Porto
* [ ] [Hanno Becker](https://github.com/hanno-becker), AWS
* [X] [Nigel Jones](https://github.com/planetf1), IBM
* [X] [Matthias J. Kannwischer](https://github.com/mkannwischer), Chelpis Quantum Tech
* [X] [Franziskus Kiefer](https://github.com/franziskuskiefer), Cryspen
* [X] [Tiago Oliveira](https://github.com/tfaoliveira), Sandbox AQ
* [ ] [John Schanck](https://github.com/jschanck), Mozilla
* [X] [Douglas Stebila](https://github.com/dstebila), University of Waterloo

### Additional attendees
