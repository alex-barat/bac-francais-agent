# ✅ Checklist de vérification de l'agent

## Étapes de vérification

### 1. ✅ Structure des fichiers

- [x] `.github/copilot/agents/bac-fr.agent.md` existe
- [x] Pas d'erreurs de syntaxe dans le fichier agent
- [x] Fichiers de documentation en place

### 2. 🧪 Test de l'agent

#### A. Vérifier que l'agent est détecté

1. Ouvrez GitHub Copilot Chat dans VS Code :

   - Raccourci : `Cmd+Shift+I` (macOS) ou `Ctrl+Shift+I` (Windows/Linux)

2. Dans le chat, tapez `@` et vérifiez que `@Bac-de-Francais` apparaît dans la liste

3. Si l'agent n'apparaît pas :
   - Rechargez VS Code : `Cmd+Shift+P` → "Developer: Reload Window"
   - Attendez quelques secondes que l'extension se charge
   - Réessayez

#### B. Test simple

1. Ouvrez le fichier `TEST.md`
2. Sélectionnez le poème de Victor Hugo (lignes 10-21)
3. Ouvrez GitHub Copilot Chat (`Cmd+Shift+I`)
4. Tapez exactement :

```
@Bac-de-Francais Explique ce texte en appliquant la méthodologie de l'explication linéaire.
C'est un poème de Victor Hugo, "Demain dès l'aube" extrait des Contemplations (1856),
parcours "Les Mémoires d'une âme".
```

5. Vérifiez que la réponse contient :
   - Une introduction avec accroche, situation, problématique et annonce
   - Un développement en plusieurs mouvements
   - Des procédés littéraires nommés (métaphore, anaphore, etc.)
   - Des citations avec numéros de lignes
   - Une conclusion avec bilan et ouverture

#### C. Test avec un extrait de prose

1. Ouvrez `examples/input/extrait_prevost_manon_lescault.txt`
2. Sélectionnez tout le texte
3. Tapez :

```
@Bac-de-Francais Analyse cet extrait de Manon Lescaut de l'abbé Prévost (1731).
Il s'agit de la première rencontre entre Des Grieux et Manon.
```

4. Comparez avec l'exemple fourni dans `examples/output/` (si disponible)

### 3. 🎯 Tests avancés

#### Test de la méthodologie

Demandez à l'agent :

```
@Bac-de-Francais Explique-moi comment rédiger une bonne problématique pour une explication de texte
```

#### Test de correction

Envoyez une introduction mal rédigée et demandez :

```
@Bac-de-Francais Améliore cette introduction en la rendant conforme à la méthodologie du bac :

Au 19e siècle, Victor Hugo écrit des poèmes. Ce texte parle de sa fille.
C'est triste. Je vais analyser le texte.
```

#### Test sur des procédés

```
@Bac-de-Francais Quels sont les procédés littéraires typiques de la poésie romantique ?
```

## ❌ Problèmes courants et solutions

### L'agent n'apparaît pas dans la liste

**Solution 1** : Vérifier le fichier agent

```bash
cat .github/copilot/agents/bac-fr.agent.md | head -5
```

Devrait afficher :

```
---
name: Bac-de-Francais
description: Agent expert pour...
---
```

**Solution 2** : Recharger VS Code

- `Cmd+Shift+P` (macOS) ou `Ctrl+Shift+P` (Windows/Linux)
- Taper : "Developer: Reload Window"
- Attendre 10-20 secondes

**Solution 3** : Vérifier l'extension

- Ouvrir Extensions (`Cmd+Shift+X`)
- Chercher "GitHub Copilot Chat"
- Vérifier qu'elle est installée et à jour

### L'agent répond mais pas de façon pertinente

**Problème** : Contexte insuffisant

**Solution** : Fournir plus d'informations :

- Auteur et titre exact
- Date de publication
- Mouvement littéraire
- Parcours associé (le cas échéant)
- Contexte de l'extrait dans l'œuvre

### L'analyse manque de détails

**Solution** : Demander explicitement plus de détails

```
@Bac-de-Francais Développe davantage le mouvement 2 en ajoutant plus de procédés
littéraires et d'interprétations
```

### Les numéros de lignes ne correspondent pas

**Problème** : Le texte n'est pas numéroté ou mal numéroté

**Solution** : Numéroter manuellement le texte :

```
1. La veille même de celui que je devais quitter cette ville,
2. étant à me promener avec mon ami, qui s'appelait Tiberge,
3. nous vîmes arriver le coche d'Arras...
```

## 📊 Critères de succès

L'agent fonctionne correctement si :

- ✅ Il apparaît dans la liste des agents avec `@`
- ✅ Il génère une introduction structurée (accroche, situation, problématique, annonce)
- ✅ Il identifie et nomme précisément les procédés littéraires
- ✅ Il interprète les procédés (pas seulement les liste)
- ✅ Il cite le texte avec les numéros de lignes
- ✅ Il structure l'analyse en mouvements cohérents
- ✅ Il propose une conclusion avec bilan et ouverture
- ✅ Il maintient un niveau de langue soutenu

## 📝 Notes de test

Date du test : ****\_\_\_****

Résultat :

- [ ] Agent détecté dans la liste
- [ ] Test simple réussi (poésie)
- [ ] Test avec prose réussi
- [ ] Méthodologie respectée
- [ ] Qualité de l'analyse satisfaisante

Problèmes rencontrés :

```
[À compléter]
```

Actions correctives :

```
[À compléter]
```

---

**Si tous les tests passent, l'agent est prêt à être utilisé ! 🎉**

Consultez le [Guide d'utilisation](GUIDE_UTILISATION.md) pour plus d'informations.
