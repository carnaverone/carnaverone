# Plan de déploiement des fichiers IA dans les dépôts

**Statut :** plan progressif  
**Principe :** inspecter avant d’écrire; ne pas appliquer un modèle identique aveuglément à tous les dépôts

## Objectif

Chaque assistant IA qui ouvre un dépôt Carnaverone doit comprendre rapidement :

- ce que le dépôt représente;
- ce qu’il ne représente pas;
- son état réel;
- sa relation avec les autres dépôts;
- les validations déjà exécutées;
- les blocages;
- la prochaine tâche exacte;
- les règles de commit, push et release.

## Dépôts vides

Les dépôts vides restent intacts pour le moment.

Aucun de ces fichiers ne doit y être ajouté avant décision sur leur utilité :

- `AI_HANDOFF.md`;
- `AGENTS.md`;
- `CLAUDE.md`;
- `CODEX.md`;
- `CHATGPT.md`.

Leur statut reste uniquement enregistré dans `REPOSITORY_REGISTRY.md`.

## Structure pour un produit actif

```text
AI_HANDOFF.md
AGENTS.md
CLAUDE.md
CODEX.md
CHATGPT.md
docs/IMPLEMENTATION_STATUS.md
docs/REPOSITORY_RELATIONSHIPS.md
docs/SECURITY_MODEL.md        # lorsque pertinent
```

## Source de vérité

### `AI_HANDOFF.md`

Source dynamique canonique du dépôt :

- mission;
- architecture réelle;
- état courant;
- branche et PR en cours;
- travail terminé;
- validations exécutées;
- validations manquantes;
- risques;
- prochaine tâche;
- dernière sauvegarde GitLab.

### `AGENTS.md`

Règles stables et ordre de lecture pour les agents de code, particulièrement Codex.

### `CLAUDE.md`, `CODEX.md`, `CHATGPT.md`

Instructions spécifiques à chaque environnement. Ces fichiers doivent rester courts et pointer vers `AI_HANDOFF.md`; ils ne doivent pas recopier tout le statut dynamique.

### `docs/IMPLEMENTATION_STATUS.md`

Tableau des capacités :

- implémentée;
- validée;
- partielle;
- expérimentale;
- planifiée;
- retirée avec justification.

### `docs/REPOSITORY_RELATIONSHIPS.md`

Document essentiel pour l’écosystème Carnaverone :

- dépôt parent;
- produit principal;
- modules;
- dépendances;
- miroirs;
- prédécesseurs;
- successeurs;
- dépôts à ne pas confondre;
- dépôt GitLab de sauvegarde.

### `docs/SECURITY_MODEL.md`

À ajouter pour les applications qui traitent :

- secrets;
- authentification;
- données utilisateur;
- fichiers hostiles;
- réseau;
- Electron;
- archives;
- publication sociale;
- agents avec outils;
- exécution de commandes;
- distribution desktop.

## Règles anti-confusion

Chaque dépôt actif doit répondre explicitement aux questions suivantes :

```text
Ce dépôt est :
Ce dépôt n’est pas :
Dépôt canonique :
Produits parents :
Modules ou services liés :
Dépôts similaires à ne pas confondre :
Entrées :
Sorties :
Réseau autorisé :
Données persistées :
État de release :
```

## Protocole avant ajout des fichiers IA

1. Lire le README et les documents existants.
2. Inspecter la branche par défaut et les PR ouvertes.
3. Identifier le dernier travail réel.
4. Examiner les scripts de build, test et release.
5. Repérer les fichiers IA déjà présents.
6. Conserver leur contenu utile plutôt que les écraser.
7. Vérifier les relations avec les autres dépôts.
8. Rédiger un handoff fondé sur des preuves.
9. Créer une branche documentaire séparée.
10. Ouvrir une PR en brouillon.
11. Ne fusionner qu’après revue du propriétaire.

## Ordre de déploiement

### Lot 1 — actifs prioritaires

1. `social-automation`
2. `carnaflow`
3. `carnaverone_studio_suite_creative_ai`
4. `carnastudiocyber2`
5. `Z3TA_RAG_SYSTEM`
6. `zeta-swarm-command-center`
7. `agent_ai_carnaverone_studio`
8. `panzoom-slideshow`
9. `Carnaverone-Studio-PodViralQC-Studio`
10. `archiva-extractor-airgap`

`archiva-extractor-airgap` possède déjà une structure IA avancée; il sert de référence, mais son contenu ne doit pas être copié mot pour mot dans les autres produits.

### Lot 2 — architecture centrale

1. `Zeta-COMMAND-CENTER`
2. `JARVIS_RAG_MODULE`
3. `Carnaverone-Agent-Forge-V1`
4. `ghost-audio-libre`
5. `prog_clipmaker`
6. `audio-book-maker-ai-stuido-gogo`
7. `archiva-extractor`

### Lot 3 — familles à consolider

- prompts et personas;
- anciens Agent Forge;
- variantes Command Center;
- Swarm PC1 et observatoire;
- projets audio/mastering;
- mémoire Zeta/Jarvis/Obsidian/Antigravity;
- anciens studios centraux;
- petits outils et scripts.

### Lot 4 — dépôts vides

Aucune action avant décision explicite.

## Format minimal de `AI_HANDOFF.md`

```markdown
# AI HANDOFF — Nom du projet

## Mission

## Ce dépôt est

## Ce dépôt n’est pas

## Architecture vérifiée

## État Git actuel

## Travail terminé

## Validation réellement exécutée

## Validation manquante

## Risques et limites

## Relations avec les autres dépôts

## Prochaine tâche exacte

## Sauvegarde GitLab

## Journal de passation
```

## Journal de passation

Chaque changement matériel doit ajouter une entrée concise :

```text
Date :
Agent :
Branche :
Commit :
Portée :
Fichiers changés :
Tests réussis :
Tests non exécutés ou échoués :
Risques connus :
Prochaine tâche :
Sauvegarde GitLab :
```

## Interdictions communes

- ne pas déclarer une fonction terminée uniquement parce qu’elle apparaît dans le README;
- ne pas supprimer une feuille de route sans décision;
- ne pas pousser directement sur `main` sans autorisation;
- ne pas fusionner une PR sans autorisation;
- ne pas inventer des tests ou résultats;
- ne pas mélanger Creative Suite, Command Center, Swarm, CarnaFlow, Social Automation, Jarvis, Z3TA RAG et Archiva;
- ne pas ajouter de cloud ou télémétrie à un produit local sans demande explicite;
- ne pas copier des secrets dans les rapports;
- ne pas modifier les dépôts vides;
- ne pas renommer les dépôts avant la cartographie fonctionnelle.

## Critère de réussite

Le déploiement est réussi lorsqu’une IA peut ouvrir un dépôt sans historique de conversation et répondre précisément :

1. quel produit elle regarde;
2. où le travail s’est arrêté;
3. quels tests ont réellement passé;
4. ce qui reste à faire;
5. quels autres dépôts ne doivent pas être modifiés;
6. si une release et une sauvegarde GitLab existent.