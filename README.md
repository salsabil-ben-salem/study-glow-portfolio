# 🌸 Study & Glow

## 📄 Description du projet

Study & Glow est une plateforme web dédiée aux étudiantes universitaires, conçue pour les aider à gérer leur bien-être et leur vie académique en un seul endroit.

Le système permet de :

- 💡 Consulter des conseils de bien-être personnalisés (peau, sommeil, nutrition, sport, mental)
- 📊 Calculer sa moyenne selon le système tunisien (DS, TP, Examen par matière)
- ⏱️ Gérer ses sessions d'étude avec un minuteur Pomodoro
- ✅ Organiser ses tâches et deadlines académiques
- 📬 Contacter l'équipe via un formulaire de feedback

Le projet est développé dans le cadre d'un **TP Web — Sciences Informatiques** à la FST-SBZ (A.U. 2025-2026).

---

## 👩‍🎓 Acteurs et fonctionnalités principales

| Acteur | Fonctionnalités principales |
|---|---|
| 🎓 Étudiante | Consulter les conseils bien-être, calculer sa moyenne, gérer ses tâches, utiliser le minuteur |
| 📬 Visiteur | Envoyer un message via le formulaire de contact, noter le site |

---

## 🛠️ Technologies utilisées

- **Frontend :** HTML5 + CSS3 + JavaScript Vanilla
- **Stockage :** localStorage (données persistantes côté navigateur)
- **Polices :** Google Fonts (Playfair Display + Nunito)
- **Design :** CSS Variables, Grid, Flexbox, Animations CSS
- **Compatibilité :** Responsive Mobile + Desktop

---

## 🗂️ Architecture du projet

### Structure globale

```
study-glow/
├── index.html       # Page Bien-être (conseils rapides)
├── planner.html     # Page Agenda (moyenne, minuteur, tâches)
├── contact.html     # Page Contact (formulaire + tableau messages)
└── style.css        # CSS partagé entre les 3 pages
```

---

## 📄 Pages & Fonctionnalités

### 🌸 index.html — Bien-être

```
index.html
├── Navigation fixe (liens vers les 3 pages)
├── Hero (titre animé)
└── Conseils rapides
    ├── 10 cartes colorées par catégorie
    ├── Catégories : Peau, Sommeil, Nutrition, Sport, Mental
    └── Bouton Afficher / Masquer les conseils
```

### 📚 planner.html — Agenda

```
planner.html
├── Onglet 1 : Moyenne Tunisienne
│   ├── 6 modules / 11 matières avec coefficients fixes
│   ├── Formule avec TP   : DS×20% + TP×10% + Examen×70%
│   ├── Formule sans TP   : DS×30% + Examen×70%
│   ├── Total coef        : 15
│   └── Résultat : moyenne générale + mini-cartes par module
├── Onglet 2 : Minuteur d'Étude (Pomodoro)
│   ├── Mode Focus : 25 min
│   ├── Mode Pause : 5 min
│   └── Cercle SVG animé + sons
└── Onglet 3 : Gestion des Tâches
    ├── Ajout : nom, date, catégorie, priorité
    ├── Filtres : Tout / En cours / Terminé
    ├── Tri automatique par date
    └── Sauvegarde localStorage
```

### 📬 contact.html — Contact

```
contact.html
├── Carte info (email, département, délai, localisation)
└── Formulaire
    ├── Champs : nom, email, année, sujet, message
    ├── Notation étoiles (1 à 5)
    ├── Case consentement
    ├── Validation JS complète
    ├── Message de succès après envoi
    └── Tableau des messages envoyés (localStorage)
```

---

## 🗃️ Modules & Matières (Système Tunisien)

| Module | Matière | Coef | TP |
|---|---|---|---|
| Bases de données et Réseaux | Ingénierie des Bases de Données | 1.5 | ✅ |
| Bases de données et Réseaux | Services des Réseaux | 1 | ✅ |
| CPOO | Conception des Systèmes d'Information | 1.5 | ❌ |
| CPOO | Programmation Java | 2 | ✅ |
| Probabilité | Probabilité et Statistique | 2 | ❌ |
| Automates et Optimisation | Théorie des Langages et des Automates | 1 | ❌ |
| Automates et Optimisation | Graphes et Optimisation | 1 | ❌ |
| Langue et Culture d'Entreprise | Anglais 3 | 1 | ❌ |
| Langue et Culture d'Entreprise | Gestion d'Entreprise | 1 | ❌ |
| UEO3 | JEE | 1.5 | ✅ |
| UEO3 | Développement Mobile et Préparation à la Certification | 1.5 | ✅ |

**Total coefficients : 15**

---

## 🎨 Design System (style.css)

```
style.css
├── Variables CSS
│   ├── --couleur-principale : #c97ba8 (rose)
│   ├── --couleur-secondaire : #7b9e87 (vert)
│   ├── --couleur-accent     : #f4a261 (orange)
│   └── --couleur-sombre     : #2d2235 (violet foncé)
├── Composants
│   ├── Navigation fixe + Hero animé
│   ├── Cartes (.card) avec hover
│   ├── Boutons (.btn-primary / secondary / outline)
│   ├── Tabs (.tabs-header / .tab-panel)
│   ├── Formulaires (.form-group)
│   ├── Timer SVG animé
│   ├── Tâches (.task-item)
│   ├── Tips cards (.tip-card)
│   └── Notifications (.notif)
└── Responsive : Mobile + Desktop (breakpoints 480px / 768px)
```

---

## 💾 Stockage des données (localStorage)

| Clé | Contenu | Page |
|---|---|---|
| `tasks` | Liste des tâches (JSON) | planner.html |
| `contactMessages` | Messages envoyés (JSON) | contact.html |

---

## 👩‍💻 Auteure

**Salsabil Ben Salem** — Étudiante en Sciences Informatiques (LSI2)
Université — Département Informatique — A.U. 2025-2026

---

*Fait avec 💜 pour chaque étudiante universitaire ✨ Study & Glow — 2026*
