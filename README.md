# 📡 HAM Exam Trainer (Canada) — Bilingual Study App

A free, offline-ready HTML tool to help you practice for the **Canadian Amateur Radio Basic and Advanced exams*.

- 🇨🇦 Based on the official ISED question banks
- 🇬🇧🇫🇷 Fully bilingual interface (English & French)
- 📱 Mobile-friendly (desktop + dedicated mobile layout)
- 🧠 Multiple study modes, including official exam structures
- 🧾 Optional CSV question bank with explanations and memory tricks
- 💾 Auto-saves your session (local only, in your browser)

Created by **Fabien Clermont**.  
Licensed under **CC BY-NC-SA 4.0** (non-commercial, attribution, share-alike).
:contentReference[oaicite:0]{index=0}

---

## ✨ Main Features

### 📚 Supports Both Official ISED Question Banks

The app can load the **official delimited TXT files** published by ISED:

- `amat_basic_quest_delim2025.txt` (Basic)
- `amat_adv_quest_delim2025.txt` (Advanced)

You can either:

- Load them **directly from GitHub** using the built-in buttons  
  *(Requires internet to load from GitHub)*, or  
- Download them yourself and use **“Choose a file (local)”** to load a local copy.  
  *(Use this option to load a local file.)*

When an official bank is loaded, the app:

- Follows the **real exam category distributions**:
  - Basic: 100 questions (8 categories, fixed counts)
  - Advanced: 50 questions (7 categories, fixed counts)
- Displays **per-category statistics**, **weak-area detection**, and a **category heatmap**:
  - Strong categories: shown in a “good” colour
  - Weak categories: highlighted when results fall below the target threshold

> 🔎 The official ISED banks are *questions + answers only* — no explanations.

---

## 🧾 Optional CSV Question Bank (With Explanations & IDs)

In addition to the official TXT banks, the app supports a **custom CSV format** so that *you* can add:

- Detailed **explanations** for each question  
- **Memory tricks** and learning tips  
- HTML-safe formatted text (for use inside the app)  
- A **BankQuestionID** that matches the official ISED question ID

A sample CSV is provided in the repository, for example:

- `BankQuestionJuly2025.csv`

Typical workflow:

1. Download the CSV from GitHub.
2. Open it in Excel, Google Sheets, or LibreOffice.
3. Edit or add explanations, memory tricks, or improved wording.
4. Save as CSV and load it using **“Choose a file (local)”** in the app.

When a compatible CSV is loaded:

- The app displays an **Explanation** section after you press **“Check Answer”**.
- The explanation is taken from the `explanation` column of the CSV.
- The **BankQuestionID** (from `BankQuestionID`) is shown above the question, so students can map the question directly to the official bank.

> 💡 Notes  
> - The official government TXT banks do **not** include explanations.  
> - The CSV explanation bank is a **user-created enhancement**. You are encouraged to customize your own CSV for personal study.

### 📁 Recommended CSV Structure

Recommended columns:

- `BankQuestionID` — Official ID for the question (e.g. `B-001-001-002`)  
- `question` — Question text  
- `optionA`, `optionB`, `optionC`, `optionD` — Answer choices  
- `correctOption` — Correct answer label (`A`, `B`, `C`, or `D`)  
- `explanation` — HTML-safe explanation text (shown after “Check Answer”)  

The app is flexible, but following this structure gives the best experience.

---

## 🧪 Study & Exam Modes

The app supports several modes to match different study styles.

### 🎯 Exam Mode (Official Structure)

- **Basic:** 100 questions chosen to match the official category distribution.
- **Advanced:** 50 questions chosen to match the official category distribution.

Exam mode shows:

- Final score and percentage
- **Pass / Fail / Pass with Honours** (≥ 80%)
- Category breakdown (e.g. Regulations, Operating, Electronics…)
- **Weak-area detection** (flags categories under a threshold, e.g. 70%)
- Category heatmap (visual overview of strong vs weak areas)
- “**Practice only this category**” buttons
- “**Retake only wrong questions**” button

### 🔄 Random Mode

- Picks random questions from the loaded bank.
- Good for quick mixed practice.

### ♻️ No-repeat Mode

- Goes through all questions **without repeats** until the set is exhausted.
- Ideal for full-bank coverage.

### 🧩 Category Training (By Topic)

- Lets you focus on one or more specific categories (e.g. only “Propagation”, only “Antennas”).
- Great for targeting known weak areas.

### 🔁 Retake Wrong Questions

- After an exam, you can start a session that contains **only the questions you answered incorrectly**.
- Perfect for focused error correction.

### 🧠 Smart Difficulty Mode (Adaptive Learning)

- A special mode that **adapts difficulty over time** based on your performance:
  - If you do well, the app gradually serves questions from more challenging categories.
  - If you struggle, the app prioritizes weaker categories or recently missed questions.
- Designed to keep you in the ideal learning zone instead of always randomizing blindly.

### 🔍 Exam Review Mode

- After completing an exam, you can enter **review mode**:
  - Step through all exam questions again (in order).
  - See which option you chose and which was correct.
  - Read explanations (if using a CSV bank).
- Useful for detailed post-exam analysis.

---

## 📊 Progress, Stats & Heatmap

Throughout use, the app tracks:

- Total questions answered
- Correct answers
- Current percentage

In exam mode, the final summary includes:

- Overall percentage and result (Pass / Fail / Honours)
- Per-category statistics
- Highlighted weak categories
- **Category heatmap** summarizing performance visually

A **mode badge** above the progress bar shows the current mode (Exam, Random, Smart Difficulty, etc.), so you always know what the app is doing.

---

## 🌐 Bilingual Interface & Smart Language Switching

From **Step 1**, you can choose:

- 🇬🇧 **English**
- 🇫🇷 **Français**

The app includes:

- Full bilingual UI (labels, buttons, messages, steps)
- Bilingual category names and report headings
- Bilingual Pass / Fail / Honours labels
- Bilingual About / Support content
- Bilingual license notice & footer

You can switch language **at any time**:

- The app updates visible labels immediately.
- Wherever possible, texts that depend on UI language (messages, mode labels, badges) are updated dynamically using **smart bilingual switching**.

*(Note: Question content itself comes from the official TXT/CSV file, so that text stays exactly as stored in the file.)*

---

## 🌓 Theme, Layout & Mobile Optimizations

The app includes several UI / UX features:

### 🎨 Theme & Display

- **Dark mode** toggle.
- **Theme colour selector** (accent colour).
- **Fullscreen toggle** to maximize study space in supporting browsers.
- Clear **mode badges** and labels to show:
  - Current mode (Exam / Random / Category / Smart Difficulty / Review / etc.)
  - Current language  
  - Question / exam progress

### 📱 Mobile Mode & Orientation

- A dedicated **mobile layout** optimized for phones.
- **Auto-detects mobile orientation** and adjusts layout for better use in portrait vs landscape.
- Mobile reset behaviour:
  - **Reset** not only clears the app state, but scrolls back to the top and returns you to the initial step on mobile, to mirror the desktop UX as closely as possible.

---

## 💾 Auto-save Session (Local Only)

The app uses local browser storage (e.g., `localStorage`) to **auto-save session data**, such as:

- Selected language
- Current mode
- Current question index and score
- Recently answered / wrong questions  
- Basic UI preferences (e.g. dark mode, mobile layout)

If you close and reopen the page in the same browser, the app can resume where you left off.

You can use the **Reset** button at any time to:

- Clear the current session state, and
- Return to Step 1 (language and load bank).

*(Auto-save is strictly local to your device and browser — nothing is sent to any server.)*

---

## 🧭 Basic Usage (Step-by-Step)

1. **Choose language (EN/FR).**  
2. **Load a question bank:**
   - Official Basic / Advanced from GitHub *(requires internet)*, or
   - TXT / CSV local file via **“Choose a file (local)”**.
3. **Pick a mode:**
   - Random / No Repeats / Exam / Category Training / Smart Difficulty / Exam Review.
4. **Start the session:**
   - Click **“Next Question”** to get a question.
   - Select an answer and click **“Check Answer”** to see if you are correct.
5. **Use explanations (if available):**
   - If using a CSV with explanations, read the **Explanation** block that appears after checking the answer.
6. **Review & improve:**
   - Use “Retake wrong questions” and category training to focus on weak areas.
   - Use the category heatmap and per-category stats to guide your study.

At any time, click **Reset** to clear the current session and restart from Step 1.

---

## 💬 About, Support & Issues

This free bilingual HAM Exam Trainer was created to help students prepare using real-style questions, official exam structures, and detailed statistics.

- License: **CC BY-NC-SA 4.0** (non-commercial, attribution, share-alike)
- Free for personal and educational use
- Not to be resold or bundled into paid products/services

If this app helps you and you’d like to support future improvements:

- ☕ Buy Me a Coffee: https://buymeacoffee.com/fabiolus  
- 💻 GitHub: https://github.com/Fabiolus2020/HamExamTrainer2025  

To report a bug, suggestion, or typo:

- Use the **“Report an issue”** link in the app (Support section/footer), which opens the GitHub issues page with useful context, or  
- Open an issue manually on the GitHub repository.

---

## 📜 License (Summary)

This project is licensed under:

**Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)**

You are free to:

- **Share** — copy and redistribute the material in any medium or format  
- **Adapt** — remix, transform, and build upon the material  

Under the following terms:

- **Attribution** — Credit **Fabien Clermont**, provide a link to the license, and indicate if changes were made.  
- **NonCommercial** — You may **not** use the material for commercial purposes.  
- **ShareAlike** — If you remix, transform, or build upon the material, you must distribute your contributions under the **same license**.

Full legal text: https://creativecommons.org/licenses/by-nc-sa/4.0/
