# Racine

# Multi.Agents – Vue d'ensemble

Solution qui orchestre plusieurs agents IA pour aider sur des objectifs métier, avec intégration Slack, Trello et une page de santé.

## Projets
- `Multi.Agents` : application principale (orchestrateur, intégrations externes, endpoints minimal API).
- `Multi.Agents.Tests` : tests unitaires autour de l’orchestrateur et du service de santé.

## Démarrage rapide
- Renseignez les clés Anthropic/Slack/Trello via variables d’environnement ou fichier `appsettings.local.json` (non versionné).
- Lancez : `dotnet run --project Multi.Agents.csproj`.
- Les agents résident dans `AgentsActifs/`; le health check est exposé sur `/health`.

## Sécurité
- Ne commitez jamais vos secrets (`appsettings.local.json` reste local).
- Protégez l’endpoint `/health` en production (authentification, restriction d’accès, proxy, rate limiting).




## Multi.Agents.Tests

# Multi.Agents.Tests

Projet de tests unitaires pour l’orchestrateur multi-agents.

## Ce que couvre le projet
- Vérifie le bon déroulement des chaînes d’agents et la publication des messages.
- Contrôle la santé des dépendances simulées (LLM, Slack, Trello, agents chargés).

## Exécution
- Pré-requis : SDK .NET installé.
- Lancer tous les tests : `dotnet test`.




#### Multi.Agents

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




