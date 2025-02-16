# 🚀 Introduction à Bitcoin

Bitcoin est une **monnaie numérique décentralisée** qui fonctionne sur une **blockchain sécurisée** grâce à un réseau de mineurs.  
Il permet des transactions **sans intermédiaire ni autorité centrale**.  

📥 **Téléchargez Bitcoin ici** : [Bitcoin.org](https://bitcoin.org/en/download)

---

## 📌 Comment fonctionne Bitcoin ?

📡 Lorsqu'une nouvelle transaction est initiée sur le réseau :
1. Elle est transmise de machine en machine.
2. Chaque participant en reçoit une copie.
3. Toutes les **10 minutes**, un ordinateur (*nœud*) choisi aléatoirement ajoute les transactions récentes à la blockchain.
4. Cette mise à jour est diffusée à tout le réseau.

![Screenshot1](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot1.png)

---

## ❓ Quel problème Bitcoin résout-il ?

Avant Bitcoin, il était possible d'échanger de la monnaie numérique sur un réseau informatique, **mais avec un problème majeur** :  

🔥 **Le risque de double dépense**  
Un utilisateur pouvait tenter d'utiliser la **même unité de monnaie** pour deux paiements différents en même temps.

![Screenshot3](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot3.png)

➡️ **Bitcoin empêche cela** en obligeant les nœuds à stocker **temporairement** toutes les transactions.  
✅ Toutes les **10 minutes**, un nœud est sélectionné pour inscrire ces transactions dans la blockchain, rendant toute fraude impossible.

![Screenshot4](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot4.png)

---

## ⛏️ Comment fonctionne le minage ?

Le **minage** est le processus qui permet d'enregistrer de nouveaux **blocs** de transactions sur la blockchain.

![Screenshot5](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot5.png)

🔹 **Étape 1** : Chaque nœud stocke temporairement les transactions récentes dans une mémoire appelée **mempool**.  
🔹 **Étape 2** : Un nœud sélectionné regroupe ces transactions dans un bloc.  
🔹 **Étape 3** : Il doit ensuite **résoudre un problème mathématique** complexe pour ajouter ce bloc à la blockchain.  


📌 **Pourquoi faut-il de la puissance de calcul ?**  
Pour inscrire un bloc, il faut le **haché** avec un algorithme cryptographique. 

![Screenshot6](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot6.png)

Seule une valeur respectant un **seuil précis** est acceptée. 

![Screenshot7](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot7.png)

Les mineurs doivent donc tester **des millions de combinaisons** jusqu'à obtenir une valeur correcte.

![Screenshot8](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot8.png)

🏆 **Le premier mineur à réussir ajoute son bloc et reçoit une récompense en bitcoins.**

---

## 💰 D’où viennent les bitcoins ?

Bitcoin est un **système décentralisé**, donc il ne peut pas être imprimé comme une monnaie classique.  
À la place, de **nouveaux bitcoins** sont créés **lorsqu'un mineur valide un bloc**.

![Screenshot9](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot9.png)

🎁 **Récompense du minage** :  
✅ Lorsqu’un mineur réussit à ajouter un bloc à la blockchain, il reçoit des bitcoins en récompense.  
⚠️ Cette récompense **diminue avec le temps** pour limiter l'inflation.

---

## 🏗️ Pourquoi appelle-t-on cela la "blockchain" ?

![Screenshot10](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot10.png)

🔹 **Les transactions ne sont pas inscrites une par une**, mais regroupées en **blocs** avant d’être ajoutées.  
🔹 **Chaque nouveau bloc est lié au précédent**, formant ainsi une **chaîne** de blocs, d’où le nom **blockchain**. 

![Screenshot11](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot11.png)

📌 **Sécurité et intégrité**  
- Chaque nœud du réseau considère toujours **la chaîne la plus longue** comme référence.  
- Toute tentative de modification de l’historique nécessiterait **une puissance de calcul supérieure à celle du réseau entier**, ce qui est pratiquement impossible.

---

## 💳 Comment fonctionnent les transactions Bitcoin ?

Imagine la blockchain comme un **grand registre** contenant des **enveloppes sécurisées** appelées **outputs**.

![Screenshot12](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot12.png)

![Screenshot13](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot13.png)

🔹 **Quand tu fais une transaction** :  
1. Tu ouvres une **enveloppe contenant des bitcoins**.
2. Tu crées une nouvelle enveloppe pour ton destinataire, en la verrouillant avec **sa clé publique**.
3. Si le montant est plus grand que ce que tu veux envoyer, une **deuxième enveloppe** est créée pour la monnaie restante et elle t'est retournée.

🔎 **Exemple** :  
Tu veux envoyer **30 BTC** à quelqu’un, mais tu n’as qu’un **billet de 50 BTC**.  
➡️ Tu donnes le billet, la personne prend **30 BTC**, et **on te rend la monnaie** (20 BTC).  

![Screenshot14](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot14.png)

![Screenshot15](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot15.png)

📌 **Important** :
- Les **bitcoins ne sont jamais stockés** à un endroit précis.
- Chaque transaction est liée à une précédente, assurant **une traçabilité totale**.
- Une fois qu’un **output est utilisé, il est définitivement dépensé**.

![Screenshot16](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot16.png)

---

## 🔑 Comment possèdes-tu des bitcoins ?

Pour **recevoir** des bitcoins, tu as besoin d’un **jeu de clés cryptographiques**.

![Screenshot17](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot17.png)

🔹 **Deux types de clés** :  
✅ **Clé publique** : Ton **adresse Bitcoin** (comme un IBAN), que tu peux partager.  
✅ **Clé privée** : Un **mot de passe secret**, qui te permet **d’accéder à tes fonds et de les dépenser**.  

⚠️ **Garde ta clé privée secrète !**  
Si quelqu’un la découvre, il peut voler **tous tes bitcoins**.

---

## 🔐 Comment obtenir une clé publique et une clé privée ?

📌 **La cryptographie permet de générer ces clés de manière sécurisée** :

1. **Clé privée** : Un **grand nombre aléatoire**.
2. **Clé publique** : Calculée à partir de la clé privée.

![Screenshot18](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot18.png)

💡 **Ce qui est astucieux** :  
✅ Tu peux **partager** ta clé publique sans risque.  
❌ **Personne ne peut retrouver ta clé privée** à partir de la clé publique.

---

## 🔓 Comment débloquer tes bitcoins ?

Quand tu veux **utiliser tes bitcoins**, tu dois **prouver** que tu en es bien le propriétaire.

📌 **Comment ?**  
Tu crées une **signature numérique** à l’aide de ta **clé privée**.

🔹 **Rôle de la signature** :
1. **Elle prouve que tu possèdes bien la clé privée**, sans la révéler.
2. **Elle est valable uniquement pour cette transaction précise**, empêchant toute réutilisation frauduleuse.

Grâce à ce mécanisme, **Bitcoin garantit que seuls les véritables propriétaires peuvent dépenser leurs fonds en toute sécurité**.

---

## 📢 Résumé rapide sur Bitcoin

🟢 **Bitcoin est un système de paiement décentralisé** qui permet d’envoyer de l’argent **sans intermédiaire**.  
🟢 Il repose sur **une blockchain sécurisée**, où les transactions sont **validées par le minage**.  
🟢 **Les mineurs reçoivent des bitcoins** en récompense lorsqu’ils ajoutent des transactions à la blockchain.  
🟢 **Les transactions sont cryptographiquement sécurisées** et **infalsifiables**.  
🟢 Chaque utilisateur possède **une clé privée** pour **signer ses transactions** et **une clé publique** pour recevoir des bitcoins.  

📌 **En résumé, Bitcoin offre un moyen de paiement sécurisé, transparent et sans autorité centrale !**  

---

🔗 **Téléchargez Bitcoin** : [Bitcoin.org](https://bitcoin.org/en/download)  
📖 **En savoir plus** : [Bitcoin Whitepaper](https://bitcoin.org/bitcoin.pdf)  