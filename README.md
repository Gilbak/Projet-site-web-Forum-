# Projet-site-web-Forum-
Création de site web / forum 


Plan détaillé pour la création d'un site web de forum avec HTML et CSS
1. Planification
- Objectifs du site
   
Permettre aux utilisateurs de poser des questions sur l'actualité et des cours éducatifs.
Fournir une plateforme où d'autres utilisateurs peuvent répondre à ces questions.
-Fonctionnalités principales
Page d'accueil avec une vue générale des catégories et des discussions récentes.
Page de discussion où les utilisateurs peuvent poser des questions et répondre.
Formulaire d'inscription et de connexion pour les utilisateurs.
Système de gestion des utilisateurs (inscription, connexion, déconnexion).
Catégories de discussions (actualité, cours éducatifs, etc.).

2.Structure du site
- Arborescence des fichiers
   
```bash
/project-root
    /css
        styles.css
    /images
    /js
    /pages
        home.html
        forum.html
        login.html
        register.html
    index.html
```
3. Création des pages HTML
- index.html - Page d'accueil
```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Forum</title>
    <link rel="stylesheet" href="css/styles.css">
</head>
<body>
    <header>
        <h1>Bienvenue sur le Forum</h1>
        <nav>
            <ul>
                <li><a href="index.html">Accueil</a></li>
                <li><a href="pages/forum.html">Forum</a></li>
                <li><a href="pages/login.html">Connexion</a></li>
                <li><a href="pages/register.html">Inscription</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <section>
            <h2>Catégories de Discussions</h2>
            <ul>
                <li><a href="#">Actualité</a></li>
                <li><a href="#">Cours Éducatifs</a></li>
                <li><a href="#">Autres</a></li>
            </ul>
        </section>
        <section>
            <h2>Discussions Récentes</h2>
            <!-- Exemple de discussion -->
            <div class="discussion">
                <h3><a href="#">Quel est l'impact du changement climatique sur l'économie mondiale ?</a></h3>
                <p>Posté par Utilisateur1 le 25 Mai 2024</p>
            </div>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 Forum</p>
    </footer>
</body>
</html>
```
3.2 forum.html - Page du forum
```html

<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Forum</title>
    <link rel="stylesheet" href="../css/styles.css">
</head>
<body>
    <header>
        <h1>Forum</h1>
        <nav>
            <ul>
                <li><a href="../index.html">Accueil</a></li>
                <li><a href="forum.html">Forum</a></li>
                <li><a href="login.html">Connexion</a></li>
                <li><a href="register.html">Inscription</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <section>
            <h2>Discussions</h2>
            <div class="discussion">
                <h3><a href="#">Quel est l'impact du changement climatique sur l'économie mondiale ?</a></h3>
                <p>Posté par Utilisateur1 le 25 Mai 2024</p>
                <div class="reponses">
                    <p>Réponse de Utilisateur2: Les impacts sont nombreux...</p>
                </div>
                <form action="#">
                    <textarea placeholder="Votre réponse..."></textarea>
                    <button type="submit">Répondre</button>
                </form>
            </div>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 Forum</p>
    </footer>
</body>
</html>
```
3. login.html - Page de connexion
```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Connexion</title>
    <link rel="stylesheet" href="../css/styles.css">
</head>
<body>
    <header>
        <h1>Connexion</h1>
        <nav>
            <ul>
                <li><a href="../index.html">Accueil</a></li>
                <li><a href="forum.html">Forum</a></li>
                <li><a href="login.html">Connexion</a></li>
                <li><a href="register.html">Inscription</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <form action="#">
            <label for="username">Nom d'utilisateur :</label>
            <input type="text" id="username" name="username" required>
            <label for="password">Mot de passe :</label>
            <input type="password" id="password" name="password" required>
            <button type="submit">Se connecter</button>
        </form>
    </main>
    <footer>
        <p>&copy; 2024 Forum</p>
    </footer>
</body>
</html>
```
3.4 register.html - Page d'inscription
```html

<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Inscription</title>
    <link rel="stylesheet" href="../css/styles.css">
</head>
<body>
    <header>
        <h1>Inscription</h1>
        <nav>
            <ul>
                <li><a href="../index.html">Accueil</a></li>
                <li><a href="forum.html">Forum</a></li>
                <li><a href="login.html">Connexion</a></li>
                <li><a href="register.html">Inscription</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <form action="#">
            <label for="username">Nom d'utilisateur :</label>
            <input type="text" id="username" name="username" required>
            <label for="email">Email :</label>
            <input type="email" id="email" name="email" required>
            <label for="password">Mot de passe :</label>
            <input type="password" id="password" name="password" required>
            <button type="submit">S'inscrire</button>
        </form>
    </main>
    <footer>
        <p>&copy; 2024 Forum</p>
    </footer>
</body>
</html>
```
4. Création des styles CSS
   - styles.css
```css

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: white;
    padding: 10px 0;
    text-align: center;
}

nav ul {
    list-style: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin-right: 10px;
}

nav ul li a {
    color: white;
    text-decoration: none;
}

main {
    padding: 20px;
}

footer {
    text-align: center;
    padding: 10px 0;
    background-color: #333;
    color: white;
    position: fixed;
    bottom: 0;
    width: 100%;
}

section {
    margin-bottom: 20px;
}

.discussion {
    background-color: white;
    padding: 10px;
    margin-bottom: 10px;
    border-radius: 5px;
}

.discussion h3 {
    margin: 0;
}

.reponses {
    margin-top: 10px;
    padding-left: 10px;
    border-left: 2px solid #ddd;
}

form {
    margin-top: 10px;
}

form textarea {
    width: 100%;
    height: 100px;
    margin-bottom: 10px;
}

form button {
    display: block;
    background-color: #333;
    color: white;
    border: none;
    padding: 10px;
    cursor: pointer;
}
```
Pour rendre le forum fonctionnel (par exemple, l'ajout de nouvelles questions et réponses), il serait nécessaire d'utiliser JavaScript pour gérer les événements côté client et un langage côté serveur (comme PHP, Node.js ou Python avec Flask/Django) pour gérer la logique côté serveur et la base de données. Cependant, ce plan se concentre uniquement sur la structure HTML et les styles CSS.
