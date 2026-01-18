# Multi.Agents (application)

Application principale qui orchestre plusieurs agents IA autour d’un objectif utilisateur. Elle relaie les échanges dans Slack, peut alimenter Trello et expose une page de santé.

## Points clés
- Charge les agents décrits en JSON depuis `AgentsActifs/`.
- Utilise une clé Anthropic pour dialoguer avec le modèle LLM.
- Peut publier dans un dashboard global si configuré.

## Utilisation rapide
- Ajoutez vos clés dans des variables d’environnement ou `appsettings.local.json` (non versionné).
- Lancez : `dotnet run --project Multi.Agents.csproj`.
- Suivez les échanges dans Slack et consultez `/health` pour l’état des dépendances.
