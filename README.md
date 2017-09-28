# Exercice de découverte de la technologie JSP

Petit projet permettant de prendre en main les bases des JSP

Nécessite :

- Apache Maven
- Un IDE avec un plugin Tomcat 8.x ou supérieur

Une fois tout configuré en local avec le port 8080 et l'application lancée, l'url suivante devrait répondre "Hello World" : http://localhost:8080/decouverte-jsp/bonjour

Activités proposées :

- étape 1 : prendre connaissance de la base de code et éprouver l'application
- étape 2 : créer un fichier *hello.jsp* dans le répertoire src/main/webapp, dont la responsabilité va être d’afficher le texte “Hello World”. Dans la méthode doPost de la Servlet HelloWorld, rediriger la réponse vers hello.jsp
- étape 3 : rendre *hello.jsp* dynamique en affichant en majuscule le nom saisi dans le formulaire initial (*index.html*) de manière à afficher “Hello ERIC” si “Eric” a été saisi dans le formulaire (tout en gardant “Hello World” si rien n’a été saisi. La transformation du nom en majuscules est de la responsabilité de la Servlet
- étape 4 : protéger *hello.jsp* d'appels directs ( http://localhost:8080/decouverte-jsp/hello.jsp ) en la déplaçant dans le répertoire protégé WEB-INF. Le comportement du formulaire présent sur la page d'accueil doit bien évidemmment ne pas être impacté
- étape 5 : se concentrer sur *hello.jsp* et simplifier la scriptlet en utilisant la baliser &lt;jsp:useBean&gt; combinée à une scriptlet élémentaire de type &lt;%= maValeur %&gt;
- étape 6 : se concentrer sur *hello.jsp* et remplacer le code dynamique précédent par son équivalent en EL (ne pas se laisser influencer une éventuelle erreur (croix rouge) pouvant être matérialisée par Eclipse)
- étape 7 : réfléchir à la raison pour laquelle Eclipse pourrait matérialiser une erreur dans la JSP alors que l'application fonctionne malgré tout, puis intégrer la dépendance Maven manquante qui permettra d'améliorer l'expérience développeur dans Eclipse
- étape 8 : s'intéresser aux variables implicites disponibles avec EL, et inclure notamment l'affichage du User Agent du navigateur de l'utilisateur dans *hello.jsp* en rajoutant un message du type *Vous naviguez avec XXX*
- étape 9 : transformer le formulaire présent sur *index.html* afin de permettre la saisie d'un nom et d'un prénom, définir une classe Personne regroupant ces 2 notions, et l'utiliser dans la Servlet et la JSP afin de pouvoir regrouper les deux informations saisies dans un même objet et s'en servir pour l'affichage
- étape 10 : ajouter une nouvelle zone de saisie dans *index.html* afin de permettre la saisie du prénom du conjoint, puis exploiter les informations dans la Servlet afin de construire une liste (*java.util.List*) de 2 personnes dont on cherchera à réaliser l'affichage dans la JSP en utilisant les moyens du bord (scriptlets + structures de contrôles Java)
- étape 11 : s'intéresser à la [JSTL](https://fr.wikipedia.org/wiki/JavaServer_Pages_Standard_Tag_Library) et identifier la dépendance Maven à rajouter au projet pour pouvoir l'utiliser
- étape 12 : s'intéresser à l'intégration dans une JSP de la JSTL, en particulier de la taglib &lt;c:forEach&gt; qu'on utilisera pour remplacer les scriptlets pour affichage notre liste de personnes
