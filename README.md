[![License](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](LICENSE)
[![VSCode](https://img.shields.io/badge/VSCode-1.85%2B-blue)](https://code.visualstudio.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.3-blue.svg)](https://www.typescriptlang.org/)

# 🧠 StillMind Vault - Extension VSCode

**Multi-agent AI engine intégré à VS Code pour génération de code, analyse et exécution de tâches (OpenRouter).**

StillMind Vault apporte un agent IA intelligent directement dans votre éditeur, avec mémoire de session, panneau webview dédié et capacités de génération/analyse/édition de fichiers.

![Vault Panel Demo](./media/vault-demo.gif)
*(Ajoutez une capture/GIF du panneau Vault ici)*

## ✨ Fonctionnalités principales

- 🧑‍💻 **Panneau Vault** : Interface webview pour chat agent et suivi des tâches.
- ⚡ **Exécution de tâches** : Génération d'apps, analyse de code, exécution automatisée.
- 🧠 **Mémoire de session** : Contexte persistant sur les conversations (configurable).
- 🔑 **OpenRouter integration** : Support multi-LLM (gpt-4o-mini, Claude, etc.).
- 📝 **Édition automatique** : Création/édition de fichiers dans le workspace.
- 🚫 **Sécurisé** : API key locale, annulation des tâches.

## 🚀 Installation (sans Marketplace)

**Méthode recommandée #1 : Dev local (le plus simple)**
```
git clone [VOTRE-REPO-URL]
cd stillmind-vault
npm install
# Ouvrez dans VSCode, appuyez F5 → Extension testée dans nouvelle fenêtre !
```

**Méthode #2 : Générer & installer VSIX (partage)**
```
npm install -g @vscode/vsce
vsce package  # Crée stillmind-vault-0.1.0.vsix
# Puis : Ctrl+Shift+P → Install from VSIX → sélectionnez le .vsix
```

**Méthode #3 : VSCode UI**
Ctrl/Cmd + Shift + P → `Extensions: Install from VSIX...` (si vous avez le .vsix).

## 📋 Commandes disponibles

| Commande | Raccourci | Description |
|----------|-----------|-------------|
| `Stillmind: Execute Task` | - | Exécute une tâche IA (code, édition, etc.) |
| `Stillmind: Generate App` | - | Génère une app complète (fichiers + code) |
| `Stillmind: Analyze Code` | - | Analyse le fichier actif/context |
| `Stillmind: Set OpenRouter API Key` | - | Configure la clé API (stockée sécurisée) |
| `Stillmind: Clear Session Memory` | - | Vide la mémoire de conversation |

## ⚙️ Configuration (`.vscode/settings.json`)

```json
{
  \"stillmind.openRouterModel\": \"openai/gpt-4o-mini\",  // ou anthropic/claude-3.5-sonnet
  \"stillmind.maxContextMessages\": 24  // 4-100 messages en mémoire
}
```

**Obtenez une clé gratuite** : [OpenRouter.ai](https://openrouter.ai/keys)

## 🛠️ Développement & Contribution

1. Forkez le repo.
2. `npm install && npm run compile`.
3. Appuyez F5 pour tester en mode extension.
4. Implémentez, testez, PR !

### Scripts utiles
```
npm run compile     # Build TS → JS
npm run watch       # Rebuild auto
npm run lint        # ESLint
```

## 📁 Structure du projet

```
stillmind-vault/
├── src/
│   ├── agentCore.ts     # Moteur agent multi-phases
│   ├── extension.ts     # Activation VSCode
│   ├── memory.ts        # Mémoire session
│   ├── executor.ts      # Application fichiers
│   └── ui/webview.ts    # Panneau Vault
├── media/icon.svg       # Logo activitybar
├── package.json         # Manifest extension
├── tsconfig.json
└── out/                 # Build (gitignored)
```

## 🔗 Liens & Support

- 🐛 [Issues & Bugs](https://github.com/BarackNdenga/stillmind-vault-extension/issues)
- 💡 [Fonctionnalités](https://github.com/BarackNdenga/stillmind-vault-extension/discussions)
- 📖 [OpenRouter Docs](https://openrouter.ai/docs)
- 🏪 [VSCode Marketplace](https://marketplace.visualstudio.com/) (à soumettre)

Développé par [Barack Ndenga](https://github.com/BarackNdenga)  
🧠 **StillMind - L'agent qui booste votre productivité**

## 🏷️ Tags
`vscode-extension` `ai-agent` `openrouter` `code-generation` `typescript` `llm` `rag` `memory` `stillmind`

## 📜 Licence
[Apache 2.0](LICENSE) © 2026 Barack Ndenga
