# Enzan preview issuer pins

Preview: not for production or regulated use.

This public-only repository distributes key-binding metadata for the Enzan
developer preview. It contains no application Source, private custody material,
private key, live receipt or Passport. Signup and waitlist remain closed.

The versioned directory is issuers/preview-live-issuer-2026-11-13.v2/.
The manifest preserves both historical dogfood issuer pairs and adds the
generated preview issuer key pending activation. Its original preparation
status is retained in the exact manifest bytes; the separate signed anchor
binds that captured manifest, not active service availability.

The selected offline operator signer has public SPKI DER SHA256:

    46859f05c986e8f9b3b9e31cafc1f3cad31d74d43d7b1d617a08c1c84fbf6769

The operator signer is distinct from every receipt issuer key. The Ed25519
envelope signs UTF-8 ENZAN_PREVIEW_ISSUER_ANCHORS_V1 plus one LF byte plus the
existing Core canonical JSON bytes of payload. anchor-signing-input.bin and
anchor-signature.bin expose those exact public bytes for standard Ed25519
verification. anchor-payload.json repeats the signed payload. The envelope
contains issuance/expiry Unix milliseconds with a30day interval; these are not
a fresh revocation oracle or an automatically refreshed CLI trust decision.

Select the Enzan22 GitHub account/repository and expected signer fingerprint
through a channel you independently trust before accepting these materials.
Downloading a key alongside its signature does not establish that trust. This
publication establishes no previously approved external signer identity, issuer
authority, work correctness, permissions or current key status. It does not
replace the runbook's separate DNS/channel verification. The CLI keeps unknown
issuer refusal and does not discover trust from this repository or a receipt
website automatically.
