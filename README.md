🛰️ Amateur Radio Exam Practice App
Bilingual (EN/FR) • Basic + Advanced • Offline • Official ISED Exam Simulator

A powerful, standalone HTML application for practicing the Basic and Advanced Canadian Amateur Radio exams.
Runs entirely offline, loads the official ISED question banks, and simulates the real government exam experience — including category weighting, bilingual content, and pass/honours scoring.

⭐ Features
🇨🇦 Official ISED Exam Simulation

Supports Basic (100 questions)

Supports Advanced (50 questions)

Uses official category distributions exactly like the government exam

Generates a government-style score report with per-category analysis

🌐 English / French Bilingual Mode

Upload the official amat_basic_quest_delim.txt (or Advanced equivalent)

Toggle instantly between English and Français

All questions, answers, and explanations switch seamlessly

🤖 Automatic Exam Profile Detection

The app detects the bank type from BankQuestionID:

B-###-### → Basic Exam Profile

A-###-### → Advanced Exam Profile

UI automatically updates:

Profile indicator

Exam mode label (“100 questions” or “50 questions”)

Category definitions

Distribution rules

🎯 Three Training Modes

Random

No Repeats (cycle through all questions once)

Official Exam Mode

Basic: 100 questions weighted by category

Advanced: 50 questions weighted by category

Includes Pass / Pass with Honours evaluation

📊 End-of-Exam Results Report

Government-style report includes:

% per category

correct / # asked per category

Overall score

Pass / Pass with Honours

Exportable list of incorrect questions

📝 HTML-safe Explanations

Supports:

HTML tables

Code formatting

Math

Special characters (&nbsp;, &#39;, etc.)

🗂️ Supports Multiple File Formats
Format	Description	Use Case
ISED Delimited TXT	Official bilingual file	Basic & Advanced from government
Vertical CSV	One field per line	Fabien’s study bank format
Horizontal CSV	One question per row	Spreadsheet-style editing
🧠 Official Exam Category Structures
📘 BASIC (100 questions)
Category	Description	Questions
001	Regulations & Policies	25
002	Operating & Procedures	9
003	Station Assembly, Practice & Safety	21
004	Circuit Components	6
005	Basic Electronics & Theory	13
006	Feedlines & Antenna Systems	13
007	Radio Wave Propagation	8
008	Interference & Suppression	5
📕 ADVANCED (50 questions)
Category	Description	Questions
001	Advanced Theory	5
002	Advanced Components & Circuits	12
003	Measurements	6
004	Power Supplies	4
005	Transmitters, Modulation & Processing	9
006	Receivers	5
007	Feedlines, Matching & Antenna Systems	9
🚀 How to Use
1. Open the HTML file

Just double-click ham_quiz_APP.html — no installation required.

2. Load a question bank

Supported formats:

amat_basic_quest_delim.txt

amat_advanced_quest_delim.txt

CSV files (vertical or horizontal format)

3. Choose your language

English

Français

4. Select a mode

Random

No Repeats

Exam (official 100/50 question structure)

5. Click "Next Question" to begin studying
📥 Supported Question Bank Formats
ISED Official TXT Format (EN/FR)
question_id;question_en;correct_en;distr1_en;distr2_en;distr3_en;question_fr;correct_fr;distr1_fr;distr2_fr;distr3_fr

Vertical CSV Format
question
optionA
optionB
optionC
optionD
correctOption
explanation
BankQuestionID

Horizontal CSV Format
question,optionA,optionB,optionC,optionD,correctOption,explanation,BankQuestionID

📊 Exam Report Example (Basic or Advanced)
Categories                           Correct   Questions   Percentage
001 - Regulations & Policies         22        25          88%
002 - Operating & Procedures          8         9          88%
003 - Station Assembly               17        21          81%
...
Overall Score: 84%
PASS WITH HONOURS

📦 Recommended Repository Structure
/HAM-Exam-App
│── ham_quiz_APP.html
│── README.md
│── /question_banks
│     ├── amat_basic_quest_delim.txt
│     ├── amat_advanced_quest_delim.txt
│     ├── BankQuestionBasic.csv
│     └── BankQuestionAdvanced.csv
│── /examples
│     └── WrongQuestionsSample.csv

🛠️ Development Notes

No external libraries required

App runs in any modern browser

No data leaves your computer

Works offline for classroom or exam prep sessions

❤️ Credits

This project was developed collaboratively with the goal of helping Amateur Radio students study faster, more effectively, and with full compatibility with ISED Canada standards.

Happy studying & 73!
Fabien Clermont
fabien.clermont@gmail.com
