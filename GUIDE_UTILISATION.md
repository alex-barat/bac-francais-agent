# Guide d'utilisation de l'agent Bac-de-Francais

## 🎯 Objectif

Cet agent GitHub Copilot vous aide à réaliser des explications de texte linéaires conformes aux exigences de l'oral du baccalauréat de français.

## ✅ Vérification de l'installation

1. **Vérifiez que l'agent est détecté** :

   - Ouvrez GitHub Copilot Chat dans VS Code (`Cmd+Shift+I` sur macOS)
   - Tapez `@` et vous devriez voir apparaître `@BacDeFrancais` dans la liste des agents disponibles

2. **Si l'agent n'apparaît pas** :
   - Vérifiez que le fichier `.github/copilot/agents/bac-fr.agent.md` existe
   - Rechargez VS Code (Cmd+Shift+P → "Developer: Reload Window")
   - Assurez-vous que vous avez la dernière version de l'extension GitHub Copilot Chat

## 📝 Comment utiliser l'agent

### Méthode 1 : Analyse d'un texte sélectionné

1. Créez ou ouvrez un fichier contenant votre extrait littéraire
2. Numérotez les lignes du texte (important pour l'analyse)
3. Sélectionnez le texte à analyser
4. Ouvrez GitHub Copilot Chat (`Cmd+Shift+I`)
5. Tapez votre demande en mentionnant l'agent :

```
@BacDeFrancais Explique ce texte de [Auteur], [Titre de l'œuvre], [Date], en appliquant la méthodologie de l'explication linéaire. Le texte appartient au parcours [nom du parcours].
```

### Méthode 2 : Demande d'aide sur la méthodologie

Vous pouvez aussi demander de l'aide sur des points spécifiques :

```
@BacDeFrancais Comment rédiger une bonne accroche pour une explication de texte du XVIIIe siècle ?
```

```
@BacDeFrancais Quels sont les procédés littéraires typiques de la poésie romantique ?
```

### Méthode 3 : Révision et amélioration

Si vous avez déjà rédigé une explication, vous pouvez demander à l'agent de l'améliorer :

```
@BacDeFrancais Améliore cette introduction en la rendant plus conforme à la méthodologie du bac :
[Votre texte]
```

## 🎓 Conseils d'utilisation

### Informations à fournir pour une analyse complète

Pour obtenir la meilleure analyse possible, précisez :

- **Auteur et titre de l'œuvre**
- **Date de publication**
- **Mouvement littéraire** (Classicisme, Romantisme, Réalisme, etc.)
- **Parcours associé** (si applicable)
- **Contexte de l'extrait** dans l'œuvre
- **Numérotation des lignes** (indispensable)

### Exemple de demande complète

```
@BacDeFrancais Analyse cet extrait de Manon Lescaut de l'abbé Prévost (1731).
Il s'agit de la première rencontre entre Des Grieux et Manon.
Parcours : personnages en marge, plaisirs du romanesque.

[Votre texte numéroté]
```

## 📚 Structure de l'analyse produite

L'agent génère une analyse complète comprenant :

### 1. Introduction

- Accroche (contexte historique et littéraire)
- Situation du passage
- Problématique (question en "Comment...")
- Annonce des mouvements (avec numéros de lignes)

### 2. Développement (2 à 4 mouvements)

Pour chaque mouvement :

- Titre explicite
- 3 effets avec procédés littéraires nommés
- Citations avec numéros de lignes
- Interprétation des procédés
- Conclusions partielles
- Transition vers le mouvement suivant

### 3. Conclusion

- Bilan de l'analyse
- Ouverture vers une autre œuvre ou un autre mouvement

## 🔍 Exemples d'utilisation

Consultez les fichiers dans le dossier `examples/` :

- `examples/input/` : textes à analyser
- `examples/output/` : analyses complètes produites par l'agent

Vous pouvez aussi utiliser le fichier `TEST.md` à la racine du projet pour tester rapidement l'agent.

## ❓ Résolution de problèmes

### L'agent ne répond pas correctement

- Vérifiez que vous avez bien mentionné `@BacDeFrancais` dans votre message
- Assurez-vous que le texte est sélectionné avant d'envoyer la demande
- Fournissez plus de contexte (auteur, date, mouvement littéraire)

### L'agent n'apparaît pas dans la liste

- Rechargez VS Code (Cmd+Shift+P → "Developer: Reload Window")
- Vérifiez que le fichier `.github/copilot/agents/bac-fr.agent.md` n'a pas d'erreurs
- Assurez-vous d'avoir la dernière version de GitHub Copilot Chat

### L'analyse manque de détails

- Précisez davantage votre demande
- Fournissez le contexte de l'œuvre et du parcours
- Demandez explicitement plus de détails sur un mouvement spécifique

## 💡 Astuces

- **Pour la lecture expressive** : Demandez à l'agent de baliser le texte pour la lecture à voix haute
- **Pour les fiches de révision** : Demandez une version synthétique de l'analyse
- **Pour les procédés** : Demandez d'identifier uniquement les procédés littéraires si vous voulez vous entraîner à les interpréter vous-même

## 📞 Support

Pour signaler un problème ou suggérer une amélioration :

- Ouvrez une issue sur GitHub : [github.com/alex-barat/bac-francais-agent](https://github.com/alex-barat/bac-francais-agent)

Bon courage pour vos révisions ! 🎓📚
