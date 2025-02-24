# Les Outputs : Le Mécanisme Fondamental des Transactions Bitcoin

## Qu’est-ce qu’un Output dans Bitcoin ?

Dans le système de transactions Bitcoin, les bitcoins sont envoyés et reçus sous forme de "lots", appelés outputs.

Contrairement à un compte bancaire où un solde est mis à jour après chaque transaction, Bitcoin fonctionne avec des entrées et des sorties (inputs et outputs).

img1

Chaque transaction utilise des outputs existants (en tant qu’inputs) pour en créer de nouveaux outputs, qui seront ensuite utilisés comme inputs dans les futures transactions.

## D’où viennent les outputs ?

Tout commence avec le minage.

- Lorsqu’un mineur trouve un bloc, il reçoit une récompense en bitcoins (block reward).
- Cette récompense est envoyée à son adresse Bitcoin sous forme d’output.
- Ce nouvel output peut être utilisé pour effectuer d’autres transactions.

img2

💡 Exemple :

Un mineur trouve un bloc et reçoit 3.125 BTC (récompense actuelle du minage).

Son adresse Bitcoin contient maintenant un seul output de 3.125 BTC.

## Comment fonctionnent les outputs lors d’une transaction ?

### Dépenser un output existant
Imaginons que vous ayez un output de 3.125 BTC et que vous souhaitez payer 0.125 BTC pour un achat.

Vous ne pouvez pas diviser un output comme on le ferait avec un billet de banque. Vous devez utiliser l’output en entier et créer de nouveaux outputs.

✔ 0.125 BTC va au commerçant (le paiement).
✔ 3 BTC vous reviennent en tant que monnaie ("change").

img3

L’output de 3.125 BTC est maintenant "dépensé" et ne peut plus être réutilisé. À la place, deux nouveaux outputs ont été créés.

img4

### Dépenser plusieurs outputs dans une transaction

Parfois, vous ne possédez pas un seul output suffisant pour un paiement.

Imaginons que vous voulez payer 1.40 BTC pour acheter quelque chose, mais que vous avez plusieurs outputs plus petits :

Outputs disponibles (UTXOs)
- 0.125 BTC
- 1 BTC
- 0.01 BTC
- 0.33 BTC

Vous pouvez combiner des outputs pour avoir au moins 1.40 BTC.

img5

Après la transaction, les outputs utilisés deviennent invalides et deux nouveaux outputs sont créés :
- 1.40 BTC pour le vendeur.
- 0.055 BTC pour l’acheteur (monnaie rendue).

Voici les outputs de l'adresse 2 après la transaction. (Les outputs rouges ne sont plus utilisables).

img6

## Les frais de transaction Bitcoin

Dans Bitcoin, les frais ne sont pas explicitement indiqués dans la transaction. Ils sont calculés automatiquement comme la différence entre la somme des entrées et la somme des sorties.

img7

📌 Exemple :

Si une transaction utilise 1.455 BTC en entrées mais ne crée que 1.40 BTC + 0.052 BTC en sorties, alors :

Frais = Entrees − Sorties = 1.455 − (1.40 + 0.052) = 0.003 BTC

Ces 0.003 BTC restants seront récupérés par le mineur qui inclut la transaction dans un bloc.

img

💡 Si vous oubliez d’ajouter une sortie pour votre "change", le mineur prendra le montant entier comme frais ! Heureusement, les portefeuilles Bitcoin gèrent automatiquement cela.

## UTXO : Unspent Transaction Output

Un UTXO (Unspent Transaction Output) est un output qui n’a pas encore été dépensé.

📌 Exemple :
Si vous possédez trois outputs :

✔ 0.8 BTC
✔ 0.2 BTC
✔ 1.5 BTC

Votre "solde" total est de 2.5 BTC. Mais techniquement, vous ne possédez pas "2.5 BTC" sur un compte, vous possédez trois UTXOs distincts.

img9

## Comment un portefeuille Bitcoin choisit-il les outputs à utiliser ? (UTXO Selection)

Lorsqu’une transaction est initiée, le portefeuille doit choisir quels UTXOs utiliser pour couvrir le montant souhaité.

📌 Exemple :
Vous devez envoyer 1.2 BTC et votre portefeuille a ces UTXOs disponibles :

✔ 0.5 BTC
✔ 0.8 BTC
✔ 1 BTC

Plusieurs options sont possibles :

- Utiliser 0.5 BTC + 0.4 BTC + 0.3 BTC de monnaie rendue.
- Utiliser 1 BTC + 0.2 BTC et ne pas générer de monnaie.
- Utiliser seulement 1.5 BTC et récupérer 0.3 BTC en monnaie.

Les portefeuilles Bitcoin optimisent cela pour minimiser les frais et éviter de générer trop de petites pièces numériques (dust outputs).

img10