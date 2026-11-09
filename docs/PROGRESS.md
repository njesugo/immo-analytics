# Progression

## Contexte confirmé
- Compte Snowflake : AWS eu-west-3 (Paris), édition à préciser
- Accès GitHub : SSH, clé déjà enregistrée (test `ssh -T git@github.com` à faire à l'étape 0.2)
- WSL Ubuntu 26.04, uv 0.13.7, git 2.53. Python système 3.14.4 : **non retenu pour dbt**, version plus ancienne à épingler via uv.

## Phase 0 : repo, venv, Git/GitHub
- [ ] 0.1 `git init` (branche `main`), venv uv avec Python épinglé, liste d'ignores justifiée
- [ ] 0.2 `.gitignore`, structure des dossiers, premier commit, remote GitHub en SSH

## Décisions prises
- Python épinglé en dessous de 3.14 : compatibilité de dbt-snowflake avec 3.14 non confirmée dans la doc. Version exacte à justifier.

## Points à vérifier (règle 6)
- dbt Projects on Snowflake : GA depuis nov. 2025, runtime managé en dbt Core 1.12.x. `dbt deps` exige une External Access Integration, non supportée en essai. À tester sur le compte.
- `source freshness` : listé comme supporté, note de bas de page non lue. À tester en essai.
- Version Python supportée par dbt-snowflake : à lire sur PyPI.
- MFA imposé sur le compte (impact auth par clés) : à vérifier en phase 1.
- Tableau Public et connexion directe à Snowflake : à vérifier avant la phase 4.

## Questions ouvertes
- Édition du compte Snowflake (Standard ou Enterprise), visible dans Snowsight.
- Dépôt distant GitHub déjà créé ?
