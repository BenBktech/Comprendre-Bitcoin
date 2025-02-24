# Signatures Numériques : Comment Sécuriser les Transactions Bitcoin

## Qu’est-ce qu’une signature numérique ?

Une signature numérique permet de prouver que vous possédez la clé privée associée à une adresse Bitcoin sans jamais la révéler.

📌 En d’autres termes :
- Elle permet de signer une transaction pour prouver qu’elle vient bien du propriétaire légitime.
- Elle empêche quiconque d’utiliser votre clé privée pour voler vos fonds.

![img1](https://raw.githubusercontent.com/BenBktech/Comprendre-Bitcoin/refs/heads/main/12.%20Signatures%20Num%C3%A9riques/images/1.png)

## Pourquoi Bitcoin utilise-t-il des signatures numériques ?

Dans Bitcoin, chaque transaction doit prouver que l’expéditeur est bien le propriétaire des bitcoins qu’il veut envoyer.

🚨 Mais si la clé privée était directement inscrite dans la transaction, tout le monde pourrait la voir et l’utiliser !

![img2](https://raw.githubusercontent.com/BenBktech/Comprendre-Bitcoin/refs/heads/main/12.%20Signatures%20Num%C3%A9riques/images/2.png)

💡 Solution :
Au lieu de mettre la clé privée dans la transaction, on utilise une signature numérique pour prouver qu’on la possède sans jamais la révéler.

![img3](https://raw.githubusercontent.com/BenBktech/Comprendre-Bitcoin/refs/heads/main/12.%20Signatures%20Num%C3%A9riques/images/3.png)

📌 Comparaison :

- Clé privée → Comme un stylo personnel que seul vous possédez.
- Signature numérique → Comme une signature que vous laissez sur un document, prouvant que vous l’avez signé, mais sans donner votre stylo.

## Comment fonctionne une signature numérique dans Bitcoin ?

Une signature numérique se base sur deux éléments :
- Votre clé privée (gardée secrète).
- Les données de la transaction (ce que vous voulez signer).

![img4](https://raw.githubusercontent.com/BenBktech/Comprendre-Bitcoin/refs/heads/main/12.%20Signatures%20Num%C3%A9riques/images/4.png)

Le processus se fait en deux étapes :

1️⃣ Création de la signature

- Votre clé privée est combinée avec les données de la transaction.
- Un algorithme mathématique (ECDSA) génère une signature unique.
- Cette signature est incluse dans la transaction, prouvant que vous êtes l’expéditeur légitime.


2️⃣ Vérification de la signature

- Toute personne peut vérifier la signature en utilisant votre clé publique.
- Si la signature est valide, cela prouve que la transaction a bien été signée avec la clé privée correspondante.

💡 Une signature numérique est unique pour chaque transaction !
Si quelqu’un essaie de copier votre signature et de l’utiliser dans une autre transaction, elle sera invalide.

## Que se passe-t-il si quelqu’un essaie de modifier la transaction ?

Si quelqu’un tente de modifier une transaction après qu’elle ait été signée (par exemple, en changeant le montant ou l’adresse du destinataire), la signature ne correspondra plus aux nouvelles données.

![img5](https://raw.githubusercontent.com/BenBktech/Comprendre-Bitcoin/refs/heads/main/12.%20Signatures%20Num%C3%A9riques/images/5.png)

📌 Résultat : La transaction sera immédiatement rejetée par le réseau Bitcoin.

💡 Cela garantit que personne ne peut modifier votre transaction après que vous l’ayez signée.