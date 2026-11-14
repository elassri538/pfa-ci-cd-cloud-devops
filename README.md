# PFA chez OCP Group — pipeline CI/CD Cloud & DevOps

**L’Houcine El Assri · élève ingénieur à l’INSEA · projet de fin d’année**

J’ai conçu un pipeline GitHub Actions réutilisable pour des applications Java/Maven. L’objectif est de vérifier le code et l’image avant d’envisager leur publication et leur déploiement. Ce dépôt public présente le projet, mes contributions et l’état des vérifications. Le dépôt de code et les paramètres d’infrastructure restent privés.

## En bref

| Question | Réponse |
| --- | --- |
| Problème | Répéter les mêmes contrôles de livraison sur plusieurs applications sans recopier toute la CI |
| Ma contribution | Workflow réutilisable, tests, contrôles de sécurité, image Docker validée et préparation du chemin AWS |
| Démonstration | Tasks API comme application de référence ; intégration du workflow Java dans Skill Exchange |
| Technologies | GitHub Actions, Maven, Docker, Trivy, Terraform, AWS ECR, OIDC, Systems Manager, Linux et Bash |

## Ce que j’ai réalisé

1. Paramétré un workflow CI pour les projets Java/Maven.
2. Ajouté la compilation, les tests, la détection de secrets et l’analyse de l’image Docker avec Trivy.
3. Prévu la transmission de l’image validée aux étapes suivantes sans nouvelle construction.
4. Préparé la configuration Terraform et l’authentification AWS par OIDC pour la publication et le déploiement.
5. Défini les contrôles de santé et la procédure de restauration de l’image précédente en cas d’échec.
6. Intégré la CI Java dans Skill Exchange, projet réalisé en équipe.

## Parcours de livraison

`Code → tests et scans → image Docker validée → publication prévue sur ECR → déploiement prévu via Systems Manager → contrôle de santé → restauration si nécessaire`

## Vérifications et limites

La CI de l’application de référence a été exécutée avec succès. Les contrôles locaux et les tests simulés de déploiement ne constituent pas une preuve de déploiement AWS actif. La configuration cloud exige un environnement provisionné et des autorisations dédiées. Le rollback décrit concerne l’image applicative et ne restaure pas automatiquement les données PostgreSQL.

Le code source du PFA et les détails d’infrastructure ne sont pas publiés ici. Cette fiche rend le périmètre du projet consultable sans exposer la configuration privée.

## Explorer mon portfolio

- [Profil GitHub et projets publics](https://github.com/elassri538)
- [Fiche détaillée du PFA](https://github.com/elassri538/elassri538/blob/main/projects/pfa-pipeline.md)
- [Ma contribution DevOps à Skill Exchange](https://github.com/elassri538/elassri538/blob/main/projects/skill-exchange-devops.md)
- [Cabinet médical conteneurisé](https://github.com/elassri538/cabinet-medical-docker)
