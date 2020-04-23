### EN
# hort introduction
I met a lot of people who wanted to create their own routers for various reasons. In the end, using the vanilla JS router can reduce your dependence on infrastructure. As long as you understand all the independent parts of its manufacture, you can easily create your own vanilla Javascript router.

## Here are the key things to know to create your own JS router:

1. The key to vanilla JS routing is the location.pathname property.
2. Listen for the "popstate" event to respond to .pathname changes. This happens whenever a new URL is typed into the browser's address bar but we don't want to refresh the page - we simply want to refresh the view by loading new content.
3. You can optionally store routes in a routes[] array.
4. Knowledge of JavaScript Regular Expressions (RegEx) to parse the URL is necessary.
5. Basic understanding of history and history.pushState (JavaScript's History API) is critical if you wish to integrate your router into native browser architecture.

## A quick review of the JavaScript History API
I've seen so many vanilla JS router tutorials that don't mention JavaScript's History API. Too bad, because clicking the browser's Back and Forward buttons has everything to do with navigating between URLs in browsing history. You can't speak about routing without the History API.
1. history.back() is the same as history.go(-1), or when user clicks the Back button in their browser. You can use either method to the same effect.
2. history.forward() executes when user presses the browser's Forward button, and it is equivalent to history.go(1).
3. go() is similar to the .back() and forward() methods, except you can specify how many steps back or forward you want to go within the browser history stack.
4. pushState() will push new state to the History API.
5. .length property is the number of elements in the session history.
6. .state property is used to look up state without listening to the "popstate" event.

### FR
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
