# 2024-07-18 :  TSC Agenda

## Agenda

* Welcome
* [Minutes/actions from previous meeting](https://github.com/pq-code-package/tsc/pull/81/files)
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
* [API requirements](https://github.com/pq-code-package/tsc/issues/4) - random source, rust vs C, unpacked keys
* [open TSC issues](https://github.com/orgs/pq-code-package/projects/4/views/1):  
* Any other business

## Minutes/actions from previous meeting

Nothing to note.

### Updates from related communities

#### PQCA

* Continuing [review](https://github.com/PQCA/TAC/issues/24) of Project Lifecycle document.
  * Sub-projects expected to be clear on their production quality.

#### OQS

* Added [Mayo](https://pqmayo.org/) signature scheme (including @bhess + @mkannwischer).
* [PR](https://github.com/open-quantum-safe/liboqs/pull/1745) in review for [libjade](https://github.com/formosa-crypto/libjade) Kyber implementation (help from @tfaoliveira) - preview/test run of what we will do with pqcp in future.
* 0.11 expected in August.
* [trail of bits](https://www.trailofbits.com/) audit underway - started Monday, will last 4 weeks.
@ajbozarth leading initiative to revive [oqs-demos](https://github.com/open-quantum-safe/oqs-demos) - feedback invited on priority of each demo.

### Review of subprojects

#### mlkem-c-embedded

* Adding RISC-V support - harder than expected due to toolchain support (nix)

#### mlkem-c-aarch64

* In process of adding fast keccak - needs more work on an infrastructure project

#### mlkem-c-libjade

* Minor release/update to provide updated license to liboqs. (changes to CI, infra updates, compiler/easycrypt). Next major release will have a restructure to split into multiple repositories. Currently prototyping. Will update to SHA3 to move to mlkem. Doesn't block current integration but sets future direction.
* De-randomized api makes testing easier, discussion about private keys & what part part may explicitly be public - to help with constant time checking. Using [timecop](https://post-apocalyptic-crypto.org/timecop/). Should document info about key.

#### mlkem-c-libcrux

* @franziskuskiefer has first [PR](https://github.com/pq-code-package/mlkem-rust-libcrux/pull/3). Need to fix up licenses. Then will open up more issues.

#### Open TSC issues

A lot of discussion around the API

* [#86](https://github.com/pq-code-package/tsc/issues/86)
  * Many libraries such as nss have their own random number generators.
  * NIST require both.
  * wonder underway in liboqs to add derandomized api.
  * probably should have a random function - may be harder to integrate without.
  * Q about whether this affects certification - lib wouldn't be certified, rather a full module like openssl, so another team would take our library, bundle it with a random number generator, and that would be tested together.
  * liboqs provides random function, delegates to reasonable dependency library/platform  (windows, mac, openssl etc)
  * Any real implementation needs [drpg](https://csrc.nist.gov/glossary/term/deterministic_random_bit_generator) for certification in any case
  * continue discussion towards decision in issue
* [Deserialized API](https://github.com/pq-code-package/tsc/issues/4#issuecomment-2228072893)
  * Many implementations offer this (Microsoft, BoringSSL)
  * Avoids need to constantly serializing/deserializing when you already have the key.
  * Structured api (vs. byte)- relates also to doc above on keys and what is secret.
  * Should have both serialised and deserialized apis.

Andrés asked if there's any help needed with open reach, such as getting input from community.

### Any other business

None.

## Action items

No updates.

## Recordings

* [Recordings are available on your Open Profile page](https://openprofile.dev/my-meetings) under Past Meetings.

## Upcoming TAC meetings

The next meeting is canceled (multiple vacation), we will continue in in 4 weeks time - 1300 UTC on 2024-08-15.

[Please check the calendar](https://pqca.org/calendar/)

## Attended by

### TSC voting members

* [ ] [Manuel Barbosa](https://github.com/mbbarbosa), University of Porto
* [X] [Hanno Becker](https://github.com/hanno-becker), AWS
* [X] [Nigel Jones](https://github.com/planetf1), IBM
* [X] [Matthias J. Kannwischer](https://github.com/mkannwischer), Chelpis Quantum Tech
* [X] [Franziskus Kiefer](https://github.com/franziskuskiefer), Cryspen
* [X] [Tiago Oliveira](https://github.com/tfaoliveira), Sandbox AQ
* [ ] [John Schanck](https://github.com/jschanck), Mozilla
* [X] [Douglas Stebila](https://github.com/dstebila), University of Waterloo

### Additional attendees

* Alex Bozarth, IBM
* Andrés Vega, Fianu Labs
