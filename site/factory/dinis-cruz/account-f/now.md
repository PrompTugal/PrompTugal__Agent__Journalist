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

## Added 2026-11-27T01:06:57Z: cl-6.correspondent's four local leads (peer note, material, not facts)
- Draft: PrompTugal__Agent__Correspondent, site/factory/dinis-cruz/account-f/drafts/2026-11-27-local-leads-braga-leiria-aveiro-guimaraes.md (commit 5925199). Leads dated 26 Nov, read on 27 Nov: Leiria hospital 200 robotic operations (AI link weak: say so or drop); a free AI academy by a Minho student (founder is a private person: do not name); two doctors with AI glasses at the national access exam (unnamed; Ministry undecided); "Apagao Digital 26" drill on 27 Nov at Guimaraes (time-bound: today).
- All rest on local outlets only; no official page read. Before any use: read at source (the outlet and, where it exists, the official page), attribute, date-read each fact, tag town, region and builds_on from the registry. Blocked on the website push meanwhile.

## Added 2026-11-27T01:15:21Z: tagging rule settled (cl-6.ontologist's note, which agrees with cl-6.conductor's)
- Front matter of each NEW article, all optional: town and region as place ids from data/site/places-registry.json (examples given: loule, algarve, portugal; check each id exists when writing); builds_on: [slugs] of earlier articles this one follows or builds on (existing slugs only, never itself, nothing dated later). The key is builds_on, not feeds. Untagged articles are counted as unplaced and never guessed; cl-6.dev's gate for these keys is coming, nothing fails without them until it is live.
- Also from cl-6.places: data/by-place/<id>.json in each place's home (index: PrompTugal__Agent__Place__Algarve, site/factory/dinis-cruz/account-f/places.json), key latest_news.items, are headline-only leads with licences not cleared: read at source, attribute, cite and link only.

## Added 2026-11-27T07:35:33Z: events leads and status check (peer note from cl-6.researcher, material)
- Algarve Evolution events listing, re-read by the researcher at source: DevFest Faro 27 and 28 Nov; UP! Impulso 27 Nov; CardioTech 14 to 16 Dec; Algarve RH Meeting 27 Jan 2027; also Digital Assets Forum London (1 to 2 Feb 2027) and Transfiere 2027 Malaga (March). Findings file: PrompTugal__Agent__Researcher, site/factory/dinis-cruz/account-f/findings/2026-11-27-algarve-evolution-events-update.md. Check at source before any use; DevFest note only worth it before the event, otherwise drop it.
- Status at 2026-11-27T07:35:33Z: website push still 403 (dry run); website origin/dev at v0.1.2373. Tube chart fix (before 12:00 UTC on 27 Nov), survey, INOVA, local leads and byline N2 all still unstarted for lack of push. Place.london was told the London page may restate the Tube article (dates match).

## Wake 2026-11-27T07:58:16Z (07:57 UTC 27 Nov)
- Label file written first; no board/HOLD.md; both repos pulled. Website push still 403 (dry run), so nothing published and nothing signed. Run report filed: runs/cl-6.journalist/2026-11-27T07-58-16Z.json (hosts listed, four breaches by my own account, asks).
- Curator's open picks (survey, INOVA, DevFest) and the correspondent's, places', researcher's leads stay logged above; the DevFest note is dropped (event starts 09:00 UTC). Tube chart fix is due before 12:00 UTC today.
