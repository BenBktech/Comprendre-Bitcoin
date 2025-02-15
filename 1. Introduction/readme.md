# Introduction à Bitcoin

Bitcoin est une monnaie numérique décentralisée qui fonctionne sur une blockchain sécurisée grâce à un réseau de mineurs, permettant des transactions sans intermédiaire ni autorité centrale.

Bitcoin est un programme informatique, vous pouvez le télécharger ici : [Bitcoin.org](https://bitcoin.org/en/download)

![Screenshot1](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot1.png)

Lorsqu'une nouvelle transaction est initiée sur le réseau, elle est transmise de machine en machine jusqu'à ce que tous les participants en aient une copie. Environ toutes les 10 minutes, un ordinateur (nœud) choisi aléatoirement ajoute les transactions récentes à la blockchain et diffuse cette mise à jour à l'ensemble du réseau.

![Screenshot2](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot2.png)

Le protocole Bitcoin repose sur un vaste réseau d'ordinateurs interconnectés qui échangent en permanence un registre commun et l’actualisent avec chaque nouvelle transaction.


## Quel problème Bitcoin résout-il ?

Bitcoin apporte une solution à l’absence d’un système de paiement fonctionnant sans autorité centrale.

Avant son invention, il était déjà possible d’échanger des transactions via un réseau informatique. Toutefois, un problème majeur subsistait : la possibilité d’introduire des transactions contradictoires. Par exemple, un utilisateur pouvait tenter d’utiliser une même unité de monnaie numérique pour effectuer deux paiements distincts et les diffuser simultanément sur le réseau.

Ce phénomène est appelé "double dépense".

Certains ordinateurs recevront d’abord la transaction verte, tandis que d’autres recevront en premier la transaction rouge.

Dans un système de paiement électronique sans autorité centrale, il devient alors complexe de déterminer laquelle de ces transactions a réellement eu lieu en premier, car chaque machine du réseau fonctionne de manière indépendante.

Qui doit donc trancher et décider quelle transaction doit être validée et inscrite dans le registre ?

Bitcoin résout ce problème en obligeant les nœuds du réseau à stocker temporairement toutes les transactions qu’ils reçoivent avant de les inscrire dans la blockchain. Toutes les 10 minutes environ, un nœud sélectionné au hasard ajoute ces transactions à l’historique, garantissant ainsi l’intégrité du système.

Une fois mis à jour, ce registre est diffusé à l’ensemble du réseau. Les nœuds considèrent alors les transactions qu’il contient comme valides et éliminent de leur mémoire celles qui entrent en conflit avec ces dernières.

Ainsi, aucune transaction en double ne peut être enregistrée, et tous les nœuds synchronisent régulièrement leur copie du registre pour garantir une version unique et cohérente.

L'ajout de nouvelles transactions au registre, connu sous le nom de minage, repose sur une compétition ouverte à l’ensemble du réseau, empêchant ainsi tout contrôle par un seul nœud.

## Comment fonctionne le minage ?

Le minage consiste à enregistrer de nouveaux blocs de transactions sur la blockchain.

Dans un premier temps, chaque nœud conserve les transactions récentes dans une mémoire temporaire appelée mempool.

N'importe quel nœud du réseau peut alors tenter d'inscrire ces transactions sur la blockchain. Pour cela, il regroupe les transactions de sa mempool dans un bloc, puis utilise sa puissance de calcul pour essayer d'ajouter ce bloc à la chaîne existante.

### Quel rôle joue la puissance de calcul ?

Pour inscrire un bloc sur la blockchain, il faut le soumettre à une fonction de hachage. Il s’agit d’un programme qui transforme une quantité quelconque de données en une séquence chiffrée unique et imprévisible. Ce processus repose sur des calculs intensifs, nécessitant une puissance de traitement considérable.

Pour qu’un bloc soit validé et intégré à la blockchain, son empreinte numérique (ou hash du bloc) doit être inférieure à un seuil prédéfini, accepté par l’ensemble du réseau.

Si le hash obtenu pour le bloc ne respecte pas le seuil requis, il est possible de modifier légèrement certaines données à l'intérieur du bloc, puis de le soumettre à nouveau à la fonction de hachage. Chaque tentative génère un nouveau résultat totalement différent, dans l'espoir d'obtenir une valeur conforme au seuil fixé. Si ce n'est pas le cas, le processus est répété jusqu'à obtenir un hash valide.

Avec le temps, l’un des nœuds du réseau (ou mineurs) finit par générer un hash de bloc respectant le seuil requis. Ce bloc de transactions est alors validé et ajouté à la blockchain.

Une fois ce bloc intégré, le processus recommence pour l’ajout du bloc suivant.

En résumé, le minage repose sur l’utilisation de puissance de calcul pour effectuer un grand nombre de tentatives de hachage le plus rapidement possible, dans l’espoir d’être le premier à produire un hash conforme aux critères fixés. Le mineur qui réussit peut alors inscrire son bloc de transactions dans la blockchain et le partager avec l’ensemble du réseau.

L’utilisation d’une fonction de hachage associée à une valeur cible crée une compétition ouverte à tous, empêchant ainsi qu’un seul ordinateur ou acteur ne contrôle l’enregistrement des transactions. Ce mécanisme garantit un système de validation distribué, sans autorité centrale.

Bien que techniquement accessible à n’importe qui, le minage sur un ordinateur personnel est devenu obsolète. Aujourd’hui, seules des machines spécialisées, conçues pour exécuter ces calculs de manière extrêmement rapide et économe en énergie, permettent de rester compétitif. En conséquence, le minage est désormais principalement pratiqué par ceux ayant accès à ces équipements et à une électricité à moindre coût.

## D’où viennent les bitcoins ?

Pour encourager l'utilisation de puissance de calcul dans l'ajout de nouveaux blocs à la blockchain, chaque bloc validé génère un certain nombre de bitcoins qui n’existaient pas auparavant. Ainsi, lorsqu’un mineur parvient à inscrire un bloc, il reçoit ces nouveaux bitcoins en récompense de ses efforts.

Ce lot de bitcoins nouvellement créés, appelé récompense de bloc, est la raison pour laquelle ce processus porte le nom de minage, en référence à l’extraction de ressources précieuses.

## Pourquoi appelle-t-on cela la "blockchain" ?

Les transactions ne sont pas inscrites une par une, mais regroupées en blocs avant d’être ajoutées. Chaque nouveau bloc vient se greffer sur le précédent, formant ainsi une chaîne de blocs – d’où le terme blockchain.

De plus, chaque nœud du réseau considère toujours la chaîne de blocs la plus longue comme la version référence de la blockchain.

Ainsi, les mineurs ajoutent systématiquement leurs nouveaux blocs à l’extrémité de cette chaîne dominante, car toute transaction située en dehors de cette dernière est considérée comme invalide.

Ainsi, toute tentative de modification de l’historique des transactions nécessiterait de reconstruire une chaîne de blocs plus longue que celle existante, afin qu’elle soit reconnue comme la nouvelle référence par les autres nœuds. Cependant, pour y parvenir, un mineur isolé devrait posséder une puissance de calcul supérieure à celle de l’ensemble du réseau combiné.

Grâce à la puissance collective du réseau, il devient quasiment impossible pour un individu de surpasser l’ensemble des mineurs et de modifier la blockchain.

Autrement dit, l’intégrité de l’historique des transactions – et donc la sécurité des fonds – est assurée par l’énorme quantité d’énergie investie dans le minage.

## Comment fonctionnent les transactions Bitcoin ?

Imagine la blockchain comme un grand registre contenant des enveloppes sécurisées, appelées outputs.

Chaque enveloppe contient une certaine quantité de bitcoins et est verrouillée avec une clé unique. Ces outputs représentent les fonds disponibles et servent à effectuer des transactions.

Quand tu effectues une transaction en Bitcoin, tu ouvres certaines enveloppes contenant des bitcoins, puis tu crées de nouvelles enveloppes avec des montants mis à jour et tu les verrouilles avec les clés des nouveaux propriétaires.

Lorsque tu envoies des bitcoins à quelqu'un, tu ne les transfères pas directement comme un virement bancaire. En réalité, tu places une certaine quantité de bitcoins dans une nouvelle "enveloppe" et tu y mets un verrou que seul le destinataire pourra ouvrir avec sa clé privée.

Exemple : Si je veux t’envoyer des bitcoins, je vais :

- Choisir des fonds que je peux déverrouiller sur la blockchain.
- Créer une nouvelle enveloppe contenant le montant que je t’envoie et y placer un verrou que seule ta clé peut ouvrir.
- Recevoir la monnaie en retour : si le montant que j’ai débloqué est plus grand que ce que je veux t’envoyer, je crée une deuxième enveloppe avec la différence, qui me revient.

Ce système fonctionne comme si tu donnais un billet de 50 € pour payer 30 € : on ne coupe pas le billet, on te rend la monnaie avec une nouvelle enveloppe contenant la somme restante. 

Lorsque tu veux à ton tour envoyer des bitcoins à quelqu’un, tu répètes le même processus : tu débloques des fonds existants, puis tu crées de nouvelles "enveloppes" avec un verrou destiné au nouveau propriétaire.

Ainsi, chaque transaction est liée à une précédente, formant une chaîne d’échanges interconnectés où les bitcoins circulent à travers une suite de transactions successives.

Une fois qu’une transaction est validée et ajoutée à la blockchain, les anciennes "enveloppes" utilisées sont définitivement considérées comme dépensées et ne peuvent plus être réutilisées. En revanche, les nouvelles enveloppes créées deviennent disponibles et pourront être utilisées dans de futures transactions.

Une partie des fonds est transférée au destinataire, tandis que l’excédent (la monnaie) est retourné à l’expéditeur sous forme d’un nouvel output.

Ce qu'il faut comprendre
- Les bitcoins ne sont jamais "stockés" à un endroit précis : ils circulent sous forme d’outputs qui sont continuellement dépensés et recréés.
- Chaque transaction dépend des précédentes : il y a une traçabilité totale des fonds, chaque bitcoin ayant une "histoire" liée à son origine.
- Les UTXO garantissent qu’un même bitcoin ne peut pas être dépensé deux fois, car une fois qu’un output est utilisé, il devient invalide et ne peut plus être réutilisé.

En résumé, ce schéma montre que Bitcoin fonctionne comme un système de billets numériques : tu ne retires pas une somme exacte de ton compte, mais tu utilises des "billets" existants en les fractionnant et en recevant la monnaie en retour. 

## Comment possèdes-tu des bitcoins ?

Pour recevoir des bitcoins, tu as besoin d’un jeu de clés uniques.

Ces clés fonctionnent un peu comme un numéro de compte et un mot de passe, mais dans Bitcoin, elles sont appelées clé publique et clé privée.

- La clé publique est comme ton adresse e-mail : tu peux la partager pour recevoir des bitcoins.
- La clé privée est comme ton mot de passe : elle te permet d’accéder à tes fonds et de les envoyer.

Exemple :

- Tu veux recevoir des bitcoins ? Tu donnes ta clé publique à l’expéditeur.
- Lorsqu’il t’envoie des bitcoins, ils sont verrouillés avec ta clé publique.
- Plus tard, si tu veux les envoyer à quelqu’un d’autre, tu devras utiliser ta clé privée pour déverrouiller ces fonds et les transférer.

C’est un peu comme si quelqu’un déposait de l’argent dans un coffre à ton nom, et que toi seul pouvais l’ouvrir avec ta clé privée. 

## Comment obtenir une clé publique et une clé privée ?

Grâce à la cryptographie, tu peux générer toi-même ces clés de manière sécurisée.

- La clé privée est simplement un grand nombre aléatoire.
- La clé publique est ensuite calculée à partir de cette clé privée.

💡 Ce qui est astucieux, c'est que tu peux partager ta clé publique sans risque :
➡️ Elle permet aux autres de t’envoyer des bitcoins.
❌ Mais il est impossible de retrouver ta clé privée à partir de la clé publique.

C’est ce principe qui garantit la sécurité et l’inviolabilité des fonds dans Bitcoin. 

## Comment débloquer tes bitcoins ?

Lorsque tu veux utiliser des bitcoins associés à ta clé publique, tu dois prouver que tu en es bien le propriétaire. Pour cela, tu utilises ta clé privée pour créer une signature numérique.


Cette signature a deux rôles importants :

- Elle prouve que tu possèdes bien la clé privée, sans jamais la révéler.
- Elle est valable uniquement pour cette transaction précise, ce qui signifie qu’elle ne peut pas être réutilisée pour débloquer d’autres fonds liés à la même clé publique.

Grâce à ce mécanisme, Bitcoin garantit que seuls les véritables propriétaires peuvent dépenser leurs bitcoins en toute sécurité.

## Résumé rapide sur le fonctionnement de Bitcoin

Bitcoin est un système de paiement décentralisé permettant d’échanger de la valeur sans intermédiaire. Conçu après la crise financière de 2008, il fonctionne grâce à la blockchain, un registre immuable partagé entre tous les participants du réseau.

Les transactions sont sécurisées par la cryptographie et validées par un processus appelé minage, où des ordinateurs résolvent des calculs pour ajouter de nouveaux blocs à la blockchain. En échange, les mineurs reçoivent une récompense en bitcoins.

Bitcoin garantit des transactions sécurisées, traçables et infalsifiables, sans passer par une autorité centrale. Son modèle repose sur la preuve de travail (Proof of Work), rendant toute falsification quasiment impossible.

Enfin, chaque utilisateur possède une clé privée pour signer ses transactions et une clé publique pour recevoir des fonds. Cela permet d’assurer la propriété et la sécurité des bitcoins, sans dépendre d’une banque. 