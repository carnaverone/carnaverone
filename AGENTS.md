# AGENTS — Registre central Carnaverone

## Ordre de lecture

1. `AI_HANDOFF.md`
2. `REPOSITORY_REGISTRY.md`
3. `AI_REPOSITORY_ROLLOUT.md`
4. `GITLAB_RELEASE_BACKUP_POLICY.md`
5. `README.md`

## Mission

Maintenir la cartographie des dépôts Carnaverone et empêcher les agents IA de confondre produits, modules, prototypes, miroirs, archives et dépôts vides.

## Règles obligatoires

- Inspecter le dépôt cible avant de modifier son statut dans le registre.
- Marquer les inférences comme provisoires.
- Ne pas toucher aux dépôts vides sans autorisation explicite.
- Ne pas renommer, archiver, fusionner ou supprimer un dépôt sans autorisation explicite.
- Ne pas pousser directement sur `main` sans autorisation.
- Utiliser une branche documentaire et une PR en brouillon pour chaque lot.
- Ne pas mélanger Creative Suite, Command Center, Swarm, CarnaFlow, Social Automation, Jarvis, Z3TA RAG et Archiva.
- Enregistrer les relations confirmées dans `REPOSITORY_REGISTRY.md`.
- Enregistrer l’état du travail dans `AI_HANDOFF.md`.
- Appliquer `GITLAB_RELEASE_BACKUP_POLICY.md` seulement aux versions importantes et validées.

## Livrable attendu pour chaque dépôt revu

```text
Nom actuel :
Rôle vérifié :
Statut :
Dépôt canonique :
Dépôts liés :
Dépôts à ne pas confondre :
Branche par défaut :
PR ouvertes :
Tests réellement exécutés :
Fichiers IA existants :
Fichiers IA ajoutés ou corrigés :
Sauvegarde GitLab :
Prochaine action :
```

## Interdiction de propagation aveugle

Ne pas déposer automatiquement les mêmes fichiers dans tous les dépôts. Les règles communes peuvent être réutilisées, mais la mission, l’architecture, les tests, les risques et les relations doivent être vérifiés dans chaque projet.