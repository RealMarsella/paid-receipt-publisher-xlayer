# Repo Plan

Updated 2026-05-22 — repo migrated from `gabrielantonyxaviour` to `RealMarsella` per `/Users/gabrielantonyxaviour/Documents/hackathons/PERSONA_ALLOCATION.md`.

## Repo (current)

- Name: `paid-receipt-publisher-xlayer`
- Owner: `RealMarsella`
- Visibility: public
- URL: `https://github.com/RealMarsella/paid-receipt-publisher-xlayer`

## Identity Proof

- Persona: Marsella (Chrome `Profile 19`, `testerbuster564@gmail.com`).
- GitHub login: `RealMarsella` (id `215697020`), confirmed via `curl -H "Authorization: token $MARSELLA_GITHUB_PAT" https://api.github.com/user`.
- PAT generated 2026-05-22 via agent-browser sudo flow (Stimulus `sudo-credential-options` POST to `/sessions/sudo/email`, OTP read from `testerbuster564@gmail.com` Gmail, sudo cookie set via `/sessions/sudo`, token issued via `/settings/tokens` form). Saved as `MARSELLA_GITHUB_PAT` in vault.

## Creation Method

Use the GitHub REST API directly with `MARSELLA_GITHUB_PAT` because local `gh` CLI auth is `gabrielantonyxaviour`, not Marsella. Pushes use the PAT inline (`https://RealMarsella:<pat>@github.com/...`).

## Push Steps

1. Build and test locally. Done.
2. Ensure no `.env`, private keys, API keys, or generated secrets are tracked.
3. Create public GitHub repo via REST `POST /user/repos` with PAT. Done.
4. Update `origin` remote to RealMarsella URL.
5. Push `main`.
6. Verify visibility via `GET /repos/RealMarsella/paid-receipt-publisher-xlayer`.
7. (Optional) Publish static demo via gh-pages branch with PAT-authed push.

## Migration Path (followed 2026-05-22)

1. Update `TEAM.md` + `REPO_PLAN.md` to Marsella persona. Done.
2. Generate `MARSELLA_GITHUB_PAT` via agent-browser. Done.
3. Create new repo `RealMarsella/paid-receipt-publisher-xlayer`. Done.
4. Update `origin` remote, push `main`.
5. Archive (or rename) `gabrielantonyxaviour/paid-receipt-publisher-xlayer` using Gabriel's gh auth.

## Current Status

- Repo URL: `https://github.com/RealMarsella/paid-receipt-publisher-xlayer` (after migration)
- Visibility: public
- Initial migration commit pending push.
- gh-pages demo: pending re-publish under Marsella account.
