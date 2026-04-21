# Approach

## Phases

### 1. Context capture (now)
Record every tidbit the user shares in `NOTES.md` as dated, append-only entries. No summarization, no editorializing — raw information first, synthesis later. This is the source of truth for what the project actually is.

### 2. Research
Augment user-provided context with external research on the underlying science / methodology. Likely domains:
- Active fixed income management — alpha sources, factor models, credit selection.
- Risk and quantitative techniques used in bond markets — duration, convexity, spread modeling, liquidity, factor decomposition, attribution.
- Academic/industry literature on whatever specific topic the project addresses.

Every external source gets a citation in `NOTES.md` (author, title, year, link). No unsourced claims in the deck.

### 3. Framing
Decide the single thesis of the presentation — one sentence the audience should walk away remembering. The whole deck is then structured backward from that sentence:
- What does the audience need to believe to accept the thesis?
- What evidence supports each belief?
- What's the strongest counter-argument, and where does it go (main deck vs. appendix)?

### 4. Outline
Draft `OUTLINE.md` as main-deck skeleton + appendix topic list. Iterate with user before building slides.

### 5. Knowledge base
Once the outline is stable, consolidate notes into a structured knowledge base (likely `knowledge/` directory, one file per topic). The KB is what the slides are built from; the slides are the tip of the KB iceberg.

### 6. Slides
Produced last, from the KB. Form follows content. Defer format/tool decisions (HTML deck, PDF, PowerPoint, etc.) until content is settled.

## Rules for this project
- **Terse, scripted, rigorous.** All quantitative claims in the deck must come from a reproducible script, not LLM estimation.
- **No black ink, no curves in charts** — straight lines, visible dots, theme colors.
- **Source everything.** A claim without a citation does not go in the deck.
- **Root-cause discipline.** If a number looks wrong, fix it at the source. Don't fudge.
- **Appendix is a weapon, not a graveyard.** Every appendix slide anticipates a specific question and answers it decisively.

## Information collection protocol
The user will specify how they want information collected in the next message. Until then, default assumption is: user feeds tidbits → I log them → I do external research when explicitly asked.
