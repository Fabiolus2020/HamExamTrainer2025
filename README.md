# 📘 READ ME FIRST — Amateur Radio Exam Practice App
*A complete guide to using the HTML exam simulator*
*(Applies to the version included here: `ham_quiz_APP.html`)*

--------------------------------------------------------------------------------

## ⭐ Overview
This app is a **self-contained, offline amateur radio exam simulator** that runs entirely in your web browser.  
No installation, no server, no internet required once you have the HTML file.

It supports:

- **ISED Basic Question Bank**  
- **ISED Advanced Question Bank**  
- Your own custom training sets  
- Any CSV formatted according to the structure explained below  

You can practice in **random mode**, **no-repeat mode**, or the official **100-question Basic exam format** with category weighting identical to the Government of Canada’s online practice exam.

--------------------------------------------------------------------------------

## 🧩 1. How to Load a Question Bank

### Step 1 — Export your bank as CSV  
You can use:

- The official Basic exam question bank  
- The official Advanced exam question bank  
- Your own customized question collection  

Export the file as **CSV**.

### Step 2 — Load into the app  
Click **Choose File**, select the CSV, and the app will parse everything automatically.

If everything is valid, you will see:

- Total number of questions loaded  
- Quiz controls  
- Wrong-question counter  

--------------------------------------------------------------------------------

## 🔍 2. Supported CSV Formats

### **A) Vertical Format** (Fabien’s format)
A set of key/value rows per question:

question | text  
optionA | text  
optionB | text  
optionC | text  
optionD | text  
correctOption | A/B/C/D  
Explanation | text  
BankQuestionID | B-001-001-001  

### **B) Horizontal Format** (Official ISED format)

One row per question:

question,optionA,optionB,optionC,optionD,correctOption,explanation,BankQuestionID  

Both formats are fully supported.

--------------------------------------------------------------------------------

## 📚 3. Using Government of Canada Question Banks

The Government publishes:

- **Basic Question Bank** (~984 questions)  
- **Advanced Question Bank** (several hundred technical questions)

You may copy these into Excel, export as CSV, and load directly into this application.

--------------------------------------------------------------------------------

## 🧠 4. How Categories Work

Category comes from BankQuestionID:

- B-001 → Category 001  
- B-002 → Category 002  
- … etc.

Mapped to:

001 – Regulations and Policies  
002 – Operating and Procedures  
003 – Station Assembly, Practice and Safety  
004 – Circuit Components  
005 – Basic Electronics and Theory  
006 – Feedlines and Antenna Systems  
007 – Radio Wave Propagation  
008 – Interference and Suppression  

Used for:

- Exam selection  
- Category scoring  
- End-of-exam breakdown  

--------------------------------------------------------------------------------

## 📝 5. Exam Mode Question Distribution (Official)

The Basic exam uses:

Category | Questions  
---------|----------  
001 | 25  
002 | 9  
003 | 21  
004 | 6  
005 | 13  
006 | 13  
007 | 8  
008 | 5  

This app automatically selects **exactly these amounts** for each exam session.

--------------------------------------------------------------------------------

## 🧮 6. Quiz Modes

### 🎲 Random Mode  
Displays a random question (may repeat).

### 🔄 No-Repeat Mode  
Shows every question exactly once until the entire bank is exhausted.

### 📝 Exam Mode (100-question official format)  
- Uses official category weighting  
- Tracks score  
- Displays Pass / Pass with Honours  
- Shows full category analysis  

--------------------------------------------------------------------------------

## 🧾 7. Explanation Rendering

Explanations support:

- HTML tags  
- Tables  
- Line breaks  
- Bold/italic  
- HTML entities  

Because the app uses `innerHTML`, complex formatting will display correctly.

--------------------------------------------------------------------------------

## 🚫 8. Wrong Answer Tracking & Export

Every unique wrong question is stored once.

You may:

- Review wrong questions  
- Export them as CSV  
- Reload as a custom study set  

--------------------------------------------------------------------------------

## 📊 9. End-of-Exam Category Breakdown

At the end of Exam Mode, the summary includes:

- Correct answers  
- Total questions per category  
- Percentage  
- Official-style format  

--------------------------------------------------------------------------------

## 💾 10. Fully Offline

No processing is done online.  
Everything runs in your browser for complete privacy.

--------------------------------------------------------------------------------

## 🏗️ 11. Extensible Design

Any CSV with:

- question  
- optionA–optionD  
- correctOption  
- explanation (optional)  
- BankQuestionID (optional but recommended)

…will load correctly.

Supports **Basic**, **Advanced**, or custom question banks.

--------------------------------------------------------------------------------

## 🏁 12. Recommended Folder Layout

/YourStudyFolder  
  |-- ham_quiz_exam_mode.html  
  |-- README_FIRST.txt  
  |-- Basic_QuestionBank.csv  
  |-- Advanced_QuestionBank.csv  
  |-- Custom_Set.csv  
  |-- WrongQuestions_YYYYMMDD.csv  

--------------------------------------------------------------------------------

## 💙 Final Note

This tool was built to make studying faster, clearer, and more enjoyable.  
Load any question bank, customize your study path, and track progress like the real exam system.

If the Government updates their question set, simply export a new CSV and load it — no code changes needed.

Happy studying & 73!
Fabien Clermont
fabien.clermont@gmail.com
