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
>     - **台**（たい）= platform/stand, as in 台風（たいふう "typhoon"）
>         - *Parts:* 厶 + 口（radical 口・くち "mouth"）; 台 also serves as a phonetic element
>         - *Readings:* 音 タイ／ダイ ／ 訓 —（no common kun reading）
>         - *Phonetic series:* 台（タイ）→ 怠（タイ "idle"）・胎（タイ "womb"）・苔（タイ "moss"）
>     - **頭**（とう）= head, as in 先頭（せんとう "the lead/front"）
>         - *Parts:* 豆 (phonetic) + 頁（radical おおがい — the "head/face" element in 顔・額・頬）
>         - *Readings:* 音 トウ／ズ ／ 訓 あたま・かしら
>         - *Phonetic series:* 豆（トウ）→ 登（トウ "climb"）・痘（トウ "smallpox"）
>     - Literally: "head onto a platform" → rising up to a prominent position
> - **Type:** Noun / suru-verb (名詞・する動詞)
> - **Nuance:** Formal and somewhat literary. Common in news, business, and
>   historical/political analysis for a new force, trend, or figure *emerging and
>   gaining influence* — often with a sense of rising against or displacing what
>   came before. Not used for everyday "appearing."
> - **Example Sentences:**
>     - 新興勢力（しんこうせいりょく）の台頭が業界（ぎょうかい）を揺（ゆ）るがした。
>         - *The rise of new players shook the industry.*
>     - SNSの台頭により、情報（じょうほう）の伝（つた）わり方（かた）が大（おお）きく変（か）わった。
>         - *With the rise of social media, the way information spreads has changed dramatically.*
>     - 若手（わかて）選手（せんしゅ）の台頭が著（いちじる）しい。
>         - *The emergence of young players is striking.*
> - **Related Words:**
>     - 出現（しゅつげん）= appearance, emergence (more neutral — simply coming into view)
>     - 進出（しんしゅつ）= advance/expansion into (entering a new field or market)
>     - 躍進（やくしん）= rapid progress, leap forward (emphasizes speed)
>     - 興隆（こうりゅう）= rise and prosperity (of a nation or culture; grander, historical)
>     - 勃興（ぼっこう）= sudden rise (literary, of powers rising abruptly)
>
> ### Key Patterns
>
> **〜の台頭** — "the rise of ～"
>
> - 中国（ちゅうごく）経済（けいざい）の台頭 (the rise of the Chinese economy)
> - 新（あたら）しい価値観（かちかん）の台頭 (the emergence of new values)
>
> **台頭する** — "to rise / emerge"
>
> - 新（あたら）しいリーダーが台頭する (a new leader rises to prominence)
>
> ### Usage Note
>
> Mostly written or formal-spoken — you'll meet 台頭 in newspapers, business
> reports, and history texts far more than in casual conversation. In everyday
> speech, people are likelier to say 出（で）てくる or 人気（にんき）が出る. It
> carries a weighty, analytical tone.
>
> ### Example Contexts
>
> - 右派（うは）の台頭 (the rise of the right wing)
> - AIの台頭 (the rise of AI)
> - 新人（しんじん）の台頭 (the emergence of newcomers)
> - 地方（ちほう）都市（とし）の台頭 (the rise of regional cities)

</details>

<details open>
<summary>Example output for <strong>目を見張る</strong></summary>

> ## 目（め）を見張（みは）る
>
> - **Meaning:** to open one's eyes wide (in surprise or admiration), to be struck/amazed
> - **Kanji Breakdown:**
>     - **目**（め）= eye, as in 目的（もくてき "purpose"）
>         - *Parts:* pictograph of an eye（象形文字）; itself the "eye" radical, in 眼・眠・睡
>         - *Readings:* 音 モク／ボク ／ 訓 め・ま
>         - *Phonetic series:* — (pictograph, no phonetic component)
>     - **見**（み）る = to see, as in 見学（けんがく "observation visit"）
>         - *Parts:* 目 (eye) + 儿 (person)（会意文字 "person + eye → look"）; itself a radical in 視・親・観
>         - *Readings:* 音 ケン ／ 訓 み・る
>         - *Phonetic series:* — (ideographic, no phonetic component)
>     - **張**（は）る = to stretch/spread, as in 引（ひ）っ張る（ひっぱる "to pull"）
>         - *Parts:* 弓 (bow, radical) + 長 (phonetic)（形声文字）
>         - *Readings:* 音 チョウ ／ 訓 は・る
>         - *Phonetic series:* 長（チョウ）→ 帳（チョウ "notebook"）・脹（チョウ "swell"）
>     - Literally: "to stretch one's eyes (wide)"
> - **Type:** Idiom / Godan verb phrase (慣用句・五段動詞)
> - **Nuance:** A vivid, slightly literary idiom for eyes widening from astonishment
>   or admiration. Almost always positive or impressed — remarkable growth, dazzling
>   skill, breathtaking scenery. Stronger and more pictorial than simply 驚（おどろ）く.
> - **Example Sentences:**
>     - 彼女（かのじょ）の成長（せいちょう）には目を見張ることがある。
>         - *Her growth is, at times, truly remarkable.*
>     - 会場（かいじょう）の豪華（ごうか）さに思（おも）わず目を見張った。
>         - *I couldn't help widening my eyes at the splendor of the venue.*
>     - その技術（ぎじゅつ）の進歩（しんぽ）は目を見張るほどだ。
>         - *The advance of that technology is astonishing.*
> - **Related Words:**
>     - 驚（おどろ）く = to be surprised (general, neutral)
>     - 見（み）とれる = to gaze admiringly, be entranced (absorbed by beauty)
>     - 目を奪（うば）われる = to have one's eyes stolen → be captivated (by something dazzling)
>     - 舌（した）を巻（ま）く = to be lost in admiration (impressed by skill/ability)
>     - 息（いき）をのむ = to gasp, hold one's breath (struck by awe or shock)
>
> ### Key Patterns
>
> **目を見張るものがある** — "there is something remarkable about it"
>
> - 彼（かれ）の努力（どりょく）には目を見張るものがある (his effort is remarkable)
>
> **目を見張るほど** — "to an astonishing degree"
>
> - 目を見張るほど美（うつく）しい (stunningly beautiful)
>
> ### Usage Note
>
> Common in writing and in admiring or formal speech — reviews, reports, and
> speeches praising someone's progress. The set phrase 目を見張るものがある is
> especially frequent. In casual chat, people more often just say すごい or
> びっくりした.
>
> ### Example Contexts
>
> - 目を見張る進歩（しんぽ） (remarkable progress)
> - 目を見張る美（うつく）しさ (breathtaking beauty)
> - 目を見張る活躍（かつやく） (an impressive performance)
> - 目を見張る光景（こうけい） (an astonishing sight)

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
