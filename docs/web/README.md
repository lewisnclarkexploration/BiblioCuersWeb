# Bienvenue dans la documentation de Biblio Cuers

Site statique HTML + CSS, sans JavaScript. Chaque page s'ouvre dans un navigateur
(`index.html` pour commencer) et se convertit en PDF via « Imprimer → Enregistrer en PDF ».

## Structure

- `index.html` : présentation générale (les atouts et les 5 besoins concrets).
- `carte-adherent.html`, `prets-echances.html`, `rappels-notifications.html`,
  `decouvrir-livres.html`, `listes-favoris-a-lire.html`, `deja-lu.html` : une page par
  fonctionnalité.
- `assets/style.css` : habillage partagé (vert de l'application).
- `assets/captures/` : les captures d'écran des pages, déjà insérées (cliquables pour un grand format).

## Captures d'écran déjà en place

| Fichier | Page |
|---|---|
| `capture_CarteNumerique.png` | Carte d'adhérent (la carte numérique) |
| `capture_Setings.png` | Carte d'adhérent (les réglages) |
| `capture_MesPrets.png` | Prêts (liste des prêts) |
| `capture_RéglagesNotification.png` | Rappels (réglage des rappels) |
| `capture_Recherche01.png` / `capture_Recherche02.png` | Découvrir (résultat d'un scan) |
| `capture_Favoris.png` | Favoris &amp; À lire (liste des favoris) |
| `capture_DejaLus.png` | Déjà lu (mémoire des emprunts) |

## Ajouter une nouvelle capture plus tard

Déposez le PNG dans `assets/captures/`, puis insérez dans la page voulue la miniature **et** sa
popup d'agrandissement (les images sont cliquables — popup CSS sans JavaScript) :

```html
<figure>
  <a class="shot-link" href="#shot-mon-image" aria-label="Agrandir la capture">
    <img class="shot" src="assets/captures/mon-image.png" alt="Description de la capture">
  </a>
  <figcaption>Légende sous l'image.</figcaption>
</figure>

<div id="shot-mon-image" class="lightbox" role="dialog" aria-label="Grand format — mon-image">
  <a class="lightbox-backdrop" href="#" aria-label="Fermer"></a>
  <img class="lightbox-img" src="assets/captures/mon-image.png" alt="Description de la capture">
  <a class="lightbox-close" href="#" aria-label="Fermer">&times;</a>
</div>
```

`id` de la popup et `href` de la miniature doivent correspondre. Les images sont classées dans une
rangée centrée : enveloppez plusieurs `<figure>` dans un `<div class="figure-row">`.