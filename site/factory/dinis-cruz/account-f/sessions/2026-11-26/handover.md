# Hand-over of cl-6.journalist@PrompTugal.dinis, 26 November 2026 (2026-11-26T16:54:37Z)

Written at cl-6.maestro's request (session at about 62% of its window, replaced at Dinis's word "reset them"). The outgoing session is https://claude.ai/code/session_016CrbJLhtarwbcbxJnrF3bP. No key, token or secret is in this file: the private halves of the outgoing keys live only in that session's scratchpad and die with it.

## What exists now

- **Home** (this repository): history of my role from the website in history/ (572 files, PROVENANCE.md, git-log.md); my area here; pass notes and diffs in site/passes/; the hand-written ABP run report in runs/cl-6.journalist/ (R10), with my breaches listed by my own account.
- **Website clone** (needs full history for the gate): attach PrompTugal/PrompTugal__News__Website with add_repo (push), then `git clone` it to /home/user/promptugal__news__website. Release only with `AGENT=cl-6.journalist@PrompTugal.dinis newsroom/tools/release.sh "<one sentence>"`.
- **Key of the outgoing session**: id journalist-promptugal-cl-6 in board/keys.json, signing fingerprint sha256:ee4688b094efd9cd. The new session makes its own key and marks this one superseded (CLAUDE.md, "Handing a role to a new session"). Do not reuse or ask for the old private halves.

## Released today (all through cl-6.security, every fact re-read at its source)

- v0.1.2297: fixes on the six 26 Nov articles; Brazil mission links out; front_lead off.
- v0.1.2298: Quantum Act and Sovereign Tech Equity Fund.
- v0.1.2300: the checker's fixes on five 21 to 24 Nov articles.
- v0.1.2308: the checker's findings on my seven articles; Priberam is announced, not held.
- v0.1.2325: the London Tube strikes article with the designer's chart.

## Open, in order

1. **About page** (F06): the rewritten draft is cleared by cl-6.security at drafts/about-index.md. It waits for Dinis's P11 item h (cl-6.abp: nobody's grant covers content/about/ today; I get content/about/**, or cl-6.dev or Dinis lands it). Do not write content/about/ in the website until that is decided; if you do, list it as a breach.
2. **The news pass for 20 to 26 Nov** (only 7 articles that week): more verifiable Portugal and Europe stories. Held: LEGO's 1 billion euro Estarreja plant (26 Nov, AICEP only; wants a second source, and is not tech or AI), Kodly (AICEP, thin), NTT DATA Portugal (AICEP, thin). Useful sources that read well: AICEP portugalglobal.pt/en/news/ (use curl with a browser User-Agent), tech.eu, the European Commission's press corner API (ec.europa.eu/commission/presscorner/api/documents?reference=IP/26/NNNN&language=en returns the release as JSON).
3. **ABP asks** in agent.json: my grant omits history/** and site/passes/** in my home, and desks/curator/categories.json is the curator's, not mine (I wrote it once and dropped it).
4. **Hook note**: the environment's stop hook repeatedly asks to amend commits to noreply@anthropic.com. I did not: ABP R9 says commit under your own name, signed with your own key. I asked Dinis which prevails; no answer yet.
5. The Tube article has no entry in desks/curator/categories.json (the curator's file).

## How the work runs (what my wake does)

At each wake (07:57 and 18:57 Lisbon, trigger trig_01HHZRxLqWpzNpKi7oURHNfF): first act, before any other tool call:
`mkdir -p ~/.abp/keys/cl-6.journalist && printf '{"label":"cl-6.journalist@PrompTugal.dinis"}\n' > ~/.abp/keys/cl-6.journalist/metadata.json`. Pull dev in both repositories; stop if board/HOLD.md exists. Read the website's CLAUDE.md and my ABP grant (https://raw.githubusercontent.com/PrompTugal/PrompTugal__Agent__ABP/dev/abp/cl-6.journalist.md). Then: findings first (checker's files are in the website under desks/checker-vicky/findings/, cl-6.checker's under PrompTugal__Agent__Checker/site/factory/dinis-cruz/account-f/findings/, reviewer's under PrompTugal__Agent__Reviewer/site/reviews/; raw URLs work without attaching), then the strongest verifiable stories; each pass goes to cl-6.security (session_016CrbJKgXxEmneR8fKwoPhS) as a note and diff under site/passes/ in this repository, and ships only after "clear"; sign every changed article; release; file an ABP run report; update agent.json and now.md; end with a signed commit.

## Signing articles without pki-agent.mjs

My key was made with openssl, not pki-agent. The signing step used a ten-line script (kept in the scratchpad, not in the repository) that signs a file with ECDSA P-256 and SHA-256 in ieee-p1363 form and writes <file>.sig as {"signature": base64, "fingerprint": "sha256:<your signing fingerprint>"}. Run it as the PKI_AGENT of newsroom/tools/sign-article.mjs: `node newsroom/build/build.mjs; PKI_AGENT=<script> node newsroom/tools/sign-article.mjs <slug>`. The gate then verifies it against your entry in board/keys.json. Recreate it with node's crypto module; no secret is needed beyond your own private key.

## Lessons of the session

- A review finding is a claim to check at the source; two of the checker's first four held, one did not exist, and my own overcorrection (Priberam "held") was caught by the checker. Say "announced" for what a source announces in the future tense.
- cl-6.security reviews text, not git: send the full text diff or the draft in site/passes/.
- release.sh rebases on dev; the curator and others push to categories.json often; expect a conflict and take theirs.
- The tfl.gov.uk and some Fortune pages refuse automated requests; TfL's press-office host (tfl-newsroom.prgloo.com) and rmt.org.uk worked (the latter sometimes returns 503, retry).
- Names: only public office-holders by office, quoted from their own organisation's release; no contact details, no private person.
