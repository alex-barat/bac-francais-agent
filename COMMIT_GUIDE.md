# 📝 Guide de commit des corrections

## Fichiers modifiés et nouveaux

### Fichiers modifiés ✏️

- `.github/copilot/agents/bac-fr.agent.md` - Corrigé (syntaxe + structure)
- `README.md` - Mis à jour (instructions d'utilisation)
- `examples/input/extrait_prevost_manon_lescault.txt` - (modifications à vérifier)

### Nouveaux fichiers ✨

- `.vscode/settings.json` - Configuration VS Code
- `CORRECTIONS.md` - Documentation des corrections
- `GUIDE_UTILISATION.md` - Guide utilisateur complet
- `TEST.md` - Fichier de test rapide
- `VERIFICATION.md` - Checklist de vérification

## Commandes Git recommandées

### Option 1 : Commit tout en une fois

```bash
cd /Users/alexandre.barat/Documents/perso/iker/agent-fr

# Ajouter tous les fichiers
git add .

# Commit avec message détaillé
git commit -m "fix: Correction de l'agent Bac-de-Francais pour VS Code

- Correction de la syntaxe du fichier agent (suppression bloc markdown)
- Suppression des attributs non supportés (id, files, slashCommands)
- Renommage de l'agent en Bac-de-Francais (sans caractères spéciaux)
- Intégration complète de la méthodologie dans le fichier agent
- Ajout de documentation complète (guide, vérification, test)
- Configuration VS Code optimisée
- Mise à jour du README avec nouvelles instructions

L'agent est maintenant entièrement fonctionnel dans VS Code."

# Pusher vers GitHub
git push origin main
```

### Option 2 : Commits séparés (plus détaillé)

```bash
cd /Users/alexandre.barat/Documents/perso/iker/agent-fr

# 1. Correction de l'agent
git add .github/copilot/agents/bac-fr.agent.md
git commit -m "fix(agent): Correction syntaxe et structure pour VS Code

- Suppression du bloc markdown autour du frontmatter
- Suppression des attributs non supportés (id, files, slashCommands)
- Renommage en Bac-de-Francais
- Intégration complète de la méthodologie
- Ajout d'exemple complet (Manon Lescaut)"

# 2. Documentation
git add GUIDE_UTILISATION.md VERIFICATION.md TEST.md CORRECTIONS.md
git commit -m "docs: Ajout de documentation complète

- Guide d'utilisation détaillé
- Checklist de vérification
- Fichier de test rapide
- Documentation des corrections"

# 3. Configuration
git add .vscode/settings.json
git commit -m "chore: Configuration VS Code optimisée"

# 4. README
git add README.md
git commit -m "docs: Mise à jour des instructions d'utilisation

- Correction des commandes (@BacDeFrancais au lieu de @bac-fr /expliquer)
- Ajout de liens vers la documentation"

# 5. Autres modifications
git add examples/input/extrait_prevost_manon_lescault.txt
git commit -m "fix: Correction du texte d'exemple"

# Pusher tous les commits
git push origin main
```

## Message de commit recommandé (si tout en une fois)

```
fix: Correction de l'agent Bac-de-Francais pour VS Code

Problèmes corrigés :
- ❌ Syntaxe invalide : bloc markdown autour du frontmatter YAML
- ❌ Attributs non supportés : id, files, slashCommands
- ❌ Nom avec caractères spéciaux : Bac de Français (Explication Linéaire)
- ❌ Structure inadaptée à VS Code

Corrections apportées :
- ✅ Frontmatter YAML correct (sans bloc de code)
- ✅ Attributs valides uniquement (name, description)
- ✅ Nom conforme : Bac-de-Francais
- ✅ Méthodologie intégrée directement dans l'agent
- ✅ Exemple complet (Manon Lescaut) dans le fichier

Documentation ajoutée :
- ✅ GUIDE_UTILISATION.md : guide complet
- ✅ VERIFICATION.md : checklist de tests
- ✅ TEST.md : test rapide avec poème de Victor Hugo
- ✅ CORRECTIONS.md : résumé des corrections
- ✅ .vscode/settings.json : configuration optimale

Utilisation :
Avant : @bac-fr /expliquer
Après : @BacDeFrancais + votre demande

L'agent fonctionne maintenant correctement dans GitHub Copilot Chat (VS Code).
```

## Vérification avant de commit

Avant de commit, vérifiez :

```bash
# Aucune erreur
code --status

# L'agent est valide
cat .github/copilot/agents/bac-fr.agent.md | head -10

# Devrait afficher :
# ---
# name: Bac-de-Francais
# description: Agent expert...
# ---
```

## Après le commit

1. **Vérifier sur GitHub** : Allez sur votre repo et vérifiez que tous les fichiers sont bien présents

2. **Tester l'agent** :

   - Ouvrez VS Code
   - Rechargez la fenêtre : `Cmd+Shift+P` → "Developer: Reload Window"
   - Ouvrez le chat Copilot : `Cmd+Shift+I`
   - Tapez `@` et vérifiez que `@BacDeFrancais` apparaît

3. **Suivre la vérification** : Utilisez `VERIFICATION.md` pour une vérification complète

## Notes importantes

- 🔥 **Ne pas oublier de pusher** : `git push origin main`
- 📝 **Mettre à jour le README sur GitHub** si nécessaire
- ✅ **Vérifier que l'agent fonctionne** avant de clore le travail
- 🎯 **Suivre VERIFICATION.md** pour confirmer que tout est opérationnel

## En cas de problème

Si après le commit l'agent ne fonctionne toujours pas :

1. Vérifier qu'il n'y a pas d'erreurs de syntaxe : consultez les erreurs VS Code
2. Recharger VS Code : `Cmd+Shift+P` → "Developer: Reload Window"
3. Vérifier la structure du fichier agent avec `cat .github/copilot/agents/bac-fr.agent.md | head -20`
4. Consulter `VERIFICATION.md` pour le dépannage

---

**Prêt à commit ? Suivez les commandes ci-dessus ! 🚀**
