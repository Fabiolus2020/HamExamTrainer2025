📘 README_FIRST — Amateur Radio Exam Practice App

A complete guide to the bilingual Basic & Advanced ISED exam simulator
(Updated for the latest version of ham_quiz_APP.html)


README_FIRST

⭐ Overview

This HTML application is a fully offline, bilingual Amateur Radio exam simulator for:

Basic Qualification

Basic + Honours

Advanced Qualification

It automatically detects whether you upload a Basic or Advanced question bank and adjusts:

Category names

Exam mode question counts

Category distribution

Pass/Pass with Honours thresholds

Test report structure

It requires no installation, no server, and runs 100% inside your browser.

🚀 NEW FEATURES (2025 UPDATE)
✅ Automatic Basic vs Advanced Profile Detection

The app detects the exam type based on the BankQuestionID:

B-xxx → Basic exam profile

A-xxx → Advanced exam profile

Once detected, the UI displays:

Profile: Basic (official structure: 100 questions)
or
Profile: Advanced (official structure: 50 questions)

✅ Official Exam Mode for Both Basic & Advanced

When using Exam mode, the app now uses the exact question distribution used by the Government of Canada.

BASIC — 100-question distribution
Category	Questions
001 – Regulations and Policies	25
002 – Operating and Procedures	9
003 – Station Assembly, Practice & Safety	21
004 – Circuit Components	6
005 – Basic Electronics & Theory	13
006 – Feedlines & Antenna Systems	13
007 – Radio Wave Propagation	8
008 – Interference & Suppression	5
ADVANCED — 50-question distribution
Category	Questions
001 – Advanced Theory	5
002 – Advanced Components & Circuits	12
003 – Measurements	6
004 – Power Supplies	4
005 – Transmitters, Modulation & Processing	9
006 – Receivers	5
007 – Feedlines, Matching & Antenna Systems	9

Exam mode automatically adjusts based on the detected profile.

✅ Dynamic Exam Mode Label

The Exam mode button now shows:

Exam (official structure: 100 questions)

Exam (official structure: 50 questions)

depending on which bank is loaded.

✅ English/French Language Toggle

For official bilingual files (amat_basic_quest_delim.txt):

Question text

Answer choices

Explanations

…all switch between EN ↔ FR instantly.

✅ HTML-safe Explanation Rendering

Explanations can include:

HTML tables

Bold/italic

Code blocks

Math

Special characters (&nbsp;, &#39;, etc.)

The app uses innerHTML, so formatting displays exactly as intended.

✅ Correct Answer Highlighting Fixed

Selected wrong answers highlight in red, correct ones in green, matching the earlier behaviour.

✅ Correct “Pass / Pass with Honours” Display

After completing an exam:

≥ 80% → Pass with Honours

70–79% → Pass

<70% → Fail

This matches ISED scoring rules.

✅ End-of-Exam Category Breakdown Report

At the end of Exam mode, the app generates a government-style category report:

Correct answers per category

Total questions in that category

Percentage per category

Overall score

Pass status

Wrong question list export

Works for both Basic and Advanced.

📁 FILE FORMATS SUPPORTED
✔ 1. Official ISED bilingual delimited format

The app now reads the original government TXT file:

question_id;question_en;correct_en;distr1_en;distr2_en;distr3_en;question_fr;correct_fr;distr1_fr;distr2_fr;distr3_fr


No CSV conversion required.

✔ 2. Vertical CSV (Fabien’s format)
question
optionA
optionB
optionC
optionD
correctOption
explanation
BankQuestionID


Supports multiline explanations.

✔ 3. Horizontal CSV (1 row per question)
question,optionA,optionB,optionC,optionD,correctOption,explanation,BankQuestionID

🧠 CATEGORY SYSTEM

Categories are determined through BankQuestionID, e.g.:

B-001-003-004 → Basic Category 001

A-004-005-002 → Advanced Category 004

These values drive:

Exam mode distribution

End-of-exam reports

Profile selection

🎮 QUIZ MODES
1. Random

Questions chosen randomly (may repeat).

2. No Repeats

Cycles through every question exactly once.

3. Official Exam Mode

Basic → 100 questions
Advanced → 50 questions

Uses official ISED category weighting and produces a government-style report.

🧾 WRONG QUESTION TRACKING & EXPORT

The app keeps a unique set of wrong questions and allows exporting them as CSV for focused study.

📥 HOW TO USE THE APP
Step 1 — Load a question file

Supports TXT (ISED) and CSV.

Step 2 — Select language (EN/FR)

Only shown if a bilingual bank is loaded.

Step 3 — Choose quiz mode

Random

No repeat

Exam (official mode)

Step 4 — Start quiz

Click Next Question.

🔧 HOW THE DATABASE WORKS

The app reads TXT/CSV line by line.

Each question becomes a standardized internal object.

If using ISED TXT:

English & French text is stored in parallel.

If using CSV:

Explanations are HTML-ready.

Category IDs from BankQuestionID determine exam distribution structure.

🏁 RECOMMENDED FILE STRUCTURE FOR GITHUB
/HAM-Exam-App
│── ham_quiz_APP.html
│── README_FIRST.txt
│── /question_banks
│     ├── amat_basic_quest_delim.txt
│     ├── amat_advanced_quest_delim.txt
│     ├── BankQuestionBasic.csv
│     └── BankQuestionAdvanced.csv
│── /examples
│     └── WrongQuestionsSample.csv

💬 FINAL NOTE

This application now replicates the official ISED Basic and Advanced exam engines, works offline, supports bilingual content, and is flexible enough for any custom training bank.

You can now study:

Faster

Smarter

With the same structure used by ISED

In English or French

With complete progress tracking

This tool was built to make studying faster, clearer, and more enjoyable.  
Load any question bank, customize your study path, and track progress like the real exam system.

If the Government updates their question set, simply export a new CSV and load it — no code changes needed.

Happy studying & 73!
Fabien Clermont
fabien.clermont@gmail.com
