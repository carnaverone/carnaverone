# Politique de sauvegarde des releases vers GitLab

**Statut :** politique proposée  
**Portée :** programmes Carnaverone importants et versions de release validées

## Objectif

GitLab doit servir de sauvegarde vérifiable des versions importantes, pas de copie automatique de tous les prototypes GitHub.

Cette politique vise à conserver :

- le code source exact d’une release;
- l’historique Git nécessaire à sa reconstruction;
- les artefacts de release validés;
- les preuves d’intégrité;
- la documentation de validation;
- un chemin de récupération indépendant de GitHub.

## Rôles des plateformes

### GitHub

- développement principal pour les dépôts actuellement actifs;
- branches de travail et pull requests;
- déploiements connectés, lorsque requis;
- releases publiques ou privées selon le produit.

### GitLab

- miroir ou archive de sécurité des produits importants;
- conservation des branches et tags de release;
- second emplacement pour le code et les manifestes;
- CI de validation lorsque GitHub Actions est bloqué ou lorsque GitLab est mieux adapté;
- aucun remplacement automatique de la source canonique sans décision explicite.

## Dépôts admissibles

Une sauvegarde GitLab complète est prioritaire pour :

1. produits actifs ou vendables;
2. applications desktop distribuées;
3. services ou bibliothèques partagés par plusieurs produits;
4. sites ou infrastructures critiques;
5. versions comportant une release, un tag ou un jalon stable;
6. dépôts dont la perte ferait perdre un travail difficile à reconstruire.

Les dépôts vides, prototypes abandonnés, essais de quelques fichiers et doublons non analysés ne sont pas sauvegardés automatiquement comme releases.

## Conditions avant sauvegarde d’une release

Une version doit avoir :

- un dépôt canonique identifié;
- une branche par défaut comprise;
- un numéro de version ou un identifiant de jalon;
- un commit exact choisi;
- les validations disponibles exécutées;
- les échecs et limites documentés;
- une vérification des secrets;
- une revue des fichiers générés et binaires;
- une décision claire sur ce qui doit être inclus.

Une version partiellement validée peut être sauvegardée comme **snapshot**, mais ne doit pas être présentée comme release stable.

## Niveaux de sauvegarde

### Niveau 1 — miroir Git

- branches importantes;
- branche par défaut;
- tags;
- historique complet;
- comparaison du SHA entre GitHub, local et GitLab.

### Niveau 2 — archive de récupération

En plus du miroir :

- bundle Git complet;
- archive source de la release;
- manifeste des fichiers;
- sommes SHA-256;
- notes de release;
- commandes de validation et résultats.

### Niveau 3 — conservation de distribution

En plus des niveaux précédents :

- AppImage, paquet Linux, NSIS, DMG ou autres artefacts réellement validés;
- SBOM lorsque disponible;
- inventaire de licences;
- signature ou attestation lorsque disponible;
- instructions de restauration et reconstruction.

## Nommage recommandé

### Tags

```text
vMAJEUR.MINEUR.CORRECTIF
```

Exemple :

```text
v0.4.0
```

### Snapshots non stables

```text
snapshot-AAAA-MM-JJ-description
```

### Archives et bundles

```text
nom-projet-vX.Y.Z-AAAA-MM-JJ.tar.gz
nom-projet-vX.Y.Z-AAAA-MM-JJ.bundle
nom-projet-vX.Y.Z-AAAA-MM-JJ-manifest.txt
nom-projet-vX.Y.Z-AAAA-MM-JJ-SHA256SUMS
```

## Procédure de sauvegarde d’une release

1. Vérifier l’état local :

   ```bash
   git status --short
   git branch --show-current
   git log -5 --oneline
   ```

2. Exécuter les validations du dépôt.
3. Choisir et enregistrer le SHA exact.
4. Vérifier l’absence de secrets, bases utilisateur et fichiers temporaires.
5. Créer ou confirmer le tag de release.
6. Pousser la branche et le tag vers GitHub.
7. Pousser les mêmes références vers GitLab.
8. Comparer les SHA GitHub, local et GitLab.
9. Créer le bundle Git complet.
10. Vérifier le bundle avec `git bundle verify`.
11. Créer l’archive source et le manifeste.
12. Calculer les SHA-256.
13. Ajouter les notes de release et résultats de tests.
14. Vérifier que les artefacts de distribution correspondent au même SHA.
15. Enregistrer le résultat dans le registre central et dans `AI_HANDOFF.md` du dépôt.

## Contenu interdit dans les sauvegardes

Ne jamais inclure sans décision explicite :

- `.env` réel;
- clés API, tokens, certificats privés ou secrets OAuth;
- bases SQLite utilisateur;
- sessions, cookies ou profils navigateur;
- répertoires utilisateur Electron;
- caches;
- `node_modules`;
- environnements Python;
- modèles dont la redistribution n’est pas autorisée;
- médias ou datasets sans droits vérifiés;
- artefacts non testés présentés comme officiels.

## Manifeste minimal

Chaque sauvegarde de release doit enregistrer :

```text
Projet :
Dépôt GitHub :
Dépôt GitLab :
Version ou snapshot :
Date :
Branche :
SHA GitHub :
SHA GitLab :
SHA local :
Identiques : oui/non
Tag :
Bundle :
Résultat git bundle verify :
SHA-256 du bundle :
Archive source :
SHA-256 de l’archive :
Artefacts inclus :
Tests exécutés :
Tests réussis :
Tests non exécutés ou échoués :
Risques connus :
Responsable de validation :
```

## Stratégie de déploiement progressive

### Phase 1

Définir les dépôts canoniques et leur rôle dans `REPOSITORY_REGISTRY.md`.

### Phase 2

Ajouter les fichiers de suivi IA aux produits actifs.

### Phase 3

Identifier les releases réellement importantes et leurs tags.

### Phase 4

Créer ou vérifier les dépôts GitLab correspondants.

### Phase 5

Effectuer la première sauvegarde Niveau 2 des produits prioritaires.

### Phase 6

Ajouter les artefacts de distribution validés et passer au Niveau 3 lorsque pertinent.

## Priorité provisoire de sauvegarde

À confirmer après revue de chaque dépôt :

1. `carnaverone_studio_suite_creative_ai`;
2. `social-automation`;
3. `carnaflow`;
4. `archiva-extractor-airgap`;
5. `carnastudiocyber2`;
6. `Z3TA_RAG_SYSTEM`;
7. `zeta-swarm-command-center`;
8. `ghost-audio-libre`;
9. `Carnaverone-Agent-Forge-V1`;
10. produits audio, vidéo et podcast ayant une version réellement distribuable.

Cette liste ne signifie pas que les autres dépôts seront supprimés. Elle définit seulement l’ordre de création des sauvegardes de release vérifiables.