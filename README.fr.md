<p align="center"><a href="https://bestimage.ai/"><img src="assets/bestimage-logo.svg" width="72" alt="Logo de bestimage.ai"></a></p>

# Awesome Wan 3.0 Prompts — Guide français

**148 consignes de réalisation vidéo réparties en 14 catégories, adaptées et maintenues par l’équipe [bestimage.ai](https://bestimage.ai/).** Définissez un événement clair, attribuez un rôle aux éléments fournis, puis dirigez la caméra, le son et la continuité.

[Guide anglais](README.md) · [Les 15 langues](locales/README.md) · [Index complet](prompts/README.md) · [Contribuer](CONTRIBUTING.md)

![Illustration conceptuelle : un archiviste déplie une carte du ciel dans un observatoire à l’aube](assets/wan-3-prompt-collection-hero.png)

*Illustration fixe créée avec l’outil intégré de génération d’images, et non une vidéo produite par Wan 3.0. Voir les [consignes d’illustration et leur provenance](assets/README.md).*

## Contenu et premiers pas

**148 consignes de réalisation vidéo réparties en 14 catégories**. Les six premières catégories contiennent des consignes en chinois, les huit autres en anglais. Les 15 langues concernent les guides d’accueil et un exemple comparatif commun, **pas la traduction intégrale des 148 consignes**. Les traductions et l’exemple comparatif ne sont pas comptés comme des entrées supplémentaires.

1. Choisissez une consigne dans l’[index complet](prompts/README.md).
2. Adaptez les variables et préparez chaque élément requis. Les références indiquent des rôles ; leurs fichiers ne sont pas fournis dans ce dépôt.
3. Choisissez le mode approprié et réglez durée, format, résolution et son dans l’interface. Le texte seul ne configure pas une requête API.
4. Faites un essai limité, puis examinez l’action, la géométrie, l’identité, le rythme et le son selon les critères de la consigne.

## Formule en huit couches

```text
[Sortie] durée + format + médium visuel
[Sujet] repères d’identité réutilisables + détails immuables
[Univers] moment + lieu + météo + profondeur spatiale
[Action] déclencheur → mouvement continu → résultat visible
[Caméra] valeur de plan + angle + un trajet + cadre final
[Aspect] lumière + palette + matières + rendu du mouvement
[Son] ambiance + bruitages + musique + dialogue
[Contraintes] éléments à préserver + erreurs les plus probables
```

Employez une langue principale pour la description visuelle et précisez séparément la langue et les répliques exactes du dialogue. Les possibilités et réglages dépendent du produit, de la région et de la plateforme.

## Exemple comparatif complet

**Mode :** texte vers vidéo · **Réglages :** 10 secondes, 16:9, son activé · **Entrées :** aucune

```text
Créez un plan documentaire de 10 secondes au format 16:9 dans une bibliothèque d’outils de quartier au calme. Une personne adulte bénévole, aux cheveux courts et bouclés, portant un tablier moutarde et une chemise bleu marine aux manches retroussées, répare un petit ventilateur de bureau rouge débranché. De 0 à 3 secondes, elle pose la grille de protection démontée à côté du ventilateur immobile. De 3 à 7 secondes, elle essuie la poussière sur une pale avec un chiffon doux pendant que la caméra glisse lentement vers la droite à hauteur du plateau de la table. De 7 à 10 secondes, elle pose le chiffon et aligne la grille avec le boîtier, sans brancher ni mettre en marche le ventilateur. La lumière de la fenêtre révèle le métal usé et la texture du coton. Son : frottement du chiffon, un léger clic de la grille, ambiance calme de la pièce ; ni parole ni musique. Conservez la même personne, le même ventilateur, ses trois pales, son boîtier rouge et son câble débranché. Aucune pale en rotation, aucun outil supplémentaire, aucune étiquette lisible, aucun sous-titre ni aucune coupe.
```

**Variables :** couleur du tablier, couleur du ventilateur, éclairage de la pièce. **Contrôle :** le ventilateur reste débranché et immobile ; le nombre de pales et le contact des mains restent cohérents. Il s’agit d’un concept créatif, pas d’une instruction de réparation électrique.

## API Wan 3.0 sur bestimage.ai

Ces pages en anglais présentent l’interface d’essai et les exemples publics de requêtes.

| Mode | Préparation et objectif |
|---|---|
| [Texte vers vidéo](https://bestimage.ai/models/alibaba/wan-3-0-text-to-video/) | Une scène complète avec une cause, une action intermédiaire et un résultat visible. |
| [Image vers vidéo](https://bestimage.ai/models/alibaba/wan-3-0-image-to-video/) | Une image initiale **et une image finale** pour le mode documenté ; décrire la transition et préserver géométrie et composition. |
| [Références vers vidéo](https://bestimage.ai/models/alibaba/wan-3-0-reference-to-video/) | Références facultatives d’identité, d’objet, d’espace, de mouvement ou de son ; un rôle par ressource. |
| [Modification vidéo](https://bestimage.ai/models/alibaba/wan-3-0-video-edit/) | Un extrait source et une modification délimitée ; préserver le jeu, la durée, la caméra et les zones inchangées. |

Le [guide API et maîtrise des coûts](guides/bestimage-wan-3-api.md) explique les requêtes, le suivi des tâches et la planification des essais. **Le serveur d’API de bestimage.ai est `https://api.flaq.ai`.** Utilisez une clé d’API émise depuis votre compte bestimage.ai.

Consultez la page du modèle et votre compte avant de consommer des crédits. Ces modes correspondent à la documentation bestimage.ai, sans garantir que tous les produits Wan proposent les mêmes commandes.

## GPT Image 2 pour préparer les images de référence

[GPT Image 2](https://bestimage.ai/models/openai/gpt-image-2/) génère des images fixes ; [GPT Image 2 Edit](https://bestimage.ai/models/openai/gpt-image-2-edit/) modifie des images et combine des références visuelles. Ils permettent de préparer une fiche de personnage, une référence produit ou des compositions initiale et finale validées avant une tâche vidéo.

Ce sont **des modèles d’image distincts**, pas des interfaces vidéo Wan. Exportez et examinez les images avant de les fournir au mode Wan adapté. Le dépôt n’automatise pas cette transmission et n’affirme pas que ses illustrations conceptuelles proviennent de ces API. Consultez le [processus de préparation des références](guides/bestimage-wan-3-api.md#gpt-image-2-reference-frame-workflow).

## Navigation, guides et contributions

L’[index des 148 consignes](prompts/README.md) couvre le récit cinématographique, les produits, les contenus de créateurs, l’alimentation et les voyages, le sport, l’animation, la musique, les services, les sciences, l’architecture, la production, le commerce, les dialogues, la nature et l’industrie.

Les guides de [rédaction](guides/prompting-guide.md), de [capacités et limites](guides/model-capabilities.md) et de [dépannage](guides/troubleshooting.md) sont en chinois simplifié. Le guide API est en anglais. Une image conceptuelle ne démontre ni continuité temporelle, ni synchronisation labiale, ni précision du modèle, ni sécurité du procédé représenté.

Consultez les [consignes de contribution](CONTRIBUTING.md) avant de partager un texte ou un média. Indiquez les réglages exacts, le rôle des entrées, les droits d’utilisation, vos observations et un statut testé ou non testé fidèle à la réalité. Ne partagez aucun identifiant secret, document privé ou lien signé vers un média qui expire. Utilisez le [formulaire de contribution](.github/ISSUE_TEMPLATE/prompt.yml) pour préparer les informations requises.

## À propos de bestimage.ai

L’équipe [bestimage.ai](https://bestimage.ai/) sélectionne et maintient cette bibliothèque de prompts, qui relie les pratiques de création aux API de modèles d’image et de vidéo.

## Gagnez des commissions avec bestimage.ai

Vous publiez des tutoriels, des prompts ou des intégrations d’API ? Rejoignez le [programme d’affiliation bestimage.ai](https://bestimage.ai/affiliate-program/) et recevez des commissions en recommandant bestimage.ai à votre public.

- **20 %** sur la première commande payante admissible d’un utilisateur parrainé.
- **10 %** sur ses commandes payantes admissibles suivantes, effectuées dans les **60 jours après son inscription**.

L’admissibilité des commandes et les versements sont régis par l’[accord d’affiliation en vigueur](https://bestimage.ai/affiliate-agreement/).

## Licence

[MIT](LICENSE).
