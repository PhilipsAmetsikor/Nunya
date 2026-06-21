# Nunya — Mathematics in Twi, Gã, Eʋe & English

An interactive, open-source tool for learning the basics of mathematics in **Twi (Akan)**, **Gã** and **Eʋe (Ewe)**, with **English shown alongside** every concept. It is built for learners with limited English fluency: you meet each idea first in a language you already think in, and the English grows beside it.

> **Nunya** is the Eʋe word for *knowledge / wisdom*.

It is a single HTML file — no build step, no server, no dependencies — so it runs anywhere and is easy to host for free on GitHub Pages.

---

## Why it works this way

The goal is **concept first, language bridge second**. For each topic the learner sees:

1. a short explanation in **their language** (Twi, Gã or Eʋe), highlighted in gold;
2. the **same idea in simple English**, beside it;
3. a **hands-on activity** using everyday objects (cowrie shells, shared bread), with feedback in all three languages.

By the time someone has counted shells, added groups, and shared a whole, the English words for those ideas are no longer abstract — they are attached to something the learner has already done and understood in their own language.

---

## What's inside

- **Numbers (1–10)** — a tap-to-count tray that shows the number, the word in your language, and the English word together.
- **Addition (+)** — putting groups together, with a visual and practice questions.
- **Subtraction (−)** — taking away, shown with shells crossed out.
- **Multiplication (×)** — equal groups (“3 groups of 2”).
- **Division (÷)** — sharing equally into baskets.
- **Fractions (½)** — cut a whole into parts and tap the parts you take.
- **Number words** — a quick reference: tap any number to see it in Twi, Gã, and English.
- A **language switch** (Twi / Gã / Eʋe) that updates every explanation, heading, and label live — and **remembers your choice** for next time.
- **Bilingual section headings** and a short **how-to-use hint**, so the whole screen stays in the learner's language.
- Works on phones, keyboard-navigable, and respects reduced-motion preferences.

---

## ⚠️ Help wanted: translation review

**The Twi, Gã and Eʋe text in this project is a best-effort first draft and has not yet been checked by native speakers.** Some wording is likely to be unnatural or wrong. Please do not treat it as authoritative until it has been reviewed.

**This is the single most valuable way to contribute.** All language content lives in one place, so corrections are quick:

1. Open `index.html`.
2. Find the block near the top of the `<script>` marked **`CONTENT — EDIT TRANSLATIONS HERE`**.
3. Edit the `twi:`, `ga:` and `ewe:` values in:
   - `NUMBERS` — the number words 1–10
   - `FEEDBACK` — “Correct!” / “Try again”
   - `UI` — button labels (Add, Remove, Check, etc.)
   - `TOPICS` — each topic's title and explanation
4. When a topic's text has been verified, set its `review:` flag to `false` to remove the orange “needs review” badge.

No programming knowledge is needed beyond editing the text between the quotation marks.

> **Note on dialects:** Twi here is intended as **Asante Twi**. Twi, Gã and Eʋe all have spelling and dialect variation — if you adjust conventions, please keep them consistent across the file and mention your choice in your pull request.

### A note on using Google Translate

Google Translate now supports Twi, Gã and Eʋe, so it is a handy **cross-check** while reviewing the text. Two cautions, though: machine translation is still weak for these languages and can produce unnatural or wrong wording, and it is poor at short maths phrasing (for example “3 groups of 2”). Treat it as a starting hint, and let a **fluent speaker have the final say** — especially for the explanations.

### Adding another language

The app is built so a new language is a small, repeatable edit. In `index.html`:

1. Add an entry to the `LANGS` list (its `id`, button label, and an accent colour name).
2. Add a matching key (e.g. `ewe:`) to every entry in `NUMBERS`, `FEEDBACK`, `UI`, and each topic's `title` and `ex`.

The language button, the live switch, and the number-words table all pick it up automatically.

---

## Run it locally

No installation needed. Either:

- **Double-click `index.html`** to open it in any browser, or
- serve the folder (useful while editing):

  ```bash
  # Python 3
  python3 -m http.server 8000
  # then open http://localhost:8000
  ```

---

## Publish it free on GitHub Pages

1. Create a new repository on GitHub and push these files to it:

   ```bash
   git init
   git add index.html README.md
   git commit -m "Nunya: math in Twi, Ga, Ewe & English"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
   git push -u origin main
   ```

2. On GitHub: **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Select branch **`main`** and folder **`/ (root)`**, then **Save**.
5. After a minute your app is live at:

   ```
   https://YOUR-USERNAME.github.io/YOUR-REPO/
   ```

(Replace `YOUR-USERNAME` and `YOUR-REPO`.)

---

## Contributing

Contributions are welcome — especially from Twi and Gã speakers and teachers.

- **Fix or improve translations** (see the section above).
- **Add a topic** — copy an existing entry in the `TOPICS` array and adjust it.
- **Report problems** by opening an issue describing what looked wrong and which language.

Please keep the project a single self-contained `index.html` so it stays easy to host and edit.

---

## License

No license is included yet. Until you add one, others have limited rights to reuse the work. A common choice for an open educational project is the **MIT License** (very permissive). To use it, create a file named `LICENSE` with the MIT text and your name and year, and add a line here pointing to it.

---

## Credits

Created by **Seyram** to help Ghanaian learners meet mathematics in their own languages. Built to be copied, corrected, and carried forward by the community it serves.
