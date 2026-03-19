# VERIFICATION.md — How to Verify a Signed Proof

This document explains how to verify that a signed file or message
from this repository genuinely came from the key published here.
If someone sent you a link to a proof file and you want to confirm
it is real, this is the right place to start.

---

## What You Are Verifying

Every proof file in the [`proofs/`](proofs/) directory is
clear-signed. That means the content is plain text anyone can read,
and the GPG signature wrapped around it confirms it came from the
key published in this repository and has not been changed since it
was signed. You do not need to decrypt anything. You are only
confirming that the signature is genuine.

---

## Before You Verify

You will need the public key imported into whatever tool you are
using. The key file is at [`keys/openpgp-publickey.asc`](keys/openpgp-publickey.asc).
Download or copy that file before following the instructions below.

The primary key fingerprint for this repository is:

EFFD FF12 80E6 3B08 B5FB  5A97 4D84 6A2D C20A 7DE6

When your verification tool reports a successful result, compare
to the fingerprint given above. If they match, the proof is
genuine. If they do not match, stop and do not trust what you
are reading.

---

## On Android — OpenKeychain

OpenKeychain is the recommended tool for verifying on a phone.

First, import the key. Open OpenKeychain, go to the key management
section, and choose to import a key from a file or from clipboard.
If you downloaded the `.asc` file, import it from your downloads
folder. If you copied the key text, use the clipboard option.
Once imported, the key will appear in your keyring under the name
Echi Hearthstone.

To verify a proof, open the Encrypt/Decrypt section of the app.
Paste the full contents of the proof file — everything from
`-----BEGIN PGP SIGNED MESSAGE-----` to
`-----END PGP SIGNATURE-----` — into the input area and tap
the decrypt button. OpenKeychain will show you the plain text
content and report that the message is signed. A successful
verification will show the signer's name and confirm the signature
is valid. The message will be reported as not encrypted, which is
correct and expected — proof files are intentionally readable
by anyone.

Compare to the fingerprint given above to confirm the proof
is genuine.

---

## On Windows — Kleopatra

Download and install [gpg4win](https://gpg4win.org), which includes
Kleopatra as its main interface. Once installed, import the public
key by opening Kleopatra, selecting Import from the toolbar, and
choosing the `openpgp-publickey.asc` file. The key will appear in
your certificate list under the name Echi Hearthstone.

To verify a proof file, select Decrypt/Verify from the toolbar,
navigate to the proof file, and open it. Kleopatra will process
the file and display a results dialog showing whether the signature
is valid and which key it came from. A successful verification
will show a green result with the signer's name and fingerprint.
If the result shows a warning or error, the file should not be
trusted.

---

## On Mac — GPG Suite

Download and install [GPG Suite](https://gpgtools.org). Import the
public key by double-clicking the `.asc` file, which GPG Suite will
handle automatically. To verify a proof file, right-click it in
Finder, choose Services, and select the OpenPGP verification option.
A successful result will show a green confirmation with the signer's
name and fingerprint.

---

## On Linux

If you are on Linux, you should already know what GnuPG is — import
with `gpg --import` and verify with `gpg --verify`. If you are just
getting started, check the man page with `man gpg` or head to
[gnupg.org](https://gnupg.org) for the full documentation.

---

## In a Browser — No Installation Required

If you absolutely cannot install anything and need to verify
something right now, browser-based tools exist for that purpose.
Before you go that route though, it is worth saying plainly: you
will likely find more frustration than convenience here. Browser
tools are inconsistent, depend on the site staying online and
behaving honestly, and give you no way to audit what is actually
running. Downloading Kleopatra or OpenKeychain is a fifteen minute
task and will serve you far better in the long run. The browser
option is a last resort, not a recommendation.

If you must, these tools have shown to be functional, though no
strong claims are made about either:

[kleopatra.app](https://kleopatra.app)
[toolsley.com/verify.html](https://www.toolsley.com/verify.html)

Paste the full contents of the public key file into the key field
and the full proof file contents into the message field, then run
the verification. A successful result will confirm the signature
is valid and show the fingerprint it was verified against.

Trust these tools at your own risk and never paste anything you
are not willing for others to potentially see. For anything
sensitive, use a local tool without exception.

## A Note on Verifying the Tools Themselves

If you want to be thorough, the tools listed in this document are
themselves distributed with verification files by their respective
projects. Before installing any of them, check the download page
for a checksum or a GPG-signed release file and verify it against
what you downloaded. Each project's download page will explain
how to do this. It is an extra step, but for anyone who wants a
complete chain of trust from the software itself to the signature
it produces, it is the right one to take.

As the saying goes among those who work in security and secure
communications, trust, but verify. That principle applies at
every layer of this process, from the tools you use to the
signatures you check with them. The math confirms the signature
is genuine. Your judgment and your verification habits are what
confirm everything else in the chain is what it claims to be.