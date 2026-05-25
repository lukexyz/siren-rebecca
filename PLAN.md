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
