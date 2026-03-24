# MDTechs - Site Web

Site web multipage professionnel pour MDTechs.

## Structure du site

- `index.html` - Page d'accueil
- `visualisation-3d.html` - Page service Visualisation 2D/3D
- `conseil-materiel.html` - Page service Conseil matériel
- `montage-depannage.html` - Page service Montage & dépannage
- `configuration-reseau.html` - Page service Configuration réseau
-  `configuration-reseau.html` - Page service Création Site Web
- `contact.html` - Page de contact avec formulaire
- `styles.css` - Feuille de styles globale
- `script.js` - JavaScript partagé
- `favicon.png` - Logo carré pour l'icône du navigateur
- `logo-horizontal.png` - Logo horizontal dans le footer

## Hébergement GitHub Pages

Le site est actuellement sur GitHub Pages. Voici comment configurer un nom de domaine personnalisé :

### 1. Acheter un nom de domaine

Registrars recommandés :
- **Cloudflare Registrar** (prix au coût, pas de marge)
- **OVH** (français, bon rapport qualité/prix)
- **Gandi** (interface propre, support FR)
- **Namecheap** (international, bon prix)

Prix moyen : 10-15€/an pour un .fr ou .com

### 2. Configurer le DNS

Dans les paramètres DNS de votre registrar, créer :

**Pour un domaine apex (mdtechs.fr) :**
```
Type: A
Nom: @
Valeur: 185.199.108.153
```
```
Type: A
Nom: @
Valeur: 185.199.109.153
```
```
Type: A
Nom: @
Valeur: 185.199.110.153
```
```
Type: A
Nom: @
Valeur: 185.199.111.153
```

**Pour www (www.mdtechs.fr) :**
```
Type: CNAME
Nom: www
Valeur: votre-username.github.io
```

### 3. Configurer GitHub Pages

Dans votre repo GitHub :
- Settings → Pages
- Custom domain : entrer `mdtechs.fr` (ou .com)
- Cocher "Enforce HTTPS" (après propagation DNS, ~24h)

### 4. Email professionnel

Pour `contact@mdtechs.fr`, plusieurs options :

**Option 1 : Google Workspace (recommandé pro)**
- 6€/mois/utilisateur
- Gmail avec votre domaine
- Drive, Calendar, Meet inclus
- Interface que tu connais
- Configuration DNS automatique

**Option 2 : Cloudflare Email Routing (gratuit)**
- Redirection email gratuite
- Redirige `contact@mdtechs.fr` vers ton Gmail perso
- Pas d'envoi depuis `@mdtechs.fr` (que réception)
- Configuration DNS simple

**Option 3 : Proton Mail**
- 4€/mois
- Focus privacy
- Interface web + apps mobiles
- Domaine personnalisé inclus

**Option 4 : OVH Email Pro**
- ~3€/mois
- Email hébergé en France
- Webmail basique mais fonctionnel

**Ma recommandation :**
- Si budget micro-entreprise → Google Workspace (pro, fiable)
- Si juste besoin de recevoir → Cloudflare Email Routing (gratuit)
- Si privacy important → Proton Mail

### Configuration DNS email (exemple Google Workspace)

Google te donnera des enregistrements MX à ajouter :
```
Type: MX
Priorité: 1
Valeur: aspmx.l.google.com
```
+ 4-5 autres enregistrements MX de backup

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
    <img src="images/ton-image.jpg" alt="Description">
</div>
```

### Modifier les coordonnées de contact

Dans le footer de chaque page et sur la page contact, modifiez :
- Email : `contact@mdtechs.fr`
- Téléphone : `+33 (0)0 00 00 00 00`

### Formulaire de contact

Le formulaire utilise actuellement un système de `mailto:` simple. Pour une solution professionnelle, intégrez un service comme :
- **Formspree** (gratuit jusqu'à 50 soumissions/mois)
- **EmailJS** (gratuit jusqu'à 200 emails/mois)
- Un backend PHP avec PHPMailer

## Navigation

- Tous les liens du footer fonctionnent
- La navigation entre pages est opérationnelle
- Les liens d'ancres (#services) fonctionnent sur la page d'accueil
- Les cards de service sur l'accueil sont cliquables et mènent aux pages correspondantes
- Favicon visible dans l'onglet du navigateur
- Logo horizontal dans le footer de toutes les pages

## Style

Le design est sobre et professionnel avec :
- Palette claire (blanc/gris/bleu)
- Animations subtiles
- Responsive complet (desktop → mobile)
- Performance optimisée
- Logo intégré (favicon + footer)
