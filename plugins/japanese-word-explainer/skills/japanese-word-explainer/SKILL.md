---
name: japanese-word-explainer
description: Use this skill whenever the user asks about a Japanese word, phrase, grammar point, or expression and wants a detailed explanation. Triggers include asking what a word means, how to use it, comparing two similar Japanese words or grammar patterns (e.g. "X v/s Y"), requesting breakdowns of kanji compounds, or asking for nuance/usage notes on Japanese vocabulary. Also use when the user pastes a Japanese word or short phrase and expects an explanation. This skill produces richly formatted markdown explanations with kanji breakdowns, example sentences, nuance comparisons, and usage notes. Use this skill even if the user just drops a Japanese word with no other context — they likely want the full explanation.
---

# Japanese Word Explainer

This skill produces detailed, richly formatted markdown explanations of Japanese words, phrases, and grammar points. The output should feel like a premium study reference — thorough but scannable.

## Output Format

Every explanation MUST follow this template structure. Adapt sections as needed (not every word needs every section), but the core structure should remain consistent.

```markdown
## [Word] ([reading])

- **Meaning:** [English meanings, separated by commas]
- **Kanji Breakdown:**
    - [Kanji 1] ([reading]) = [meaning], [example word using this kanji]
    - [Kanji 2] ([reading]) = [meaning], [example word using this kanji]
    - Literally: "[literal meaning combining both kanji]"
- **Type:** [Part of speech in English + Japanese] (e.g., Noun (名詞), Godan verb (五段動詞))
- **Nuance:** [2-3 sentences explaining the feeling, tone, and contexts where this word is used; mention formality level; note if literary, casual, formal, etc.]
- **Example Sentences:**
    - [Japanese sentence 1]
        - *[Natural English translation]*
    - [Japanese sentence 2]
        - *[Natural English translation]*
    - [Japanese sentence 3]
        - *[Natural English translation]*
- **Related Words:**
    - [Word 1] ([reading]) = [meaning] ([brief nuance difference])
    - [Word 2] ([reading]) = [meaning] ([brief nuance difference])
    - [Word 3] ([reading]) = [meaning] ([brief nuance difference])
    - [Word 4] ([reading]) = [meaning] ([brief nuance difference])
```

After the core block, include **2-4 additional sections** chosen from the following based on relevance:

### Available Additional Sections

Pick the sections that are most useful for the specific word. Not every word needs every section.

#### Key Patterns
Show common grammatical patterns or collocations using the word. Use the format:

```markdown
### Key Patterns

**[Pattern in Japanese]** — "[English meaning of pattern]"

- [Example sentence] ([translation])
- [Example sentence] ([translation])
```

#### Important Nuance: [Word] v/s [Similar Word(s)]
When there are easily confused similar words, create a comparison. Use a concise table or bullet list highlighting the core differences in feeling, usage, and context.

```markdown
### Important Nuance: A v/s B v/s C

| Word | Feeling |
|---|---|
| **A** | [short nuance description] |
| **B** | [short nuance description] |
| **C** | [short nuance description] |
```

Or for richer comparisons:

```markdown
| Word | Feeling | Who/What? |
|---|---|---|
| **A** | [nuance] | [who uses it / what context] |
| **B** | [nuance] | [who uses it / what context] |
```

#### Usage Note
A short paragraph about when and where native speakers actually use this word — is it common in daily speech? Mostly written? Literary? Slang? Does it appear more in certain genres or contexts?

#### Writing Variations
When a word has multiple written forms (kanji, kana, slang), show them:

```markdown
### Writing Variations

| Form | Formality | Context |
|---|---|---|
| **[Kanji form]** | ★★★☆☆ | Written, standard |
| **[Kana form]** | ★★☆☆☆ | Casual written |
| **[Shortened form]** | ★☆☆☆☆ | Casual spoken |
```

#### Compound Verb Patterns
When explaining a compound verb (e.g., ～出す, ～込む, ～合う), explain the pattern itself with additional examples:

```markdown
### The ～出す (dasu) Compound Pattern

[Brief explanation of what this pattern adds]

- [Compound verb 1] ([reading]) = [meaning]
- [Compound verb 2] ([reading]) = [meaning]
- **[The word being explained]** ([reading]) = [meaning]
```

#### Example Contexts
End with 3-4 short, natural usage examples without full translations — just the Japanese with brief context. These serve as quick-reference phrases:

```markdown
### Example Contexts

- [Japanese phrase] ([very brief English gloss])
- [Japanese phrase] ([very brief English gloss])
- [Japanese phrase] ([very brief English gloss])
- [Japanese phrase] ([very brief English gloss])
```

## Guidelines for Quality

### Hiragana Readings (REQUIRED)
Every kanji word that appears anywhere in the explanation MUST be immediately followed by its hiragana reading in full-width brackets （）the **first time** that word appears. This applies everywhere — example sentences, nuance descriptions, key patterns, comparison tables, usage notes, related words, and example contexts — not just the headword and kanji breakdown.

- Gloss each kanji *word* (not each individual character) on its first occurrence: 世界経済（せかいけいざい）, not 世界（せかい）経済（けいざい）— unless the components are naturally separate words in the sentence.
- Once a word has been glossed in the response, you don't need to repeat the reading for later occurrences of that same word.
- Kana-only words (です, ある, から, etc.) never need readings.
- Use full-width parentheses （） directly after the word with no space.

Example:
- 彼（かれ）の成長（せいちょう）には目（め）を見張（みは）るものがある。
    - *His growth is truly remarkable.*

### Accuracy (REQUIRED)
A wrong reading or a fabricated example is worse than a missing one — a learner will memorize the mistake. Hold yourself to these rules:

- **Never invent or guess a reading.** If a word's reading is uncertain, rare, or genuinely ambiguous in the given context, say so explicitly rather than picking one silently. For example, 行った can be いった ("went") or おこなった ("carried out") — note both if context doesn't disambiguate.
- **Surface meaning-changing readings.** When a word has multiple readings that change its meaning, mention them: 辛い（からい "spicy" ／つらい "painful"), 入る（はいる "to enter" ／いる "to need/contain"), 上手（じょうず "skilled" ／うわて／かみて). Default to the most common reading for the headword but flag the alternatives.
- **Use only real, common example words** in kanji breakdowns and Related Words. Do not fabricate compounds to fit a slot — if you can't recall a natural example for a kanji, give its plain meaning instead.
- **Respect okurigana and word boundaries.** Attach readings to the actual word as written; don't split a single word's reading across unrelated kanji.
- **Pitch accent is optional** — only include it if you are confident. An omitted pitch accent is fine; a wrong one is not.
- If you are unsure about any fact (etymology, register, regional usage), hedge honestly ("commonly", "often", "in my experience") rather than stating it as certain.

### Example Sentences
- Use natural, native-sounding Japanese — not textbook-stiff sentences
- Vary the contexts (daily life, work, emotions, stories)
- English translations should be natural and idiomatic, not word-for-word
- Italicize English translations
- Add hiragana readings in （）for every new kanji word (see "Hiragana Readings" above)

### Nuance Descriptions
- Be specific about the *feeling* of the word, not just the dictionary meaning
- Mention formality level explicitly
- Note if the word is more common in writing vs. speech
- Compare to English equivalents when helpful (e.g., "closer to 'the abyss' than simply 'the dark'")

### Kanji Breakdowns
- Always give the reading of each kanji component
- Provide at least one familiar example word using that kanji
- Include the "Literally: ..." line combining the components — this helps with memorization

### Related Words
- Choose 4-5 related words that a learner might confuse or want to know
- Add a brief parenthetical noting the key difference
- Order from most to least similar

### Comparisons (v/s format)
When the user asks about two or more similar words/grammar points (indicated by "v/s", "vs", "versus", "difference between"):

- Explain each item separately first using the standard format above
- Then provide a comparison section with a table highlighting key differences
- Include side-by-side example sentences showing the same situation expressed with each word
- Add a mnemonic or memory hack if possible
- End with practice questions if it's a grammar comparison

## Tone and Style
- Warm and knowledgeable, like a great language tutor
- Use markdown formatting consistently (bold for Japanese words in explanations, tables for comparisons)
- Keep the structure scannable — a learner should be able to skim and find what they need
- Don't over-explain obvious things, but don't assume advanced knowledge either
- Use em dashes freely for asides and clarifications

## What NOT to do
- Don't give bare dictionary definitions without nuance
- Don't skip the kanji breakdown for compound words
- Don't write stilted/textbook example sentences
- Don't forget to mention formality and common usage contexts
- Don't create walls of text without structure — use headers, bullets, and tables
- Don't leave any new kanji word without its hiragana reading in （）on first appearance
- Don't invent readings or example words to fill the template — accuracy beats completeness
- Don't silently pick one reading for a word that has several with different meanings — flag the alternatives
- Don't state uncertain facts (etymology, pitch accent, regional nuance) as if they were certain
