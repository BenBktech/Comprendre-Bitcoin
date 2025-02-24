# Clés et Adresses : Le Système d'Identification de Bitcoin

## Comment envoyer et recevoir des bitcoins ?

Pour utiliser Bitcoin, vous avez besoin de trois éléments essentiels :

- **Clé privée** → C’est votre mot de passe secret qui vous permet d’accéder à vos bitcoins.
- **Clé publique** → Un identifiant associé à votre clé privée.
- **Adresse Bitcoin** → Une version simplifiée de votre clé publique, utilisée pour recevoir des bitcoins.

📌 **Comparaison avec un compte bancaire :**

- **Adresse Bitcoin** = Votre numéro de compte.
- **Clé privée** = Votre mot de passe.
- **Clé publique** = Un identifiant associé à votre compte.

⚠️ **Important** : **Ne partagez jamais votre clé privée !** Si quelqu’un l’obtient, il peut voler vos bitcoins.

![img1](https://raw.githubusercontent.com/BenBktech/Comprendre-Bitcoin/refs/heads/main/11.%20Cl%C3%A9%20publique%20%26%20Cl%C3%A9%20priv%C3%A9e/images/1.png)

## D’où viennent les clés et les adresses Bitcoin ?

Les clés sont générées aléatoirement sur votre ordinateur ou votre portefeuille Bitcoin.

### La Clé Privée

Tout commence avec la génération d’un nombre aléatoire extrêmement grand.

![img2](https://raw.githubusercontent.com/BenBktech/Comprendre-Bitcoin/refs/heads/main/11.%20Cl%C3%A9%20publique%20%26%20Cl%C3%A9%20priv%C3%A9e/images/2.png)

📌 Exemple de clé privée (en hexadécimal) :
```
ef235aacf90d9f4aadd8c92e4b2562e1d9eb97f0df9ba3b508258739cb013db2
```

Une clé privée est un nombre compris entre 1 et 2²⁵⁶.

Cela représente un nombre de combinaisons si grand qu’il est mathématiquement impossible de le deviner.

La clé privée Bitcoin est un nombre compris entre 1 et : 115792089237316195423570985008687907852837564279074904382605163141518161494336

🌌 Il y a environ 10⁷⁸ à 10⁸² atomes dans l’univers observable.
👉 La probabilité que deux personnes génèrent par hasard la même clé privée est donc bien plus faible que de trouver une particule spécifique dans tout l’univers.

🌍 Il y a environ 10⁴⁹ atomes sur Terre.
👉 Trouver la même clé privée par hasard reviendrait à sélectionner un atome précis parmi des milliards de milliards de milliards de planètes comme la Terre.

💾 Un disque dur de 1 To contient environ 10¹² bits d’information.
👉 Il faudrait bien plus que tous les ordinateurs du monde travaillant pendant des milliards d’années pour espérer générer une clé déjà existante.

📌 Conclusion : Il est mathématiquement impossible que deux personnes génèrent la même clé privée par hasard.

💡 Pourquoi utiliser de l'hexadécimal (0-9 et a-f) ?

- Parce que c’est plus court qu’un nombre en base 10 et plus lisible pour un ordinateur.

### La Clé Publique

Une fois la clé privée générée, on l’utilise pour calculer la clé publique grâce à une fonction mathématique appelée cryptographie elliptique (secp256k1 pour Bitcoin).

📌 Propriété importante :
- Il est impossible de retrouver la clé privée à partir de la clé publique.

C’est une fonction à sens unique :

![img3](https://raw.githubusercontent.com/BenBktech/Comprendre-Bitcoin/refs/heads/main/11.%20Cl%C3%A9%20publique%20%26%20Cl%C3%A9%20priv%C3%A9e/images/3.png)

📌 Exemple de clé publique (format compressé) :

```
02b4632d08485ff1df2db55b9dafd23347d1c47a457072a1e87be26896549a8737
```

💡 Pourquoi ne pas utiliser directement la clé publique ?

Parce qu’elle est trop longue et peu pratique à manipuler.

### L’Adresse Bitcoin

Puisque la clé publique est trop encombrante, on en dérive une version plus courte et lisible : l’adresse Bitcoin.

📌 Processus de transformation :
- La clé publique est compressée avec SHA-256 et RIPEMD-160 (deux fonctions de hachage).
- On ajoute une somme de contrôle pour éviter les erreurs de saisie.
- On encode le tout en Base58 (alphabet sans caractères ambigus comme "0" et "O").

![img4](https://raw.githubusercontent.com/BenBktech/Comprendre-Bitcoin/refs/heads/main/11.%20Cl%C3%A9%20publique%20%26%20Cl%C3%A9%20priv%C3%A9e/images/4.png)

📌 Exemple d’adresse Bitcoin :
```
1EUXSxuUVy2PC5enGXR1a3yxbEjNWMHuem
```

💡 Propriété importante :

✔ On ne peut pas remonter à la clé publique ou privée à partir d’une adresse Bitcoin.

### Dois-je retenir toutes ces clés ?

Non, car tout découle de la clé privée.

- Clé publique = Calculée à partir de la clé privée.
- Adresse Bitcoin = Dérivée de la clé publique.

💡 Tant que vous possédez la clé privée, vous pouvez toujours recréer votre adresse et votre clé publique.

## Que se passe-t-il si je perds ma clé privée ?

Si vous perdez votre clé privée, vous perdez définitivement l’accès à vos bitcoins.

📌 Propriétés du système Bitcoin :
- On ne peut pas retrouver la clé privée à partir de l’adresse ou de la clé publique.
- Il n’existe aucun service de récupération.

💡 Bitcoin ne possède pas de "support client" pour récupérer vos fonds. Si vous perdez votre clé, vos bitcoins sont bloqués à jamais.

📌 Exemple :
- Imaginons que vous ayez 1 BTC stocké sur une adresse Bitcoin.
- Si vous perdez la clé privée associée, ces bitcoins restent sur la blockchain, mais personne ne pourra jamais les récupérer.

![img5](https://raw.githubusercontent.com/BenBktech/Comprendre-Bitcoin/refs/heads/main/11.%20Cl%C3%A9%20publique%20%26%20Cl%C3%A9%20priv%C3%A9e/images/5.png)