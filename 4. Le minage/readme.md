# Le Minage Bitcoin : Comment Fonctionne-t-il ?

## Qu’est-ce que le minage de Bitcoin ?

Le minage Bitcoin est le processus qui permet d’enregistrer définitivement les transactions sur la blockchain. Il repose sur un mécanisme appelé preuve de travail (Proof of Work), qui garantit la sécurité du réseau en empêchant toute tentative de fraude ou de manipulation des transactions.

Mais contrairement à un simple enregistrement de données, le minage impose une compétition ouverte entre des ordinateurs spécialisés qui effectuent des calculs complexes. Cette compétition permet de sélectionner de manière impartiale et aléatoire quel bloc sera ajouté à la blockchain.

Sans le minage, Bitcoin ne pourrait pas fonctionner, car il n’y aurait aucun moyen fiable d’accorder l’ensemble du réseau sur un même historique des transactions.

## Comment fonctionne le minage ?

### Le mempool : la salle d’attente des transactions

Lorsqu’une transaction est initiée sur Bitcoin, elle est diffusée aux nœuds du réseau et stockée temporairement dans un espace appelé mempool. Il s’agit d’un réservoir où les transactions attendent d’être confirmées et intégrées dans un bloc.

![1](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/4.%20Le%20minage/images/1.png)

Tous les mineurs ont accès à ces transactions et essaient de les inclure dans un bloc, mais seules les transactions incluses dans un bloc validé seront officiellement enregistrées dans la blockchain.

![2](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/4.%20Le%20minage/images/2.png)

### La preuve de travail (Proof of Work)

Le minage repose sur un problème mathématique complexe appelé preuve de travail.

Concrètement, les mineurs doivent :

- **Prendre toutes les transactions du bloc** et les transformer en une empreinte numérique unique, appelée hash.
- **Tester différentes valeurs pour le nonce**, afin de générer un nouveau hash.
- **Trouver un hash qui commence par un certain nombre de zéros**, selon la difficulté imposée par le réseau.

Ce processus est totalement aléatoire et repose sur la force brute : le mineur doit essayer des milliards de combinaisons avant de trouver la bonne.

![3](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/4.%20Le%20minage/images/3.png)

Lorsque l’un des mineurs parvient à trouver une solution valide, il diffuse son bloc au réseau, qui le vérifie et l’ajoute à la blockchain.

![4](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/4.%20Le%20minage/images/4.png)

## Pourquoi le minage est-il essentiel ?

Le minage joue plusieurs rôles fondamentaux dans le réseau Bitcoin :

### Sécurisation du réseau

Le mécanisme de preuve de travail empêche un attaquant de modifier les transactions passées ou de dépenser deux fois les mêmes bitcoins. Pour falsifier une transaction, il faudrait remonter toute la blockchain et recalculer tous les blocs précédents, ce qui est pratiquement impossible en raison de la puissance de calcul nécessaire.

### Résolution du problème du double spending

Lorsque vous effectuez une transaction en bitcoins, tous les nœuds du réseau n'en sont pas informés instantanément. En effet, les transactions se déplacent sur le réseau bitcoin en passant d'un nœud à l'autre.

![5](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/4.%20Le%20minage/images/5.png)

Imaginons qu’un utilisateur tente de dépenser les mêmes bitcoins deux fois, en envoyant une transaction à deux commerçants différents. Ces deux transactions circuleraient sur le réseau en même temps, créant un conflit.

![6](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/4.%20Le%20minage/images/6.png)

- Certains nœuds reçoivent la transaction rouge en premier (et ignorent la transaction verte).
- Certains nœuds reçoivent la transaction verte en premier (et ignorent la transaction rouge).

Pourtant, même si nous savons que vous avez effectué la transaction rouge en premier, en raison de la façon dont les transactions se déplacent sur le réseau bitcoin, le réseau serait en désaccord sur la question de savoir s'il faut passer la transaction rouge ou verte.

La règle du minage est simple : seule la première transaction incluse dans un bloc validé sera enregistrée, tandis que l’autre sera automatiquement rejetée.

Par exemple, si un nœud avec la transaction verte réussit à miner un bloc, c'est cette transaction qui est ajoutée à la blockchain, et la transaction rouge est exclue du réseau.

Cette méthode de sélection des transactions semble peu orthodoxe, je le sais, mais c'est la solution qu'utilise le réseau bitcoin pour parvenir à un consensus en cas de transactions contradictoires (également connues sous le nom de « double dépense »).

![7](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/4.%20Le%20minage/images/7.png)

### Émission de nouveaux bitcoins

Le minage est aussi le seul moyen de créer de nouveaux bitcoins. Chaque fois qu’un mineur trouve un bloc valide, il reçoit une récompense en bitcoins, appelée block reward.

Cette récompense suit un programme prédéfini appelé halving : tous les 210 000 blocs (environ tous les 4 ans), la récompense est divisée par deux.

- 2009 : 50 BTC par bloc
- 2012 : 25 BTC
- 2016 : 12,5 BTC
- 2020 : 6,25 BTC
- 2024 : 3,125 BTC (prochain halving)

Cela garantit une émission contrôlée et déflationniste de Bitcoin, jusqu’à atteindre un maximum de 21 millions de BTC en circulation.

## Comment la difficulté du minage s’adapte-t-elle ?

Le protocole Bitcoin ajuste la difficulté du minage toutes les 2016 blocs (environ toutes les deux semaines).

Si les blocs sont minés trop rapidement, la difficulté augmente.
Si les blocs prennent plus de temps à être validés, la difficulté diminue.

Ce mécanisme permet de maintenir un rythme constant d’un bloc environ toutes les 10 minutes, quel que soit le nombre de mineurs en activité.

## Peut-on encore miner Bitcoin aujourd’hui ?

Oui, mais pas avec un simple ordinateur.

### L’évolution du matériel de minage

- 2009-2011 : CPU mining → Possibilité de miner avec un simple processeur.
- 2011-2013 : GPU mining → Les cartes graphiques sont devenues plus performantes que les CPU.
- 2013-2015 : FPGA mining → Des circuits programmables plus spécialisés sont apparus.
- Depuis 2015 : ASIC mining → Machines ultra-spécialisées uniquement dédiées au minage de Bitcoin.

Aujourd’hui, pour être rentable, il faut utiliser des ASICs (Application-Specific Integrated Circuits), qui sont des machines optimisées pour effectuer uniquement du minage Bitcoin.

### Les pools de minage

Le minage individuel est devenu quasiment impossible. Pour maximiser leurs chances, les mineurs rejoignent des pools de minage, où plusieurs mineurs mettent en commun leur puissance de calcul et partagent les récompenses obtenues.

### L'impact de la consommation énergétique
Le minage Bitcoin consomme énormément d’électricité. C’est pourquoi les grandes fermes de minage sont souvent situées dans des régions où l’électricité est bon marché, comme :

- La Chine (avant les restrictions)
- Le Kazakhstan
- Le Canada
- L’Islande
- Les États-Unis (Texas, Wyoming)