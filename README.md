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

Here, we can choose which `Compiler Version` we want, which smart-contract programming language we are using (mostly you will just be using Solidity), and some further configuration options.

Note: The other programming language listed in Remix, `Yul`, is a lower-level language. It is meant for intermediate compilation, and is closer to the hardware than Solidity is. 99% of the time you will not be coding in Yul. Read more about Yul here - [https://docs.soliditylang.org/en/v0.8.9/yul.html](https://docs.soliditylang.org/en/v0.8.9/yul.html)

Clicking `Compile 1_Storage.sol` will compile the contract and make it ready for deployment.

![](https://i.imgur.com/KieTxyw.png)

Moving over to the `Deployment` tab, we will see something like this in the sidebar.

![](https://i.imgur.com/NzlQ3kM.png)

<Quiz questionId="be553003-ef98-4517-88ac-1cea9c4a4008" />

First thing to note here is the `Environment`. Remix ships with a `Javascript VM` - which is a simulator of the Ethereum Virtual Machine (EVM) in the browser. This allows for fast testing and debugging of your smart contract, as long as your contract doesn't depend on another contract deployed to a real Ethereum network. Thankfully, our Storage contract does not, so we can test it right here in the Javascript VM.

To deploy to actual networks, we will want to change our `Environment` to one of the other options listed there (more on this later).

<Quiz questionId="b4e0f228-abc7-4384-ba92-2839fe77ed11" />

Along with the `Javascript VM`, Remix creates a set of fake accounts, all loaded up with 100 ETH, to test with. 

Select the `1_Storage.sol` contract from the dropdown, and click `Deploy` to deploy the contract. 

![](https://i.imgur.com/mjfULEw.png)

Once the contract is deployed, you will see it under the `Deployed Contracts` section - where you can now call functions on your smart contract.

Calling the `retrieve` function will return a value of `0` right now, which is the default value for integers in Solidity. 

![](https://i.imgur.com/B0tBUt0.png)

Also, we will see in the Output panel some logs about the call to `Storage.retrieve` which is our function.

Now, let's try calling the `store` value with the number `5`.

![](https://i.imgur.com/m3BwJCc.png)

Again, we see some logs in the output panel about the call to `Storage.store`. Now, if we try to `retrieve` again, the output will be `5`. 

![](https://i.imgur.com/8PdOvHf.png)


**NOTE** - None of these function calls/transactions we made opened up your digital wallet (Metamask). This is because we are testing in the `Javascript VM` currently, and that is just a simulator working with fake accounts. When deploying to a real network (Testnet or mainnet), transactions need to be confirmed and signed through your digital wallet. 

## Recommended

To learn more about Remix, we recommend:

- Go through the documentation at [Remix IDE Docs](https://remix-ide.readthedocs.io/en/latest/)
- Play around with the default smart contracts that Remix ships with to get a handle on the workflow

## DYOR Questions
<Quiz questionId="1f9f5213-43dc-4e2b-9daa-64dec004af6e" />
<Quiz questionId="a8f3391a-00f5-4632-a25d-2515bd9523b2" />
<Quiz questionId="c0cb59fd-60df-404b-a052-6b7d360da2b4" />

<SubmitQuiz />
