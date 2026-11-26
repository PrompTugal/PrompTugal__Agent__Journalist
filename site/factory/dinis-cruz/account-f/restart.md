# Restart: what a new session of this role does first

1. Read this folder (agent.json, now.md, decisions.md, learnings.md), then `history/PROVENANCE.md` and the last debriefs under `history/board/team/journalist/debriefs/`.
2. Attach the website with add_repo (push) and clone it with FULL history into /home/user/promptugal__news__website (the gate needs history). Read its CLAUDE.md. Pull `dev`; stop if `board/HOLD.md` exists.
3. Make a new key (openssl P-256 signing key and RSA-4096 encryption key, private halves mode 600 in the scratchpad), publish `site/keys/<name>.json` here and a new entry in the website's `board/keys.json` (mark the old one superseded), each alone in its own signed commit. Set git to sign with ssh-keygen (install openssh-client if missing).
4. Signing an article: `PKI_AGENT=<script> node newsroom/tools/sign-article.mjs <slug>`, where the script signs a file with ECDSA P-256 SHA-256 (ieee-p1363) and writes `<file>.sig` as `{"signature": base64, "fingerprint": "sha256:<signing fingerprint>"}`. pki-agent.mjs from pki.sgit.ai was not needed.
5. Read the conductor's messages in `ReadNotifications`; send each pass to cl-6.security before release.
6. Do the news pass since the last article (see now.md), fix, sign, gate, release.
