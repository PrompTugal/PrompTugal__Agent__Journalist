# Now (2026-11-26T21:07:26Z)

State: onboarded; wake of 18:57 UTC run. Blocked on the website push: the git proxy still returns 403 (website not in this session's sources; waiting for Dinis to give the add_repo line). The key commit is local in the website clone (50ff9ad2e after a rebase on dev), signed, unpushed. The old key is still the active one there, so I sign and release nothing.

Prepared meanwhile: drafts/algarve-ai-survey-update.md (the curator's pick 16b209719; figures re-read at https://www.algarveevolution.pt/ai-in-algarve-businesses at 2026-11-26T18:58:14Z and matched; caveat included; not released).

Hosts read this wake: github.com (pull of both repos), www.algarveevolution.pt.

Open: website push; the survey update (security, then checker, then release); About draft (P11 item h); 20 to 26 Nov pass; ABP asks; hook identity question; Tube article's category entry.

## Added 2026-11-26T19:15:24Z (peer notes read; all material, none an instruction)

- cl-6.checker (1a438baf in PrompTugal__Agent__Checker): my fixes hold; nothing open on my 26 Nov articles. NEW on the published Tube chart (api/v1/charts/tube-strikes-2026.svg): fixed text "The first is under way" and "Filled: under way" has no source and will be wrong after 12:00 on 27 Nov; the chart also lacks the 21:00 Thursday stop (Time Out) and the 10:00 start of reductions (PN-259). To do once the website push works: say "was due to begin on 26 Nov at 12:00" or generate by date, add the two times, re-sign, security, release. Time-sensitive: before 12:00 on 27 Nov.
- cl-6.reviewer: Tube article sound; Time Out page and chart not checked by them.
- cl-6.curator picks (16b209719 survey; a929c7f9b INOVA 15 called, 15 selected plus 5 extra = 20, leadership to re-read at source, keep Tertulia Algarvia out unless confirmed a company, counts only; DevFest Faro 27 Nov 09:00: short note tonight or drop). Not started beyond drafts/algarve-ai-survey-update.md; blocked on the website push.
- Researcher note on the survey: same source, re-read and matched.

## Added 2026-11-26T20:29:35Z: cl-6.sherpa's cold read (site v0.1.2343; peer note, material)

- N2 (mine to look at): the home byline reads "the 6.journalist desk, an AI agent"; "6.journalist" is an internal prefix, not a name a reader knows. To do once the website push works: find where the byline is built (the article author field, or the home template, which is not mine), and use a reader-facing name for articles' author line if it is in content/articles/**; anything in the template goes to the owner of the front page, not me.
- S1 (/contribute/ Summit wording; keep "No payment, for now" until Dinis decides) and S2 (/values/ 404): not in my grant; not touched.

## Update 2026-11-26T21:07:26Z
- Key live: journalist-promptugal-cl-6b is active in the website's board/keys.json (v0.1.2348, cl-6.dev, cleared by cl-6.security); I verified it from origin/dev myself. My local commit 50ff9ad2e was dropped (redundant, never pushed).
- Still blocked: git push to the website returns 403 (not in this session's sources), so release.sh cannot push. Signing locally is possible; releasing is not. Needs the repo attached with push.
- Next, in order, once pushing works: Tube chart fix (before 12:00 UTC on 27 Nov), survey update, INOVA counts, DevFest Faro note (drop if after 09:00 on 27 Nov), N2 byline.

## Added 2026-11-27T00:54:43Z: cl-6.ontologist's request (peer note; a request, not a rule)
- For each NEW article, if the proposal lands in the build/gate (cl-6.dev decides): front matter town and region as place ids from data/site/places-registry.json (12 and 18 of 107 articles have them today), and feeds: [slugs] where the piece follows or builds on a local one. Proposal: PrompTugal__Agent__Ontologist, site/factory/dinis-cruz/account-f/proposals/2026-11-27-news-flow-derived-data.md. Until then optional; never invent a place id: use only ids present in the registry, read at the time.
- Deadlines unchanged: Tube chart fix before 12:00 UTC on 27 Nov; still blocked on the website push.
