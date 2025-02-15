# Introduction à Bitcoin

Bitcoin est une **monnaie numérique décentralisée** qui fonctionne sur une **blockchain sécurisée**. Son réseau repose sur des mineurs qui valident les transactions **sans intermédiaire ni autorité centrale**.

Vous pouvez télécharger le programme ici : [Bitcoin.org](https://bitcoin.org/en/download).

![Screenshot1](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot1.png)

Lorsque vous envoyez une transaction sur le réseau Bitcoin, elle est transmise de machine en machine jusqu’à ce que tous les participants l’aient enregistrée. Toutes les **10 minutes environ**, un ordinateur (nœud) sélectionné au hasard **ajoute les transactions récentes à la blockchain** et partage cette mise à jour avec le réseau.

![Screenshot2](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot2.png)

Le protocole Bitcoin repose sur un vaste réseau d’ordinateurs interconnectés qui **échangent et mettent à jour un registre commun** avec chaque nouvelle transaction.

---

## 📌 Quel problème Bitcoin résout-il ?

Bitcoin a été conçu pour résoudre le problème des **paiements électroniques sans autorité centrale**.

Avant son invention, il était déjà possible de transmettre des transactions sur un réseau informatique. Cependant, un problème majeur persistait :  
💡 **La double dépense** → Un utilisateur pouvait envoyer la même unité de monnaie numérique **deux fois** en simultané sur le réseau.

### 🔴 Le problème de la double dépense

Dans un réseau sans intermédiaire, certaines machines pourraient **recevoir la transaction A en premier**, tandis que d’autres recevraient **la transaction B**.  
Le problème est alors de **déterminer laquelle est valide** sans autorité centrale.

### ✅ Comment Bitcoin règle ce problème ?

Bitcoin empêche la double dépense grâce à un mécanisme de **validation des transactions** :
1. **Les nœuds du réseau stockent temporairement toutes les transactions** qu’ils reçoivent.
2. **Toutes les 10 minutes**, un nœud (sélectionné au hasard) **ajoute ces transactions à la blockchain**.
3. **Le réseau adopte ensuite cette mise à jour** et **rejette toutes les transactions conflictuelles**.

Ainsi, **toutes les machines du réseau conservent la même version de la blockchain**, empêchant toute tentative de fraude.

---

## ⛏️ Comment fonctionne le minage ?

Le **minage** est le processus qui permet d'ajouter de nouveaux blocs de transactions à la blockchain.

### 🔹 Étape 1 : Collecte des transactions  
Chaque nœud conserve les transactions récentes dans une **mémoire temporaire** appelée **mempool**.

### 🔹 Étape 2 : Création d’un bloc  
Un nœud sélectionné regroupe ces transactions dans un **bloc**, qu’il tente d’ajouter à la blockchain.

### 🔹 Étape 3 : Calcul du hash  
Pour inscrire un bloc, il doit être **haché** à l’aide d’une **fonction cryptographique**.  
Un "hash" est une **empreinte numérique unique** qui doit respecter une **condition spécifique**.

### 🔹 Étape 4 : Preuve de travail  
Les mineurs modifient certaines valeurs et **recalculent le hash** en boucle jusqu'à obtenir un résultat valide.  
C’est un processus exigeant **beaucoup de puissance de calcul**.

### 🔹 Étape 5 : Validation et diffusion  
Lorsqu’un mineur **trouve un hash valide**, son bloc est ajouté à la blockchain et partagé avec l’ensemble du réseau.

### 💡 Pourquoi parle-t-on de minage ?
Le terme "minage" vient du fait que les mineurs sont **récompensés** avec de nouveaux bitcoins à chaque bloc validé. Cette récompense est appelée **récompense de bloc**.

---

## 🏗️ Pourquoi appelle-t-on cela la "blockchain" ?

Les transactions ne sont pas enregistrées individuellement, mais regroupées en **blocs**.  
Chaque bloc est lié au précédent, **formant une chaîne inaltérable** : **la blockchain**.

📌 **Règles essentielles de la blockchain :**  
- Le réseau considère toujours **la plus longue chaîne** comme la version officielle.  
- Pour modifier l’historique des transactions, il faudrait **recalculer une chaîne plus longue**, ce qui est **quasiment impossible** sans contrôler la majorité du réseau.  

Ce mécanisme garantit **l’intégrité et la sécurité** du registre Bitcoin.

---

## 💰 D’où viennent les bitcoins ?

Les nouveaux bitcoins sont créés par le **minage**.  
Lorsqu’un mineur valide un bloc, il **reçoit une récompense** en bitcoins fraîchement générés.

🎯 **Pourquoi cette récompense ?**  
Elle **incite les mineurs à sécuriser le réseau**, tout en assurant une **distribution progressive des nouveaux bitcoins**.

---

## 🔄 Comment fonctionnent les transactions Bitcoin ?

Bitcoin fonctionne comme un **portefeuille rempli de billets numériques** appelés **outputs** :

1. **Chaque output contient une somme précise de bitcoins**.
2. **Quand tu envoies une transaction, tu sélectionnes un ou plusieurs outputs** que tu possèdes.
3. **Tu crées de nouveaux outputs** en répartissant le montant entre le destinataire et toi (la monnaie rendue).
4. **Une fois un output utilisé, il devient invalide** et ne peut plus être dépensé.

📌 **Comparaison simple :**
- 🔹 **Tu as un billet de 50€ et tu dois payer 30€**.  
- 🔹 **Tu ne peux pas couper ton billet**, alors tu **le donnes en entier** et on te rend 20€.  
- 🔹 En Bitcoin, c’est pareil : un nouveau "billet" (output) est créé pour **rendre la monnaie**.

---

## 🔑 Comment posséder des bitcoins ?

Pour recevoir et stocker des bitcoins, tu as besoin de **deux clés cryptographiques** :

- **Clé publique 🔓** → C’est comme une **adresse e-mail** pour recevoir des bitcoins.  
- **Clé privée 🔑** → C’est comme un **mot de passe** qui permet d’envoyer tes bitcoins.  

⚠️ **Il est impossible de retrouver une clé privée à partir de la clé publique.**  
Cela garantit que seul le propriétaire légitime peut accéder à ses fonds.

---

## 🖊️ Comment débloquer ses bitcoins ?

Lorsque tu veux **envoyer des bitcoins**, tu dois prouver que tu es bien leur propriétaire.  
Pour cela, tu crées une **signature numérique** avec ta clé privée.  

✅ **Cette signature a deux rôles :**  
1. **Elle prouve que tu possèdes la clé privée** (sans la révéler).  
2. **Elle est unique pour chaque transaction**, donc **ne peut pas être réutilisée**.  

Grâce à ce système, **seul le détenteur de la clé privée peut envoyer les bitcoins**.

---

## 📌 Résumé rapide sur le fonctionnement de Bitcoin

✔ Bitcoin est un **système de paiement décentralisé**, basé sur la **blockchain**.  
✔ Les transactions sont sécurisées par la **cryptographie** et validées par le **minage**.  
✔ La **preuve de travail (Proof of Work)** empêche toute falsification.  
✔ Chaque utilisateur possède une **clé privée pour dépenser** et une **clé publique pour recevoir** des bitcoins.  
✔ Bitcoin fonctionne sans banque ni autorité centrale, **offrant un système sécurisé et accessible à tous**. 🚀  