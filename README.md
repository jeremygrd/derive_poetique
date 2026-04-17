# Dérive Poétique

**Dérive Poétique** est une application web expérimentale qui transforme progressivement un texte, mot par mot, à l’aide de modèles de langage masqués exécutés directement dans le navigateur.

L’application procède par **substitutions locales contrôlées** : elle sélectionne certains mots du texte, cherche des remplaçants plausibles dans leur contexte, puis les remplace selon un degré d’éloignement sémantique réglable.

L’objectif est de produire une **dérive lexicale progressive** : à mesure que les passes s’accumulent, le texte peut s’éloigner fortement de sa version d’origine tout en conservant, au moins localement, une certaine cohérence grammaticale et contextuelle.

## Fonctionnement

Pour chaque mot sélectionné, l’application :

1. détecte la langue du texte ;
2. choisit automatiquement un modèle adapté ;
3. masque localement un mot dans son contexte ;
4. récupère des candidats plausibles avec un modèle de type BERT / CamemBERT ;
5. filtre et classe ces candidats ;
6. choisit un remplaçant selon les paramètres définis par l’utilisateur ;
7. répète l’opération sur une ou plusieurs passes.

## Paramètres disponibles

L’interface permet de régler :

- **le pourcentage de mots à modifier** ;
- **la distance sémantique** entre le mot d’origine et le mot de remplacement ;
- **le nombre de passes** successives ;
- **la stratégie de transformation** d’une passe à l’autre ;
- l’**affichage des substitutions**.

Plus le nombre de passes est élevé, plus le texte final peut devenir éloigné du texte initial.

## Détection de langue

L’application détecte automatiquement la langue du texte saisi et sélectionne le modèle le plus approprié :

- **français** → modèle de type CamemBERT  
- **anglais** → modèle de type BERT  
- **autres cas** → modèle multilingue

## Cas d’usage

Cette application est particulièrement adaptée pour :

- explorer des transformations poétiques ou littéraires ;
- produire des variations lexicales contrôlées ;
- faire dériver progressivement un texte vers une version plus étrangère, plus décalée ou plus abstraite ;
- expérimenter avec la matière verbale comme outil de création.

## Utilisation

1. Collez ou écrivez un texte dans la zone principale.
2. Réglez les paramètres de transformation.
3. Lancez la dérive.
4. Observez l’évolution du texte passe après passe.
5. Relancez avec d’autres réglages pour explorer d’autres trajectoires.

## Important

- L’application fonctionne **entièrement dans le navigateur**.
- Elle ne nécessite **pas de backend dédié**.
- Le premier chargement peut être plus long, car les modèles sont téléchargés localement.
- Les lancements suivants sont généralement plus rapides grâce au cache du navigateur.


## Limites

Dérive Poétique ne produit pas une paraphrase parfaite ni une réécriture “intelligente” au sens humain du terme.  
Les résultats dépendent :

- du modèle utilisé ;
- de la langue détectée ;
- du contexte local ;
- des heuristiques de sélection des remplaçants.

Le résultat doit donc être compris comme une **expérimentation de dérive textuelle contrôlée**, et non comme un outil de correction ou de reformulation classique.
