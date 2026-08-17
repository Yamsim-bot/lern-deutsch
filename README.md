# 🇩🇪 LernDeutsch — Learn German

A complete, offline-capable German learning website covering **Basic (A1–A2)**, **Intermediate (B1–B2)** and **Advanced (C1–C2)**.

**Live:** https://lernen-deutschdaily.duckdns.org/

## Features

- 📚 **22 grammar lessons** — alphabet & pronunciation, noun gender, cases, tenses, modal verbs, passive, Konjunktiv I & II, nominal style, idioms & false friends
- 🗂 **114 flashcards** with one-tap flip, shuffle, and 🔊 **German pronunciation** (browser text-to-speech, de-DE)
- ✍️ **36 quiz questions** with instant feedback and explanations, per-level best scores
- 📊 **Progress tracking** — lesson completion, quiz scores, day streak (saved in `localStorage`)
- 🔌 **Zero dependencies, works fully offline** — a single HTML file, no server needed

## How to run

Just open `index.html` in any browser. That's it.

To serve it locally:

```bash
cd lern-deutsch
python -m http.server 8080
# then open http://localhost:8080
```

## Project structure

```
lern-deutsch/
├── index.html   # the entire app (HTML + CSS + JS + content)
└── README.md
```

Everything — lessons, vocabulary, quizzes, styling and logic — lives in `index.html`. Content is data-driven: the `LEVELS` object at the top of the script defines `lessons`, `vocab` and `quiz` arrays, so adding new material is just editing that object.

## Session windows (for reference)

The site's lessons reference standard trading/learning-friendly session windows — irrelevant to learning German, but kept consistent with the project docs. 😄

## Tech notes

- Vanilla HTML/CSS/JS — no frameworks, no build step, no external requests
- Pronunciation via the Web Speech API (`speechSynthesis`, `lang="de-DE"`)
- Progress persisted with `localStorage`

## Roadmap ideas

- Spaced-repetition review mode
- Listening / dictation exercises
- More lessons per level and per-topic quizzes
