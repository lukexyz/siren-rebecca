# PLAN — `the_murder_of_odysseus.html`

A redesign of `odyssey_translations.html` that's **designed to be read**, but with a visual hierarchy that no longer buries the lede. Same evidence, same scholarship — but the **diffs are the hero**, the academic context is the **supporting actor**, and **secondary evidence sits behind disclosure** so depth is available without cluttering the surface.

## Decisions locked in (from user feedback)

- **4 sections**: Recklessness → Slavery → Character distortions → Bronze-Age vs Netflix (tonal incoherence)
- **Pan-Slaveism (§02)**: 1 hero passage (the doorway) + **expandable `<details>` blocks** for the other 4 passages — preserve full evidence, hide it until clicked
- **All sections on cream background** — drama comes from typography + numbered headings, not background swaps
- **The piece is to be read, not scrolled past** — expandable disclosures over heavy condensation; trust the reader to engage

---

## What we're keeping from the source

- The **translator overview table** at the top (it's the one part the user explicitly likes — it works because it's scannable). Keep it more or less as-is, maybe lightly visually demoted so it doesn't compete with the new section headings.
- The **Greek source quotes** (small, italic) above each diff.
- The **4-column side-by-side diff** layout with yellow/green highlighting — this is the most-engaging visual element in the original. It stays, but gets more breathing room and bigger type.
- All factual content, citations, and Whitaker's verdicts — nothing gets dropped, just visually re-ranked.

## What we're cutting / demoting

- The dense **sidebar nav** — replace with a single floating "jump to" pill or a top tab strip with just 4 chips.
- The **legend box** — fold into the first diff inline (a one-line note: "yellow = Wilson, green = the others").
- The **passage-card chrome** (dark header with `Od. X.Y` ref, gold border, etc.) — too much furniture per passage. Replace with a much simpler structure.
- The **"further critique" prose blocks at the bottom** — promote `character distortions` to its own section (#3), fold the errata / tonal-incoherence material into a single condensed "the receipts" closer.
- Multiple passage cards inside Pan-Slaveism (5 currently) — **condense to 1 hero passage + a compact strip of "and also" examples**. TikTok audience doesn't want 5 near-identical diffs in a row.

## The new structure

```
┌────────────────────────────────────────────────────┐
│  HERO — "The Murder of Odysseus"                   │
│  one-line dek: "How one translator rewrote a hero" │
│  big credit line: based on Whitaker, Acta Classica │
└────────────────────────────────────────────────────┘
┌────────────────────────────────────────────────────┐
│  TABLE — 13 translations (kept, lightly toned)     │
└────────────────────────────────────────────────────┘
┌────────────────────────────────────────────────────┐
│  01. DID ODYSSEUS EVEN TRY TO SAVE HIS MEN?        │
│      subtitle: Wilson cut the line that says he did│
│      [DIFF — hero element, big, generous spacing]  │
│      [below, smaller/lighter: Whitaker verdict]    │
└────────────────────────────────────────────────────┘
┌────────────────────────────────────────────────────┐
│  02. ARE THESE WOMEN SLAVES — OR ARISTOCRATS?      │
│      subtitle: One English word for a dozen roles  │
│      [DIFF — the doorway passage as the hero]      │
│      [Whitaker verdict, demoted styling]           │
│                                                    │
│      ▸ The ball scene (Od. 6.122) — click to open  │
│      ▸ Braided "slaves" (Od. 6.199) — click open   │
│      ▸ Canapés (Od. 4.55) — click to open          │
│      ▸ Girls executed (Od. 22.421) — click to open │
│      (each <details> contains full 4-col diff +    │
│       verdict, same pattern as the hero)           │
│                                                    │
│      [below the disclosures: the term-table        │
│       ἀμφίπολος / θεράπων / κήρυξ / ταμίη / etc.]  │
└────────────────────────────────────────────────────┘
┌────────────────────────────────────────────────────┐
│  03. DID WILSON TURN ODYSSEUS INTO A VILLAIN?      │
│      subtitle: "Wily" → "Lord of lies." "Savage"   │
│      → "a man of courage." Verbs hardened. Suitors │
│      softened.                                     │
│      [DIFF — Od. 1.1 polytropos as the hero]       │
│      [below: 5-bullet "the receipts" — the         │
│       polymetis / polytlas / hyperbion hybrin /    │
│       Cyclops / ὀλέσας examples, compact]          │
└────────────────────────────────────────────────────┘
┌────────────────────────────────────────────────────┐
│  04. IS THIS BRONZE-AGE EPIC, OR A NETFLIX SHOW?   │
│      subtitle: "There will be blood." "Babysit."   │
│      "Tote bag." "Cushy." Welcome to Ithaca.       │
│      [DIFF — Od. 18.148 "there will be blood"]     │
│      [below: the colloquial-vs-elevated word cloud │
│       or two-column list]                          │
└────────────────────────────────────────────────────┘
┌────────────────────────────────────────────────────┐
│  THE RECEIPTS — errata table, compact, collapsible │
│  source link to Acta Classica paper                │
└────────────────────────────────────────────────────┘
```

---

## Visual / typography rules (the "TikTok-ification")

### Section headings
- **Display-scale type**: `clamp(2.6rem, 7vw, 5rem)`, weight 700–800, very tight line-height (~1.0).
- Numbered (`01.`, `02.`, `03.`, `04.`) in a contrasting accent color (gold or rust), set huge and slightly offset — like the chapter numbers in a magazine feature.
- Heading itself is a **question**, not a description. Provocative > academic.
- One **subtitle** allowed, max ~12 words, set in a lighter weight (300) and ~1rem.
- Generous top-margin (4–6rem) so each section feels like its own "screen."

### Diff (the hero of every section)
- 4-column layout preserved, but **larger type** (~1rem instead of .88rem) and **more padding** (1.2rem instead of .85rem) so the text breathes.
- **Wilson column gets a visual marker** — colored left border (rust/red) or background tint — so the eye lands on it first.
- Highlights stay yellow/green but get **slightly bolder** and **animate in** on scroll (subtle fade-up).
- Greek source line moves **above** the diff in a small italic strip (one line), gloss collapsed behind an ⓘ hover/tap.

### Context (Whitaker quotes, gloss, citations)
- Set in **lighter weight (300–400)**, **smaller (.82rem)**, and a **muted text color** (~#5a5a5a on cream).
- No background, no border-left chrome — just hangs below the diff with a thin divider rule.
- Citation source as a single small line in mono or sans, very faded.

### Color palette
- Lean into the dark/gold scheme that's already there but **amp the contrast**:
  - Background: cream (`#faf7ef`) for body, **near-black sections** (`#14142b`) interleaved as section dividers.
  - Section headings on the cream get **rust/wine accent numbers** (`#8b3a2a`) + ink-black titles.
  - Some sections could be **inverted** (dark bg, cream text) for variety — every other section maybe.
- Accent for "the bad" (Wilson's contested text): rust/wine. Accent for "the rest": gold. Keep the green highlighter for accuracy.

### Motion (subtle, not gimmicky)
- Section headings **fade + slide up** on enter (`IntersectionObserver`, ~200ms).
- Highlighted diff phrases get a one-time "marker draw" animation when they scroll into view (the highlight expands from a thin line to full width).
- Otherwise no autoplay, no carousels, no parallax — readers still need to be able to read.

### Mobile-first
- The 4-column diff collapses to a single column with the 4 translations stacked, Wilson **last** (so you see the "right" versions first, then the contested one — landing the punchline).
- Section headings remain huge even on mobile (clamp does the work).
- Touch-friendly: no hover-only interactions.

---

## Section copy (proposed exact wording)

| # | Heading | Subtitle |
|---|---------|----------|
| 01 | **Did Odysseus even try to save his men?** | Wilson cut the line that says he did — and the line that blamed the men's own recklessness. |
| 02 | **Are these women slaves, or aristocrats?** | One English word — "slave" — for a dozen distinct Greek roles. And the women who actually *were* enslaved? She calls them "girls." |
| 03 | **Did Wilson turn Odysseus into a villain?** | "Wily" becomes *Lord of lies.* "Resourceful" becomes *ruthless.* The Cyclops's savagery softens to *a man of courage.* |
| 04 | **Bronze-Age epic, or Netflix show?** | "There will be blood." "Babysit." "Tote bag." "Cushy." Welcome to Ithaca. |

(The user said 3 sections explicitly + the character-distortion block; I've added #04 as the natural closer drawing on the tonal-incoherence material. If they only want 3, drop #04 and move "the receipts" / errata up.)

---

## Reusable structural pattern (per section)

```html
<section class="chapter" id="ch-01">
  <div class="chapter-num">01.</div>
  <h2 class="chapter-title">Did Odysseus even try to save his men?</h2>
  <p class="chapter-sub">Wilson cut the line that says he did…</p>

  <div class="ref-line">Od. 1.5–9 · ἀτασθαλίῃσιν · ἱέμενός περ</div>

  <div class="diff-hero">
    <!-- 4 columns, Fitzgerald · Fagles · Mendelsohn · Wilson(highlighted) -->
  </div>

  <div class="aftermath">
    <!-- Whitaker quote, lighter and smaller -->
    <!-- citation as a faded one-liner -->
  </div>
</section>
```

Every section uses this same skeleton; the variable is what goes in `diff-hero` and `aftermath`.

---

## Implementation steps

1. Create `the_murder_of_odysseus.html` as a **standalone file** (no shared CSS — keep it self-contained like the original).
2. Reuse the **CSS reset, font stack, color tokens, and the 4-column diff grid** from the source. Drop the rest of the CSS (sidebar, passage-card, tab-bar, critique-prose-block, etc.).
3. Add new CSS for: hero, chapter (the new section block), big numbered headings, demoted-aftermath block, the "and also" strip, the receipts closer.
4. Lift the table HTML from the source (rows 887–~1750 is the original table block — port verbatim with maybe a `details`/`summary` wrapper to collapse it after the hero).
5. Lift the 4 diff blocks needed:
   - **01**: `#p-atasthalie` (rows 1859–1926)
   - **02**: `#p-doorway` as hero + tiny strips drawn from `#p-ballscene`, `#p-braided`, `#p-canapes`, `#p-execution`
   - **03**: `#p-proem` as hero + bullets drawn from the `character distortions` prose block (rows 2344–2355)
   - **04**: `#p-blood` (rows 2285–2339) + word lists drawn from the `diction` prose block (rows 2405–2412)
6. Lift the **errata table** (rows 2417–2433) into the closer, in a `<details>` collapsed by default.
7. Add the IntersectionObserver script for the fade-in animation (one small block, no dependencies).
8. Test in a browser at desktop and mobile widths.

---

## The disclosure pattern (new — used in §02 and §03)

For "and also" evidence — extra passages, extra examples — use a native `<details>`/`<summary>` pattern styled to feel intentional, not like a browser default:

```html
<details class="also">
  <summary>
    <span class="also-chev">▸</span>
    <span class="also-label">The ball scene</span>
    <span class="also-ref">Od. 6.122 · ἔσφηλεν δ' ἐπὶ δίνην</span>
  </summary>
  <div class="also-body">
    <!-- full 4-col diff + verdict, same skeleton as the hero -->
  </div>
</details>
```

Styling: a single-line summary with a chevron that rotates when open, a subtle separator rule between disclosures, generous internal padding when expanded. No JS needed — `<details>` is native.

Where the pattern applies:
- **§02 Slavery**: 4 expandable passages (ball scene, braided slaves, canapés, executed girls) beneath the doorway hero
- **§03 Villain**: the polymetis/polytlas/hyperbion/Cyclops/ὀλέσας bullet list can either stay as inline bullets *or* become 5 small disclosures — recommend inline bullets here since each item is one line, not a full diff
- **Closer**: the errata table inside one big disclosure ("the receipts — 12 errors of fact, click to inspect")

## Open questions (resolved)

1. ~~Three sections or four?~~ → **Four**
2. ~~Pan-Slaveism: condense or show all five?~~ → **Hero + 4 expandable disclosures** (preserves depth, surface stays clean)
3. ~~Dark/light alternating, or all cream?~~ → **All cream**
4. **Keep the original file?** Yes — `the_murder_of_odysseus.html` is the punchy reading version; `odyssey_translations.html` stays as the long-form reference.

---

# PART 2 — LOOKING THROUGH THE MIRROR

A parallel page that does the **inverse** of `the_murder_of_odysseus.html`. Same evidence-based diff format, same visual language, same level of scholarly grounding — but this time collating the **positive critical reception** of Wilson's translation and letting *her* be the column that wins the comparison.

The premise: a single-academic takedown (Whitaker, *Acta Classica* 2020) is not the whole picture. Wilson received major endorsements from the NYT Magazine, LRB, BMCR, *New Statesman*, *Australian Book Review*, the Guardian, and dozens of working classicists. A balanced repo shows both readings side-by-side and lets the reader form their own view. That is far more interesting — and more honest — than a one-sided dunk.

## The framing principle

> The same passage is evidence for the prosecution **and** the defence, depending on the values you bring to it.

The murder page treats "slave" as flattening; the mirror page treats it as honest. The murder page treats "complicated" as foreclosing; the mirror page treats it as opening. Both readings cite the same Greek, the same lines, the same translation choices. **That's the point.** Translation is interpretation, and interpretation is contested.

## What's already in `RESEARCH.md` (positive corpus)

Six positive Wilson reviews are already documented:
- **Pache (BMCR 2018.10.58)** — "amazing achievement … the best English translation … sturdier than the original"
- **Johnson (Australian Book Review 2018)** — "may be the definitive modern English Odyssey for contemporary readers"
- **Burrow (LRB 2018)** — appreciates her as a skilled "moderniser"; epithets as "running commentary on emotional and social relationships"
- **Mason (NYT Magazine 2017)** — "floored" by the opening; praised "radically contemporary voice"
- **Balmer (New Statesman 2018)** — "a careful and creative scholar"
- **Wilson herself** — the 70-page translator's introduction is its own primary source

## Research still needed (before coding)

1. **Pull the full Mason NYT Magazine piece** ("The First Woman to Translate the 'Odyssey' Into English", Nov 2017) — likely names specific passages he was floored by. This is the highest-profile positive piece and probably the single best source of "hero passages" for the mirror.
2. **Pull the LRB Burrow piece** in full — he cites specific epithet renderings; find which passages he singles out.
3. **Pull Wilson's translator's introduction** — the prosecution rebuttal in her own words. Especially the slavery passage where she explains *why* she translated δμωαί uniformly.
4. **Hunt for additional positive reviews not yet in RESEARCH.md**:
   - Madeline Miller (WaPo) — likely positive given her own classical fiction
   - Guardian — Charlotte Higgins reviewed it
   - *The Atlantic* / *Slate* / *Vox* — popular cultural coverage
   - Mary Beard's commentary (Twitter/blog) — if she weighed in
   - Yopie Prins / Sheila Murnaghan — academic feminists who likely endorsed
5. **Find Wilson's responses to criticism** — she's been active publicly defending choices; her own Twitter/X threads on translation are a legitimate primary source

Save findings into `RESEARCH.md` under a new top-level header **"POSITIVE WILSON CORPUS — EXPANDED"** before drafting the HTML.

## Chapter selection — driven by the research, not the rebuttal

Deliberately *not* pre-deciding the 6 chapters here. The point of the research pass is to surface the **strongest independent positive arguments** reviewers actually made — not to manufacture a counterpoint for each of Whitaker's complaints. Some chapters may end up arguing against Whitaker on the same passage; others may spotlight wins Whitaker never engaged with (e.g. the line-count match, the introduction, the reception in classrooms). Lock the 6 sections only after the corpus is in.

## What the diff looks like in mirror mode

Same 4-column layout. Same translators. Same highlighting palette. What changes:

- **Wilson's column gets the green highlight** (the "win" colour from the murder page's accuracy markers) instead of the rust/wine "contested" treatment
- **The other columns get a muted treatment** with specific phrases flagged as *euphemism*, *padding*, *archaism*, or *expansion* — the things positive reviewers praise Wilson for *not* doing
- **The aftermath block** quotes Pache, Mason, Johnson, Burrow instead of Whitaker. Citation block looks identical.
- **The Greek source line is unchanged** — same italic strip, same gloss. The Greek doesn't care which side you're on.

The visual rhyme between the two pages is the whole experience: a reader who's seen both walks away understanding that *both arguments are made of the same material*.

## Filename — locked

**`the_complicated_man.html`** — Wilson's signature line from Od. 1.1, the rendering that floored Wyatt Mason and became the public shorthand for her whole project. The title carries the argument: "complicated" is a *good* translation of πολύτροπος, not a flattening of it.

## Cross-linking strategy

Both pages get a small **top strip** above the hero:

```
┌─────────────────────────────────────────────────────────┐
│  ← Read the case AGAINST   |   Read the case FOR →     │
└─────────────────────────────────────────────────────────┘
```

- From `the_murder_of_odysseus.html` the link points to `the_complicated_man.html` and reads "Read the case **for** Wilson →"
- From `the_complicated_man.html` the link points back to murder and reads "← Read the case **against** Wilson"
- README updates to introduce the project as a **paired reading**, not a hit piece. New phrasing:
  > A paired reading of Emily Wilson's 2017 Odyssey: a critical case drawn from Richard Whitaker's 2020 *Acta Classica* review, and a defence drawn from the positive critical reception (Mason, Burrow, Pache, Johnson, Balmer).
- Sidebar nav on both pages gets a final entry: **"The other reading"** that jumps to the cross-link

## Optional third page — `the_verdict.html`

A short meta-essay (max ~1,000 words) that:
- Names the deeper question: *what is a translation for?* (scholarly access? poetic experience? political reframing? classroom utility?)
- Shows that Whitaker and Wilson's defenders are partly **arguing past each other** — they want different things from a translation
- Points to translation theory: dynamic vs. formal equivalence (Nida), domestication vs. foreignization (Venuti)
- Doesn't pick a winner. Names the tradeoff.

This is the strongest possible closer for the project — but it's optional. The two-page paired reading already accomplishes the main thing.

## Implementation order

1. **Research pass** — fetch positive reviews; expand `RESEARCH.md`. *Do not start coding until this is done.* (Brief below — can be handed to a cheaper model.)
2. **Lock the 6 chapters** with the user — picked from the strongest independent arguments the research surfaces
3. **Copy `the_murder_of_odysseus.html` → `the_complicated_man.html`** as the scaffold; reuse all CSS verbatim
4. **Rewrite the 6 chapter blocks** with positive content; flip the highlight palette in the Wilson column
5. **Add the top cross-link strip** to both pages
6. **Update README** with the paired-reading framing
7. **Update GitHub Pages link list** — both pages get linked
8. *(Optional)* Draft `the_verdict.html` as the closing meta-essay

## Open questions (revisit after research is in)

1. **Cross-linking placement** — top strip on both pages, or a single "the other reading" footer link? (Lean top strip.)
2. **Optional `the_verdict.html` closer** — yes, maybe, or skip?
3. **Tone of the mirror page** — sober and measured (mirror Whitaker's academic register), or punchy and provocative (mirror the murder page's TikTok-ified energy)? Lean sober — the contrast is the point.

---

## Research brief (hand to a cheaper agent)

**Task:** Expand `D:\python\siren-rebecca\RESEARCH.md` with the strongest positive critical reception of Emily Wilson's 2017 Odyssey translation, with enough specificity that her defenders' arguments can be reconstructed and quoted in a public web essay.

**Why this matters:** The repo currently has one HTML page (`the_murder_of_odysseus.html`) built on Richard Whitaker's negative *Acta Classica* 2020 review. A second page (`the_complicated_man.html`) will be built on the positive corpus — but we need the corpus first. Six positive reviews are already partially documented in `RESEARCH.md` under the **EMILY WILSON (2017)** section: Pache, Whitaker (already done — negative), Johnson, Burrow, Mason, Balmer. Most of these are summarised but **not deep**. Some lack key quotes, named passages, or full URLs.

**Working directory:** `D:\python\siren-rebecca`
**File to edit:** `RESEARCH.md`
**Existing structure to follow:** see how the negative Whitaker review (lines ~175–187) and the existing positive reviews (lines ~159–223) are formatted — same heading style, bullets, **Verdict / Key arguments / Key quotes / Source** structure.

### Step 1 — Read what's already there

- Read the full **EMILY WILSON (2017)** section in `RESEARCH.md` to know what's already documented
- Note which reviews have full text vs. just a summary line — those summary-only ones need fleshing out

### Step 2 — Deepen the existing entries

For each of these already-listed reviews, find the **full text or the longest excerpt available online** and pull out:
- Direct quotes of 1–3 sentences (the most memorable / quotable lines)
- **Specific passages from the Odyssey** the reviewer cites approvingly (e.g. "Mason was floored by the opening line: 'Tell me about a complicated man'")
- Any specific Greek words or epithets the reviewer praises Wilson's handling of

Reviews to deepen:
1. **Wyatt Mason — NYT Magazine, Nov 2 2017** — "The First Woman to Translate the 'Odyssey' Into English." This is the most important single positive piece. Find the full text (the NYT URL is public; archive.org may have a non-paywalled version). Pull every specific passage Mason singles out.
2. **Colin Burrow — LRB 2018** — find the issue date and full URL. Quote the "running commentary" line in context. Find which epithets / passages he praises specifically.
3. **Corinne Pache — BMCR 2018.10.58** — already linked (https://bmcr.brynmawr.edu/2018/2018.10.58/). Re-read it and pull every positive passage citation; we currently only have a partial list.
4. **Marguerite Johnson — Australian Book Review, Dec 2018** — link: https://www.academia.edu/39297440. Pull the full review's strongest arguments and the specific epithet examples she cites.
5. **Josephine Balmer — New Statesman 2018** — find the original URL and the strongest pull quotes.

### Step 3 — Find additional positive reviews not yet documented

Look for, and document in the same format:
- **Madeline Miller (Washington Post)** — novelist of *Circe* and *Song of Achilles*; almost certainly reviewed Wilson; if so, find URL + quotes
- **Charlotte Higgins (The Guardian)** — culture editor, frequently writes on classics; check for a Wilson review or column
- **Mary Beard** — blog posts on her TLS blog "A Don's Life", Twitter/X threads, or any TLS coverage on Wilson
- **The Atlantic / Slate / Vox / The New Yorker** — popular culture coverage of Wilson's translation
- **Yopie Prins, Sheila Murnaghan, or other academic feminist classicists** — any journal articles or chapters discussing Wilson favourably
- **BMCR — any review beyond Pache** that touches on Wilson positively
- **Classroom adoption** — is Wilson now assigned in undergraduate Homer courses? Any syllabus evidence, professor blog posts, or *Classical Journal* / *Classical World* notes endorsing it for teaching?

For each new source: same template — reviewer, affiliation, publication + date, verdict, key arguments, key quotes, source URL.

### Step 4 — Pull material from Wilson's own translator's introduction

Wilson's 70-page introduction to her Odyssey is itself a primary source for the defence. Find excerpts available online (Google Books preview, Norton sample chapters, archive.org). Document under a new sub-heading **"Wilson's translator's introduction — her own defence"**:
- Her stated approach to slavery vocabulary (why she translates δμωαί uniformly as "slave")
- Her stated approach to epithets (why she varies them rather than fossilising)
- Her stated approach to metre (iambic pentameter, line-count match)
- Her stated approach to sexual violence / women's voices
- Any direct rebuttal to charges of anachronism

### Step 5 — Pull material on the line-count achievement

Verify / document the line-count claim: Homer's Odyssey is 12,110 lines; Wilson's English translation is 12,109. Cross-check this against:
- Wilson's own statements (interviews, intro)
- Reviewers who note this as a technical achievement
- Comparison numbers for Fagles, Fitzgerald, Lattimore, Mendelsohn

This is the cleanest "objective" win for Wilson and deserves its own short sub-section.

### Step 6 — Structure the output

Append a new top-level section to `RESEARCH.md`:

```markdown
---

## POSITIVE WILSON CORPUS — EXPANDED

> Research conducted [DATE] for `the_complicated_man.html`.
> Deepens the existing reviews and adds new sources. Same format as the rest of the file.

### {Reviewer name} — deepened / new
{full template — verdict, arguments, quotes, source}

...

### Wilson's translator's introduction — her own defence
{her stated rationale, organised by topic}

### The line-count achievement
{numbers, sources, reviewer commentary}
```

Keep `RESEARCH.md`'s existing structure intact above this — only append.

### Constraints

- **Do not modify any HTML files.** This is research only.
- **Do not modify the existing EMILY WILSON (2017) section** in `RESEARCH.md`. Append the new findings to the new **POSITIVE WILSON CORPUS — EXPANDED** section.
- **Cite real URLs** — if a source is paywalled, say so explicitly rather than fabricating quotes.
- **No invented quotes.** If a quote cannot be verified, mark it `[paraphrase, verify before use]`.
- **Keep it to verifiable scholarly / journalistic sources** — Twitter threads from named classicists are OK and useful; anonymous Reddit / blog posts are not.

### When done

Print a one-paragraph summary of:
1. How many new positive reviews were added
2. How many existing reviews were deepened
3. The 3 strongest *specific passage citations* the corpus now points to (e.g. "Mason singles out Od. 5.X; Pache singles out Od. 6.Y; Johnson singles out Od. 1.1")
4. Any gaps that remain (paywalled sources, missing reviews you couldn't find)
