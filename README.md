# MDTechs - Site Web

Site web multipage professionnel pour MDTechs.

## Structure du site

- `index.html` - Page d'accueil
- `visualisation-3d.html` - Page service Visualisation 2D/3D
- `conseil-materiel.html` - Page service Conseil matériel
- `montage-depannage.html` - Page service Montage & dépannage
- `configuration-reseau.html` - Page service Configuration réseau
- `contact.html` - Page de contact avec formulaire
- `styles.css` - Feuille de styles globale
- `script.js` - JavaScript partagé

## Personnalisation

### Ajouter vos images

Sur chaque page de service, vous trouverez des placeholders d'images dans les sections portfolio :

```html
<div class="portfolio-image">
    <!-- Placeholder pour votre image -->
    <span>📸 Insérez votre image ici</span>
</div>
```

Remplacez ces divs par vos propres images :

```html
<div class="portfolio-image">
    <img src="chemin/vers/votre-image.jpg" alt="Description">
</div>
```

### Modifier les coordonnées de contact

Dans le footer de chaque page et sur la page contact, modifiez :
- Email : `contact@mdtechs.fr`
- Téléphone : `+33 (0)0 00 00 00 00`

### Formulaire de contact

Le formulaire utilise actuellement un système de `mailto:` simple. Pour une solution professionnelle, intégrez un service comme :
- Formspree
- EmailJS
- Un backend PHP avec PHPMailer

## Hébergement

Le site est entièrement statique (HTML/CSS/JS). Vous pouvez l'héberger sur :
- Netlify (gratuit, recommandé)
- Vercel
- GitHub Pages
- N'importe quel hébergement web traditionnel

## Navigation

- Tous les liens du footer fonctionnent
- La navigation entre pages est opérationnelle
- Les liens d'ancres (#services) fonctionnent sur la page d'accueil
- Les cards de service sur l'accueil sont cliquables et mènent aux pages correspondantes

## Style

Le design est sobre et professionnel avec :
- Palette claire (blanc/gris/bleu)
- Animations subtiles
- Responsive complet (desktop → mobile)
- Performance optimisée