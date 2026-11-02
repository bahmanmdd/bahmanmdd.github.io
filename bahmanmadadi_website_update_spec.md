# bahmanmadadi.com – Website update spec for the site agent

Nov 2, 2026

## 0. Instructions for the agent

This spec lists every change to make on bahmanmadadi.com (Hugo Blox Builder, academic-cv template). Apply only what is listed here. Every other word, page, image and setting stays as it is.

**Ground rules**

- No new items in the top navigation. The menu keeps its seven entries in the same order; only the label "Supervision" becomes "Team" (Section 4).
- Tabs inside a page are allowed and are used on three pages: Papers, Team and Experience. Reuse the tab pattern already used on the GREENSHIFT page (Overview / Consortium / News / Vacancies), so the look stays consistent.
- All text is in English. Use the exact wording given in this spec; where it says "suggested wording", minor edits for layout are fine.
- Keep existing URLs working. If you rename a page or its slug, keep the old URL (e.g. `/supervision/`) working with a Hugo `aliases` entry.
- Before adding an entry (talk, paper, person), check whether it already exists in the content folders. If it does, update it instead of creating a duplicate.
- Do not show supervision percentages, funding amounts for PhD contracts, rejected proposals, or evaluation scores anywhere on the site.
- Do not change the GREENSHIFT page in any way. Its postdoc vacancy stays as it is (interviews are ongoing).
- Do not change the Courses page, the Professional Summary on the homepage, or the Positions and Education entries on the Experience page (only their placement into tabs changes).
- When finished, rebuild locally and report back the list of files you created or changed, plus any item you could not complete and why.

## 1. Bio (homepage): add a News section

Add a short, dated News list to the homepage, placed directly after the biography block (Professional Summary, Education, Interests) and before "Featured Publications". Do not edit the Professional Summary text.

**Implementation**

- In the homepage content file (`content/_index.md` or equivalent), add a new section block of type `markdown`, titled **News**, between the biography block and the featured-publications block. Give it the anchor id `news`.
- Format: one line per item, newest first: **Month Year** – one sentence, with at most one or two links.
- Hard cap of 8 items. When a new item is added later, delete the oldest one.

**Content (newest first)**

| Date | News item (suggested wording) | Links |
| --- | --- | --- |
| 2026 *(confirm month with Bahman)* | Call for papers open: special issue "Open Science in Transportation: Establishing a Foundation for Transparent, Reproducible, and Collaborative Research" in *Transportation Engineering* (Elsevier), for which I am lead guest editor. | [Call for papers](https://www.sciencedirect.com/special-issue/337680/open-science-in-transportation-establishing-a-foundation-for-transparent-reproducible-and-collaborative-research) |
| October 2026 | Louis Rivière joined the team as a postdoctoral researcher on transport network resilience to major disruptions (MOBILIENCE project, ANR – PEPR IRiMa). | Team page |
| September 2026 | I was appointed Associate Editor of *Transportation Engineering* (Elsevier). | [Editorial board](https://www.sciencedirect.com/journal/transportation-engineering/about/editorial-board) |
| August 2026 | My ANR JCJC project GREENSHIFT on multimodal mobility hub networks was accepted for funding (2027–2031). | GREENSHIFT page |
| 2026 *(confirm month)* | Our paper "Measuring the state of open science in transportation using large language models" was published in *Transportation Research Part C*. | Publication page on this site; [DOI](https://doi.org/10.1016/j.trc.2026.106024) |
| 2026 *(confirm month)* | At hEART 2026 in Paris, I co-organised a reproducibility workshop at the PhD summer school with Silvia Varotto, and Tristan Lemoalle presented his first PhD results on bike-inclusive road network design. | Talks entry for the hEART 2026 paper |
| October 2025 – January 2026 | Three PhD candidates joined the team: Tristan Lemoalle (Oct 2025), Sina Sabzekar (Nov 2025) and Zohre M. Mosammam (Jan 2026). | Team page |
| 2025 *(confirm month)* | Tristan Lemoalle received the Citec prize 2025 for his master thesis on bikeability, which I supervised. | – |

Internal links: use the site's own URLs (`/greenshift/`, `/team/` or `/supervision/`, the TR-C publication page, the hEART 2026 talk page from Section 3). Rows marked *(confirm month)* need the month from Bahman before publishing; if not provided, show the year only.

## 2. Papers page (/publications/): two tabs and one new entry

Split the Publications page into two tabs: **Publications** (the existing list, unchanged apart from the one new entry below) and **Software & Data** (new). The "Papers" menu item and the homepage papers section stay as they are.

**Implementation**

- Use the same tab component as on the GREENSHIFT page. If the publications list template cannot hold tabs, turn `content/publications/_index.md` into a landing page with a tabs block whose first tab renders the existing publication collection and whose second tab is a markdown block.
- The Publications tab keeps the current listing, order and links exactly as they are now.

### 2a. Publications tab: add the Springer book chapter

Create a new publication entry (folder e.g. `content/publications/b2026-cav-readiness/`) with these fields:

| Field | Value |
| --- | --- |
| Title | A framework for road authorities to assess their readiness to support connected and automated driving |
| Authors | I. Guy, A. Wright, K. McPherson, B. But, R. Öörni, J. McCarthy, Bahman Madadi, A.P. Silvano, J. Andersson, A. Adesiyun |
| Year | 2026 |
| Type | Book chapter (Hugo Blox `publication_types: ["6"]`, book section) |
| Book | Transport Transitions: Advancing Sustainable and Inclusive Mobility (eds. C. McNally, P. Carroll, B. Martinez-Pastor, B. Ghosh, M. Efthymiou, N. Valantasis-Kanellos) |
| Publisher, pages | Springer Nature, Cham, pp. 815–821 |
| DOI | [10.1007/978-3-032-04774-8_116](https://doi.org/10.1007/978-3-032-04774-8_116) |
| Project | DiREC (CEDR Transnational Road Research Programme) |
| Featured | No |

Add a "Related talk" link on this entry to the existing talk page `/events/c2026-cav-readiness/`, and a "Publication" link back from that talk page to the new chapter. Keep the talk entry as it is.

### 2b. Software & Data tab (new)

Short intro line (suggested wording): *"I release the code and data behind my papers under open licenses so that results can be reproduced and reused."*

Then one card or one row per item, in this order:

| Name | What it is (one line) | License | Link | Related paper |
| --- | --- | --- | --- | --- |
| HDLMF_GIN-GA | Hybrid deep-learning–metaheuristic framework: a graph neural network surrogate inside a genetic algorithm for bi-level network design | MIT | [GitHub](https://github.com/bahmanmdd/HDLMF_GIN-GA) | ESWA 2024 |
| Equilibrium-Traffic-Networks | Three benchmark datasets of traffic networks with user-equilibrium solutions, for training and testing surrogate models | CC BY 4.0 | [Figshare](https://doi.org/10.6084/m9.figshare.27889251) | ESWA 2024 |
| MOST | LLM-based pipeline that measures the availability of code and data in transportation research papers (developed within RERITE) | Use license shown in the repository | Use the same repository URL already linked on the TR-C publication entry (currently `github.com/RRinTransportation/OpenMOST`) | TR-C 2026 |
| TOD_simulation | Agent-based discrete event simulation of teleoperated truck driving, used for fleet sizing | MIT | [GitHub](https://github.com/bahmanmdd/TOD_simulation) | TRIP 2026 |
| GINGA-mini | Teaching mini-projects on graph neural networks and genetic algorithms for network design (ENS de Lyon transport week, 2025) | MIT | [GitHub](https://github.com/bahmanmdd/GINGA-mini) | – |
| DAP | Java implementation of simultaneous perturbation stochastic approximation (SPSA) for anchorage planning | Use license shown in the repository | [GitHub](https://github.com/bahmanmdd/DAP) | ESWA 2020 |

"Related paper" cells link to that paper's page on this site. Check that every external link resolves before publishing.

## 3. Talks (/events/): six new entries and two "Invited" labels

No structural change to the Talks page. Add the entries below as new event pages in `content/events/`, following the format of the existing ones (title, authors, event name, location, date, one-line summary, featured image if available). Then relabel the two invited talks.

### 3a. New entries

| Folder (suggested) | Title | Authors (as on the paper) | Event, location | Date | One-line summary |
| --- | --- | --- | --- | --- | --- |
| `c2026-vppc` | Enhancing battery health in shared electric vehicles for V2G services to support grid and mobility systems: Review and outlook | Zohre M. Mosammam, Bahman Madadi, Rochdi Trigui | IEEE Vehicle Power and Propulsion Conference (VPPC 2026), Lyon, France | October 2026 | Review of battery-health-aware V2G services for shared electric vehicles |
| `c2026-heart-bikeability` | Bi-modal road network design framework using bikeability | Tristan Lemoalle, Bahman Madadi, Angelo Furno | hEART 2026 – 14th Symposium of the European Association for Research in Transportation, Paris, France | 2026 *(confirm date)* | Road network design for cars and bicycles using a bikeability measure |
| `c2026-heart-openscience` | Measuring the state of open science in transportation using large language models (poster) | Junyi Ji, Ruth Lu, Linda Belkessa, Liming Wang, Silvia Varotto, Yongqi Dong, Nicolas Saunier, Mostafa Ameli, Gregory S. Macfarlane, Bahman Madadi, Cathy Wu | hEART 2026, Paris, France | 2026 *(same date as above)* | Poster version of the TR-C paper; link to its publication page |
| `c2026-instr` | Mobility hubs for transportation resilience: A systematic literature review | Sina Sabzekar, Bahman Madadi, Angelo Furno | 10th International Symposium on Transport Network Resilience (INSTR 2026), Lyon, France | 2026 *(confirm date)* | Systematic review of how mobility hubs contribute to urban transport resilience |
| `c2025-ens-lyon` | Transport network design and machine learning (original title: "Conception des réseaux de transport et apprentissage automatique") | Bahman Madadi | Invited lecture, transport thematic week, ENS de Lyon, France | January 2025 | Invited lecture with hands-on mini-projects; link to the GINGA-mini repository |
| `c2019-cictp` *(only if not already on the site, see 3c)* | Scenario-based infrastructure requirements for automated driving | Xiaolin Lu, Bahman Madadi, Haneen Farah, Maaike Snelder, Jan Anne Annema, Bart van Arem | CICTP 2019 – 19th COTA International Conference of Transportation Professionals, Nanjing, China | 6–8 July 2019 | Infrastructure requirements for SAE Level 4 automated driving under future scenarios; proceedings pp. 5684–5695, [DOI](https://doi.org/10.1061/9780784482292.489) |

For dates marked *(confirm date)*, ask Bahman for the exact day; until then use the first day of the conference month only if he gives the month.

### 3b. Mark invited talks

- `c2025-xai-lyon` (Explainable graph neural networks for traffic assignment and road network design): change the summary from "Conference presentation on explainable GNNs for network design" to **"Invited talk, Workshop on the Use of Explainable AI in Transportation Research, Lyon"**.
- `c2025-ens-lyon` (new): summary starts with **"Invited lecture"**.
- If the template supports tags, add the tag `invited` to both.

### 3c. Check before adding

- Search `content/events/` for an existing CICTP 2019 entry ("Scenario-based infrastructure requirements"). If it exists, keep it and only make sure the author list and DOI match the table above. If it does not exist, create `c2019-cictp`.
- The ICASP14 entry (`c2023-icasp14`, Mert Dönmez's work) already exists. Do not duplicate it; it is linked from the Team page (Section 4).

## 4. Supervision page becomes "Team"

Rename the page and its menu label from "Supervision" to **Team**, keep its position in the menu, and restructure it as: a notice box, a one-line intro, then two tabs, **Current team** and **Alumni**.

**Implementation**

- Move the page to `/team/` and add `aliases: ["/supervision/"]` so the old URL still works. Update the menu entry label and URL.
- Change the page meta description from "Current PhD students under supervision" to "Team: PhD candidates, postdoctoral researcher and alumni".
- Reuse the existing PhD cards (photo, name linked to LinkedIn, topic, director) for all current members.

### 4a. Notice box (top of page, above the tabs)

Use a visible callout/alert style (Hugo Blox `callout` or `alert` shortcode, "note" or "warning" type). Exact wording:

> **No open positions.** I currently have no open PhD, postdoc or internship positions. Unsolicited applications will not receive a reply. Any future openings will be announced on this page.

### 4b. Intro line (replaces the current one)

Suggested wording: *"My team works on learning-based optimisation of transport and energy networks. All PhD candidates are co-supervised with colleagues at ENTPE and Université Gustave Eiffel."*

### 4c. Tab "Current team"

Keep the three existing PhD cards and add two fields to each (**Started** and **Funding**). Add one new postdoc card. Order: postdoc first, then PhD candidates by start date (newest first).

| Name | Role | Topic | Started | Funding | Director / main supervisor |
| --- | --- | --- | --- | --- | --- |
| Louis Rivière | Postdoctoral researcher | Modelling transport network resilience to major disruptions | October 2026 | MOBILIENCE project (ANR, France 2030 PEPR IRiMa) | Dr. Angelo Furno (project lead at the lab), co-supervised by me |
| Zohre M. Mosammam | PhD candidate | (keep existing topic text) | January 2026 | MEGA doctoral school contract, Université Gustave Eiffel | Prof. Rochdi Trigui, HDR (keep existing) |
| Sina Sabzekar | PhD candidate | (keep existing topic text) | November 2025 | MEGA doctoral school contract, ENTPE | Prof. Angelo Furno, HDR (keep existing) |
| Tristan Lemoalle | PhD candidate | (keep existing topic text) | October 2025 | ITPE doctoral contract, French Ministry for Ecological Transition | Prof. Angelo Furno, HDR (keep existing) |

For Louis Rivière: no photo or LinkedIn link is known. Ask Bahman for both; if not provided, show the card with a generic avatar and no link.

### 4d. Tab "Alumni"

Heading inside the tab: **Former master students** (newest first). One compact line per person: name, year, institution/programme, thesis topic, and any output link. No photos needed.

| Name | Year | Programme / context | Thesis or project topic | Note / output |
| --- | --- | --- | --- | --- |
| Jules Journoux | 2026 | ENTPE, research internship at ETH Zurich | Integrating cycling as a feeder mode in public transport network design and timetabling | – |
| Tristan Lemoalle | 2025 | ENTPE, master thesis | Towards a comprehensive bikeability measure: combining qualitative and quantitative approaches | Citec prize 2025 (best master thesis in transport); now a PhD candidate in the team |
| Marie Deruyck | 2025 | ENTPE, research internship at the University of Florida | Bicycle accessibility of urban areas | – |
| Adam Courtois | 2024 | ENTPE, research internship at Polytechnique Montréal (co-supervised with C. Buisson and C. Morency) | The potential of bike–metro intermodal trips in Montréal | – |
| Mert Dönmez | 2023 | TU Delft, MSc Construction Management and Engineering (co-supervised with M. Nogal) | Optimizing the bridge maintenance schedule of transportation networks under uncertainty | Conference paper at ICASP14 2023: link to `/events/c2023-icasp14/` |
| Xiaolin Lu | 2018 | TU Delft, MSc Construction Management and Engineering (graduation committee member) | Infrastructure requirements for automated driving ([thesis](https://repository.tudelft.nl/file/File_21b7b3a0-ed60-4863-ba3e-0e419989c899?preview=1)) | Conference paper at CICTP 2019: link to the CICTP 2019 talk page (Section 3) |

Do not add supervision percentages or student photos to this tab.

## 5. Experience page: three tabs, one new Service tab

Split the Experience page into three tabs: **Positions**, **Education** and **Service**. Positions and Education hold the two existing sections exactly as they are now, including all older entries; nothing is trimmed or reworded. Service is new.

**Implementation**

- Use the same tab component as on the GREENSHIFT page. Tab 1 = the existing "Experience" timeline (rename its heading to "Positions"), tab 2 = the existing "Education" timeline, tab 3 = a new markdown block.
- Tab order: Positions, Education, Service. Positions opens by default.

### 5a. Service tab content

Three short groups, each a heading plus a list, most recent first within each group.

**Editorial**

- Associate Editor, *Transportation Engineering* (Elsevier), since September 2026 – [editorial board](https://www.sciencedirect.com/journal/transportation-engineering/about/editorial-board)
- Lead Guest Editor, special issue "Open Science in Transportation: Establishing a Foundation for Transparent, Reproducible, and Collaborative Research", *Transportation Engineering* (Elsevier), 2026–2027 – [call for papers](https://www.sciencedirect.com/special-issue/337680/open-science-in-transportation-establishing-a-foundation-for-transparent-reproducible-and-collaborative-research)

**Research community**

- Elected Steering Committee member and Communication Officer, [RERITE](https://www.rerite.org/) – REproducible Research In Transportation Engineering, since 2024

**Conference organisation**

- Co-organiser, with Silvia Varotto (TU Delft), of a workshop on reproducible research in transportation at the hEART 2026 PhD summer school, Paris, 2026
- Programme Committee member, INSTR 2026 – 10th International Symposium on Transport Network Resilience, Lyon, 2026
- Session chair: hEART 2026 (Paris), INSTR 2026 (Lyon), EWGT 2023 (Santander)

Nothing else goes in this tab: no reviewing lists, thesis examinations or committee memberships beyond those above.

## 6. Final checklist for the agent

- [ ] Homepage: News section added after the biography block, 8 items, newest first; Professional Summary unchanged
- [ ] Papers page: tabs "Publications" and "Software & Data"; Springer 2026 chapter added and cross-linked with `/events/c2026-cav-readiness/`
- [ ] Software & Data tab: 6 items, all external links resolve
- [ ] Talks: VPPC 2026, hEART 2026 (×2), INSTR 2026, ENS Lyon 2025 added; CICTP 2019 checked and added only if missing
- [ ] Talks: XAI Lyon and ENS Lyon labelled "Invited"
- [ ] Menu: "Supervision" renamed "Team", same position; `/supervision/` still resolves via alias
- [ ] Team page: no-open-positions notice at top; Current team tab (1 postdoc + 3 PhDs with start date and funding); Alumni tab (6 former master students with ICASP14 and CICTP links)
- [ ] Experience page: tabs Positions / Education / Service; Positions and Education unchanged; Service tab with 3 groups
- [ ] GREENSHIFT and Courses pages untouched
- [ ] No new top-menu items; no supervision percentages, grant amounts or rejected proposals anywhere
- [ ] Site rebuilt locally without errors; mobile layout of the new tabs checked
- [ ] Report back: list of changed or created files, plus open questions

**Open questions to ask Bahman before publishing**

- Month of the special-issue call, the TR-C publication and the Citec prize (News rows marked *confirm month*).
- Exact dates of hEART 2026 and INSTR 2026 (Talks).
- Photo and LinkedIn URL for Louis Rivière (Team).
