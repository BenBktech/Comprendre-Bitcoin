# 🏆 Introduction à Bitcoin

Bitcoin est une monnaie numérique décentralisée qui fonctionne sur une **blockchain sécurisée** grâce à un réseau de mineurs, permettant des **transactions sans intermédiaire ni autorité centrale**.

🔗 **Télécharger Bitcoin ici :** [Bitcoin.org](https://bitcoin.org/en/download)

![Bitcoin Screenshot](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot1.png)

Lorsqu'une nouvelle transaction est initiée sur le réseau, elle est transmise de machine en machine jusqu'à ce que **tous les participants en aient une copie**.  
Toutes les **10 minutes**, un ordinateur (nœud) **ajoute les transactions récentes à la blockchain** et diffuse cette mise à jour à l'ensemble du réseau.

![Blockchain Screenshot](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot2.png)

Le protocole Bitcoin repose sur un vaste **réseau d'ordinateurs interconnectés** qui échangent **un registre commun** et l’actualisent avec chaque nouvelle transaction.

---

## 🔍 Quel problème Bitcoin résout-il ?

Bitcoin apporte une solution à **l’absence d’un système de paiement fonctionnant sans autorité centrale**.

Avant son invention, il était déjà possible d’échanger des transactions via un réseau informatique.  
❌ **Problème** : la possibilité d’introduire **des transactions contradictoires**, ce qui permettait la **double dépense**.

💡 **Exemple :**  
- Un utilisateur pouvait tenter d’utiliser **la même unité de monnaie numérique** pour effectuer **deux paiements distincts** en les diffusant simultanément sur le réseau.
- Certains ordinateurs recevront d’abord la **transaction verte**, tandis que d’autres recevront en premier la **transaction rouge**.
- **Qui décide laquelle est valide ?** 🤔

✔ **Solution Bitcoin** :
- **Les nœuds stockent temporairement** toutes les transactions avant leur inscription sur la blockchain.
- Toutes les **10 minutes**, un nœud est **sélectionné pour inscrire ces transactions** de manière irréversible.
- **Les transactions en conflit sont supprimées**, garantissant ainsi l’intégrité du système.

🔗 **Ainsi, aucune transaction en double ne peut être enregistrée.**

---

## ⛏️ Comment fonctionne le minage ?

Le **minage** consiste à **enregistrer de nouveaux blocs de transactions** sur la blockchain.

### 📌 Étapes du minage :

1️⃣ Chaque nœud conserve les transactions récentes dans une mémoire temporaire appelée **mempool**.  
2️⃣ Un nœud sélectionné regroupe ces transactions dans un **bloc**, qu’il tente d’ajouter à la blockchain.  
3️⃣ Le bloc doit passer par une **fonction de hachage**, qui génère un **hash unique** et imprévisible.  
4️⃣ Pour être accepté, ce hash doit respecter une **condition spécifique** définie par le réseau.  
5️⃣ Les mineurs tentent **des milliards de calculs** pour trouver un **hash valide**.  

📌 **Une fois un mineur trouve un hash valide**, son **bloc est ajouté à la blockchain** et partagé avec l’ensemble du réseau.

✅ **Avantage :**  
✔ Sécurise le réseau  
✔ Empêche la falsification des transactions  
✔ Assure un **système de validation distribué** sans autorité centrale  

---

## 💰 D’où viennent les bitcoins ?

Bitcoin **récompense les mineurs** en créant **de nouveaux bitcoins** à chaque bloc validé.

- **Récompense de bloc** 🎁 : le mineur qui valide un bloc reçoit **une quantité fixe de bitcoins**.  
- **Pourquoi cette récompense ?**  
  ✔ Incite les mineurs à sécuriser le réseau  
  ✔ Assure une distribution progressive des nouveaux bitcoins  

---

## 🔗 Pourquoi appelle-t-on cela la "blockchain" ?

Les transactions ne sont **pas enregistrées individuellement**, mais **regroupées en blocs**, qui sont ensuite **enchaînés** les uns aux autres.

🔗 **Chaque bloc contient une référence au précédent**, créant une **chaîne continue** : **la blockchain**.

✔ **Règles essentielles de la blockchain** :  
- Le réseau adopte **toujours la chaîne la plus longue** comme version officielle.  
- Modifier des transactions passées nécessiterait **de recalculer une chaîne plus longue** que l’originale, ce qui est **quasiment impossible**.  

🔒 **La blockchain est protégée par la puissance collective du réseau.**

---

## 🔄 Comment fonctionnent les transactions Bitcoin ?

Bitcoin fonctionne comme un **portefeuille rempli de billets numériques** appelés **outputs**.

📌 **Comment ça marche ?**  
1️⃣ **Chaque output contient une somme précise de bitcoins**.  
2️⃣ **Quand tu envoies une transaction, tu sélectionnes un ou plusieurs outputs** que tu possèdes.  
3️⃣ **Tu crées de nouveaux outputs** en répartissant le montant entre le destinataire et toi (la monnaie rendue).  
4️⃣ **Une fois un output utilisé, il devient invalide** et ne peut plus être dépensé.

📌 **Comparaison simple :**  
- 🔹 **Tu as un billet de 50€ et tu dois payer 30€**.  
- 🔹 **Tu ne peux pas couper ton billet**, alors tu **le donnes en entier** et on te rend 20€.  
- 🔹 En Bitcoin, c’est pareil : un nouveau "billet" (output) est créé pour **rendre la monnaie**.

---

## 🔑 Comment posséder des bitcoins ?

Pour recevoir et stocker des bitcoins, tu as besoin de **deux clés cryptographiques** :

- **Clé publique 🔓** → **Comme une adresse e-mail**, elle permet de **recevoir** des bitcoins.  
- **Clé privée 🔑** → **Comme un mot de passe**, elle permet de **dépenser** tes bitcoins.

⚠️ **Il est impossible de retrouver une clé privée à partir de la clé publique.**  
Cela garantit que **seul le propriétaire légitime peut accéder à ses fonds**.

---

## 🖊️ Comment débloquer ses bitcoins ?

Lorsque tu veux **envoyer des bitcoins**, tu dois prouver que tu en es **bien le propriétaire**.  
Pour cela, tu crées une **signature numérique** avec ta clé privée.

✅ **Cette signature a deux rôles :**  
1️⃣ Elle **prouve que tu possèdes la clé privée** (sans la révéler).  
2️⃣ Elle est **unique pour chaque transaction**, donc **ne peut pas être réutilisée**.

✔ Grâce à ce système, **seul le détenteur de la clé privée peut envoyer ses bitcoins.**

---

## 📌 Résumé rapide sur le fonctionnement de Bitcoin

✔ Bitcoin est un **système de paiement décentralisé**, basé sur la **blockchain**.  
✔ Les transactions sont sécurisées par la **cryptographie** et validées par le **minage**.  
✔ La **preuve de travail (Proof of Work)** empêche toute falsification.  
✔ Chaque utilisateur possède une **clé privée pour dépenser** et une **clé publique pour recevoir** des bitcoins.  
✔ Bitcoin fonctionne sans banque ni autorité centrale, **offrant un système sécurisé et accessible à tous**. 🚀  