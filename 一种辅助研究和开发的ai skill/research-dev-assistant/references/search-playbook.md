# Search playbook — where to look and how to judge quality

## Where to search academic papers
- **arXiv** (arxiv.org) — preprints; fastest for ML/CS/physics. Note: not peer-reviewed.
- **Google Scholar** (scholar.google.com) — broad; shows citation counts and versions.
- **Semantic Scholar** (semanticscholar.org) — good for influence and "cited by".
- **Papers with Code** (paperswithcode.com) — links papers to benchmarks AND running code.
- **OpenReview** (openreview.net) — peer reviews are public; read the reviewer concerns.
- **ACL Anthology** (NLP), **ACM Digital Library**, **IEEE Xplore** — venue-of-record.
- **Connected Papers / Litmaps** — to map a topic's neighborhood and find the seminal work.

## Where to search industry-common practice
- **Official docs** of the library/framework — the source of truth for "intended use".
- **GitHub** — stars, last commit date, open issues, and how others use it in code search.
- **Benchmarks / leaderboards** — Papers with Code, MLPerf, framework-specific benchmarks.
- **Engineering blogs** — from the teams who run it at scale (read critically, they sell).
- **Stack Overflow** — common pitfalls and the accepted, voted answers.
- **Standards / RFCs** — for protocols, formats, security.

## How to turn a task into queries
- Write the task in plain words, then extract the technical noun + the action.
- Try 2–3 phrasings: the problem name, a known method name, and "<problem> survey".
- A recent **survey / review paper** is the highest-leverage first read.

## How to judge a source's quality
Prefer sources that score well on:
- **Peer reviewed** > preprint > blog > forum post.
- **Reproduced / widely cited** > single uncited paper.
- **Has runnable code** > pseudocode only > claims only.
- **Recent** for fast-moving fields; **seminal** for fundamentals (old can be fine).
- **Reports baselines and failure cases** > only-wins papers (suspicious).
- **Sample size / evaluation** is adequate for the claim.

## How much to read
- Minimum: one survey OR 2–4 primary sources that agree, plus one that disagrees.
- Stop when new sources stop changing your conclusion (saturation), not after one hit.

## When you can't find a paper
- Say so explicitly.
- Fall back to a **named** industry practice (cite the doc/repo/standard), not a guess.
- Lower your confidence statement accordingly and flag it to the user.
