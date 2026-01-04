# Agent Bac de Français 📚

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Copilot](https://img.shields.io/badge/GitHub%20Copilot-Agent-blue?logo=github)](https://github.com/features/copilot)
[![Status](https://img.shields.io/badge/status-stable-green)]()
[![Language](https://img.shields.io/badge/language-Français-blue)]()

Agent GitHub Copilot spécialisé dans l'explication de texte linéaire pour l'oral du baccalauréat de français.

## ✨ Fonctionnalités

- Analyse linéaire méthodique suivant les exigences du bac
- Structure en mouvements avec identification des procédés littéraires
- Introduction, développement et conclusion conformes à la méthodologie officielle
- Exemples de référence intégrés

## 🚀 Installation

### Prérequis

- Visual Studio Code
- Extension GitHub Copilot Chat
- Accès aux Agents GitHub Copilot

### Configuration

1. Clonez ce dépôt :

```bash
git clone https://github.com/alex-barat/bac-francais-agent.git
cd bac-francais-agent
```

2. Ouvrez le projet dans VS Code :

```bash
code .
```

3. L'agent sera automatiquement détecté par GitHub Copilot

## 📖 Utilisation

### Dans VS Code

1. Ouvrez un fichier texte contenant l'extrait à analyser
2. Sélectionnez le texte à analyser
3. Ouvrez GitHub Copilot Chat (`Ctrl+Shift+I` ou `Cmd+Shift+I`)
4. Tapez `@Bac-de-Francais` suivi de votre demande, par exemple :
   - `@Bac-de-Francais Explique ce texte en appliquant la méthodologie de l'explication linéaire`
   - `@Bac-de-Francais Propose une analyse complète avec introduction, développement et conclusion`

### Documentation complète

📘 Consultez le [Guide d'utilisation détaillé](GUIDE_UTILISATION.md) pour :

- Vérifier l'installation
- Découvrir toutes les façons d'utiliser l'agent
- Résoudre les problèmes courants
- Obtenir des astuces et conseils

### Exemple rapide

Voir le fichier [`TEST.md`](TEST.md) pour tester l'agent rapidement, ou le dossier [`examples/`](examples/) pour des exemples d'utilisation complets.

## 🎯 Méthodologie

L'agent suit rigoureusement la méthodologie de l'explication linéaire :

- **Introduction** : accroche, situation, problématique, annonce des mouvements
- **Développement** : analyse linéaire par mouvements (2-4 mouvements)
- **Conclusion** : bilan et ouverture

Pour plus de détails, consultez [methode_expli_texte.md](.github/copilot/agents/methode_expli_texte.md).

## 📚 Exemples intégrés

L'agent s'appuie sur des exemples de référence :

- [Manon Lescaut - Première rencontre](.github/copilot/agents/docs/manon_lescaut_premiere_rencontre.md)

## 🤝 Contribution

Les contributions sont les bienvenues ! Pour ajouter des exemples :

1. Forkez le projet
2. Créez une branche (`git checkout -b feature/nouvel-exemple`)
3. Ajoutez votre exemple dans `.github/copilot/agents/docs/`
4. Commitez (`git commit -m 'Ajout exemple [titre]'`)
5. Pushez (`git push origin feature/nouvel-exemple`)
6. Ouvrez une Pull Request

## 📝 License

Ce projet est sous licence MIT. Voir [LICENSE](LICENSE) pour plus de détails.

## 👥 Auteurs

- Alexandre Barat - [@alex-barat](https://github.com/alex-barat)

## 🙏 Remerciements

Basé sur la méthodologie officielle de l'Éducation Nationale française.
