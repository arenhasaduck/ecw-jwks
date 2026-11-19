# ecw-jwks

Public JSON Web Key Set (JWKS) for the Concierge Dashboard's eClinicalWorks **Backend Services** (SMART on FHIR) app.

- JWKS URL: `https://arenhasaduck.github.io/ecw-jwks/jwks.json`
- Algorithm: RS384 (RSA 3072-bit), `use: sig`
- `kid` is the RFC 7638 SHA-256 thumbprint of the key.

This repo contains **public keys only**. The private key is never stored here.

## Rotating keys
Add the new public key to `keys` alongside the old one, update the app to sign with the new `kid`, then remove the old key once eCW no longer needs it.
