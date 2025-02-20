# Le Hash : Le Fondement Cryptographique de Bitcoin

## Qu’est-ce qu’un hash ?

Un hash est une empreinte numérique unique générée à partir d’un ensemble de données. C’est une fonction mathématique qui convertit une entrée (texte, nombres, fichiers, transactions...) en une sortie unique de longueur fixe.

![1](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/3.%20Hash/images/1.png)

Dans Bitcoin, les fonctions de hachage cryptographiques sont utilisées pour garantir la sécurité, l’intégrité et l’immuabilité des données.

L’algorithme de hachage utilisé dans Bitcoin est SHA-256 (Secure Hash Algorithm 256 bits), qui produit des empreintes de 64 caractères hexadécimaux (ou 256 bits en binaire).

## Exemple de hash SHA-256

Si nous appliquons SHA-256 à une phrase simple :
```SHA-256("Bitcoin")```

Nous obtenons cette empreinte unique :
```6b9d2c6c9eaa5a9ed7d6398850e663d3b7ee68a731c5c822dd3d5fa95e8d29a5``` 

![1](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/3.%20Hash/images/1.png)

Ce hash est irréversible, c'est-à-dire qu'il est impossible de retrouver le texte original à partir du hash seul.

## Les propriétés fondamentales d’un hash

Les fonctions de hachage cryptographiques comme SHA-256 possèdent plusieurs caractéristiques essentielles pour la sécurité de Bitcoin :

### Longueur fixe

Quelle que soit la taille de l’entrée, la sortie a toujours la même longueur (256 bits pour SHA-256).

- "Bitcoin" =	6b9d2c6c9eaa5a9ed7d6398850e663d3b7ee68a731c5c822dd3d5fa95e8d29a5
- "Hello, world!" = 315f5bdb76d0f40a97d2a5c8b96e5310ed3e42482f70a4e1a9808e2d19f11679
- "Bitcoin is decentralized" = 5d1c3bfaeb6c7dbaf7b2a3545461c3c62088a02a4b423f5ebd503a2f7a55ed1b

![2](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/3.%20Hash/images/2.png)

### Effet avalanche (sensibilité aux modifications)

Un petit changement dans l’entrée entraîne un hash totalement différent.

- "Bitcoin" = 6b9d2c6c9eaa5a9ed7d6398850e663d3b7ee68a731c5c822dd3d5fa95e8d29a5
- "bitcoin" (lettre minuscule) = b15e3e02d8ed0c04dfbbd3b6b1b1d87731716acfc7c2e5f4a72f69a5f3e9f002

Bien que les deux textes soient presque identiques, le hash obtenu est complètement différent.

Cela garantit l'intégrité des données, car une modification, même minime, d’un bloc Bitcoin changera entièrement son empreinte.

![3](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/3.%20Hash/images/3.png)

### Irréversibilité (fonction unidirectionnelle)

On peut générer un hash à partir d’une donnée, mais il est impossible de retrouver la donnée originale à partir du hash seul.

Bitcoin utilise cette propriété pour sécuriser les transactions et protéger les informations sensibles sans avoir besoin de les chiffrer.

![4](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/3.%20Hash/images/4.png)

### Résistance aux collisions

Une collision se produit lorsque deux entrées différentes produisent le même hash.

Avec SHA-256, la probabilité d'une collision est extrêmement faible, rendant Bitcoin très sécurisé.