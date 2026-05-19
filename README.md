# 📰 MAJMC Mock Test Website

A modern, bilingual mock test platform for **Master of Arts in Journalism & Mass Communication (MAJMC)** — Semester II, 2025–26.

🔗 **Live Site:** [https://niksheydhiman-musician.github.io/majmc_mock_test/](https://niksheydhiman-musician.github.io/majmc_mock_test/)

---

## 📚 Subjects Covered

| Subject | Course Code | Questions | Units |
|---|---|---|---|
| 📻 Radio Broadcasting | 01196003 | 250 | 5 |
| 💻 Information & Communication Technology | 01196004 | 250 | 5 |
| 🌐 Development & International Communication | — | 250 | 5 |
| 🏛️ Iconic Personalities of Media | 02196002 | 250 | 2 |

---

## ✨ Features

- **Tiered Scoring** — Easy = 1 mark, Moderate = 5 marks, Hard = 10 marks
- **Instant Feedback** — Green highlight for correct, red for incorrect answers
- **Countdown Timer** — Animated ring timer per question (30s / 45s / 60s / 90s / 2min or off)
- **Hindi / English Toggle** — Switch the entire interface and questions to Hindi or English
- **Smart Filters** — Filter by Unit, Difficulty level, and number of questions
- **Subject-wise Full Bank Loading** — “All Questions” loads the complete JSON bank for the selected subject only
- **Results Summary** — Score, accuracy, correct/incorrect/skipped breakdown
- **Wrong Answer Review** — See every missed question with the correct answer at the end
- **Retake Test** — Instantly reshuffle and retake with the same settings
- **Responsive Design** — Works on mobile, tablet, and desktop
- **Glassmorphism UI** — Deep navy palette with editorial typography

---

## 🧾 About the Website

This website is a browser-based MAJMC mock test platform for Semester II students. It combines subject-wise question banks, bilingual UI support, timer-based practice, tiered scoring, wrong-answer review, and local progress tracking in one static site.

You can:

- choose a subject and start practicing instantly
- filter by unit, difficulty, and number of questions
- use **All Questions** to load the complete JSON bank for the selected subject
- review your performance immediately after every test
- track progress locally in the browser without signing in

The site is built with HTML, Tailwind CSS via CDN, and vanilla JavaScript, with separate JSON files for the full subject banks.

---

## 🚀 How to Use Locally

No installation is required for the main interface. Open `index.html` in any browser.

> Note: the **All Questions** option reads the subject JSON files, so serving the folder through a simple local web server is recommended for full subject-bank loading.

```
python3 -m http.server 8000
# then open http://localhost:8000/
```

---

## ➕ How to Add More Questions

There are now two question sources:

1. The quick in-page question bank inside `index.html`
2. The complete subject JSON banks used by the **All Questions** option

### Update the in-page bank

Open `index.html` in any text editor, find the `questionBank` object inside the `<script>` tag, and add to the relevant subject array:

```javascript
{
  q: "Your question text?",
  opts: ["Option A", "Option B", "Option C", "Option D"],
  ans: 1,           // 0=A, 1=B, 2=C, 3=D  ← index of correct answer
  diff: "easy",     // "easy" | "moderate" | "hard"
  unit: "Unit 2",   // must match the existing unit name
  qHi: "हिंदी में प्रश्न?",              // optional Hindi translation
  optsHi: ["A", "B", "C", "D"]          // optional Hindi options
}
```

**Scoring is automatic** — `easy` gives 1 mark, `moderate` gives 5, `hard` gives 10.

### Update the full subject banks

Edit the relevant JSON file:

- `radio.json`
- `information_communication_technology.json`
- `dev_international_comm.json`
- `iconic_personalities.json`

These JSON files are normalized by the website and used when the user selects **All Questions** for a subject.

---

## 🗂️ Project Structure

```
index.html                                ← Entire app UI, logic, and quick question bank
radio.json                                ← Full Radio question bank
information_communication_technology.json ← Full ICT question bank
dev_international_comm.json               ← Full Development & International Communication bank
iconic_personalities.json                 ← Full Iconic Personalities bank
README.md                                 ← This file
```

---

## 🛠️ Built With

- HTML5
- Tailwind CSS (via CDN)
- Vanilla JavaScript
- Google Fonts — Playfair Display, DM Sans, JetBrains Mono

---

## 👩‍🎓 Academic Details

- **Program:** MA Journalism & Mass Communication (MAJMC)
- **Semester:** II
- **Session:** 2025–26
- **Department:** Journalism & Mass Communication

---

## 📄 License

This project is for personal academic use. Question content belongs to the respective faculty members.
