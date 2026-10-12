# AutoLoc 🚗

## Présentation du projet

**AutoLoc** est une application développée avec **Spring Boot** dans le cadre du module **Architecture des Systèmes d’Information (ASI)** à **ESPRIT**, pour l’année universitaire 2026–2027.

Le projet consiste à concevoir une plateforme de gestion de location de véhicules permettant de centraliser les opérations de plusieurs agences.

Le développement se fera progressivement tout au long du semestre. Chaque séance permettra d'introduire de nouvelles fonctionnalités et de mettre en pratique les concepts d'architecture et de développement logiciel étudiés en cours.

## Modèle du système

Le diagramme suivant présente les principales entités du système AutoLoc ainsi que les relations entre elles.

![Modèle EA AutoLoc](./docs/autoLoc-model.png)

## Technologies utilisées

- **Java** : langage de programmation.
- **Spring Boot** : framework de développement de l'application.
- **Spring Data JPA** : gestion de la persistance des données.
- **Spring MVC** : développement des contrôleurs et des API Web.
- **MySQL / PostgreSQL** : systèmes de gestion de bases de données.
- **Maven** : gestion des dépendances et construction du projet.
- **Git & GitHub** : gestion des versions et collaboration.
- **Swagger / OpenAPI** : documentation et test des API REST.

## Notions abordées

Au cours du semestre, le projet permettra d'étudier et d'appliquer les concepts suivants :

- Architecture en couches.
- Entités JPA et associations entre entités.
- Repositories et services.
- Développement d'API REST.
- DTO et validation des données.
- Principes SOLID.
- Design Patterns.
- Gestion des transactions.
- Requêtes JPQL et pagination.
- Planification des tâches avec Spring Scheduler.
- Programmation orientée aspect avec Spring AOP.
- Qualité logicielle et analyse du code.

## Installation et démarrage

### Prérequis

Avant de démarrer le projet, vérifiez que les outils suivants sont installés :

- Java JDK 17 ou la version compatible avec le projet.
- Maven ou le Maven Wrapper fourni avec le projet.
- MySQL, si cette base de données est utilisée.
- Git.

### 1. Cloner le dépôt GitHub

Ouvrez un terminal et exécutez les commandes suivantes :

```bash
git clone <URL_DU_DEPOT>
cd AutoLoc
```

Remplacez `<URL_DU_DEPOT>` par l'URL réelle du dépôt GitHub.

### 2. Configurer la base de données

Ouvrez le fichier `src/main/resources/application.properties` et vérifiez la configuration de la base de données.

Exemple pour MySQL :

```properties
spring.application.name=AutoLoc
server.port=9090

spring.datasource.url=jdbc:mysql://localhost:3306/AutoLoc?createDatabaseIfNotExist=true
spring.datasource.username=root
spring.datasource.password=VOTRE_MOT_DE_PASSE

spring.jpa.show-sql=true
spring.jpa.hibernate.ddl-auto=update
```

Adaptez les identifiants de connexion à votre environnement local. Assurez-vous également que le serveur MySQL est démarré.

### 3. Vérifier les versions installées

Pour vérifier la version de Java :

```bash
java -version
```

Pour vérifier la version de Maven :

```bash
mvn -version
```

### 4. Démarrer l'application

**Avec Maven :**

```bash
mvn spring-boot:run
```

**Avec le Maven Wrapper sous Windows :**

```bash
mvnw.cmd spring-boot:run
```

**Avec le Maven Wrapper sous Linux ou macOS :**

```bash
./mvnw spring-boot:run
```

Une fois l'application démarrée correctement, les messages de démarrage apparaîtront dans le terminal.

### 5. Accéder à l'application

Si le port configuré est `9090`, l'application sera accessible à l'adresse suivante :

- Application : http://localhost:9090
- Documentation Swagger : http://localhost:9090/swagger-ui/index.html

*La page Swagger sera accessible uniquement si Swagger/OpenAPI est installé et correctement configuré dans le projet.*

### 6. Compiler et générer le fichier JAR

Pour nettoyer les fichiers précédemment générés et compiler le projet :

```bash
mvn clean package
```

Pour démarrer l'application à partir du fichier JAR généré :

```bash
java -jar target/nom-du-fichier.jar
```

Remplacez `nom-du-fichier.jar` par le nom réel du fichier généré dans le dossier `target`.

## Structure générale du projet

Le projet Spring Boot suit une organisation classique en couches, qui pourra évoluer selon les besoins du système.

```text
AutoLoc/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── ...
│   │   └── resources/
│   │       └── application.properties
│   └── test/
├── docs/
│   └── autoLoc-model.png
├── pom.xml
└── README.md
```

Cette structure est indicative et doit être adaptée à l'organisation réelle du dépôt.

## Objectifs pédagogiques

Le projet AutoLoc vise à mettre en pratique les concepts étudiés en Architecture des Systèmes d'Information, à travers la conception et le développement progressif d'une application de gestion de location de véhicules multi-agences.

Il permettra de renforcer les compétences en développement Java, en architecture logicielle, en gestion des données et en conception d'API REST.

---

**Projet pédagogique réalisé à ESPRIT dans le cadre du module Architecture des Systèmes d'Information (ASI) — Année universitaire 2026–2027.**