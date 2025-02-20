# Les Blocs : L’Unité Fondamentale de la Blockchain Bitcoin

## Qu’est-ce qu’un bloc dans Bitcoin ?

Un bloc est un regroupement de transactions qui ont été validées et ajoutées à la blockchain.

Chaque bloc contient :
- Une liste de transactions récentes.
- Des métadonnées (informations sur le bloc lui-même).
- Un lien cryptographique avec le bloc précédent.

L’enchaînement de ces blocs forme la blockchain, garantissant ainsi l’intégrité et la sécurité du réseau Bitcoin.

![1](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/6.%20Les%20Blocs/images/1.png)

## Comment sont formés les blocs ?

Les blocs sont créés au cours du processus de minage.

Lorsque vous effectuez une transaction Bitcoin, celle-ci n’est pas immédiatement ajoutée à la blockchain. Elle est d’abord placée dans un espace temporaire appelé mempool (ou "pool de mémoire"), qui regroupe toutes les transactions en attente de validation.

![2](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/6.%20Les%20Blocs/images/2.png)

## Construction d’un bloc candidat

Un mineur sélectionne des transactions du mempool et les regroupe dans ce que l’on appelle un bloc candidat.

![3](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/6.%20Les%20Blocs/images/3.png)

Ce bloc candidat n’est pas encore ajouté à la blockchain : il doit d’abord être validé à travers la preuve de travail (Proof of Work).

Les mineurs sélectionnent en priorité les transactions avec les frais les plus élevés, car ils sont directement récompensés par ces frais.

## La structure d’un bloc Bitcoin

Chaque bloc Bitcoin contient deux parties :

- Le bloc de transactions : Une liste de transactions confirmées.
- L’en-tête du bloc (block header) : Une série de métadonnées qui décrit le bloc et permet son intégration dans la blockchain.

![4](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/6.%20Les%20Blocs/images/4.png)

### Le bloc de transactions

C’est la partie principale du bloc : elle contient toutes les transactions validées par le mineur.

Pour s’assurer de l’intégrité des transactions dans le bloc, Bitcoin utilise une structure de données appelée "Merkle Tree".

Le Merkle Root, inclus dans l’en-tête du bloc, est une empreinte cryptographique unique qui résume toutes les transactions contenues dans le bloc.

![5](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/6.%20Les%20Blocs/images/5.png)

### L’en-tête du bloc (Block Header)

L’en-tête du bloc contient des informations essentielles pour relier chaque bloc aux précédents et garantir sa validité. Il comprend :

- **Version** : Indique la version du protocole Bitcoin.
- **Hash du bloc précédent** : Permet de relier le bloc au précédent et assure l’intégrité de la blockchain.
- **Merkle Root** : Hash cryptographique unique qui représente toutes les transactions du bloc.
- **Horodatage** : Heure à laquelle le bloc a été miné.
- **Cible (Target)** : Valeur définissant la difficulté du minage.
- **Nonce** : Nombre utilisé par les mineurs pour tenter de résoudre le bloc.

Le hash du bloc précédent est crucial : il garantit que chaque bloc est lié au précédent, formant ainsi une chaîne sécurisée et infalsifiable.

![6](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/6.%20Les%20Blocs/images/6.png)

## Comment un bloc est-il ajouté à la blockchain ?

Une fois qu’un mineur a constitué un bloc candidat, il doit résoudre un problème cryptographique pour que son bloc soit accepté par le réseau.

### Le rôle de la preuve de travail (Proof of Work)

Le mineur doit générer un hash du bloc (à partir de l’en-tête du bloc) qui respecte une contrainte précise : il doit être inférieur à une valeur cible définie par le réseau.

Plus la difficulté est élevée, plus cette valeur cible est basse, ce qui rend la recherche d’un hash valide plus difficile.

![7](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/6.%20Les%20Blocs/images/7.png)

### Utilisation du nonce pour trouver un hash valide

Comme le hash du bloc est déterminé par son contenu, le mineur ne peut pas le modifier directement. Pour tenter de produire un hash valide, il modifie un champ appelé nonce et recommence le calcul jusqu’à ce qu’il trouve une solution qui respecte la cible imposée.

![8](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/6.%20Les%20Blocs/images/8.png)

Le processus :

- Le mineur essaie une valeur de nonce, calcule le hash du bloc et vérifie s’il respecte la cible.
- Si ce n’est pas le cas, il modifie le nonce et recommence.
- Lorsqu’un hash valide est trouvé, le bloc est considéré comme résolu et est proposé au réseau pour validation.

Ce processus est purement aléatoire et demande une énorme puissance de calcul, d’où l’utilisation de machines spécialisées (ASICs) dans le minage Bitcoin.

![9](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/6.%20Les%20Blocs/images/9.png)

## Que se passe-t-il lorsqu’un bloc est miné ?

Une fois qu’un mineur a trouvé un hash valide, son bloc est ajouté à la blockchain et propagé à l’ensemble du réseau.

![10](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/6.%20Les%20Blocs/images/10.png)

Tous les autres nœuds vérifient alors :
- Que le hash respecte bien les critères de difficulté.
- Que les transactions contenues dans le bloc sont valides.
- Que le bloc suit bien le précédent dans la chaîne.

Si tout est correct, les autres mineurs acceptent ce nouveau bloc et commencent immédiatement à travailler sur le suivant.

Chaque nouveau bloc doit inclure le hash du bloc précédent, ce qui crée une chaîne inaltérable où toute modification d’un bloc passé rendrait invalides tous les blocs suivants.