# 📰 MAJMC Mock Test Website

A modern, bilingual mock test platform for **Master of Arts in Journalism & Mass Communication (MAJMC)** — Semester II, 2025–26.

🔗 **Live Site:** [https://YOUR-USERNAME.github.io/majmc-mock-test/](https://YOUR-USERNAME.github.io/majmc-mock-test/)

---

## 📚 Subjects Covered

| Subject | Course Code | Questions | Units |
|---|---|---|---|
| 📻 Radio Broadcasting | 01196003 | 50 | 5 |
| 💻 Information & Communication Technology | 01196004 | 50 | 5 |
| 🌐 Development & International Communication | — | 50 | 4 |
| 🏛️ Iconic Personalities of Media | 02196002 | 50 | 2 |

---

## ✨ Features

- **Tiered Scoring** — Easy = 1 mark, Moderate = 5 marks, Hard = 10 marks
- **Instant Feedback** — Green highlight for correct, red for incorrect answers
- **Countdown Timer** — Animated ring timer per question (30s / 45s / 60s / 90s / 2min or off)
- **Hindi / English Toggle** — Switch the entire interface and questions to Hindi or English
- **Smart Filters** — Filter by Unit, Difficulty level, and number of questions
- **Results Summary** — Score, accuracy, correct/incorrect/skipped breakdown
- **Wrong Answer Review** — See every missed question with the correct answer at the end
- **Retake Test** — Instantly reshuffle and retake with the same settings
- **Responsive Design** — Works on mobile, tablet, and desktop
- **Glassmorphism UI** — Deep navy palette with editorial typography

---

## 🚀 How to Use Locally

No installation needed. Just download `index.html` and open it in any browser.

```
Double-click index.html → Opens in browser → Start testing
```

---

## ➕ How to Add More Questions

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

---

## 🗂️ Project Structure

```
index.html   ← Entire app (HTML + CSS + JS + Question Bank in one file)
README.md    ← This file
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
