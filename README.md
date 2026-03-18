
# Hearthstone Familia Identification
### Echi Hearthstone — Public Key & Identity Reference

This repository holds my public OpenPGP key and serves as a
permanent reference for anyone who needs to verify that I am
who I say I am. If someone sent you here, you are in the right place.

---

**Primary Key Fingerprint**
EFFD FF12 80E6 3B08 B5FB  5A97 4D84 6A2D C20A 7DE6

Status: Active
Last updated: 2026-03-17

---

## My Key

My public OpenPGP key is in [`keys/openpgp-publickey.asc`](keys/openpgp-publickey.asc).
You can import it into any standard GPG tool. Subkey fingerprints,
expiration dates, and current key status are in
[`keys/current-key-metadata.yml`](keys/current-key-metadata.yml).

If you want to verify something I signed, or send me something that
only I can read, this is the key you need.

---

## Proofs

The [`proofs/`](proofs/) directory holds signed plain text files
committed directly from my terminal. Every commit in this repository
is signed by the same key published above, and verified by GitHub.
The combination of signed content and verified commit history confirms
that whoever holds this key also controls this repository at the time
of each commit.

If we have agreed on a phrase between us, I will commit a signed proof
containing that phrase alongside a timestamp and send you the direct
link. The signed content will be clear-signed, meaning the text is
readable by anyone and the signature confirms it came from me.

If you have never verified a GPG signature before, see
[`VERIFICATION.md`](VERIFICATION.md) for instructions on every platform
including browser-based options that require no installation.

---

## Getting in Touch

If you need to reach me or request verification and we are not already
in contact, open an issue in this repository. I will respond with a
signed proof commit.

If you want to communicate privately, import the key, encrypt your
message to it, and send it my way. If you are willing to go that far,
I want to hear from you.

---

## New to GPG?

GPG is a tool for proving that a message came from who it claims to
come from, and for sending messages that only the intended recipient
can read. The public key in this repo is the part anyone can use to
verify my signatures or send something encrypted to me. The private
key is what only I hold and it never leaves my hardware.

If you want to understand what GPG is and why it matters, the
Electronic Frontier Foundation's [Surveillance Self-Defense guide](https://ssd.eff.org)
is the best plain-language starting point. The official reference
and documentation lives at [gnupg.org](https://gnupg.org).

For understanding how GPG keys work with hardware tokens like YubiKeys,
the [drduh YubiKey Guide](https://github.com/drduh/YubiKey-Guide)
is thorough, maintained, and the gold standard for this subject.

If you are ready to get started, these are the tools for your platform.

Windows: [gpg4win](https://gpg4win.org)
Android: [OpenKeychain](https://www.openkeychain.org)
Mac: [GPG Suite](https://gpgtools.org)
Linux: you already know.

---

## Something Looks Wrong?

If you have reason to believe this key has been compromised or you
are seeing something that does not add up, see [`SECURITY.md`](SECURITY.md).
