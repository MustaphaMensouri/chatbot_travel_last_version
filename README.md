# Chatbot Rasa pour Agence de Voyage 🤖✈️

Un chatbot intelligent développé avec Rasa pour assister les clients d'une agence de voyage dans leurs réservations de vols et d'hôtels de la langue arabe.

## ✨ Fonctionnalités

### Intents Implémentés
- **Intents par défaut Rasa** : salutations, affirmations, négations, etc.
- **`book_flight`** : Réservation de vols avec gestion des entités
- **`book_hotel`** : Réservation d'hôtels avec critères spécifiques
- **`select_option`** : Sélection parmi les options proposées
- **`change_option`** : Modification des paramètres de recherche
- **`confirm_reservation`** : Confirmation finale de la réservation

### Entités Gérées

#### Pour les Vols
- `ville_depart` : Ville de départ
- `ville_destination` : Ville de destination
- `date_depart` : Date de départ
- `date_retour` : Date de retour (pour aller-retour)
- `classe` : Classe de voyage (économique, affaires, première)
- `type` : Type de vol (aller-simple, aller-retour)

#### Pour les Hôtels
- `categorie` : Catégorie d'hôtel (étoiles)
- `ville` : Ville de séjour
- `quartier` : Quartier préféré
- `nombre_personnes` : Nombre de voyageurs

## 🛠️ Technologies Utilisées

- **Rasa** : Framework de chatbot conversationnel
- **Python 3.8+** : Langage de programmation principal
- **HTML/CSS/JavaScript** : Interface utilisateur webls

## 📋 Prérequis

Avant de commencer, assurez-vous d'avoir installé :

```bash
Python 3.8 ou supérieur
pip (gestionnaire de paquets Python)
Git
```

### Versions Compatibles
- Python : 3.8+
- Rasa : 3.x

## 🚀 Installation

1. **Cloner le repository**
```bash
git clone [https://github.com/MustaphaMensouri/chatbot_travel_last_version.git]
cd rasa_travel_chatbot
```

2. **Créer un environnement virtuel**
```bash
python -m venv venv
source venv/bin/activate  # Sur Windows: venv\Scripts\activate
```

3. **Installer Rasa**
```bash
pip install rasa
```

## ⚙️ Configuration

1. **Vérifier la configuration**
```bash
rasa --version
```

2. **Entraîner le modèle**
```bash
rasa train
```

3. **Tester la configuration**
```bash
rasa data validate
```

## 🎮 Utilisation

### 1. Démarrer le serveur d'actions
```bash
rasa run actions
```



### 2. Démarrer l'interface web
```bash
rasa run --enable-api --cors "*"
```

### 3. Accéder à l'interface web
Ouvrez index.html dans votre navigateur.

## 📁 Structure du Projet

```
rasa-travel-chatbot/
├── data/
│   ├── nlu.yml              # Données d'entraînement NLU
│   ├── stories.yml          # Histoires de conversation
│   └── rules.yml            # Règles de dialogue
├── actions/
│   ├── __init__.py
│   └── actions.py           # Actions personnalisées
├── models/                  # Modèles entraînés
├── tests/                   # Tests unitaires
├── web/                     # Interface web
│   ├── index.html
│   ├── style.css
│   └── script.js
├── config.yml               # Configuration Rasa
├── domain.yml               # Définition du domaine
├── endpoints.yml            # Configuration des endpoints
├── credentials.yml          # Identifiants des canaux
├── requirements.txt         # Dépendances Python
├── air_maroc
├── index.htmls
└── README.md               # Ce fichier

```

### Scénarios Testés
1. **Réservation de vol** : Recherche et sélection d'un vol aller-retour
2. **Réservation d'hôtel** : Recherche d'hôtel avec critères spécifiques
3. **Modification** : Changement des paramètres de recherche
4. **Confirmation** : Finalisation de la réservation

