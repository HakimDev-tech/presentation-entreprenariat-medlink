# MedLink DZ — Présentation entrepreneuriale

Présentation interactive de **32 diapositives**, conçue comme un PowerPoint piloté par le présentateur. Le passage d'une diapositive à l'autre est toujours manuel : aucune lecture automatique.

## Présenter

- **→ / Espace / Page suivante** : diapositive suivante
- **← / Page précédente** : diapositive précédente
- **Home / End** : première / dernière diapositive
- **F** : plein écran
- **G** : vue d'ensemble et accès direct à une diapositive
- **?** ou **/** : aide clavier
- **Échap** : fermer la vue d'ensemble ou quitter le plein écran
- Sur écran tactile : balayage horizontal

Les animations d'entrée, graphiques, particules et éléments WebGL ne changent jamais la diapositive à ta place.

## Structure du deck

| Diapositives | Partie | Responsable |
|---|---|---|
| 01 | Couverture | Collectif |
| 02–06 | Identification du problème | Salma Mazari |
| 07–11 | Étude du marché | Mezeghrane Imane |
| 12–16 | Concurrence | Massout Imane |
| 17–21 | Conception de la solution | KOUMAD Abdelhakim |
| 22–26 | Modèle économique | Ya Yacine |
| 27–31 | Étude juridique | Rafiq Kherchaoui |
| 32 | Conclusion | Collectif |

## Images à ajouter

Les images sont facultatives. Si un fichier n'existe pas, un emplacement de remplacement reste visible. Ajoute les images avec les noms exacts suivants :

- `assets/images/cover-medlink.webp`
- `assets/images/patient-dashboard.png`
- `assets/images/doctor-dashboard.png`
- `assets/images/admin-dashboard.png`
- `assets/images/architecture.png`

Tu peux ensuite ajouter des visuels d'enquête et de concurrence dans :

- `assets/images/survey/`
- `assets/images/competition/`

Les chemins sont relatifs à la racine du dépôt. Après ajout et commit, les images apparaîtront automatiquement au prochain chargement de la présentation.

## Technologie

- HTML sémantique, CSS responsive et JavaScript natif en modules ES.
- Navigation clavier et tactile, vue d'ensemble, plein écran et progression.
- Canvas 2D pour le champ de particules.
- Three.js / WebGL pour l'objet 3D d'ambiance, avec repli CSS si WebGL n'est pas disponible.
- Animations CSS et transitions JavaScript déclenchées au changement manuel de diapositive.
- Mode impression 16:9 pour export PDF depuis le navigateur.

Three.js est chargé depuis jsDelivr et les polices depuis Google Fonts. Pour un fonctionnement totalement hors ligne, il faudra héberger localement ces dépendances.

## Déploiement GitHub Pages

Le workflow `.github/workflows/deploy.yml` publie le contenu de la branche `main` sur GitHub Pages à chaque push.

**Activation initiale requise (une seule fois) :** ouvre [Settings → Pages](https://github.com/HakimDev-tech/presentation-entreprenariat-medlink/settings/pages), puis sélectionne **GitHub Actions** dans « Build and deployment → Source ». Le jeton de cette session ne dispose pas du droit administratif nécessaire pour créer le site Pages à ta place. Après cette activation, le workflow publiera automatiquement le site à chaque push sur `main`.

URL cible : https://hakimdev-tech.github.io/presentation-entreprenariat-medlink/

## Périmètre et exactitude des informations

Les données d'enquête et hypothèses financières sont reprises du dossier fourni par l'équipe. La taille de l'échantillon, sa méthode de recrutement et la date de collecte n'étant pas documentées dans les éléments disponibles, les pourcentages sont présentés comme des résultats exploratoires, pas comme des statistiques représentatives de tous les médecins algériens.

Les coûts, prix, revenus, ROI et seuil de rentabilité sont des hypothèses de scénario, non des résultats commerciaux garantis. Les fonctionnalités futures ne sont pas présentées comme déjà opérationnelles. Le produit ne réalise ni diagnostic, ni prescription, ni décision clinique autonome.

Les références juridiques sont des pistes de cadrage qui nécessitent une validation par un professionnel du droit algérien avant tout lancement public. Le deck ne prétend pas qu'une autorisation, une conformité complète ou un label startup ont déjà été obtenus.

## Modifier le contenu

Le tableau `slides` et le moteur de navigation sont dans `assets/js/app.js`. Les styles et composants visuels sont dans `assets/css/styles.css`. Le point d'entrée est `index.html`.

Pour modifier une diapositive, éditer son objet dans `slides` sans changer l'ordre ou le nombre d'entrées, sauf décision explicite de l'équipe.
