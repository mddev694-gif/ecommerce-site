# Site Web E-commerce

Un site web e-commerce complet avec front-end React et back-end Node.js/Express.

## Fonctionnalités

✅ **Catalogue de produits** - Affichage, recherche et filtrage des produits
✅ **Panier d'achat** - Gestion du panier avec ajout/suppression de produits
✅ **Système de paiement** - Intégration Stripe pour paiements sécurisés
✅ **Compte utilisateur** - Inscription, connexion, profil utilisateur
✅ **Commandes** - Historique et suivi des commandes
✅ **Tableau de bord administrateur** - Gestion des produits, commandes et statistiques

## Stack Technologique

### Backend
- **Node.js** avec Express.js
- **MongoDB** pour la base de données
- **JWT** pour l'authentification
- **Stripe** pour les paiements

### Frontend
- **React 18** pour l'interface utilisateur
- **React Router** pour la navigation
- **Axios** pour les requêtes API

## Installation

### 1. Cloner le dépôt
```bash
git clone https://github.com/mddev694-gif/ecommerce-site.git
cd ecommerce-site
```

### 2. Configuration du serveur
```bash
# Installer les dépendances
npm install

# Créer le fichier .env
cp .env.example .env

# Remplir les variables d'environnement
# PORT, MONGODB_URI, JWT_SECRET, STRIPE_KEYS, etc.

# Lancer le serveur
npm run dev
```

### 3. Configuration du client
```bash
cd client

# Installer les dépendances
npm install

# Lancer le client
npm start
```

## Structure du projet

```
ecommerce-site/
├── models/              # Modèles Mongoose
│   ├── User.js
│   ├── Product.js
│   ├── Cart.js
│   └── Order.js
├── routes/              # Routes API
│   ├── auth.js
│   ├── products.js
│   ├── cart.js
│   ├── orders.js
│   └── admin.js
├── client/              # Application React
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── App.js
│   │   └── index.js
│   └── package.json
├── server.js            # Serveur principal
├── package.json
└── .env.example
```

## API Endpoints

### Authentication
- `POST /api/auth/register` - Inscription
- `POST /api/auth/login` - Connexion

### Products
- `GET /api/products` - Tous les produits
- `GET /api/products/:id` - Détail d'un produit
- `POST /api/products` - Créer un produit (admin)
- `PUT /api/products/:id` - Modifier un produit (admin)
- `DELETE /api/products/:id` - Supprimer un produit (admin)

### Cart
- `GET /api/cart/:userId` - Récupérer le panier
- `POST /api/cart/add` - Ajouter au panier
- `POST /api/cart/remove` - Retirer du panier
- `POST /api/cart/clear/:userId` - Vider le panier

### Orders
- `GET /api/orders/user/:userId` - Commandes de l'utilisateur
- `POST /api/orders/create` - Créer une commande
- `PUT /api/orders/:orderId` - Mettre à jour le statut (admin)

### Admin
- `GET /api/admin/orders` - Tous les commandes
- `GET /api/admin/stats` - Statistiques
- `GET /api/admin/sales/monthly` - Ventes mensuelles

## Variables d'environnement

```env
PORT=5000
NODE_ENV=development
MONGODB_URI=mongodb://localhost:27017/ecommerce
JWT_SECRET=your_secret_key
STRIPE_PUBLIC_KEY=your_public_key
STRIPE_SECRET_KEY=your_secret_key
FRONTEND_URL=http://localhost:3000
```

## Contribuer

Les contributions sont bienvenues ! Veuillez créer une branche pour vos changements et soumettre une pull request.

## License

MIT License
