
# Hearthstone_Familia_Identification Security Protocol
- Key Security & Revocation Policy

This document describes what to expect if something goes wrong with
the key published in this repository, and what actions will be taken
in each scenario. It is written for anyone who communicates with or
relies on signatures from Echi Hearthstone.

---

## What This Document Covers

This document covers three things. First, the scenarios under which
the published key may be revoked or retired. Second, what a legitimate
revocation notice looks like and where it will appear. Third, what
you should do with communications you have already received if a
revocation is published.

---

## Revocation Scenarios

Not all revocations mean the same thing, and the reason matters for
how you interpret past and future communications.

Key rotation is a planned and orderly transition. The current key
is being retired in favor of a new one. This is not an emergency.
Past signatures made by the current key remain fully valid. A new
key fingerprint will be published alongside the revocation notice.

Key loss means the hardware token holding the key material is no
longer accessible. There is no evidence of compromise, but the key
cannot be used and is being retired out of caution. Past signatures
are presumed valid. Whether a replacement key will be issued will be
stated in the revocation notice.

Key compromise is the high severity scenario. There is reason to
believe the private key material may be in unauthorized hands. In
this case, treat any signature from this key after the date on the
revocation notice with skepticism regardless of what it claims. Do
not accept new subkeys appearing under this fingerprint after that
date. If you have received communications purportedly from this key
after that date, verify them through a separate channel you already
trust before acting on them.

---

## What a Legitimate Revocation Looks Like

A legitimate revocation notice will always appear as a committed file
in this repository, on a verified commit. The notice will be
clear-signed by the key being revoked, which means you can verify
its authenticity using the public key published in this repository
before that key was retired. The plain-language description within
the notice will state the reason and what you should do next.

Any communication claiming this key has been compromised that does
not appear as a verified commit in this repository should be treated
with skepticism until confirmed here.

---

## What Happens to Past Signatures

Revoking a key does not invalidate signatures made before the
revocation date. A commit, proof file, or message signed by this
key before revocation was valid at the time it was made and remains
historically verifiable. Revocation only affects trust in signatures
made after the revocation date. In the compromise scenario, the
notice will state clearly from what date signatures should be
treated as suspect.

---

## On Communications Claiming to Be Mine

If you receive any communication stating to be from me and you are
unable to obtain a verified signature from this key, take it with
a bucket of salt. Regardless of the platform, regardless of the
context, if it cannot be verified, do not trust it. If you need
verification and are in contact with me, I can provide a signed
proof on request. If something feels wrong and you cannot reach
me directly, open an issue here.

---

## If You Find Something That Does Not Add Up

If you come across a message, a file, or anything else claiming to
be from this identity and something feels wrong, the fingerprint
does not match what is published here, the signature does not
verify, or it simply does not seem right, and you have no existing
way to reach me directly, open an issue in this repository.

This is the right path for concerns that come up outside of an
active conversation. It creates a visible record and gives me a
way to respond with a signed proof commit, which means my response
itself can be verified against the key published here.

If the repository itself appears to have been changed without
verified commits, treat that as a serious signal and do not rely
on anything you find here until you can confirm it through another
channel you already trust.
