# Les Locks : Le Mécanisme qui Protège vos Bitcoins

## Pourquoi vos Bitcoins ne peuvent-ils pas être volés ?

Chaque output dans une transaction Bitcoin est verrouillé par un ensemble de conditions qui doivent être remplies pour pouvoir être dépensé dans une future transaction.

💡 En d'autres termes, ces verrous empêchent les bitcoins d’être volés, car ils garantissent que seul le propriétaire légitime peut les utiliser.

Lorsque vous recevez des bitcoins, ils sont stockés sous forme d’outputs, chacun verrouillé par une condition spécifique qui doit être satisfaite pour être dépensé.

img1

## Quand un lock est-il ajouté à un output ?

Rappelons le fonctionnement d’une transaction Bitcoin :

- Elle utilise des outputs existants (qui deviennent les inputs de la transaction).
- Elle crée de nouveaux outputs, chacun étant verrouillé à une adresse.
- C'est au moment de la création de ces nouveaux outputs que le verrou est défini.

💡 Exemple :
- Vous envoyez 0.5 BTC à votre ami.
- La transaction crée un nouvel output de 0.5 BTC et le verrouille à l’adresse Bitcoin de votre ami.

img2

Désormais, seule la personne possédant la clé privée de cette adresse peut utiliser ces 0.5 BTC.

Chaque output est verrouillé et ne peut être dépensé que par celui qui peut prouver qu’il en est le propriétaire.

img3

## Où les bitcoins sont-ils réellement stockés ?

Les bitcoins ne sont pas physiquement stockés sur votre ordinateur ou dans un fichier.

En réalité, ils existent uniquement sur la blockchain sous forme d'outputs verrouillés.

img4

img5

Lorsque vous effectuez une transaction, vous sélectionnez des outputs disponibles sur la blockchain, et une fois qu’ils sont utilisés, ils sont remplacés par de nouveaux outputs avec de nouveaux locks.

img6

💡 Ainsi, la blockchain est en réalité un gigantesque stockage de bitcoins verrouillés !

## À quoi ressemble un verrou dans Bitcoin ?

Les locks sont définis en Bitcoin Script, un langage de programmation simple utilisé dans les transactions.

img7

Un verrou standard pour protéger un output ressemble à ceci :

```
OP_DUP OP_HASH160 <Adresse Bitcoin> OP_EQUALVERIFY OP_CHECKSIG
```

🔹 Décryptons ce script :
- OP_HASH160 <Adresse Bitcoin> → Vérifie que l’output est bien verrouillé à cette adresse.
- OP_CHECKSIG → Vérifie si la signature du propriétaire est valide.

Cela signifie que seule la personne possédant la clé privée associée à cette adresse pourra déverrouiller l’output et l’utiliser comme input dans une future transaction.

img8

## Comment un output est-il déverrouillé ?

Lorsque vous créez une transaction, vous devez joindre un "script de déverrouillage" (unlocking script) aux outputs que vous voulez utiliser.

img9

Ensuite, pour déverrouiller un script de verrouillage typique, nous devons prouver que nous possédons l'adresse contenue dans le verrou. Pour ce faire, nous fournissons la clé privée liée à l'adresse.

img10

img11

💡 Important : Votre clé privée n’est jamais révélée dans la transaction !

Au lieu de cela, une signature numérique unique est utilisée pour prouver que vous êtes bien le propriétaire, sans jamais exposer votre clé secrète.


## Mais... est-ce qu’on ne dévoile pas notre clé privée en déverrouillant un output ?

Très bonne question !

Si le réseau Bitcoin exigeait que vous fournissiez votre clé privée pour prouver que vous êtes le propriétaire, cela poserait un énorme problème de sécurité.

🔹 La solution : les signatures numériques

img12

- Au lieu de fournir la clé privée, vous utilisez la clé privée pour générer une signature unique.
- Cette signature est spécifique à cette transaction, ce qui signifie qu’elle ne peut pas être réutilisée.
- Grâce à un mécanisme mathématique, le réseau peut vérifier que la signature provient bien du propriétaire, sans jamais voir la clé privée.

img13

## Bitcoin : Une monnaie programmable grâce aux locks

Les locks standard permettent de verrouiller un output pour une seule adresse, mais Bitcoin Script permet de créer des locks bien plus complexes !

💡 Exemples de verrous avancés :

- Multisig (Multisignature) → Déverrouillage possible uniquement si plusieurs signatures sont fournies.

img14

- Timelocks → L’output ne peut être dépensé qu’après une certaine date.

img15

Ces possibilités font de Bitcoin une monnaie programmable, ouvrant la porte à des contrats intelligents simples directement sur la blockchain.