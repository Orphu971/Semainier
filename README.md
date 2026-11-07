# Semainier

Application web pour téléphone : l'emploi du temps de la semaine en grille, avec un tiroir de tâches classées par catégorie, à glisser au doigt dans la semaine.

Style « Nuit wax » : fond brun sombre, couleurs d'inspiration africaine.

## Fonctions

- Grille de la semaine (lundi → dimanche, 7h → 21h), jour actuel mis en relief, ligne de l'heure actuelle.
- Cours fixes par jour et par semaine A / B / les deux, verrouillés dans la grille.
- Tâches en 5 catégories : Activité professionnelle (indigo), Maison (terre cuite), Activités et loisirs (vert palme), Administratif (ocre), Santé (bordeaux).
- Glisser-déposer : appui long sur une carte ou un bloc, puis glisser. Pas de 15 minutes, créneau vert (libre) ou rouge (occupé). Glisser vers le tiroir pour retirer de la semaine.
- « Caser » : place automatiquement les tâches du tiroir dans les trous de la semaine (8h–19h), en respectant les échéances.
- Barre d'équilibre du temps par catégorie (touchable pour mettre une catégorie en avant).
- Bouton « Annuler » après chaque action.
- Les tâches non faites d'un jour passé reviennent dans le tiroir.
- Fonctionne hors ligne et s'installe sur l'écran d'accueil (PWA).

## Données

Tout est enregistré **dans le navigateur du téléphone** (localStorage). Rien n'est envoyé sur un serveur.
Dans « Mes cours » (icône calendrier), utilisez **Sauvegarder dans un fichier** pour garder une copie, et **Restaurer une sauvegarde** pour la recharger (changement de téléphone, nettoyage du navigateur…).

## Mise en ligne avec GitHub Pages

1. Créez un dépôt sur GitHub (par exemple `semainier`).
2. Déposez-y tous les fichiers de ce dossier (bouton **Add file → Upload files**).
3. Dans **Settings → Pages**, choisissez **Deploy from a branch**, branche `main`, dossier `/ (root)`, puis **Save**.
4. Après une ou deux minutes, l'appli est disponible à l'adresse `https://<votre-identifiant>.github.io/semainier/`.
5. Sur le téléphone Android, ouvrez cette adresse dans Chrome, puis menu ⋮ → **Ajouter à l'écran d'accueil**.

## Fichiers

| Fichier | Rôle |
|---|---|
| `index.html` | L'application complète |
| `manifest.webmanifest` | Nom, couleurs et icônes pour l'installation |
| `sw.js` | Fonctionnement hors ligne |
| `icon.svg`, `icon-192.png`, `icon-512.png` | Icônes |

## Mettre à jour

Remplacez `index.html` dans le dépôt. Pour forcer les téléphones à recharger les fichiers en cache, changez aussi `semainier-v1` en `semainier-v2` dans `sw.js`.
