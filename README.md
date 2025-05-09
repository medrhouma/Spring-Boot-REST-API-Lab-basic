    # Student Management System API

Une API RESTful simple pour gérer les étudiants, construite avec Spring Boot, JPA et une base de données H2 en mémoire.

## 🧠 Objectifs d'apprentissage

- Comprendre les principes de l'architecture REST
- Créer une application Spring Boot from scratch
- Implémenter des endpoints REST avec les bonnes méthodes HTTP
- Manipuler les données JSON avec mapping objet
- Gérer les erreurs de base
- Tester l'API avec Postman

## 🛠️ Technologies utilisées

- Java 11+
- Spring Boot 3.x
- Spring Web
- Spring Data JPA
- H2 Database
- Maven
- Postman (pour tester l'API)

## 📁 Structure du projet

```
src/
├── main/
│   ├── java/
│   │   └── com/example/studentapi/
│   │       ├── controller/       → REST Controller
│   │       ├── model/            → Classe Student (entité JPA)
│   │       ├── repository/       → Interface JpaRepository
│   │       ├── service/          → Interface + implémentation de la logique métier
│   │       └── StudentApiApplication.java → Point d'entrée
│   └── resources/
│       └── application.properties → Config de la DB H2
└── test/                         → Tests unitaires (non inclus ici)
```

## 🚀 Lancer le projet

1. Cloner le projet :
   ```bash
   git clone https://github.com/votre-utilisateur/student-api.git
   cd student-api
   ```

2. Importer dans votre IDE (IntelliJ, VS Code, Eclipse)

3. Construire et exécuter :
   ```bash
   ./mvnw spring-boot:run
   ```

4. Accéder à la console H2 (optionnel) :
   - URL : [http://localhost:8080/h2-console](http://localhost:8080/h2-console)
   - JDBC URL : `jdbc:h2:mem:studentdb`
   - User : `sa`
   - Mot de passe : *(laisser vide)*

## 📬 Endpoints de l'API

| Méthode | Endpoint              | Description                  |
|---------|-----------------------|------------------------------|
| POST    | `/api/students`       | Créer un nouvel étudiant     |
| GET     | `/api/students`       | Obtenir tous les étudiants   |
| GET     | `/api/students/{id}`  | Obtenir un étudiant par ID   |
| PUT     | `/api/students/{id}`  | Mettre à jour un étudiant    |
| DELETE  | `/api/students/{id}`  | Supprimer un étudiant        |

### Exemple de requête POST (JSON)
```json
{
  "firstName": "John",
  "lastName": "Doe",
  "email": "john.doe@example.com",
  "major": "Informatique"
}
```

## ✅ Test avec Postman

Tu peux tester l’API avec [Postman](https://www.postman.com/). N'oublie pas d’utiliser le header suivant :
```
Content-Type: application/json
```

## 📌 Remarques

- Le projet utilise une base H2 en mémoire, donc les données sont perdues à chaque redémarrage.
- Une couche de validation peut être ajoutée avec `@Valid` dans les contrôleurs.
---

## 🧠 Auteur

- Mohamed Rhouma  
- Étudiant à l’ISET Tozeur  
- [LinkedIn](https://www.linkedin.com/in/rhouma-mohamed-6291b02b4)  
- [GitHub](https://github.com/medrhouma)




    
