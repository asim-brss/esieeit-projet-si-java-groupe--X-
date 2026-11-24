# Projet SI Java — Groupe X

Projet pédagogique de SI Java réalisé en L2 à ESIEE-IT, année 2026–2027.

## Objectif

Construire progressivement une application Java organisée en couches, avec des tests automatisés et un travail collaboratif sous Git. Le projet prépare une future API Spring.

Le sujet métier et les fonctionnalités seront précisés dans le [backlog](BACKLOG.md).

## Équipe

- Groupe : X — à remplacer par le numéro du groupe.
- Membres : noms et rôles à compléter par l’équipe.

## Prérequis

- **JDK 21**, avec les commandes `java` et `javac` disponibles.
- **Git** et, sous Windows, **Git Bash** pour les commandes ci-dessous.
- Une connexion Internet pour le premier téléchargement de Gradle et des dépendances.
- IntelliJ IDEA est recommandé pour le développement.

Le wrapper **Gradle 8.14.3** est fourni : aucune installation globale de Gradle n’est nécessaire.

Vérifier Java :

```bash
java -version
javac -version
```

Les deux commandes doivent indiquer une version 21. `JAVA_HOME`, s’il est défini, doit pointer vers le JDK 21.

## Installation

```bash
git clone https://github.com/asim-brss/esieeit-projet-si-java-groupe--X-.git
cd esieeit-projet-si-java-groupe--X-
./gradlew --version
```

Dans IntelliJ, ouvrir le **dossier racine contenant `settings.gradle` et `build.gradle`**, puis laisser la synchronisation Gradle se terminer. Utiliser un JDK 21 pour le projet et la JVM Gradle.

## Exécuter l’application

Depuis la racine du dépôt, dans Git Bash :

```bash
./gradlew run
```

Le point d’entrée est `com.esiee.project.App`. L’application actuelle s’exécute dans la console.

## Tests et compilation

Exécuter les tests JUnit 5 :

```bash
./gradlew test
```

Le rapport HTML se trouve dans `build/reports/tests/test/index.html`.

Compiler et lancer les vérifications :

```bash
./gradlew build
```

Sous PowerShell, utiliser `./gradlew.bat` à la place de `./gradlew`.

## Structure du projet

```text
src/
├── main/java/com/esiee/project/
│   ├── App.java
│   ├── api/
│   │   ├── controller/
│   │   └── dto/
│   ├── domain/
│   │   ├── model/
│   │   └── enums/
│   ├── service/
│   ├── repository/
│   └── exception/
└── test/java/com/esiee/project/
    └── AppTest.java
```

Les packages destinés à la future API sont préparés ; leurs fonctionnalités seront ajoutées au fil des séances.

## Workflow Git

1. Partir d’une branche principale à jour et créer une branche par tâche :

   ```bash
   git switch -c feature/nom-de-la-tache
   ```

2. Réaliser une modification ciblée, puis lancer `./gradlew test`.
3. Examiner les changements et sélectionner les fichiers à inclure :

   ```bash
   git status
   git diff
   git add chemin/du/fichier
   git diff --cached
   ```

4. Enregistrer un commit explicite :

   ```bash
   git commit -m "Décrit la modification réalisée"
   ```

5. Lors du partage sur GitHub, faire relire la branche dans une pull request avant de la fusionner dans la branche principale.

Ne pas versionner les secrets, les sorties de compilation ou la configuration locale de l’IDE.

## Backlog

Les tâches et fonctionnalités à réaliser sont suivies dans [BACKLOG.md](BACKLOG.md).
