# Registre central des dépôts Carnaverone

**Date de l’inventaire :** 31 juillet 2026  
**Portée :** compte GitHub `carnaverone`  
**Statut du document :** classement provisoire à confirmer dépôt par dépôt

## Objectif

Ce registre sert à empêcher les humains et les assistants IA de confondre les produits, prototypes, bibliothèques, miroirs et archives Carnaverone.

Les rôles ci-dessous sont fondés sur les noms, l’activité GitHub observée, les PR ouvertes et le contexte de développement connu. Lorsqu’un rôle n’est pas encore vérifié dans le code, il est marqué **à confirmer**.

## Règles de gouvernance

1. Un dépôt ne devient pas canonique uniquement parce qu’il est plus récent ou plus gros.
2. Aucun dépôt ne doit être supprimé, renommé, fusionné ou archivé sans revue de son contenu et validation du propriétaire.
3. Les dépôts vides restent intacts pour le moment.
4. Les noms et responsabilités seront normalisés après la cartographie fonctionnelle.
5. Les versions importantes et validées seront ensuite sauvegardées vers GitLab selon `GITLAB_RELEASE_BACKUP_POLICY.md`.
6. Chaque dépôt actif recevra progressivement un ensemble de fichiers IA cohérent; aucune propagation automatique massive ne doit être faite sans inspection.
7. Le fichier `AI_HANDOFF.md` d’un dépôt actif doit rester la source dynamique de vérité pour son état local.

## Légende

- **ACTIF PRIORITAIRE** : travail récent, PR ouverte ou produit actuellement suivi.
- **STRATÉGIQUE À CARTOGRAPHIER** : dépôt utile ou important dont les frontières restent à confirmer.
- **DOUBLON / PROTOTYPE POSSIBLE** : relation avec un autre dépôt à comparer avant décision.
- **OUTIL / BIBLIOTHÈQUE** : composant transversal ou dépôt de support.
- **VIDE — NE PAS TOUCHER** : dépôt sans contenu significatif; aucune initialisation pour le moment.
- **ARCHIVÉ** : dépôt déjà archivé; ne pas réactiver sans décision explicite.

---

# 1. Dépôt central

| Dépôt | Statut | Rôle provisoire | Décision suivante |
|---|---|---|---|
| `carnaverone` | ACTIF PRIORITAIRE | Profil GitHub et registre central des projets | Maintenir la cartographie, les règles IA et la politique de sauvegarde |

---

# 2. Produits actifs prioritaires

| Dépôt | Rôle actuel | Frontière importante | Prochaine revue |
|---|---|---|---|
| `agent_ai_carnaverone_studio` | Agents IA et packs privés | Ne pas confondre avec Agent Forge ou la banque d’agents du Swarm | Lire README, PR ouvertes et architecture |
| `archiva-extractor-airgap` | Extraction, nettoyage et export d’archives entièrement local | Ne pas ajouter de crawler, cloud ou dépendance réseau implicite | Terminer validation complète et intégration Electron |
| `carnaflow` | Noyau local autonome de workflows sociaux | Ne publie pas réellement sur les réseaux dans son état actuel | Valider dépendances, UI et frontières avec Social Automation |
| `carnastudiocyber2` | Site public `carnaverone.com` | Déploiement web séparé des applications desktop | Maintenir contenu, SEO, mobile et Cloudflare |
| `carnaverone_studio_suite_creative_ai` | Atelier central modulaire de création et production | N’est pas le Command Center ni le Swarm | Consolider modules, releases et contrats internes |
| `Carnaverone-Studio-PodViralQC-Studio` | Production et contrôle de contenu podcast/viral | Produit spécialisé, pas la Suite complète | Vérifier flux runtime, auth et dépendances |
| `panzoom-slideshow` | Générateur de vidéos/slideshows par FFmpeg | Outil vidéo spécialisé | Valider rendu réel, audio et packaging |
| `social-automation` | Application autonome d’automatisation sociale | Séparée de CarnaFlow, du module historique et du Command Center | Finaliser runtime desktop et release multiplateforme |
| `Z3TA_RAG_SYSTEM` | Bibliothèque RAG interne, atomique et traçable | Ne pas confondre avec Jarvis RAG ou ancien Z3TA | Matérialiser, benchmarker et valider les fiches |
| `zeta-swarm-command-center` | Orchestration locale de mini-swarms et banque d’agents | Séparé de la Creative Suite et des applications métier | Définir noyau canonique et modules connectés |

---

# 3. Produits et composants stratégiques à cartographier

| Dépôt | Rôle provisoire | Relation à confirmer |
|---|---|---|
| `ai-online-course-creator-` | Créateur de cours ou formations assisté par IA | Comparer avec `carnaverone_formation_maker_zeta` et la Suite |
| `archiva-extractor` | Version en ligne ou base historique d’Archiva | Définir précisément la séparation avec Airgap |
| `audio-book-maker-ai-stuido-gogo` | Application de production de livres audio | Comparer avec Ghost Audio Libre et le module Livre Audio de la Suite |
| `Carnaverone-Agent-Forge-V1` | Produit Agent Forge | Comparer avec `prog_agent_forge` et `agent_ai_carnaverone_studio` |
| `carnaverone-liryc-song-maker` | Génération ou gestion de paroles musicales | Définir relation avec Album Musique et la Suite |
| `carnaverone-social-command-center` | Ancien ou autre centre social | Comparer avec `social-automation` et CarnaFlow |
| `carnaverone_audio_mixer_zeta` | Mixage audio Zeta | Comparer avec les projets de mastering et la Suite |
| `carnaverone_command-center_maclinux` | Variante Command Center Mac/Linux | Comparer avec `Zeta-COMMAND-CENTER` et le Swarm |
| `Carnaverone_Developer_Studio_ide` | IDE ou studio de développement | Définir s’il s’agit d’un produit autonome ou d’un prototype |
| `carnaverone_zeta_brain` | Composant de mémoire ou cerveau Zeta | Comparer avec ZETA CORE, Jarvis et Z3TA RAG |
| `cockpit_antigravity-` | Cockpit lié à Antigravity | Définir s’il s’agit d’un outil actif, d’une interface ou d’une archive fonctionnelle |
| `ghost-audio-libre` | Moteur vocal local Piper et génération audio | Définir son statut de service partagé ou produit autonome |
| `histoire-bd-infinite-heroes-` | Projet narratif / bande dessinée | Déterminer s’il est actif, expérimental ou contenu privé |
| `international-radio` | Application ou concept radio | Vérifier portée fonctionnelle et dépendances médias |
| `JARVIS_RAG_MODULE` | Module RAG et interface Jarvis | Comparer avec `Z3TA_RAG_SYSTEM` et `zetajarvis` |
| `mastering_audio_album_suno` | Pipeline de mastering pour albums Suno | Comparer avec `prog_CarnaMasteringsuno` et le module Album Musique |
| `memory-antigrav` | Mémoire liée à Antigravity | Comparer avec Zeta Brain, ZETA CORE et Z3TA RAG |
| `prog_CarnaMasteringsuno` | Application ou prototype de mastering Suno | Décider du dépôt canonique de mastering |
| `prog_Carnaverone-studio_central` | Ancien studio central ou prototype de hub | Comparer avec la Creative Suite actuelle |
| `prog_clipmaker` | Outil important de création de clips | Définir relation avec Clip Musique dans la Suite |
| `Z3TA-AI-System` | Ancienne fondation ou système Z3TA | Déterminer ce qui a été repris par `Z3TA_RAG_SYSTEM` |
| `Zeta-COMMAND-CENTER` | Command Center général Zeta | Clarifier la frontière avec Swarm Command Center et variantes PC/Mac |
| `ZETA-CORE-Obsidian-AI-Second-Brain` | Second cerveau Obsidian et mémoire locale | Définir rôle canonique dans l’écosystème mémoire |
| `zeta-SWARM-ORCHESTRATOR` | Orchestrateur technique du Swarm | Définir s’il est module du Command Center ou service autonome |
| `zetajarvis` | Jarvis local ou prototype d’assistant | Comparer avec JARVIS RAG MODULE et Zeta Brain |

---

# 4. Famille agents, prompts et actifs réutilisables

Ces dépôts doivent être comparés avant de choisir une bibliothèque canonique.

| Dépôt | Rôle provisoire | Risque de confusion |
|---|---|---|
| `bundle-prompt-template` | Modèles de bundles de prompts | Peut être une source historique ou un format d’export |
| `Carnaverone-Prompt-Asset-Library` | Bibliothèque de prompts et actifs | Candidate possible comme bibliothèque canonique |
| `prog_agent_forge` | Prototype ou ancien Agent Forge | Doublon possible de `Carnaverone-Agent-Forge-V1` |
| `prompt` | Petit dépôt de prompts | Nom trop générique; rôle à identifier |
| `prompt-analyze-gpt-5` | Analyse ou optimisation de prompts GPT-5 | Outil spécialisé à confirmer |
| `prompt-base` | Base de prompts plus volumineuse | Candidate comme source historique |
| `prompt-deep` | Prompts approfondis | Relation avec `prompt-base` à comparer |
| `zeta-prompt-save` | Sauvegarde de prompts Zeta | Peut être un ancien stockage |
| `persona-` | Personas ou profils d’agents | Déterminer si le contenu appartient à Agent Forge ou au Swarm |

---

# 5. Outils, bibliothèques et dépôts de support

| Dépôt | Rôle provisoire | Action de revue |
|---|---|---|
| `carna-scis` | Petit outil public | Lire le code et confirmer son usage actuel |
| `Demo-Builder-Product-Page-Generator` | Générateur de démonstrations/pages produit | Déterminer s’il doit rester autonome |
| `entlint` | Petit outil public ou expérimental | Identifier fonction et maintenance nécessaire |
| `export-save-` | Outil ou manifeste de sauvegarde/export | Vérifier branche par défaut et usage réel |
| `openhand1` | Prototype ou fork à identifier | Vérifier origine, licence et objectif |
| `save_script_prog` | Scripts de sauvegarde de programmes | Vérifier branche bootstrap et relation avec la politique GitLab |

---

# 6. Doublons, miroirs ou prototypes possibles

| Dépôt | Observation provisoire | Décision requise |
|---|---|---|
| `CarnaStudio_Dev` | Dépôt de développement ou coordination historique | Vérifier s’il contient des décisions encore utiles |
| `carnaverone-Social-Content-Studio` | Très petit dépôt Social Content Studio | Comparer avec Social Automation et le site |
| `zeta-swarm-command-center-pc1` | Semble partager au moins un commit récent avec `zeta-swarm-command-center` | Déterminer s’il s’agit d’un miroir PC1 ou d’une variante nécessaire |
| `zeta-swarm-observatory` | Observabilité du Swarm | Définir s’il doit rester module séparé |

---

# 7. Dépôts vides — laisser intacts

Aucune initialisation, aucun fichier IA et aucun renommage pour le moment.

| Dépôt | Statut actuel | Note future |
|---|---|---|
| `avatar-3d-vrm` | VIDE — NE PAS TOUCHER | Définir s’il devient un module avatar |
| `bibliotheque-prompt` | VIDE — NE PAS TOUCHER | Comparer plus tard avec les autres bibliothèques de prompts |
| `carnaverone-design-system` | VIDE — NE PAS TOUCHER | Peut devenir le design system canonique après décision |
| `carnaverone_formation_maker_zeta` | VIDE — NE PAS TOUCHER | Comparer avec le créateur de cours existant |
| `reeinvokeai` | VIDE — NE PAS TOUCHER | Identifier l’intention avant tout développement |
| `repertoire-bibliotheque-document-reference-entrainement` | VIDE — NE PAS TOUCHER | Définir politique documentaire et droits avant ajout de données |
| `social-studio-carnaverone` | VIDE — NE PAS TOUCHER | Comparer avec les produits sociaux existants |
| `workflow-ato-pipeline` | VIDE — NE PAS TOUCHER | Définir le rôle exact du pipeline |
| `zeta-control-center` | VIDE — NE PAS TOUCHER | Comparer avec les Command Centers existants |

---

# 8. Dépôt archivé

| Dépôt | Statut | Règle |
|---|---|---|
| `-Daw-audio-forge-engine-v2.1` | ARCHIVÉ | Ne pas réactiver ou modifier sans décision explicite; identifier son successeur lors de la revue audio |

---

# 9. Normalisation future des noms

La normalisation est volontairement reportée jusqu’à la revue fonctionnelle. Les problèmes à corriger plus tard comprennent :

- tirets initiaux ou finaux;
- fautes telles que `stuido` et `liryc`;
- mélange de majuscules, minuscules, tirets et underscores;
- noms génériques comme `prompt`, `persona-` ou `openhand1`;
- doublons apparents entre produits, variantes PC et anciens prototypes;
- branches par défaut inhabituelles telles que branches bootstrap ou `feature/ai-integration`.

Avant tout renommage, documenter :

1. dépôt canonique;
2. produit ou service représenté;
3. successeur et prédécesseurs;
4. dépendances entre dépôts;
5. URL de déploiement éventuelle;
6. GitLab de sauvegarde éventuel;
7. tags et releases à préserver;
8. redirections ou mises à jour nécessaires dans les autres dépôts.

---

# 10. Ordre de travail proposé

## Lot A — actifs avec PR ou développement récent

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

## Lot B — architecture centrale

1. `Zeta-COMMAND-CENTER`
2. `JARVIS_RAG_MODULE`
3. `Carnaverone-Agent-Forge-V1`
4. `ghost-audio-libre`
5. `prog_clipmaker`
6. `audio-book-maker-ai-stuido-gogo`
7. `archiva-extractor`

## Lot C — comparaison et consolidation

- familles Prompt et Agent Forge;
- variantes Command Center, Swarm et PC1;
- projets audio/mastering;
- anciens studios centraux;
- mémoire Zeta, Jarvis, Obsidian et Antigravity;
- petits outils et scripts de sauvegarde.

## Lot D — dépôts vides

Aucune action avant décision explicite sur leur utilité, leur nom et leur relation avec les produits existants.

---

# 11. Informations à enregistrer lors de chaque revue

Pour chaque dépôt examiné, compléter au minimum :

```text
Nom actuel :
Nom canonique proposé :
Produit / rôle :
Statut : actif | maintenance | prototype | historique | archivé | vide
Dépôt parent ou dépendances :
Dépôts à ne pas confondre :
Branche par défaut :
Dernière release validée :
Commandes de validation :
État des tests :
État de la documentation IA :
Sauvegarde GitLab : aucune | prévue | complète
Prochaine action :
```

Ce registre doit être mis à jour seulement à partir d’observations vérifiées dans les dépôts. Les suppositions restent explicitement marquées comme provisoires.