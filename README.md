# PEP discussion process proposal

An eight-slide introduction for a five-minute slot, using a palette inspired by the Python logo: blue (`#3776AB`) and yellow (`#FFD343`). Slides use local system fonts and CSS/SVG artwork, so presentation rendering needs no remote assets.

## Run

Requires Node.js 22 or newer.

```sh
npm install
npm run dev
```

Open http://localhost:3030. Use the arrow keys to navigate. Presenter view at http://localhost:3030/presenter includes speaker notes and a five-minute countdown.

```sh
npm run build   # Static presentation in dist/
npm run export  # pep-discussion-process.pdf
```

PDF export uses Playwright Chromium. If its browser is missing, run `npx playwright install chromium` first.

## Edit and rehearse

- `slides.md`: slide content and timed speaker notes.
- `style.css`: Python-inspired palette and deck styling.
- `global-top.vue`: slide numbers and footer.

| Slide | Topic | Time | Cumulative |
| --- | --- | --- | --- |
| 1 | Introduction and discussion/refinement cycle | 0:10 | 0:10 |
| 2 | PEP 1 quote on author responsibility | 0:20 | 0:30 |
| 3 | Why managing discussion alone is hard | 0:45 | 1:15 |
| 4 | Motives: proposed rule, rationale, and escalation | 0:35 | 1:50 |
| 5 | PEP guide | 0:35 | 2:25 |
| 6 | Proposal 3: shorter discussion threads | 0:45 | 3:10 |
| 7 | Proposal 4: changelogs and thread summaries | 0:45 | 3:55 |
| 8 | Proposal 5: final comment period | 0:35 | 4:30 |

The speaker notes total 4:30, leaving 30 seconds of buffer within the five-minute slot.

The deck presents proposed changes. The PEP guide is inspired by the Rust project's proposal guide role, as credited by Emma. It leaves guide selection, thread-locking responsibility, editorial-update exceptions, and final comment period mechanics open for discussion. It distinguishes authors' design decisions from formal PEP resolution.

Sources: [PEP 1](https://peps.python.org/pep-0001/), [Rust RFC process](https://rust-lang.github.io/rfcs/introduction.html#what-the-process-is), and [Python logo reference](https://www.python.org/community/logos/). Barry Warsaw's changelog suggestion is credited on slide 7.


The PEP 1 quotation links directly to its purpose section. The author-burden slide presents the proposal's argument about scale, impasses, shared moderation, and participation filtering. [Carter Baxter's “Feedback doesn't scale”](https://another.rodeo/feedback/) supplies a related argument about organizational leadership, not empirical evidence about PEP threads. Possible overrepresentation of negative views is framed as a concern, not an established correlation. The motives slide directs earnest concerns to the SC / PEP-Delegate or Code of Conduct Working Group, as appropriate.

PEP 1 already encourages fresh threads for major changes and includes rejected ideas and optional change history; this proposal makes the revision workflow more regular and the changelog mandatory.

Slide 6 defines the decision-triggered transition between threads; slide 7 defines the changelog and summary requirements. The workflow slide refers forward to those requirements instead of repeating them.
