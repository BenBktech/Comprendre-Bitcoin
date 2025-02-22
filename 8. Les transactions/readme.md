# Les Transactions Bitcoin : Fonctionnement et Sécurité

## Qu’est-ce qu’une transaction Bitcoin ?

Une transaction Bitcoin est simplement un ensemble de données qui contient :

- L’adresse de l’expéditeur (d’où viennent les bitcoins).
- Le montant envoyé.
- L’adresse du destinataire (où vont les bitcoins).

Contrairement aux transactions bancaires classiques, une transaction Bitcoin n'est qu’une ligne de données envoyée au réseau pour être vérifiée et inscrite dans la blockchain.

🔹 Comment fonctionne une transaction Bitcoin ?
Lorsque vous effectuez une transaction, vous ne déplacez pas des bitcoins comme des pièces physiques d’un compte à un autre.

En réalité, une adresse Bitcoin ne possède pas un solde fixe, mais une liste de paiements reçus qu’elle peut utiliser pour effectuer de nouvelles transactions.

1. Les entrées et sorties des transactions
Chaque transaction Bitcoin est constituée :

D’entrées (inputs) : ce sont des paiements reçus précédemment et utilisés pour envoyer des bitcoins.
De sorties (outputs) : ce sont les nouvelles adresses qui recevront les bitcoins.
Lorsqu’un utilisateur envoie des bitcoins, il utilise des entrées existantes et crée de nouvelles sorties qui seront utilisées par d’autres dans le futur.

💡 Exemple concret :
Imaginons que vous ayez reçu :
✔ 0.4 BTC d’un ami.
✔ 0.6 BTC d’un paiement.

Vous voulez envoyer 0.7 BTC à quelqu’un.

Vous ne pouvez pas envoyer exactement 0.7 BTC :
👉 Vous devez utiliser les 0.4 BTC + 0.6 BTC en entrées.
👉 Vous créez deux sorties :
✔ 0.7 BTC vers l’adresse du destinataire.
✔ 0.3 BTC qui vous est renvoyé (appelé "change").

C’est comme payer 7 € avec un billet de 10 € et recevoir 3 € de monnaie.

💡 Si vous ne précisez pas de "change", le réseau prendra la différence comme frais de transaction !

🔹 Pourquoi ne peut-on pas utiliser mes bitcoins sans mon autorisation ?
1. Les transactions sont verrouillées par cryptographie
Lorsque vous recevez des bitcoins, ils sont verrouillés et ne peuvent être dépensés que par quelqu’un qui possède la clé privée associée.

Chaque adresse Bitcoin a :

Une clé publique (visible par tous).
Une clé privée (secrète et connue seulement du propriétaire).
2. La signature numérique
Pour envoyer des bitcoins, vous devez signer numériquement la transaction avec votre clé privée.

Cette signature prouve au réseau que vous êtes bien le propriétaire des fonds.

🚫 Sans cette signature, la transaction sera rejetée par le réseau.

🔹 Comment une transaction est-elle validée et ajoutée à la blockchain ?
1️⃣ Création de la transaction
L’utilisateur génère une transaction avec les entrées, les sorties et sa signature numérique.

2️⃣ Propagation sur le réseau
La transaction est envoyée aux nœuds Bitcoin, qui vérifient sa validité :
✔ L’expéditeur possède-t-il réellement les bitcoins ?
✔ La signature est-elle correcte ?
✔ Ces bitcoins n’ont-ils pas déjà été dépensés ailleurs ?

3️⃣ Ajout dans un bloc
Une fois validée, la transaction est stockée dans le mempool (la salle d’attente des transactions).

Un mineur sélectionne la transaction, l’intègre dans un bloc candidat, puis tente de résoudre la preuve de travail.

4️⃣ Confirmation dans la blockchain
Si un mineur trouve un bloc valide, il l’ajoute à la blockchain et la transaction devient irréversible.

💡 Une transaction est souvent considérée comme sûre après 6 confirmations (environ 1 heure).

🔹 Les frais de transaction Bitcoin
Les frais Bitcoin varient en fonction de :
✔ La congestion du réseau (plus il y a de transactions en attente, plus les frais sont élevés).
✔ La taille de la transaction (en octets, pas en bitcoins !).

💡 Exemple :

Une transaction simple avec 1 entrée et 2 sorties coûte peu cher.
Une transaction avec plusieurs entrées et sorties est plus volumineuse et coûte plus cher.
Si vous proposez des frais trop bas, votre transaction risque d’être bloquée dans le mempool pendant longtemps.

