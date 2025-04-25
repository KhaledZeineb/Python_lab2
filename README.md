
# 📚 Quiz API – FastAPI + PostgreSQL

Bienvenue dans le projet **Quiz API** ! Ce backend simple et rapide vous permet de créer des questions à choix multiple et de les interroger via une API REST. Conçu avec amour 💙 en utilisant **FastAPI** et **PostgreSQL**.

---

## 🚀 Technologies utilisées

- 🐍 Python 3.11
- ⚡ FastAPI
- 🛢️ PostgreSQL
- 🧠 SQLAlchemy ORM
- 🔐 Pydantic
- 🧪 Swagger UI pour la documentation interactive

---

## 📦 Structure du projet

```
FastAPI_PostgreSQL/
│
├── main.py               # Fichier principal contenant les routes de l'API
├── models.py             # Définition des modèles SQLAlchemy
├── database.py           # Configuration de la base de données
├── requirements.txt      # Dépendances du projet
└── README.md             # Fichier de documentation (vous y êtes !)
```

---

## 🔧 Configuration de la base de données

Créez une base PostgreSQL nommée `quizApp` (ou changez l’URL dans `database.py`).

```sql
CREATE DATABASE quizApp;
```

Vérifiez/modifiez l'URL de connexion dans `database.py` :

```python
URL_DATABASE = 'postgresql://postgres:123456789@localhost:5432/quizApp'
```

---

## ▶️ Lancer le projet

1. Créez un environnement virtuel :

```bash
python -m venv myenv
source myenv/bin/activate  # ou myenv\Scripts\activate sous Windows
```

2. Installez les dépendances :

```bash
pip install fastapi uvicorn sqlalchemy psycopg2-binary pydantic
```

3. Lancez le serveur :

```bash
uvicorn main:app --reload
```

4. Rendez-vous sur `http://127.0.0.1:8000/docs` pour tester l’API via Swagger 🎉

---

## 🧠 Fonctionnalités disponibles

| Méthode | Endpoint                  | Description                          |
|--------|---------------------------|--------------------------------------|
| POST   | `/questions/`             | Ajouter une question avec des choix |
| GET    | `/questions/{id}`         | Obtenir une question par ID         |
| GET    | `/choices/{question_id}`  | Obtenir les choix d’une question    |
| GET    | `/`                       | Message de bienvenue                |

---

## 📌 Exemple de payload pour `/questions/`

```json
{
  "question_text": "Quel est le langage utilisé ici ?",
  "choices": [
    {"choice_text": "Python", "is_correct": true},
    {"choice_text": "JavaScript", "is_correct": false},
    {"choice_text": "C++", "is_correct": false}
  ]
}
```

---

## 🌟 À venir

- Authentification JWT
- Ajout/suppression de questions et réponses
- Tests automatisés avec Pytest
- Interface utilisateur frontend 🎨

---

## 🤝 Contribution

Toute contribution est la bienvenue ! Forkez le repo, créez une branche et soumettez une **pull request**.

---

## 🧠 Auteur

Développé par **Zeineb** – une touche d’innovation avec un soupçon d'humour et une vision tournée vers l'avenir 🚀

---

## 📜 Licence

Ce projet est open-source sous licence MIT.
