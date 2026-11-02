# 📒 Mon carnet de bord

**Nom : Geffroy** 

**Prénom : Thomas ** 

**Adresse de mon site :** https://thomasgeffroy.pythonanywhere.com

> Modifiez ce fichier directement sur GitHub (icône crayon ✏️) pour répondre aux questions de chaque exercice.
> Écrivez avec vos propres mots : une réponse courte et juste vaut mieux qu'un long copier-coller ! 🙂

---

## 🟢 Exercice 1 — Mon premier déploiement

1. Où se trouve physiquement le code qui fabrique votre page : sur votre ordinateur, sur GitHub ou sur PythonAnywhere ?

   > Sur PythonAnywhere

2. Pourquoi votre voisin(e) peut-il voir votre site, alors que vous n'avez rien installé sur son ordinateur ?

   > Parce qu'il tourne sur un serveur publique donc il lui suffit juste d'avoir l'url

---

## 🟢 Exercice 2 — Les URL et les routes

1. Dans l'URL `https://www.google.com/maps`, quel est le nom de domaine ? Quel est le chemin ?

   > Le nom de domaine est "www.google.com" et le chemin "/maps" 

2. Que veut dire le message *Not Found* ? Qui l'a envoyé : votre navigateur ou le serveur ?

   > Le serveur envoie le message qui signifie qu'il ne trouve pas de page a cette adresse

3. Que se passe-t-il si deux fonctions portent le même nom dans `flask_app.py` ? (Indice : essayez, puis lisez l'Error log.)

   Le site refuse de lancer une page. AssertionError: View function mapping is overwriting an existing endpoint function: loisirs

---

## 🔵 Exercice 3 — Le langage HTML

1. Quelle est la différence entre ce que le serveur **envoie** et ce que le navigateur **affiche** ?

   > Le serveur envoie le code html brut et le navigateur l'interprète 

2. À quoi servent les balises `<h1>`, `<p>`, `<ul>` et `<li>` ?

   > `<h1>` est un titre principal, `<p>` un paragraphe, `<ul>` le titre de la liste et `<li>` les éléments de la liste

3. Pourquoi l'image s'affiche-t-elle alors qu'elle n'est pas sur votre serveur ?

   > Elle va chercher l'image sur sur le serveur en ligne qui l'héberge ici wikimedia

---

## 🔵 Exercice 4 — Les templates

1. Pourquoi est-ce une bonne idée de séparer le code Python et le HTML ? (Pensez à une équipe avec un développeur et un graphiste.)

   > C'est mieux afin que le développeur et le graphiste travail sur deux fichiers bien distincts pour pas génerer un conflit 

2. Les `{{ prenom }}` sont-ils remplacés par le serveur ou par le navigateur ? Comment l'avez-vous vérifié ?

   > Ils sont remplacés par le serveur. Lorsque l'on fait Crtl+U on voit le code sources et le {{ prenom }} est déjà remplacé 

---

## 🔵 Exercice 5 — Le CSS et les liens

1. Quelle est la différence de rôle entre le HTML et le CSS ?

   > Le css est le style et le HTML le fond (les informations)

2. Pour afficher votre page `/presentation`, combien de fichiers le navigateur doit-il télécharger ? (Vous pourrez le vérifier à l'exercice suivant !)

   > 3

3. Pourquoi faut-il parfois faire **Ctrl + F5** pour voir les changements de CSS ?

   > Les navigateurs peuvent utiliser du cache donc Ctrl+F5 met a jour et supprime le cache

---

## 🟣 Exercice 6 — Espionner le navigateur

1. Que signifie HTTP ? Qui envoie la **requête** et qui envoie la **réponse** ?

   > HyperTextTransferProtocol, la requête est envoyé par le navigateur et la réponse par le serveur

2. Combien de requêtes votre page `/presentation` a-t-elle déclenchées ? Lesquelles ?

   > 16, presentation, style.css, FloatingActionButton.js, local-storage.js, util.js, fte-utils.js, express-fte.js, extensionShared.js, vendor.js, otherVendor.js, express-utils.js, AdobeCLean-Regular.otf, AdobeClean-Bold.otf, js.js, dom?js et js.js

3. Que signifie le code `200` ? Et le code `404` de la favicon ?

   > 200 c'est que tout va bien et  404 que le serveur n'a rien a cette adresse

4. Pourquoi les modifications faites dans l'onglet Éléments ne sont-elles pas visibles par les autres visiteurs ?

   > Les changements fait dans Elements ne sont que en local, lorsqu'on rafraichit tout redeviens comment avant

---

## 🟣 Exercice 7 — Envoyer des informations dans l'URL

1. Dans l'URL `https://www.youtube.com/results?search_query=chat`, quel est le nom du paramètre ? Quelle est sa valeur ?

   > le paramètre est search_query et la valeur est chat

2. Pourquoi le serveur plante-t-il avec `a=bonjour` ? Que faudrait-il faire pour l'éviter ?

   > il faut que a soit de type int, il faudrait faire une gestion d'erreur afin que si a est de type string un message d'erreur apparaisse 

3. Pourquoi est-il dangereux d'afficher **tel quel** ce que l'utilisateur envoie ?

   > C'est une faille de sécurité car le code s'exécute tel quel

---

## 🟣 Exercice 8 — Les formulaires

1. Quelle est la différence visible entre GET et POST ?

   > GET met les informations dans l'url contrairement a post

2. Pour un formulaire de **recherche**, quelle méthode choisiriez-vous ? Et pour un formulaire de **connexion avec mot de passe** ? Pourquoi ?

   > Pour des recheerche get afin d'avoir en stock l'url et connexion post pour pas avoir notre identifiant et mot de passe dans l'url

3. Les données envoyées en POST sont-elles vraiment « secrètes » ? (Pensez à ce que vous avez vu dans l'onglet Réseau.)

   > Non on les voit dans Réseau

---

## 🔴 Exercice 9 — Les codes de statut

1. Quelle est la différence entre une erreur `4xx` et une erreur `5xx` ? Qui est « fautif » dans chaque cas ?

   > 4xx est une erreur coté utilisateur et 5xx coté serveur

2. Comment fonctionne une redirection ? Qui fait la deuxième requête : le serveur ou le navigateur ?

   > le navigateur fait la deuxième requête

3. Donnez un exemple de situation où un vrai site utilise une redirection.

   > Lors d'une connexion ou inscription lorsque l'on clique sur le bouton on est souvent redirigé vers la page d'acceuil 

---

## 🔴 Exercice 10 — Ce que le serveur sait de vous

1. Citez trois informations que le serveur connaît sur vous, sans que vous ayez rien rempli.

   > L'adresse IP, le navigateur utilisé et la langue préféré

2. À quoi peut servir l'en-tête `Accept-Language` pour un site comme Wikipédia ?

   > Elle permet d'afficher à l'utilisateur la langue qui lui convient le mieux

3. Dans l'Access log, retrouvez une requête qui a reçu un code `404`. Quelle page était demandée ?

   > horloge

4. Après cet exercice, que pensez-vous de la notion de « navigation anonyme » ?

   > La navigation full anonyme n'existe pas, elle permet de ne pas avoir de cache et d'historique mais les serveurs ont les informations

---

## 🔴 Exercice 11 — Le Web des machines : API et JSON

1. Quelle est la différence entre une page HTML et une réponse JSON ? À qui chacune est-elle destinée ?

   > _Ma réponse :_ 

2. Dans la page `/horloge`, quel code s'exécute sur le **serveur** et quel code s'exécute dans le **navigateur** ?

   > _Ma réponse :_ 

3. Citez une application de votre téléphone qui, selon vous, utilise une API. Quelles données échange-t-elle ?

   > _Ma réponse :_ 

---

## 🏁 Pour conclure

En quelques phrases, expliquez à un ami ce qui se passe entre le moment où il tape une adresse dans son navigateur et celui où la page s'affiche :

> _Ma réponse :_ 
