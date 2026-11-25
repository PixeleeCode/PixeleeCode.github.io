# Guide GTA VI — application web

## GitHub Pages
1. Extraire ce ZIP. Copier **tous** les fichiers à la racine du dépôt (pas le dossier parent).
2. Committer et laisser GitHub Pages déployer depuis main / root.
3. Garder la même URL pour récupérer les anciennes cases du navigateur. Avant de mettre à jour, exporter la progression.
4. Après première visite en HTTPS, le service worker met les fichiers en cache. Si une mise à jour est publiée, fermer tous les onglets du guide et rouvrir. Sur iPhone : Safari > Partager > Sur l’écran d’accueil. Les liens de soluce et vidéos restent en ligne.

## Données et progression
- data.json : fiches, sources, chapitres et vues. Ne jamais changer un identifiant existant ; les étapes ont aussi des identifiants stables.
- changelog.json : versions et nouveautés. `added` contient la date d’ajout d’une fiche.
- app.js : interactions. styles.css : interface.
- sw.js : cache hors ligne ; modifier CACHE à chaque publication et conserver la liste des ressources.
- Les anciennes sauvegardes v1 sont migrées automatiquement sur la même origine ; l’import v1 crée une partie séparée. Export v2 = toutes les parties, notes, favoris et étapes. L’import v2 remplace les parties après confirmation.
- Aucun serveur, compte ni synchronisation automatique. Transfert via fichier JSON (iCloud Drive, OneDrive, etc.). Les fichiers contiennent les notes personnelles : ne pas les publier dans le dépôt.
- Chapitre actuel déclaré manuellement : les alertes ne marquent jamais une fiche manquée automatiquement. Filtres de personnage et localisations partiels ; aucune coordonnée inventée. Étapes et liens vidéo sur une sélection documentée.
- Le badge Nouveau signifie ajouté au guide, pas nécessairement découvert ce jour. Les données antérieures sont conservées sans audit intégral.
