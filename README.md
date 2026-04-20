# librarii

Catalogue de **skills** et **agents** pour VS Code, Claude Code, Cursor et Gemini CLI.

Chaque skill est un guide exécutable (markdown + frontmatter) que l'IDE/agent peut activer pour structurer une tâche précise : cadrer une idée, écrire un brief, analyser un marché, cartographier un processus, etc. Les agents orchestrent plusieurs skills pour couvrir un workflow complet.

## Structure

```
skills/
  brief/SKILL.md
  business-model/SKILL.md
  define-idea/SKILL.md
  market-analysis/SKILL.md
  process-builder/SKILL.md
  skill-creator/SKILL.md
  solution-design/SKILL.md
  user-research/SKILL.md
agents/
  cadrage/AGENT.md
registry.json
```

Chaque skill/agent est autonome — toutes les métadonnées (nom, version, auteur, tags, description) vivent dans le frontmatter du `SKILL.md` / `AGENT.md`. Le `registry.json` sert d'index pour l'extension marketplace.

## Skills disponibles

| Skill | Description | Version |
|---|---|---|
| [define-idea](skills/define-idea/SKILL.md) | Guide la définition d'une idée ou opportunité — du déclencheur brut à la fiche de synthèse structurée | 0.1.0 |
| [brief](skills/brief/SKILL.md) | Transforme un cadrage ou une idée validée en brief projet structuré | 0.1.0 |
| [user-research](skills/user-research/SKILL.md) | Identifie et caractérise les utilisateurs cibles — personas et parcours | 0.1.0 |
| [market-analysis](skills/market-analysis/SKILL.md) | Analyse marché et concurrence — acteurs, offres, différenciation | 0.1.0 |
| [solution-design](skills/solution-design/SKILL.md) | Explore et évalue les solutions possibles — tradeoffs et recommandation | 0.1.0 |
| [business-model](skills/business-model/SKILL.md) | Définit le modèle économique — proposition de valeur, segments, revenus | 0.1.0 |
| [process-builder](skills/process-builder/SKILL.md) | Cartographie un processus métier sous forme de `.process.json` | 0.2.0 |
| [skill-creator](skills/skill-creator/SKILL.md) | Guide la création d'un nouveau skill librarii bien formé | 0.1.0 |

## Agents disponibles

| Agent | Description | Skills orchestrés | Version |
|---|---|---|---|
| [cadrage](agents/cadrage/AGENT.md) | Orchestre le cadrage complet d'un projet — de l'idée au modèle économique | `define-idea`, `user-research`, `market-analysis`, `solution-design`, `business-model` | 0.1.0 |

## Versioning

- Le repo a ses propres releases (`v0.1.0`, `v0.2.0`…)
- Chaque skill/agent a sa version indépendante dans son frontmatter
- L'extension utilise les tags git pour accéder aux versions antérieures d'un skill donné

## Licence

Ce projet est sous licence **[GNU AGPL-3.0](LICENSE)**.

En clair :
- Usage interne libre (aucune obligation de partage tant que tu ne distribues pas)
- Si tu distribues ou exposes publiquement un service basé sur librarii (même modifié), tu dois publier ton code source sous AGPL-3.0
- Couvre aussi les cas SaaS / agents hébergés
