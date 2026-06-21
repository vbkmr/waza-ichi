# 技市 — Waza-Ichi

**技 (waza)** = skill · **市 (ichi)** = market → a **"skill market"**: a
[Claude Code plugin marketplace](https://code.claude.com/docs/en/plugin-marketplaces)
of skills for learning and working with the Japanese language.

Add it once, then install any plugin inside it.

## Quick start

```bash
# 1. Add this marketplace
/plugin marketplace add vbkmr/waza-ichi

# 2. Install a plugin from it
/plugin install japanese-word-explainer@waza-ichi
```

(Both commands also work from the terminal as `claude plugin marketplace add …`
and `claude plugin install …`.)

## Plugins

### 📖 japanese-word-explainer

Turns any Japanese word, phrase, or grammar point into a detailed,
study-reference-style explanation — kanji breakdowns, nuance and formality
notes, natural example sentences with full furigana, comparison tables, and
usage notes. Drop in `台頭`, `参政権`, `辛い`, or a comparison like
`〜ば v/s 〜たら` and get the full picture.

It's built to be **scannable** and **accurate** — it won't invent readings, and
it flags words whose reading changes the meaning (辛い = からい／つらい) instead of
guessing.

<details open>
<summary>Example output for <strong>台頭</strong></summary>

> ## 台頭（たいとう）
>
> - **Meaning:** rise (to prominence), emergence, gaining power
> - **Kanji Breakdown:**
>     - 台（たい）= platform/stand, 台風（たいふう "typhoon"）
>     - 頭（とう）= head, 先頭（せんとう "the lead/front"）
>     - Literally: "head onto a platform" → rising up to a prominent position
> - **Type:** Noun / suru-verb (名詞・する動詞)
> - **Nuance:** Formal and somewhat literary — common in news and analysis when a
>   new power, trend, or figure *emerges and starts to dominate*.
> - **Example Sentences:**
>     - 新興勢力（しんこうせいりょく）の台頭が業界（ぎょうかい）を揺（ゆ）るがした。
>         - *The rise of new players shook the industry.*
>
> _(…related words, usage notes, and example contexts follow)_

</details>

<details open>
<summary>Example output for <strong>目を見張る</strong></summary>

> ## 目（め）を見張（みは）る
>
> - **Meaning:** to open one's eyes wide (in surprise or admiration), to be struck/amazed
> - **Kanji Breakdown:**
>     - 目（め）= eye, 目的（もくてき "purpose"）
>     - 見（み）る = to see, 見学（けんがく "observation visit"）
>     - 張（は）る = to stretch/spread, 引（ひ）っ張る（ひっぱる "to pull"）
>     - Literally: "to stretch one's eyes (wide)"
> - **Type:** Idiom / Godan verb phrase (慣用句・五段動詞)
> - **Nuance:** A vivid idiom for being so impressed or astonished that your eyes
>   widen — usually positive, expressing admiration at remarkable growth, skill, or
>   scenery.
> - **Example Sentences:**
>     - 彼女（かのじょ）の成長（せいちょう）には目を見張ることがある。
>         - *Her growth is, at times, truly remarkable.*
>
> _(…key patterns like 目を見張るものがある, related words, and usage notes follow)_

</details>

## Repository layout

```
waza-ichi/
├── .claude-plugin/
│   └── marketplace.json                 ← the marketplace catalog
├── plugins/
│   └── japanese-word-explainer/
│       ├── .claude-plugin/
│       │   └── plugin.json              ← the plugin manifest
│       └── skills/
│           └── japanese-word-explainer/
│               └── SKILL.md             ← the skill definition
├── README.md
└── LICENSE
```

## License

[MIT](./LICENSE) — free to use, modify, and share.
