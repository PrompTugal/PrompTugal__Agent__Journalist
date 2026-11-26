# Pass 2026-11-26: fixes on the six 26 November articles (for cl-6.security, before release)

Prepared by cl-6.journalist@PrompTugal.dinis. Not yet pushed to the website: the commits are local in my clone (gate OK at v0.1.2294, `DRY=1 release.sh` clean). The full text diff of content and curator files is `2026-11-26-fixes-six-articles.diff` beside this note.

What changed, each against its source (read 26 November 2026):
- Priberam webinar: AICEP's page says it was held on 19 November. Title, summary and body now say it is past; no report of it found. Source: https://portugalglobal.pt/en/news/2026/novembro/priberam-and-kenya-s-apb-explore-ai-s-future-in-media/
- Reach AI: the page says "markets such as"; "five countries" removed. Source: https://portugalglobal.pt/en/news/2026/novembro/reach-ai-investing-in-the-new-frontier-of-digital-research/
- Smartex: Fortune says strategic suppliers to H&M are among the launch customers; The Next Web says H&M is one of the first customers. Both stated, difference shown. Sources: https://fortune.com/2026/11/19/smartex-ai-tony-fadell-fashion-hm/ and https://thenextweb.com/news/tony-fadell-joins-smartex-as-chair-as-it-launches-ai-fabric-checks-for-hm
- Portugal and Atomico: AICEP's page gives ca.finance as its source ("republishes" removed). Source: https://portugalglobal.pt/en/news/2026/novembro/portugal-enters-europe-s-top-10-for-tech-investment/
- COCUS: no stray " T" in the source, the built twin or the live page (checked); signed again under my key, text unchanged.
- Brazil startup mission: three links to event pages that came off taken out (text kept); signed again.
- Local news article: `front_lead: true` removed so the places band leads with the newest dated item (Dinis's home-page feedback).
- The "Who made this" line of the four corrected articles now says they were corrected and signed again by this agent. All changed articles are signed with journalist-promptugal-cl-6 (signing fingerprint sha256:ee4688b094efd9cd), which the gate verifies.
- Category entries for four conductor-written articles were already added upstream by the curator; nothing of mine remains there.

No contact detail, key or private person added. The one named person in COCUS (a business development manager, quoted by AICEP's public profile) is unchanged.
