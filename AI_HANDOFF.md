# AI HANDOFF — Registre des dépôts Carnaverone

**Dépôt :** `carnaverone/carnaverone`  
**Rôle :** profil GitHub et registre central de gouvernance des dépôts  
**Branche de travail actuelle :** `docs/repository-registry`

## Mission

Ce dépôt ne contient pas les applications Carnaverone principales. Il documente :

- quels dépôts existent;
- quel produit chaque dépôt représente;
- quels dépôts sont actifs, historiques, vides ou à revoir;
- les risques de doublons et de confusion;
- l’ordre de déploiement des fichiers IA;
- la stratégie de sauvegarde des releases importantes vers GitLab.

## Lire en premier

1. `REPOSITORY_REGISTRY.md`
2. `AI_REPOSITORY_ROLLOUT.md`
3. `GITLAB_RELEASE_BACKUP_POLICY.md`
4. `README.md`

## État actuel

- inventaire GitHub initial effectué le 31 juillet 2026;
- 65 dépôts observés;
- dépôts actifs, stratégiques, outils, doublons possibles, vides et archivés classés provisoirement;
- neuf dépôts vides identifiés et laissés intacts;
- un dépôt déjà archivé identifié;
- familles à risque de confusion identifiées : Command Center, Swarm, Zeta/Jarvis/RAG, Agent Forge, prompts, social et audio;
- aucun renommage ou archivage supplémentaire approuvé;
- aucune sauvegarde GitLab de release créée dans cette étape.

## Décisions actuelles

1. Ne pas toucher aux dépôts vides.
2. Ne pas renommer les dépôts avant la revue fonctionnelle.
3. Ne pas désigner un dépôt canonique sans lire son code et sa documentation.
4. Ajouter les fichiers IA progressivement, dépôt par dépôt.
5. Utiliser des branches documentaires et des PR en brouillon.
6. Sauvegarder vers GitLab seulement les programmes importants et les versions réellement validées.
7. Distinguer une release stable d’un snapshot partiellement validé.

## Prochaine tâche exacte

Commencer le Lot 1 de `AI_REPOSITORY_ROLLOUT.md` avec `social-automation` :

1. inspecter les fichiers IA déjà présents;
2. lire README, architecture, statuts et PR ouvertes;
3. identifier les frontières avec CarnaFlow et les anciens modules sociaux;
4. ajouter ou mettre à niveau `AI_HANDOFF.md`, `AGENTS.md`, `CLAUDE.md`, `CODEX.md`, `CHATGPT.md` et `docs/REPOSITORY_RELATIONSHIPS.md`;
5. ne pas fusionner les PR applicatives pendant ce travail documentaire.

## Règles pour les assistants IA

- Ce dépôt est un registre, pas un monorepo.
- Ne pas copier le code des produits ici.
- Ne pas modifier plusieurs dépôts sans enregistrer chaque opération séparément.
- Ne pas présenter les rôles provisoires du registre comme des vérités vérifiées.
- Mettre à jour `REPOSITORY_REGISTRY.md` quand une relation est confirmée.
- Mettre à jour ce handoff après chaque lot de dépôts traité.
- Toujours rapporter les branches, commits, PR et fichiers réellement modifiés.

## Journal de passation

### 2026-07-31 — ChatGPT

- création du registre provisoire des 65 dépôts;
- décision de laisser les neuf dépôts vides intacts;
- ajout de la politique de sauvegarde GitLab des releases;
- ajout du plan progressif de fichiers IA;
- aucune release ni sauvegarde GitLab exécutée;
- prochaine étape : revue documentaire de `social-automation`.