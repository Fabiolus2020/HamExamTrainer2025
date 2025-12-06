# 📡 Entraîneur d’examen radioamateur (Canada) — Application bilingue

Un outil HTML gratuit, prêt à être utilisé hors ligne, pour vous aider à pratiquer les examens **de base et avancé** de radioamateur d’ISDE (Canada).

- 🇨🇦 Basé sur les banques de questions officielles d’ISDE
- 🇬🇧🇫🇷 Interface entièrement bilingue (anglais et français)
- 📱 Mise en page adaptée au mobile (bureau + mode mobile dédié)
- 🧠 Plusieurs modes d’étude, y compris les structures d’examen officielles
- 🧾 Banque CSV optionnelle avec explications et « trucs de mémoire »
- 💾 Sauvegarde automatique de la session (localement, dans le navigateur)

Créé par **Fabien Clermont**.  
Sous licence **CC BY-NC-SA 4.0** (non commercial, attribution, partage dans les mêmes conditions).
:contentReference[oaicite:1]{index=1}

---

## ✨ Principales fonctionnalités

### 📚 Prise en charge des deux banques de questions officielles d’ISDE

L’application peut charger les fichiers TXT délimités officiels publiés par ISDE :

- `amat_basic_quest_delim2025.txt` (Base)
- `amat_adv_quest_delim2025.txt` (Avancé)

Vous pouvez :

- Les charger **directement depuis GitHub** via les boutons intégrés  
  *(Nécessite une connexion internet pour charger depuis GitHub)*, ou  
- Les télécharger vous-même et utiliser **« Choisir un fichier (local) »** pour charger une copie locale.  
  *(Utilisez cette option pour charger un fichier local.)*

Avec une banque officielle chargée, l’application :

- Respecte la **répartition réelle des catégories d’examen** :
  - Base : 100 questions (8 catégories, nombre de questions fixe)
  - Avancé : 50 questions (7 catégories, nombre de questions fixe)
- Affiche des **statistiques détaillées par catégorie**, la détection des **points faibles** et une **carte thermique (heatmap)** des catégories :
  - Catégories fortes : couleur « positive »
  - Catégories faibles : mises en évidence sous un certain seuil

> 🔎 Les banques officielles d’ISDE sont composées uniquement de *questions et réponses* — sans explications.

---

## 🧾 Banque CSV optionnelle (explications et identifiants)

En plus des fichiers TXT officiels, l’application prend en charge un **format CSV personnalisé** qui permet d’ajouter :

- Des **explications détaillées** pour chaque question  
- Des **trucs de mémoire** et astuces pédagogiques  
- Du texte compatible HTML (pour l’affichage dans l’application)  
- Un **BankQuestionID** correspondant à l’identifiant officiel de la question

Un exemple de CSV est fourni dans le dépôt, par exemple :

- `BankQuestionJuly2025.csv`

Flux de travail typique :

1. Télécharger le fichier CSV depuis GitHub.  
2. L’ouvrir dans Excel, Google Sheets ou LibreOffice.  
3. Modifier ou ajouter des explications, aides-mémoire ou reformulations plus claires.  
4. Sauvegarder en CSV et le charger à l’aide du bouton **« Choisir un fichier (local) »** dans l’application.

Lorsqu’un CSV compatible est chargé :

- L’application affiche une section **Explication** sous la question après avoir cliqué sur **« Vérifier la réponse »**.
- Le texte provient directement de la colonne `explanation` du CSV.
- Le **BankQuestionID** (colonne `BankQuestionID`) est affiché au-dessus de la question, ce qui facilite le lien avec l’ID officiel d’ISDE.

> 💡 Remarques  
> - Les banques TXT officielles du gouvernement ne contiennent **aucune** explication.  
> - La banque CSV avec explications est un **complément créé par l’utilisateur** ; chacun peut l’adapter pour son étude personnelle.

### 📁 Structure recommandée du CSV

Colonnes recommandées :

- `BankQuestionID` — Identifiant officiel de la question (ex. `B-001-001-002`)  
- `question` — Énoncé de la question  
- `optionA`, `optionB`, `optionC`, `optionD` — Choix de réponses  
- `correctOption` — Réponse correcte (`A`, `B`, `C` ou `D`)  
- `explanation` — Texte d’explication compatible HTML (affiché après « Vérifier la réponse »)  

L’application est flexible, mais cette structure offre la meilleure expérience.

---

## 🧪 Modes d’étude et d’examen

L’application propose plusieurs modes pour s’adapter à différents styles d’apprentissage.

### 🎯 Mode examen (structure officielle)

- **Base :** 100 questions selon la répartition officielle des catégories.  
- **Avancé :** 50 questions selon la répartition officielle des catégories.

Le mode examen affiche :

- Le score final et le pourcentage
- **Réussite / Échec / Distinction (honours)** à partir de 80 %
- Une répartition détaillée par catégorie (réglementation, exploitation, électronique, etc.)
- La détection des **catégories faibles** (par exemple en dessous de 70 %)
- Une **carte thermique (heatmap)** des catégories
- Des boutons « **Pratiquer uniquement cette catégorie** »
- Un bouton « **Reprendre seulement les mauvaises réponses** »

### 🔄 Mode aléatoire

- Tire des questions au hasard dans la banque chargée.
- Utile pour des sessions rapides et une révision globale.

### ♻️ Mode sans répétition

- Parcourt toutes les questions **sans répétition** jusqu’à épuisement de la banque.
- Idéal pour s’assurer d’avoir vu toutes les questions au moins une fois.

### 🧩 Entraînement par catégorie (par thème)

- Permet de cibler une ou plusieurs catégories (par exemple uniquement « Propagation », uniquement « Antennes », etc.).
- Très efficace pour travailler spécifiquement sur vos points faibles.

### 🔁 Refaire uniquement les mauvaises réponses

- Après un examen, vous pouvez lancer une session contenant **uniquement les questions auxquelles vous avez mal répondu**.
- Idéal pour corriger vos erreurs de manière ciblée.

### 🧠 Mode difficulté intelligente (Smart Difficulty / apprentissage adaptatif)

- Mode spécial qui **adapte la difficulté au fil du temps** en fonction de vos résultats :
  - En cas de bons résultats, davantage de questions issues de catégories plus exigeantes.
  - En cas de difficultés, priorité aux catégories faibles et aux questions récemment ratées.
- L’objectif est de vous maintenir dans une « zone d’apprentissage optimale », plutôt que de proposer uniquement des questions aléatoires.

### 🔍 Mode révision d’examen

- Après avoir terminé un examen, vous pouvez passer en **mode révision** :
  - Parcours de toutes les questions de l’examen (dans l’ordre).
  - Affichage de votre réponse et de la bonne réponse.
  - Affichage des explications (si vous utilisez une banque CSV).
- Très utile pour une analyse détaillée après l’examen.

---

## 📊 Progression, statistiques et heatmap

Pendant l’utilisation, l’application suit :

- Le nombre total de questions répondues  
- Le nombre de bonnes réponses  
- Le pourcentage courant  

En mode examen, le récapitulatif final inclut :

- Le pourcentage global et le résultat (Réussite / Échec / Distinction)  
- Les statistiques par catégorie  
- La mise en évidence des catégories à renforcer  
- Une **carte thermique** qui résume visuellement vos performances

Un **badge de mode** au-dessus de la barre de progression indique en permanence le mode actif (Examen, Aléatoire, Entraînement par catégorie, Difficulté intelligente, Révision, etc.).

---

## 🌐 Interface bilingue et commutation intelligente

Dès l’**Étape 1**, l’utilisateur choisit :

- 🇬🇧 **English**  
- 🇫🇷 **Français**

L’application propose :

- Une interface entièrement bilingue (libellés, boutons, messages, étapes)
- Des noms de catégories et titres de rapports bilingues
- Des libellés Réussite / Échec / Distinction bilingues
- Le contenu « À propos / Support » en deux langues
- La mention de licence et le pied de page bilingues

Vous pouvez changer de langue **à tout moment** :

- Les textes d’interface visibles sont mis à jour immédiatement.
- Partout où c’est possible, les éléments dépendant de la langue (messages, noms de modes, badges, etc.) sont mis à jour dynamiquement grâce à une **commutation bilingue intelligente**.

*(Remarque : le texte des questions provient des fichiers TXT/CSV, et reste donc dans la langue d’origine du fichier.)*

---

## 🌓 Thème, mise en page et optimisation mobile

L’application inclut plusieurs fonctionnalités d’interface :

### 🎨 Thème & affichage

- Bascule **mode sombre** / mode clair.  
- Sélecteur de **couleur de thème** (couleur d’accent).  
- Bouton **plein écran** pour maximiser l’espace de travail (navigateurs compatibles).  
- **Badges de mode** et libellés clairs indiquant :
  - Le mode courant (Examen / Aléatoire / Catégorie / Difficulté intelligente / Révision / etc.)
  - La langue active  
  - La progression dans l’examen ou la session

### 📱 Mode mobile & orientation

- Un **mode mobile dédié** optimisé pour les téléphones.  
- **Détection automatique de l’orientation** (portrait / paysage) pour adapter la mise en page.  
- Comportement spécifique du bouton **Réinitialiser** sur mobile :
  - Réinitialise l’état de l’application  
  - Revient en haut de la page et à l’étape initiale, pour se rapprocher de l’expérience sur ordinateur.

---

## 💾 Sauvegarde automatique (locale uniquement)

L’application utilise le stockage local du navigateur (par ex. `localStorage`) pour **sauvegarder automatiquement** certains éléments de la session :

- Langue sélectionnée  
- Mode courant  
- Index de question et score  
- Questions récemment répondues / mal répondues  
- Préférences d’interface (mode sombre, mise en page mobile, etc.)

Si vous fermez puis rouvrez la page dans le même navigateur, l’application peut reprendre là où vous vous étiez arrêté.

Vous pouvez cliquer sur **Réinitialiser** à tout moment pour :

- Effacer l’état de la session  
- Revenir à l’Étape 1 (choix de la langue et chargement de la banque de questions)

*(La sauvegarde automatique est strictement locale à votre appareil et votre navigateur — aucune donnée n’est envoyée à un serveur.)*

---

## 🧭 Utilisation de base (aperçu des étapes)

1. **Choisir la langue (EN / FR).**  
2. **Charger une banque de questions :**
   - Banque officielle Base / Avancé depuis GitHub *(connexion internet requise)*, ou  
   - Fichier TXT / CSV local via **« Choisir un fichier (local) »**.  
3. **Sélectionner un mode :**
   - Aléatoire / Sans répétition / Examen / Entraînement par catégorie / Difficulté intelligente / Révision d’examen.  
4. **Commencer la session :**
   - Cliquer sur **« Question suivante »** pour afficher une question.  
   - Sélectionner une réponse, puis cliquer sur **« Vérifier la réponse »** pour voir le résultat.  
5. **Utiliser les explications (si disponibles) :**
   - Si vous utilisez un CSV avec explications, lire le bloc **Explication** qui apparaît après la vérification.  
6. **Analyser & progresser :**
   - Utiliser « Reprendre seulement les mauvaises réponses » et l’entraînement par catégorie pour cibler vos faiblesses.  
   - Se servir de la heatmap et des statistiques par catégorie pour orienter votre étude.

À tout moment, cliquer sur **Réinitialiser** pour effacer la session en cours et repartir de l’Étape 1.

---

## 💬 À propos, support & signalement de problèmes

Cet entraîneur d’examen radioamateur bilingue a été créé pour aider les étudiants à se préparer avec des questions de style réel, des structures d’examen officielles et des statistiques détaillées.

- Licence : **CC BY-NC-SA 4.0** (non commercial, attribution, partage dans les mêmes conditions)  
- Utilisation gratuite pour des fins personnelles et éducatives  
- Non destiné à la revente ni à l’intégration dans des produits / services payants  

Si cette application vous aide et que vous souhaitez soutenir les futures améliorations :

- ☕ Buy Me a Coffee : https://buymeacoffee.com/fabiolus  
- 💻 GitHub : https://github.com/Fabiolus2020/HamExamTrainer2025  

Pour signaler un bogue, une suggestion ou une faute :

- Utiliser le lien **« Signaler un problème »** dans l’application (section Support / pied de page), qui ouvre la page des issues GitHub avec le contexte nécessaire, ou  
- Créer une issue directement sur le dépôt GitHub.

---

## 📜 Licence (résumé)

Ce projet est sous licence :

**Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)**

Vous êtes autorisé à :

- **Partager** — copier et redistribuer le matériel sur tout support ou format  
- **Adapter** — remixer, transformer et créer à partir de ce matériel  

Sous les conditions suivantes :

- **Attribution** — Vous devez créditer **Fabien Clermont**, fournir un lien vers la licence et indiquer si des modifications ont été apportées.  
- **NonCommercial** — Vous ne pouvez **pas** utiliser ce matériel à des fins commerciales.  
- **ShareAlike** — Si vous modifiez, transformez ou adaptez ce matériel, vous devez diffuser vos contributions sous la **même licence**.

Texte juridique complet : https://creativecommons.org/licenses/by-nc-sa/4.0/
