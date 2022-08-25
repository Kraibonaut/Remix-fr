# Level 5 - Remix IDE

![image](https://user-images.githubusercontent.com/16539849/173646901-81144afc-36aa-418c-be7f-70477b627ced.png)

Remix est un environnement de développement intégré (IDE) open-source, pour le web et le bureau, destiné au développement Ethereum. C'est l'outil de développement le plus facile à utiliser pour commencer à construire sur Ethereum, et il dispose d'une énorme collection de plugins pour étendre son expérience. 

<Quiz questionId="512d993c-ecb0-4ecd-b077-8f7eec505bec" />

Remix vous aide à écrire du code Solidity directement dans le navigateur, et dispose d'outils pour tester, déboguer et déployer votre contrat intelligent sur la blockchain.


Vous pouvez visiter Remix à l'adresse [https://remix.ethereum.org/](https://remix.ethereum.org/)

<Quiz questionId="1cbd33c7-d0ae-445e-b70b-0888666e2a9d" />

## Navigating Remix

Lorsque vous ouvrez Remix pour la première fois, vous êtes accueilli par un écran comme celui-ci.
![](https://i.imgur.com/4RqBi40.png)

Dans la barre latérale de gauche, vous pouvez basculer entre les éléments suivants `File Explorer`, le `Solidity Compiler`, le `Deployer`, et un panneau `Extensions`.

En bas, il y a un panneau de sortie, qui affiche les résultats de votre compilation, de vos déploiements et de vos appels de fonction. 

Au milieu se trouve l'endroit où vous allez éditer du code. Actuellement, il affiche l'écran d'accueil de l'IDE, mais dès que nous ouvrirons un fichier, il deviendra l'éditeur de code.

## Remix Workflow

Dans la barre latérale, si vous regardez sous la rubrique `contracts`  - Remix est livré avec 3 contrats intelligents de base pour aider les gens à apprendre Solidity. Jetons un coup d'œil à `1_Storage.sol`.

![](https://i.imgur.com/OdGQABf.png)

Nous pouvons voir l'éditeur de code maintenant.

Dans l'explorateur de fichiers, nous pouvons également voir des options pour créer un nouveau fichier ou répertoire, télécharger des fichiers locaux ou importer des fichiers de Github.

Pour compiler nos contrats, nous nous déplaçons sur l'onglet `Solidity Compiler`,  et nous verrons quelque chose comme ceci dans la barre latérale.

![](https://i.imgur.com/kr0a26J.png)

Ici, nous pouvons choisir quel`Compiler Version`que nous voulons, le langage de programmation des contrats intelligents que nous utilisons (la plupart du temps, vous utiliserez Solidity), et quelques options de configuration supplémentaires.

Remarque : L'autre langage de programmation figurant dans Remix, `Yul`, est un langage de plus bas niveau. Il est destiné à la compilation intermédiaire et est plus proche du matériel que Solidity. Dans 99% des cas, vous ne coderez pas en Yul. Pour en savoir plus sur Yul, cliquez ici - [https://docs.soliditylang.org/en/v0.8.9/yul.html](https://docs.soliditylang.org/en/v0.8.9/yul.html)

En cliquant sur `Compile 1_Storage.sol` compilera le contrat et le rendra prêt à être déployé..

![](https://i.imgur.com/KieTxyw.png)

En passant à l'onglet `Deployment`, nous verrons quelque chose comme ceci dans la barre latérale.

![](https://i.imgur.com/NzlQ3kM.png)

<Quiz questionId="be553003-ef98-4517-88ac-1cea9c4a4008" />

La première chose à noter ici est l'`Environment`. Remix est livré avec une `Javascript VM` - qui est un simulateur de la machine virtuelle Ethereum (EVM) dans le navigateur. Cela permet de tester et de déboguer rapidement votre contrat intelligent, tant que celui-ci ne dépend pas d'un autre contrat déployé sur un véritable réseau Ethereum. Heureusement, ce n'est pas le cas de notre contrat de stockage, nous pouvons donc le tester ici même dans la VM Javascript.

Pour déployer sur les réseaux réels, nous voudrons changer notre `Environment` à l'une des autres options proposées (nous y reviendrons plus tard).

<Quiz questionId="b4e0f228-abc7-4384-ba92-2839fe77ed11" />

Avec la `Javascript VM`,  Remix crée un ensemble de faux comptes, tous chargés de 100 ETH, pour les tests. 

Sélectionnez le contrat `1_Storage.sol` dans la liste déroulante, et cliquez sur `Deploy` pour déployer le contrat. 

![](https://i.imgur.com/mjfULEw.png)

Une fois le contrat déployé, vous le verrez sous la rubrique `Deployed Contracts` - où vous pouvez maintenant appeler des fonctions sur votre contrat intelligent.

Appeler la fonction `retrieve`  retournera une valeur de `0` pour l'instant, qui est la valeur par défaut des entiers dans Solidity. 

![](https://i.imgur.com/B0tBUt0.png)

De plus, nous verrons dans le panneau Output quelques logs concernant l'appel à `Storage.retrieve` qui est notre fonction.

Maintenant, essayons d'appeler la valeur `store` avec le nombre `5`.

![](https://i.imgur.com/m3BwJCc.png)

Encore une fois, nous voyons quelques logs dans le panneau de sortie à propos de l'appel à `Storage.store`. Maintenant, si on essaie encore de `retrieve`, tle résultat sera `5`. 

![](https://i.imgur.com/8PdOvHf.png)


**NOTE** aAucun de ces appels de fonction/transactions que nous avons effectués n'a ouvert votre portefeuille numérique (Metamask). Ceci est dû au fait que nous testons actuellement dans la `Javascript VM`,et il ne s'agit que d'un simulateur fonctionnant avec de faux comptes. Lors du déploiement sur un réseau réel (Testnet ou mainnet), les transactions doivent être confirmées et signées par le biais de votre portefeuille numérique. 

## Recommended

Pour en savoir plus sur Remix, nous vous recommandons :

- Consultez la documentation à l'adresse [Remix IDE Docs](https://remix-ide.readthedocs.io/en/latest/)
- Jouez avec les contrats intelligents par défaut fournis avec Remix pour vous familiariser avec le workflow

## DYOR Questions
<Quiz questionId="1f9f5213-43dc-4e2b-9daa-64dec004af6e" />
<Quiz questionId="a8f3391a-00f5-4632-a25d-2515bd9523b2" />
<Quiz questionId="c0cb59fd-60df-404b-a052-6b7d360da2b4" />

<SubmitQuiz />
