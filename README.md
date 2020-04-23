# Brève introduction
J'ai rencontré beaucoup de gens qui voulaient créer leurs propres routeurs pour diverses raisons. En fin de compte, l'utilisation du routeur JS vanilla peut réduire votre dépendance à l'égard de l'infrastructure. Tant que vous comprenez toutes les parties indépendantes de sa fabrication, vous pouvez facilement créer votre propre routeur vanilla JavaScript.

## Voici les éléments clés à savoir pour créer votre propre routeur JS :
1. La clé du routage JS vanilla est la propriété location.pathname .
2. Écoutez l' événement " popstate " auquel répondre. changements de nom de chemin . Cela se produit chaque fois qu'une nouvelle URL est saisie dans la barre d'adresse du navigateur, mais nous ne voulons pas actualiser la page - nous voulons simplement actualiser la vue en chargeant du nouveau contenu.
3. Vous pouvez éventuellement stocker des itinéraires dans un tableau d' itinéraires [] .
4. La connaissance des expressions régulières JavaScript ( RegEx ) pour analyser l'URL est nécessaire.
5. Une compréhension de base de l' histoire et de history.pushState (API historique de JavaScript) est essentielle si vous souhaitez intégrer votre routeur dans une architecture de navigateur native.

## Un examen rapide de l'API JavaScript History
J'ai vu tellement de tutoriels sur le routeur JS vanilla qui ne mentionnent pas l'API Historique de JavaScript. Dommage, car cliquer sur les boutons Précédent et Suivant du navigateur a tout à voir avec la navigation entre les URL dans l'historique de navigation. Vous ne pouvez pas parler de routage sans l'API Historique.

2. history.back () est identique à history.go (-1) , ou lorsque l'utilisateur clique sur le bouton Retour de son navigateur. Vous pouvez utiliser l'une ou l'autre méthode pour le même effet.
2. history.forward () s'exécute lorsque l'utilisateur appuie sur le bouton Suivant du navigateur , et il est équivalent à history.go (1) .
3. go () est similaire aux méthodes .back () et forward () , sauf que vous pouvez spécifier le nombre de pas en arrière ou en avant que vous souhaitez parcourir dans la pile d'historique du navigateur.
4. pushState () poussera le nouvel état vers l'API Historique.
5. La propriété .length est le nombre d'éléments dans l'historique de session.
6. La propriété .state est utilisée pour rechercher l'état sans écouter l' événement "popstate" .
