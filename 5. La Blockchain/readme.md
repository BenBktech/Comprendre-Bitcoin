# La Blockchain : Le Grand Livre Comptable de Bitcoin

## Qu’est-ce que la blockchain ?

La blockchain est un fichier qui contient l’ensemble des transactions Bitcoin depuis la création du réseau en 2009.

![1](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/5.%20La%20Blockchain/images/1.png)

Chaque utilisateur du réseau Bitcoin possède une copie de ce fichier, qui est régulièrement mis à jour avec les nouvelles transactions validées.

![2](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/5.%20La%20Blockchain/images/2.png)

## Pourquoi la blockchain est-elle essentielle ?

### Elle permet de calculer le solde des utilisateurs

Contrairement à un compte bancaire classique où un solde est mis à jour directement après chaque transaction, Bitcoin ne stocke pas les soldes des utilisateurs.

Au lieu de cela, la blockchain enregistre uniquement les transactions.

![3](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/5.%20La%20Blockchain/images/3.png)

Si vous voulez savoir combien de bitcoins sont présents sur une adresse, vous devez analyser toutes les transactions associées à cette adresse et en faire le solde.

Cela signifie que la blockchain ne ment jamais : tant qu’une transaction y est enregistrée, elle reste accessible et vérifiable par n’importe qui.

### Un registre infalsifiable

La blockchain est un fichier immuable : une fois qu’une transaction est ajoutée, elle ne peut pas être modifiée ni supprimée.

Pourquoi ? Parce que les transactions ne sont pas enregistrées individuellement mais regroupées dans des blocs, qui sont ensuite enchaînés cryptographiquement les uns aux autres.

Si quelqu’un essayait de modifier une transaction passée, cela changerait le hash du bloc concerné, ce qui casserait la liaison avec les blocs suivants. Résultat : l’ensemble du réseau rejetterait la tentative de fraude.

![4](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/5.%20La%20Blockchain/images/4.png)

C’est ce qui rend Bitcoin fiable et sécurisé.

## Pourquoi parle-t-on de “blockchain” ?

Le nom blockchain vient de la manière dont les transactions sont stockées :

- Les transactions ne sont pas enregistrées une par une mais regroupées en blocs.
- Ces blocs sont ensuite liés entre eux pour former une chaîne continue (chain).

Chaque bloc contient :

- Un ensemble de transactions validées.
- Un hash du bloc précédent, assurant la continuité et l'intégrité.
- Un numéro aléatoire (nonce) utilisé dans la preuve de travail.
- Un horodatage indiquant le moment de la validation.

Ce chaînage assure l’intégrité des données : modifier un seul bloc casserait toute la chaîne, ce qui est techniquement impossible sans un contrôle total du réseau (attaque des 51 %).

![5](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/5.%20La%20Blockchain/images/5.png)

## Comment la blockchain est-elle partagée et mise à jour ?

### Un fichier distribué sur tous les nœuds Bitcoin
La blockchain fonctionne comme un fichier partagé entre tous les nœuds Bitcoin, de manière similaire à un torrent BitTorrent.

Chaque nœud stocke une copie complète de la blockchain et la met à jour dès qu’un nouveau bloc est validé.

Si un nœud est en retard et n’a pas les derniers blocs, il les récupère automatiquement auprès des autres nœuds du réseau.

### La synchronisation des nouveaux nœuds

Lorsqu’un nouvel utilisateur télécharge un client Bitcoin (comme Bitcoin Core), le logiciel commence par télécharger l’ensemble de la blockchain pour se synchroniser avec le réseau.

- Taille actuelle de la blockchain : Environ 639.24 Go (et elle continue de croître).
- Bon à savoir : Ce téléchargement initial peut prendre plusieurs jours, mais c’est une étape unique. Une fois à jour, le client ne télécharge plus que les nouveaux blocs, qui pèsent environ 1 Mo toutes les 10 minutes.

### Comment obtenir une copie de la blockchain ?

Il est possible de télécharger la blockchain en installant un client Bitcoin officiel comme Bitcoin Core.

Une fois le client installé et lancé, il se connecte à d’autres nœuds et commence à télécharger l’intégralité de la blockchain.

Lorsque la synchronisation est terminée, vous possédez une copie complète et vérifiable de toutes les transactions Bitcoin depuis 2009.

En maintenant cette copie et en la partageant avec d’autres nœuds, vous contribuez à la décentralisation et à la sécurité du réseau.

Si vous exécutez un nœud complet, vous devenez un full node, un acteur clé du réseau Bitcoin.