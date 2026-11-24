# Backlog — MVP

Projet SI Java — Groupe X, ESIEE-IT, L2, 2026–2027.

Ce backlog décrit le périmètre minimal : inscription, connexion, gestion des projets et gestion de leurs tâches. Les critères seront affinés au fil des séances.

| ID | User story | Priorité | État |
| --- | --- | --- | --- |
| US-01 | Initialiser le projet Java | Haute | Terminé |
| US-02 | Inscrire un utilisateur (register) | Haute | À faire |
| US-03 | Connecter un utilisateur (login) | Haute | À faire |
| US-04 | Gérer les projets (CRUD Project) | Haute | À faire |
| US-05 | Gérer les tâches (CRUD Task) | Haute | À faire |

## US-01 — Initialiser le projet

**En tant que** développeur, **je veux** disposer d’un projet Java compilable et testé **afin de** commencer le développement sur une base commune.

Critères d’acceptation :

- [x] Le wrapper Gradle et la configuration Java 21 sont présents.
- [x] L’application et les tests utilisent le package racine `com.esiee.project`.
- [x] Les dossiers des futures couches de l’application sont préparés.
- [x] `./gradlew test` réussit avec le test initial.
- [x] Le README décrit l’installation, l’exécution et les tests.

## US-02 — Inscrire un utilisateur

**En tant que** nouvel utilisateur, **je veux** créer un compte **afin de** pouvoir accéder à l’application.

Critères d’acceptation :

- [ ] Une inscription avec des données valides crée un compte.
- [ ] Les champs obligatoires sont contrôlés.
- [ ] Une inscription avec une adresse e-mail déjà utilisée est refusée.
- [ ] Le mot de passe est stocké sous forme de hachage et n’est pas renvoyé dans les réponses.
- [ ] Des tests couvrent une inscription réussie et les principaux cas d’erreur.

## US-03 — Connecter un utilisateur

**En tant qu’**utilisateur inscrit, **je veux** me connecter **afin de** gérer mes projets et mes tâches.

Dépendance : US-02.

Critères d’acceptation :

- [ ] Des identifiants valides permettent de se connecter.
- [ ] Des identifiants incorrects sont refusés sans révéler si le compte existe.
- [ ] Les opérations protégées nécessitent une authentification.
- [ ] Des tests couvrent la connexion réussie, l’échec et l’accès sans authentification.

## US-04 — Gérer les projets

**En tant qu’**utilisateur connecté, **je veux** créer, consulter, modifier et supprimer mes projets **afin de** organiser mon travail.

Dépendance : US-03.

Critères d’acceptation :

- [ ] Créer un projet avec un nom valide est possible.
- [ ] Consulter la liste de ses projets et le détail d’un projet est possible.
- [ ] Modifier un projet existant est possible.
- [ ] Supprimer un projet existant est possible.
- [ ] Un projet inexistant produit une erreur explicite.
- [ ] Un utilisateur ne peut pas consulter ou modifier les projets d’un autre utilisateur.
- [ ] Des tests couvrent les opérations CRUD, les données invalides et les droits d’accès.

## US-05 — Gérer les tâches

**En tant qu’**utilisateur connecté, **je veux** créer, consulter, modifier et supprimer les tâches d’un projet **afin de** suivre son avancement.

Dépendance : US-04.

Critères d’acceptation :

- [ ] Créer une tâche avec un titre valide dans un projet accessible est possible.
- [ ] Consulter la liste des tâches d’un projet et le détail d’une tâche est possible.
- [ ] Modifier une tâche, notamment son état d’avancement, est possible.
- [ ] Supprimer une tâche existante est possible.
- [ ] Une tâche ou un projet inexistant produit une erreur explicite.
- [ ] Un utilisateur ne peut pas accéder aux tâches d’un projet qui ne lui appartient pas.
- [ ] Des tests couvrent les opérations CRUD, les données invalides et les droits d’accès.

## Définition de terminé

Une user story est terminée lorsque ses critères d’acceptation sont satisfaits, que les tests associés passent, que la documentation utile est à jour et que le code a été relu avant fusion.
