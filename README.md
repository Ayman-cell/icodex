# 🎓 ICODEX MODEL - Plateforme de Génération et Évaluation de Quiz Intelligente

**Système complet de transformation de documents en quiz interactifs avec évaluation basée sur l'IA**

<div align="center">

[![Python](https://img.shields.io/badge/Python-3.9+-blue?style=for-the-badge&logo=python)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge)](https://github.com)

</div>

---

## 📋 Vue d'ensemble

**ICODEX MODEL** est une plateforme éducative complète et intelligente qui transforme automatiquement des documents PDF en quiz structurés et évalue les réponses des étudiants avec des métriques avancées.

Ce projet combine :

- 🤖 **Intelligence Artificielle** via Cerebras Llama 3.1-8B
- 📄 **Traitement intelligent de documents** (PDF, texte)
- 🧩 **Segmentation contextuelle** en chunks optimisés
- 🏗️ **Structuration hiérarchique** automatique du contenu
- ❓ **Génération dynamique de questions** basée sur le contenu
- 📊 **Évaluation sophistiquée** des réponses étudiantes
- 🎯 **Calcul de scores de maîtrise** nuancés et robustes

C'est une **architecture full-stack éducative** démontrant des compétences avancées en traitement du langage naturel (NLP) et en apprentissage automatisé.

---

## ✨ Fonctionnalités principales

### 1. **Extraction et Transformation de Documents**
- 📄 **Support PDF** : Extraction complète du texte avec préservation du contexte
- 📝 **Support texte brut** : Chargement direct de fichiers .txt
- 🔍 **Nettoyage intelligent** : Suppression des artefacts OCR et normalisations
- 📊 **Gestion efficace** de documents volumineux (100+ pages)
- 🏷️ **Identification automatique** du contenu (cours, modules, concepts)

### 2. **Segmentation Intelligente en Chunks**
- 🧩 **Chunking adaptatif** : Tailles variables selon le type de contenu :
  - **Contenu mathématique** : 960 caractères (optimisé pour les formules)
  - **Contenu orienté code** : 720 caractères (optimisé pour la syntaxe)
  - **Contenu généraliste** : 1200 caractères (optimisé pour les textes)
  - **Contenu spécialisé** : Adaptation dynamique au contexte
- 📐 **Chevauchement configurable** : Préservation de la continuité entre chunks
- 🎯 **Séparateurs intelligents** : Respect des structures logiques (paragraphes, sections)
- 💾 **Sauvegarde optimisée** : Stockage en JSON avec métadonnées

### 3. **Structuration Hiérarchique du Contenu**
- 🏗️ **Hiérarchie à 5 niveaux** :
  - **Cours** (Course)
  - **Modules** (Modules)
  - **Mini-modules** (Mini Modules)
  - **Concepts** (Concepts)
  - **Mini-concepts** (Mini Concepts)
- 🤖 **Utilisation de LLM** pour analyser la structure logique
- 🔗 **Relations sémantiques** entre éléments
- 📋 **Métadonnées enrichies** pour chaque niveau
- 🔄 **Validation et normalisation** des structures

### 4. **Génération Dynamique de Questions**
- ❓ **Questions multi-types** :
  - Questions à choix multiples (QCM)
  - Questions vrai/faux
  - Questions ouvertes courtes
  - Questions d'appariement
  - Questions de complément
- 📊 **Génération intelligente** basée sur la structure du contenu
- 🎓 **Niveaux de difficulté variables** :
  - Facile
  - Moyen
  - Difficile
  - Très difficile
- 🎯 **Diversification du contenu** : Plusieurs variations possibles
- 💾 **Sauvegarde structurée** : Format JSON pour intégration facile

### 5. **Évaluation Avancée des Réponses**
- ✅ **Analyse de similarité** : Comparaison contextuelle des réponses
- 🧮 **Métriques multiples** :
  - **Exactitude normalisée** (Sequence Matching)
  - **Score de vitesse** (en fonction du temps)
  - **Alignement temporel** (optimalité du rythme)
  - **Confiance** (moyenne pondérée des scores)
- 🏋️ **Poids de difficulté** : Ajustement selon le niveau
- ⏱️ **Analyse temporelle** : Évaluation du temps pris vs attendu
- 📈 **Correction multi-paramètres** : Compte du contexte et des conditions

### 6. **Calcul de Scores de Maîtrise**
- 🎓 **Score sur 100** avec composants détaillés :
  - Score de base (combinaison accuracy/speed/confidence)
  - Ajustement par difficulté
  - Bonus de correction
  - Pénalité de rythme
- 🔬 **Formule scientifique** : Basée sur la pédagogie moderne
- 📊 **Métriques détaillées** : Transparence complète du calcul
- 🎯 **Adaptation contextuelle** : Prise en compte du positionnement de la question
- 💾 **Historique complet** : Suivi de la progression de l'étudiant

### 7. **Gestion Avancée des Tokens Cerebras**
- ⏱️ **Limitation des requêtes** en temps réel :
  - 30 requêtes par minute
  - 64,000 tokens par minute
  - 900 requêtes par heure
  - 1,000,000 tokens par jour
- 📊 **Affichage des statistiques d'usage** en direct
- ⏳ **Gestion automatique des files d'attente**
- 🔄 **Retry automatique** avec délai exponentiel (max 3 tentatives)
- 🛡️ **Protection contre les dépassements**

### 8. **Architecture Modulaire et Extensible**
- 🔌 **Modules indépendants** facilement testables
- 📦 **API claire** pour chaque étape du pipeline
- 🔄 **Composition flexible** : Utilisez les modules séparément ou ensemble
- 📚 **Documentation extensive** de chaque composant
- 🧪 **Tests intégrés** et validation des entrées/sorties

---

## 🛠️ Technologies utilisées

| Technologie | Utilisation |
|---|---|
| **Python 3.9+** | Langage principal |
| **Cerebras Llama 3.1-8B** | Modèle LLM pour structuration et génération |
| **PyPDF2** | Extraction de texte depuis PDF |
| **Requests** | Communications API HTTP |
| **ReportLab** | Génération de rapport PDF |
| **JSON** | Sérialisation des structures |
| **argparse** | Interface CLI robuste |

---

## 📂 Structure du projet

```
icodex_model/
│
├── 📁 questions generator/
│   ├── pdf_to_text.py                          # Extraction PDF → Texte
│   ├── text_to_chunks.py                       # Texte → Chunks optimisés
│   ├── chunks_to_structure.py                  # Chunks → Structure hiérarchique
│   ├── structure_to_questions.py               # Structure → Questions
│   ├── quiz_to_pdf.py                          # Questions → Rapport PDF
│   ├── requirements.txt                        # Dépendances
│   ├── README.md                               # Documentation
│   │
│   ├── 📁 Exemples de données/
│   ├── hibernate_extracted.txt                 # Texte extrait (Hibernate)
│   ├── hibernate_extracted_chunks.json         # Chunks structurés
│   ├── hibernate_extracted_chunks_structure.json # Structure hiérarchique
│   ├── hibernate_extracted_chunks_structure_quiz.json # Quiz généré
│   │
│   ├── python-cheatsheet_extracted.txt         # Texte extrait (Python)
│   ├── python-cheatsheet_extracted_chunks.json
│   ├── python-cheatsheet_extracted_chunks_structure.json
│   ├── python-cheatsheet_extracted_chunks_structure_quiz.json
│   │
│   ├── pithon_extracted.txt                    # Texte extrait (Python avancé)
│   ├── pithon_extracted_chunks.json
│   ├── pithon_extracted_chunks_structure.json
│   ├── pithon_extracted_chunks_structure_quiz.json
│   │
│   └── commandes.txt                           # Guide des commandes
│
├── 📁 answers evaluation/
│   ├── answer_evaluator.py                     # Évaluation des réponses
│   ├── mastery_scorer.py                       # Calcul du score de maîtrise
│   └── __pycache__/                            # Cache Python
│
└── 📁 __pycache__/                             # Cache global
```

---

## 🚀 Installation et démarrage

### 1. **Cloner le dépôt**
```bash
git clone https://github.com/Ayman-cell/icodex_model.git
cd icodex_model
```

### 2. **Créer un environnement virtuel**
```bash
python -m venv venv
```

**Activation de l'environnement :**
- **Windows** :
  ```bash
  .\venv\Scripts\activate
  ```
- **macOS/Linux** :
  ```bash
  source venv/bin/activate
  ```

### 3. **Installer les dépendances**
```bash
pip install -r questions\ generator/requirements.txt
```

### 4. **Configurer l'API Cerebras**
Définissez votre clé API Cerebras comme variable d'environnement :

```bash
# Windows
set CEREBRAS_API_KEY=votre-clé-api-ici

# macOS/Linux
export CEREBRAS_API_KEY=votre-clé-api-ici
```

Ou modifiez directement dans les scripts Python :
```python
CEREBRAS_API_KEY = "votre-clé-api-ici"
```

### 5. **Vérifier l'installation**
```bash
cd "questions generator"
python pdf_to_text.py --help
```

---

## 📖 Guide d'utilisation

### Pipeline Complet : PDF → Quiz

Transformez un PDF en quiz en 5 étapes :

#### **Étape 1 : Extraire le texte du PDF**
```bash
cd "questions generator"
python pdf_to_text.py --input document.pdf --output document_extracted.txt
```

**Options** :
- `--input` : Chemin vers le PDF
- `--output` : Fichier texte de sortie
- `--verbose` : Affichage détaillé du traitement

#### **Étape 2 : Découper en chunks optimisés**
```bash
python text_to_chunks.py --input document_extracted.txt --output document_chunks.json
```

**Options** :
- `--input` : Fichier texte
- `--output` : Fichier JSON de chunks
- `--chunk-size` : Taille des chunks (défaut: 1200)
- `--overlap` : Chevauchement entre chunks (défaut: 300)
- `--content-type` : Type de contenu (`general`, `math`, `code`)

#### **Étape 3 : Structurer le contenu**
```bash
python chunks_to_structure.py --input document_chunks.json \
                              --output document_structure.json \
                              --api-key YOUR_CEREBRAS_API_KEY
```

**Options** :
- `--input` : Fichier des chunks
- `--output` : Structure hiérarchique JSON
- `--api-key` : Clé Cerebras
- `--model` : Modèle LLM (défaut: `llama3.1-8b`)
- `--timeout` : Délai d'attente API (défaut: 300s)

#### **Étape 4 : Générer les questions**
```bash
python structure_to_questions.py --input document_structure.json \
                                 --output document_quiz.json \
                                 --api-key YOUR_CEREBRAS_API_KEY
```

**Options** :
- `--input` : Structure hiérarchique JSON
- `--output` : Quiz généré en JSON
- `--api-key` : Clé Cerebras
- `--num-questions` : Nombre de questions par concept (défaut: 3)
- `--difficulty-distribution` : Distribution des difficultés

#### **Étape 5 : Générer un rapport PDF**
```bash
python quiz_to_pdf.py --input document_quiz.json --output document_quiz.pdf
```

**Options** :
- `--input` : Quiz JSON
- `--output` : Fichier PDF
- `--include-answers` : Inclure les corrigés
- `--formatting` : Style du rapport (`academic`, `corporate`, `student`)

### Évaluation des Réponses Étudiantes

#### **Évaluer une réponse**
```bash
cd "answers evaluation"
python answer_evaluator.py \
    --question "Qu'est-ce que la POO?" \
    --correct-answer "La programmation orientée objet..." \
    --student-answer "C'est quand on utilise des objets..." \
    --time-taken 45 \
    --expected-time 60 \
    --difficulty "medium" \
    --position "3"
```

**Sortie** : Métriques d'évaluation en JSON

#### **Calculer le score de maîtrise**
```bash
# À partir d'un fichier d'évaluation
python mastery_scorer.py evaluation_result.json

# Ou depuis stdin
python answer_evaluator.py ... | python mastery_scorer.py -
```

**Résultat** : Score de maîtrise sur 100 avec décomposition des composants

### Exemple complet avec données

Les fichiers d'exemple fournis montrent le pipeline complet :

```bash
# Inspecter la structure générée
cat "questions generator/hibernate_extracted_chunks_structure.json"

# Voir le quiz généré
cat "questions generator/hibernate_extracted_chunks_structure_quiz.json"

# Évaluer une réponse exemple
python "answers evaluation/answer_evaluator.py" \
    --question "What is Hibernate?" \
    --correct-answer "Hibernate is an ORM framework" \
    --student-answer "It's a database tool" \
    --time-taken 30 \
    --expected-time 40 \
    --difficulty "medium" \
    --position "1"
```

---

## ⚙️ Configuration avancée

### Configuration des chunks

Modifiez `text_to_chunks.py` :

```python
CHUNK_CONFIG = {
    "general": {
        "chunk_size": 1200,
        "chunk_overlap": 300,
        "separators": ["\n\n", "\n", " ", ""]
    },
    "math_heavy": {
        "chunk_size": 960,
        "chunk_overlap": 225,
        "separators": ["\n\n", "\n$$", "\n$", " ", ""]
    },
    "code_heavy": {
        "chunk_size": 720,
        "chunk_overlap": 150,
        "separators": ["\n\n", "\n```", "\nclass", "\ndef", " "]
    }
}
```

### Configuration LLM Cerebras

Modifiez les scripts :

```python
LLM_CONFIG = {
    "model": "llama3.1-8b",
    "temperature": 0.7,
    "max_tokens": 2000,
    "top_p": 0.9,
    "frequency_penalty": 0.0,
    "presence_penalty": 0.0,
}

TOKEN_LIMITS = {
    "max_requests_per_minute": 30,
    "max_tokens_per_minute": 64000,
    "max_requests_per_hour": 900,
    "max_tokens_per_day": 1000000,
    "max_retries": 3,
    "delay_between_requests": 2,
}
```

### Configuration des questions

Modifiez `structure_to_questions.py` :

```python
QUESTION_CONFIG = {
    "num_questions_per_concept": 3,
    "difficulty_distribution": {
        "easy": 0.25,
        "medium": 0.5,
        "hard": 0.20,
        "very_hard": 0.05
    },
    "question_types": [
        "multiple_choice",
        "true_false",
        "short_answer",
        "matching",
        "fill_in_blank"
    ]
}
```

---

## 🔍 Format des fichiers JSON

### Structure de la structure hiérarchique

```json
{
  "course": {
    "title": "Object-Oriented Programming",
    "description": "...",
    "modules": [
      {
        "title": "Classes and Objects",
        "mini_modules": [
          {
            "title": "Class Definition",
            "concepts": [
              {
                "title": "Class Syntax",
                "mini_concepts": ["Constructor", "Methods", "Attributes"],
                "content": "..."
              }
            ]
          }
        ]
      }
    ]
  }
}
```

### Structure d'une question générée

```json
{
  "question_id": "q_001",
  "content": "What is a class in object-oriented programming?",
  "type": "multiple_choice",
  "difficulty": "medium",
  "correct_answer": "A blueprint for creating objects...",
  "options": ["Option 1", "Option 2", "Option 3", "Option 4"],
  "explanation": "...",
  "related_concepts": ["OOP", "Classes", "Objects"],
  "expected_time": 45
}
```

### Résultat d'évaluation

```json
{
  "question": "What is a class?",
  "student_answer": "A blueprint for objects",
  "correct_answer": "A blueprint for creating objects",
  "metrics": {
    "similarity": 0.92,
    "normalized_accuracy": 0.92,
    "speed_score": 0.88,
    "confidence": 0.90,
    "difficulty_weight": 1.0,
    "time_ratio": 0.75,
    "is_correct": true
  },
  "position": "question_1",
  "difficulty": "medium"
}
```

### Score de maîtrise

```json
{
  "question": "What is a class?",
  "position": "question_1",
  "difficulty": "medium",
  "mastery_score": 94.5,
  "components": {
    "base_score": 90.0,
    "difficulty_weight": 1.0,
    "difficulty_adjusted": 90.0,
    "correctness_bonus": 3.0,
    "time_penalty": 0.0,
    "final_score": 94.5
  }
}
```

---

## 💡 Cas d'usage

### 1. **Plateforme d'apprentissage adaptative**
- Convertir les ressources pédagogiques en quiz automatique
- Adapter le niveau de difficulté selon la performance
- Suivre la maîtrise progressivement

### 2. **Certification et validation des compétences**
- Générer des examens à partir de matériel pédagogique
- Évaluer objektivement les réponses
- Délivrer les certificats basés sur les scores

### 3. **Tutoring personnalisé**
- Créer des questions de révision automatiques
- Fournir des retours d'apprentissage détaillés
- Adapter le contenu aux points faibles

### 4. **Formation en entreprise**
- Convertir les documents de formation en quiz
- Évaluer les employés de manière cohérente
- Générer des rapports de compétence

### 5. **Support académique**
- Créer des examens pratiques à partir de cours publiés
- Générer des banques de questions pour les universités
- Automatiser l'évaluation des examens

### 6. **Création d'e-Learning**
- Transformer des PDFs en contenu interactif
- Générer des progressions pédagogiques
- Créer des parcours d'apprentissage

---

## 🔒 Sécurité et bonnes pratiques

### ⚠️ Points importants

1. **API Keys** : Ne commitez JAMAIS votre clé API
   ```bash
   # Utilisez des variables d'environnement
   export CEREBRAS_API_KEY="your-key"
   
   # Ou un fichier .env (NON committé)
   # .env
   # CEREBRAS_API_KEY=your-key
   ```

2. **Gestion des erreurs** :
   - Retry automatique en cas de timeout
   - Gestion des limites de tokens
   - Messages d'erreur explicites

3. **Validation des données** :
   - Vérification du format des fichiers d'entrée
   - Validation des réponses étudiantes
   - Écriture défensive des fichiers JSON

4. **Confidentialité** :
   - Les données restent locales
   - Seul le contenu est envoyé à Cerebras API
   - Aucune identité sensible n'est exposée

---

## 🐛 Dépannage

### Problème : "Clé API invalide"
```
Solution : 
1. Vérifiez que CEREBRAS_API_KEY est correctement définie
2. Testez la clé avec un appel cURL simple
3. Vérifiez les quotas de votre compte Cerebras
```

### Problème : "Fichier PDF invalide"
```
Solution :
1. Assurez-vous que le PDF n'est pas chiffré
2. Essayez un autre PDF pour isoler le problème
3. Vérifiez que le PDF contient du texte (non numérisé uniquement)
4. Pour les PDFs numérisés, utilisez OCR d'abord
```

### Problème : "Timeout API"
```
Solution :
1. Augmentez le timeout dans chunks_to_structure.py
2. Réduisez la taille des chunks
3. Attendez quelques minutes (limites de débit)
4. Vérifiez votre connexion réseau
```

### Problème : "Erreur de mémoire sur gros fichiers"
```
Solution :
1. Réduisez chunk_size (ex: 800 au lieu de 1200)
2. Traitez en plusieurs petits fichiers
3. Augmentez la RAM disponible
4. Utilisez une machine avec plus de mémoire
```

### Problème : "Questions générées de mauvaise qualité"
```
Solution :
1. Ajustez la température LLM (défaut: 0.7)
2. Vérifiez la qualité de la structure hiérarchique
3. Augmentez le nombre de tokens max
4. Relancez la génération (résultats peuvent varier)
```

---

## 📊 Mathématiques derrière le scoring

### Formule de score de base

$$\text{Base Score} = \left(0.6 \times \text{Accuracy} + 0.25 \times \text{Speed} + 0.15 \times \text{Confidence}\right) \times 100$$

### Ajustement par difficulté

$$\text{Adjusted} = \text{Base Score} \times \text{Difficulty Weight}$$

Poids de difficulté :
- Facile : 0.9
- Moyen : 1.0
- Difficile : 1.15
- Très difficile : 1.3

### Score de maîtrise final

$$\text{Mastery} = \text{Adjusted} + \text{Correctness Bonus} - \text{Time Penalty}$$

Où :
- **Correctness Bonus** = 3 points si réponse exacte
- **Time Penalty** = max(0, (Time Ratio - 1.4) × 15)

---

## 🤝 Contribution

Les contributions sont les bienvenues ! Pour contribuer :

1. **Fork** le dépôt
2. **Créez une branche** (`git checkout -b feature/AmazingFeature`)
3. **Commit** vos changements (`git commit -m 'Add AmazingFeature'`)
4. **Push** vers la branche (`git push origin feature/AmazingFeature`)
5. **Ouvrez une Pull Request**

### Domaines de contribution

- 🐛 Correction de bugs
- ✨ Nouvelles fonctionnalités
- 📖 Amélioration de la documentation
- 🧪 Ajout de tests
- 🚀 Optimisations de performance
- 🌐 Support multilingue

---

## 📝 Licence

Ce projet est sous licence **MIT** - voir le fichier [LICENSE](LICENSE) pour plus de détails.

---

## 👨‍💻 Auteur

**Ayman**
- 🔗 GitHub : [@Ayman-cell](https://github.com/Ayman-cell)
- 📧 Contact : aymen@example.com
- 🌐 Portfolio : [aymen-portfolio.com](https://aymen-portfolio.com)

---

## 🙏 Remerciements

- **Cerebras** pour leur API LLM puissante et performante
- **PyPDF2** pour l'extraction PDF robuste
- **ReportLab** pour la génération PDF de haute qualité
- **La communauté Python** pour les excellentes librairies

---

## 📚 Ressources utiles

- [Documentation Cerebras](https://docs.cerebras.ai/)
- [Documentation PyPDF2](https://pypdf2.readthedocs.io/)
- [Documentation ReportLab](https://www.reportlab.com/)
- [Bonnes pratiques NLP](https://huggingface.co/course)
- [Machine Learning en éducation](https://arxiv.org/)

---

## 📞 Support et contact

Pour toute question ou problème :

1. 📖 Vérifiez la section **Dépannage**
2. 🐛 Ouvrez une **Issue** sur GitHub
3. 💬 Consultez la **Documentation** détaillée
4. 📧 Contactez l'auteur directement

---

<div align="center">

## 🚀 Prêt à transformer vos documents en quiz intelligents ?

**[Commencer maintenant →](https://github.com/Ayman-cell/icodex_model#-guide-dutilisation)**

**Dernière mise à jour** : 16 février 2026
**Version** : 1.0.0

</div>
