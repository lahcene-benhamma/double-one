# DOUBLE ONE — Site Vitrine Officiel (Version 1)
**Boutique de vêtements Streetwear Masculin · Bab Ezzouar, Alger**

---

## 1. Présentation du Projet
Ce site vitrine a été conçu selon le **Cahier des charges Version 1** pour la boutique **DOUBLE ONE** située à **Bab Ezzouar, Alger**.

- **Style & Direction Visuelle** : Streetwear masculin, urbain, moderne et premium, décliné dans une palette monochrome Noir & Blanc haute couture avec typographies percutantes (`Space Grotesk` et `Inter`).
- **Objectif de cette Version 1** : Présenter la marque avec impact, fournir les coordonnées officielles (WhatsApp, Instagram, localisation Google Maps) et préparer une section collection évolutive prête à recevoir les futurs articles sans inventer de faux stocks.

---

## 2. Structure des Fichiers

```
double-one/
├── index.html            # Page d'accueil complète et responsive
├── style.css             # Feuille de style moderne Noir & Blanc
├── README.md             # Guide d'utilisation et d'ajout des articles
├── js/
│   ├── app.js            # Logique applicative (menu mobile, filtres, affichage dynamique)
│   └── products.js       # Base de données simple des articles (facile à éditer)
└── assets/
    ├── hero.jpg          # Visuel d'ambiance streetwear de la boutique
    └── articles/         # Dossier où déposer les photos réelles de vos futurs articles
```

---

## 3. Comment Lancer le Site Localement

### Option A — Double-clic direct
Ouvrez simplement le fichier `index.html` dans n'importe quel navigateur (Google Chrome, Safari, Mozilla Firefox, Microsoft Edge).

### Option B — Avec un serveur local (recommandé pour tester les modules JS)
Dans un terminal, placez-vous dans le dossier du projet et lancez :
```bash
# Avec Python 3 :
cd "double-one"
python3 -m http.server 8080

# Ou avec npx serve :
npx serve -l 8080 .
```
Ouvrez ensuite votre navigateur sur : `http://localhost:8080`

---

## 4. Comment Ajouter de Nouveaux Articles et Leurs Photos

La structure a été pensée pour être ultra-simple à mettre à jour, sans nécessiter de base de données complexe :

### Étape 1 : Ajouter la photo de l'article
1. Prenez en photo votre vêtement (sur mannequin, cintre ou porté).
2. Déposez l'image dans le dossier `assets/articles/` (ex: `assets/articles/hoodie-black.jpg`).

### Étape 2 : Ajouter l'article dans le fichier `js/products.js`
Ouvrez le fichier `js/products.js` avec un éditeur de texte (VS Code, Bloc-notes, etc.).

Dans le tableau `PRODUCTS`, ajoutez un bloc comme ceci :

```javascript
export const PRODUCTS = [
  {
    id: "dbl-001",
    name: "Hoodie Heavyweight Double One Noir",
    category: "hoodies", // "hoodies" | "tshirts" | "cargos" | "vestes" | "accessoires"
    description: "Coton premium 450 GSM, coupe boxy oversize, broderie discrète sur le torse.",
    price: 6800, // Prix en Dinars Algériens (DA)
    image: "assets/articles/hoodie-black.jpg",
    badge: "Nouveau", // "Nouveau", "Best-Seller", "Drop Limité" ou null
    available: true // true = disponible en boutique
  },
  {
    id: "dbl-002",
    name: "T-Shirt Acid Wash Vintage Charcoal",
    category: "tshirts",
    description: "Coton lourd 280 GSM délavé, coupe loose streetwear, col côtelé épais.",
    price: 3900,
    image: "assets/articles/tee-charcoal.jpg",
    badge: "Bestseller",
    available: true
  }
];
```

### Étape 3 : Enregistrer
Enregistrez simplement le fichier. Dès qu'au moins un article est présent dans le tableau `PRODUCTS`, le site bascule **automatiquement** du message d'attente à la grille de vos articles avec le prix en Dinars Algériens (DA) et un bouton de commande directe sur WhatsApp !

---

## 5. Coordonnées Officielles Intégrées
- **Boutique** : DOUBLE ONE (Clothing)
- **Adresse** : P59P+7C7, Bab Ezzouar, Alger, Algérie
- **Téléphone** : `0773014399`
- **WhatsApp direct** : `https://wa.me/213773014399`
- **Horaires** : Tous les jours de 10h00 à 23h00 (sous réserve de confirmation par le propriétaire)
- **Instagram** : `https://www.instagram.com/double_one.dz/?dlrf=cTQ3YzJkdnd6eWZp`
- **Google Maps** : Lien d'itinéraire direct et intégration iframe cartographique
