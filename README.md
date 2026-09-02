# JWT Decoder

Decode and inspect JSON Web Tokens, with human-readable claims and local HS256/384/512 signature verification. Nothing is uploaded.

**Live:** <https://jwt-decoder.slippylabs.com/>

## What it does

- Decodes header and payload and explains the registered claims in plain language.
- Live countdown to `exp`, and a warning when a token is already expired or not yet valid.
- Verifies HS256 / HS384 / HS512 signatures against a secret you type in.

## How it works

Signature verification uses the browser's own WebCrypto HMAC. The token and the secret are only ever held in the page — neither is sent anywhere, which is the whole reason to use a local decoder for a token you actually care about.

## Run it locally

A static site. No build step, no package manager, no dependencies:

```
git clone git@github.com:slippylabs/jwt-decoder.slippylabs.com.git
cd jwt-decoder.slippylabs.com
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

---

Part of [Slippy Labs](https://slippylabs.com). Every tool is indexed at
[projects.slippylabs.com](https://projects.slippylabs.com).
