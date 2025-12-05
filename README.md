📡 HAM Exam Trainer (Canada) — Bilingual Study App

A free, offline-ready exam practice tool for Basic & Advanced Amateur Radio certification.

## Overview

This HTML-based HAM Exam Trainer is designed for Canadian amateur radio students preparing for the ISED Basic or Advanced certification exams.  
It supports:

- English and French (bilingual UI)
- Official ISED exam structures
  - Basic (100-question official distribution)
  - Advanced (50-question official distribution)
- Official TXT-delimited question banks (Basic & Advanced)
- Optional CSV explanations file (BankQuestionJuly2025.csv) available via a dedicated download button
- Mobile-friendly interface
- Dark mode
- Category performance statistics
- Weak areas detection
- “Retake Wrong Questions” mode
- Category Training mode
- Random / No-repeat / Exam modes
- Full offline usage (no backend server required)

The app is 100% self-contained in a single `.html` file that you open in your web browser.

---

## 🚀 Features

### 🔤 Bilingual Interface (EN/FR)

- Choose your preferred language at **Step 1**.  
- All interface text, buttons, labels, and the Support/About section automatically switch between English and French.

### 📂 Load Official ISED Question Banks

- Supports the **official TXT-delimited format**:

  ```text
  question_id;question_en;optionA_en;...;question_fr;optionA_fr;...
  ```

- Works for both:
  - Official **Basic** exam question bank  
  - Official **Advanced** exam question bank

- You can load banks in two ways:
  - Using the built-in **“Load official Basic/Advanced bank (from GitHub)”** buttons
  - Or by selecting a **local TXT/CSV file** from your computer

### 📑 Download Explanation CSV (from GitHub)

- A dedicated button in **Step 2** lets users download the explanations CSV directly from GitHub:

  - File: `BankQuestions/BankQuestionJuly2025.csv`
  - Purpose: provide detailed explanations and memory tricks for many questions
  - This CSV is **optional** and meant as a companion reference; the app still works fully from the official TXT banks

- The button label is fully bilingual:
  - EN: **“Download explanation CSV (from GitHub)”**
  - FR: **« Télécharger le CSV d’explications (depuis GitHub) »**

### 🎯 Official Exam Simulation

**Exam mode** automatically selects questions according to the Government of Canada’s official category distribution.

#### Basic Exam (100 questions)

- 25 – Regulations & Policies  
- 9 – Operating & Procedures  
- 21 – Station Assembly & Safety  
- 6 – Circuit Components  
- 13 – Basic Electronics  
- 13 – Antennas & Feedlines  
- 8 – Propagation  
- 5 – Interference & Suppression  

#### Advanced Exam (50 questions)

- 5 – Advanced Theory  
- 12 – Components & Circuits  
- 6 – Measurements  
- 4 – Power Supplies  
- 9 – Transmitters & Modulation  
- 5 – Receivers  
- 9 – Antennas & Feedlines  

### 🧠 Category Training Mode

- Practice only the topics you choose (e.g., only Regulations, only Propagation, only Antennas).  
- Very useful to focus on weak areas or specific sections of the syllabus.

### 🔁 Retake Wrong Questions Mode

After completing an exam:

- The app tracks which questions you answered incorrectly.
- You can start a new session that contains **only your wrong questions**, to reinforce learning efficiently.

### 🧮 Real-time Stats & Weak Area Detection

- Correct % per category
- Questions asked vs. answered
- Highlighted **weak areas** (< 70%)
- Category-wise distribution in the final report

### 🌓 Dark Mode + 📱 Mobile Mode

- Toggle **Dark Mode** to reduce eye strain.
- Toggle **Mobile Mode** to optimize the layout for smaller screens.
- The app remains fully usable on desktops, tablets, and phones.

### ☕ Donate Button (Support / About)

The app includes a bilingual **“About & Support”** card with a **Buy Me a Coffee** link:

➡️ https://buymeacoffee.com/fabiolus

This lets grateful users support ongoing work on the trainer while keeping it free for everyone.

---

## 🖥 How to Use (English)

### 1. Open the HTML file

- Download the latest `index.html` (or app HTML file) from the repository.  
- Open it in your browser (double-click or drag into a tab).

### 2. Choose Language

- At **Step 1**, select **English** or **Français**.  
- The entire UI switches to your chosen language.

### 3. Load a Question Bank

At **Step 2**, you have three options:

1. **Load official Basic bank (from GitHub)**  
2. **Load official Advanced bank (from GitHub)**  
3. **Select local file** (TXT or CSV, compatible structure)

Additionally, you can click the **“Download explanation CSV (from GitHub)”** button to get the companion CSV file with explanations (`BankQuestionJuly2025.csv`).  
This CSV is **not required** to run the app — it’s a study aid that you can open separately (Excel, LibreOffice, etc.).

### 4. Choose Study Mode

Select one of the **Question modes**:

- **Random** — questions chosen randomly
- **No repeats** — no question repeats until the entire pool has been used
- **Exam (official structure)** — uses the official Basic (100) or Advanced (50) question distribution per category
- **Category training (by topic)** — practice only selected categories
- **Retake wrong questions** — appears after an exam and lets you retry only the missed questions

### 5. Click “Next Question”

- Use **Next Question** to move through the quiz.  
- Use **Check Answer** (if available) to verify your choice and see whether you were correct.

### 6. Review Results

At the end of an exam-style session, the app shows:

- Overall score and pass category:
  - **Pass with honours** (≥ 80%)
  - **Pass** (70–79.9%)
  - **Fail** (< 70%)
- Detailed statistics per category (questions asked, correct, percentage)
- Highlighted weak categories (< 70%)
- A button to **practice only weak categories** or to **retake wrong questions**

---

## 📱 Mobile-Friendly

The entire app is optimized for:

- iPhone / Android
- Tablets
- Desktops
- Small-screen layouts

No installation is required if you run it as a simple HTML file in a browser.  
If hosted as a PWA (Progressive Web App), it can also be **installed to the home screen** on mobile devices.

---

## 🔧 Technical Notes

- No external libraries required (vanilla JavaScript, HTML, and CSS only).
- Runs fully offline when the HTML file is opened locally or when installed as a PWA.
- All logic (parsing, exam selection, statistics, UI updates) is implemented **client-side**.
- No data is sent to any server — your study progress stays on your device.
- Official question banks remain the property of ISED; this trainer only consumes the TXT/CSV provided by the user.

---

## 💛 Support the Project

If this HAM Exam Trainer helps you prepare for your Basic or Advanced certification, please consider supporting future updates:

➡️ https://buymeacoffee.com/fabiolus

Your support helps keep the app **free** and available for the entire Canadian amateur radio community.

---

## 📜 License

This project is free for **personal and educational use**.  
Redistribution or commercial repackaging requires permission.

---

## 📬 Contact

Questions, suggestions, or feature ideas?  
Feel free to open an issue on GitHub or reach out:

Fabien  
`the_fabiolous@hotmail.com`

---

# 📡 Formateur d’Examen Radioamateur (Canada) — Application bilingue

Un outil gratuit, complet et hors ligne pour étudier l’examen de Base et l’examen Avancé d’ISED Canada.

## 🇨🇦 Aperçu

Ce formateur d’examen radioamateur en HTML a été conçu pour les étudiantes et étudiants qui préparent l’examen de Base ou l’examen Avancé d’ISED Canada.  
Il offre :

- Interface bilingue (anglais et français)
- Structure officielle des examens d’ISED
  - Base (100 questions, répartition officielle)
  - Avancé (50 questions, répartition officielle)
- Compatibilité avec les fichiers TXT délimités officiels (banques de questions Base et Avancé)
- Fichier CSV d’explications optionnel (BankQuestionJuly2025.csv) téléchargeable via un bouton dédié
- Interface adaptée au mobile
- Mode sombre
- Statistiques par catégorie
- Détection des points faibles (< 70 %)
- Mode **Reprendre les erreurs**
- Entraînement par catégorie
- Modes **Aléatoire / Sans répétition / Examen**
- Fonctionne entièrement hors ligne (aucun serveur requis)

L’application est contenue dans un seul fichier `.html` que vous ouvrez simplement dans votre navigateur.

---

## 🚀 Fonctionnalités

### 🔤 Interface bilingue (EN/FR)

- Choisissez votre langue à l’**Étape 1**.  
- Tous les textes, boutons et sections (y compris la carte « À propos et soutien ») s’adaptent automatiquement.

### 📂 Chargement des banques de questions officielles

Compatible avec le format TXT délimité fourni par ISED :

```text
question_id;question_en;optionA_en;...;question_fr;optionA_fr;...
```

Fonctionne pour :

- Banque de questions **Base**
- Banque de questions **Avancé**

Vous pouvez charger les banques de deux façons :

- À l’aide des boutons intégrés **« Load official Basic/Advanced bank (from GitHub) »**  
- Ou en sélectionnant un **fichier TXT/CSV local** sur votre ordinateur

### 📑 Téléchargement du CSV d’explications (depuis GitHub)

- Un bouton dédié à l’**Étape 2** permet de télécharger le fichier CSV d’explications directement depuis GitHub :

  - Fichier : `BankQuestions/BankQuestionJuly2025.csv`
  - Objectif : fournir des explications détaillées et des moyens mnémotechniques pour un grand nombre de questions
  - Ce fichier est **optionnel** et sert d’outil d’étude complémentaire (Excel, LibreOffice, etc.)

- Le libellé du bouton est entièrement bilingue :
  - EN : **“Download explanation CSV (from GitHub)”**
  - FR : **« Télécharger le CSV d’explications (depuis GitHub) »**

### 🎯 Simulation réelle de l’examen officiel

Le mode **Examen** sélectionne automatiquement les questions selon la répartition officielle d’ISED.

#### Examen de Base (100 questions)

- 25 – Règlements et politiques  
- 9 – Procédures d’exploitation  
- 21 – Montage et sécurité  
- 6 – Composants de circuits  
- 13 – Électronique de base  
- 13 – Antennes et lignes de transmission  
- 8 – Propagation  
- 5 – Brouillage et suppression  

#### Examen Avancé (50 questions)

- 5 – Théorie avancée  
- 12 – Composants et circuits  
- 6 – Mesures  
- 4 – Alimentations  
- 9 – Émetteurs et modulation  
- 5 – Récepteurs  
- 9 – Antennes et lignes de transmission  

### 🧠 Entraînement par catégorie

- Pratiquez uniquement les thèmes de votre choix (p. ex. seulement **Règlements**, seulement **Propagation**, seulement **Antennes**).  
- Idéal pour cibler vos points à améliorer.

### 🔁 Mode Reprendre les erreurs

Après un examen complet :

- L’application identifie les questions erronées.
- Vous pouvez lancer un nouveau quiz contenant uniquement ces questions pour consolider vos connaissances.

### 🧮 Statistiques en temps réel

- Pourcentage de bonnes réponses par catégorie  
- Suivi des questions posées / répondues  
- Mise en évidence des **catégories faibles** (< 70 %)  
- Répartition détaillée dans le rapport final

### 🌓 Mode sombre + 📱 Mode mobile

- Thème sombre activable pour réduire la fatigue visuelle.  
- Mode mobile pour une mise en page adaptée aux téléphones intelligents.  
- L’interface reste utilisable sur ordinateurs, tablettes et mobiles.

### ☕ Bouton de soutien (« À propos et soutien »)

Une section **« À propos et soutien »** inclut un bouton menant à votre page **Buy Me a Coffee** :

➡️ https://buymeacoffee.com/fabiolus

Cette option permet aux personnes reconnaissantes de soutenir le développement de l’outil tout en le gardant gratuit pour la communauté.

---

## 🖥 Comment utiliser l’application (Français)

### 1. Ouvrez le fichier HTML

- Téléchargez le dernier fichier `index.html` (ou équivalent) depuis le dépôt GitHub.  
- Ouvrez-le dans votre navigateur (double-clic ou glisser-déposer dans un onglet).

### 2. Choisissez la langue

- À l’**Étape 1**, sélectionnez **English** ou **Français**.  
- Toute l’interface s’adapte automatiquement à la langue choisie.

### 3. Chargez une banque de questions

À l’**Étape 2**, vous avez trois options :

1. **Load official Basic bank (from GitHub)**  
2. **Load official Advanced bank (from GitHub)**  
3. **Sélectionner un fichier local** (TXT ou CSV, structure compatible)

Vous pouvez également cliquer sur le bouton **« Télécharger le CSV d’explications (depuis GitHub) »** pour obtenir le fichier CSV d’explications (`BankQuestionJuly2025.csv`).  
Ce fichier n’est **pas requis** pour faire fonctionner l’application — il sert d’outil d’étude complémentaire que vous pouvez ouvrir dans Excel, LibreOffice, etc.

### 4. Choisissez un mode d’étude

Sélectionnez l’un des **modes de questions** :

- **Aléatoire** — questions choisies de façon aléatoire  
- **Sans répétition** — aucune répétition avant d’avoir parcouru toute la banque  
- **Examen (structure officielle)** — utilise la répartition officielle Base (100) ou Avancé (50) par catégorie  
- **Entraînement par catégorie** — pratique ciblée sur certaines catégories  
- **Reprendre les erreurs** — après un examen, ne reprend que les questions mal répondues

### 5. Cliquez sur « Question suivante »

- Utilisez **Question suivante** pour avancer dans le quiz.  
- Utilisez **Vérifier la réponse** (si présent) pour confirmer vos choix.

### 6. Consultez les résultats

À la fin d’une session de type examen, l’application affiche :

- Le score global et la catégorie de réussite :
  - **Réussite avec mention** (≥ 80 %)  
  - **Réussite** (70–79,9 %)  
  - **Échec** (< 70 %)  
- Des statistiques détaillées par catégorie (questions posées, bonnes réponses, pourcentage)
- Les catégories faibles (< 70 %) mises en évidence
- Des options pour **pratiquer seulement les catégories faibles** ou **reprendre uniquement les erreurs**

---

## 📱 Optimisé pour mobile

L’interface s’adapte automatiquement :

- iPhone / Android  
- Tablettes  
- Ordinateurs  
- Petits écrans intégrés

Aucune installation n’est requise si vous utilisez simplement le fichier HTML dans votre navigateur.  
Lorsqu’il est hébergé comme PWA (Progressive Web App), l’outil peut aussi être **installé sur l’écran d’accueil** des appareils mobiles.

---

## 🔧 Notes techniques

- Ne nécessite aucune bibliothèque externe.  
- Fonctionne entièrement hors ligne (en local ou en PWA).  
- Le chargement et l’analyse des questions, la logique d’examen, les statistiques et l’interface sont gérés **côté client** via JavaScript.  
- Aucune donnée n’est envoyée à un serveur — tout reste sur votre appareil.  
- Les banques de questions officielles demeurent la propriété d’ISED; l’outil ne fait qu’utiliser les fichiers TXT/CSV fournis par l’utilisatrice ou l’utilisateur.

---

## 💛 Soutenir le projet

Si cet outil vous aide à vous préparer à l’examen radioamateur, vous pouvez soutenir son développement :

➡️ https://buymeacoffee.com/fabiolus

Votre soutien aide à maintenir l’application gratuite pour l’ensemble de la communauté radioamateur du Canada.

---

## 📜 Licence

Projet gratuit pour **usage personnel et éducatif**.  
La redistribution ou la revente commerciale nécessite une autorisation.

---

## 📬 Contact

Pour toute question ou suggestion, veuillez ouvrir un billet (**issue**) sur GitHub ou communiquer avec :

Fabien  
`the_fabiolous@hotmail.com`
