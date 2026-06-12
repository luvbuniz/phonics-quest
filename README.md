# 🦊 Pip's Phonics Forest

A polished, single-file phonics learning game for early readers (ages 6–8, reading levels K–2), with IXL-style adaptive mastery. Everything — game logic, adaptive engine, and all artwork (hand-drawn inline SVG) — lives in one `index.html` with no build step and no dependencies beyond an optional Google Fonts link and the browser's built-in Web Speech API.

**Play it:** just open `index.html` in any modern browser. Works great on tablets.

## What's inside

- **A real phonics scope & sequence**, five skills in research-backed order: short vowels & CVC words → consonant digraphs (sh, ch, th, wh) → consonant blends (st, bl, gr, tr…) → long vowels & silent-e → vowel teams (ai, ee, oa, igh). Every word in a level is decodable using only skills taught at or before that level.
- **Four rotating question types:** listen-and-find, "tap the word that starts/ends with this sound," fill-in-the-missing-letter (sound→letter mapping), and rhyme matching.
- **IXL-style adaptive SmartScore (0–100, mastery at 90).** Streaks raise an invisible difficulty tier — closer distractors, four choices, less picture support. Stumbles lower it again and trigger gentle scaffolds: the sound replays and the target letters light up. Misses cost little; wrong answers are reframed as "let's try that sound again."
- **Audio-first.** Every prompt, sound, and word is read aloud via the Web Speech API with a replay button on every question — early readers can't rely on written instructions. Degrades gracefully (with a visual notice) if speech is unavailable.
- **Pip the Fox**, a hand-drawn SVG mascot who breathes, blinks, cheers on correct answers, and gives an encouraging shrug on misses.
- **A living forest world:** winding journey map with stepping-stones that bloom and earn stars when mastered, layered parallax hills, drifting clouds, falling leaves, confetti celebrations.
- **A toggleable grown-ups' dashboard** (score, questions attempted, accuracy, and mastery per skill) kept out of the kid-facing flow.
- **Anti-frustration by design:** no timers, no dead ends, no punishment — plus big tap targets, high contrast, visible focus states, and no color-only feedback.

> **Note:** progress is intentionally kept in memory only (no localStorage), so it resets on refresh.

## Host it on GitHub Pages

1. Push this repo to GitHub.
2. In the repo: **Settings → Pages → Source: Deploy from a branch → `main` / root → Save.**
3. Your game is live at `https://<your-username>.github.io/<repo-name>/` in about a minute.

## Designer's note

Pip's Phonics Forest grounds its five levels in a systematic synthetic-phonics scope and sequence — short-vowel CVC words through digraphs, blends, silent-e, and vowel teams — so children only ever decode patterns they've been taught, and every question is delivered audio-first because the target player can't yet read instructions. The adaptive engine mirrors IXL's SmartScore: a visible mastery score climbs quickly early and slows near the 90-point mastery bar, while a hidden difficulty tier rises with streaks (closer distractors, less picture support) and eases back after stumbles. Errors are treated as information rather than failure — a first miss replays the sound and highlights the target grapheme for a second try, and a second miss earns a warm reveal and forward momentum, never a penalty. The result is a practice loop that meets each child exactly where they are while keeping the emotional tone of a storybook rather than a worksheet.
