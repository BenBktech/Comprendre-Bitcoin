# 🏆 Formation sur les Wallets Bitcoin

La première étape pour utiliser Bitcoin est de se procurer un **wallet**. Un wallet permet de **stocker, envoyer et recevoir des bitcoins**.  
Il existe différents types de wallets, chacun ayant ses propres **avantages et inconvénients** en termes de **sécurité, de commodité et de contrôle**.

---

## 🔍 Types de Wallets Bitcoin

### 🔥 Wallets logiciels (*Hot Wallets*)

Un wallet logiciel est une **application** installée sur un ordinateur ou un smartphone.  
Ces wallets sont **connectés à Internet**, ce qui les rend plus exposés aux cyberattaques.

#### 🛠 Exemples :
- **Electrum** (Desktop, Android)
- **BlueWallet** (Mobile)
- **Blockstream Green** (Mobile)

✅ **Avantages :**  
✔ Faciles à utiliser  
✔ Gratuits  
✔ Disponibles sur plusieurs plateformes  

❌ **Inconvénients :**  
⚠ Vulnérables aux logiciels malveillants  
⚠ Moins sécurisés qu'un hardware wallet 

![Screenshot1](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot1.png)

![Screenshot2](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot2.png)

![Screenshot3](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot3.png)

![Screenshot4](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot4.png)

![Screenshot5](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot5.png)

---

### ❄ Wallets matériels (*Cold Wallets*)

Un wallet matériel est un **appareil physique** spécialement conçu pour **stocker des bitcoins hors ligne**.

#### 🛠 Exemples :
- **Trezor** (2014)
- **Ledger** (2016)
- **Coldcard** (2018)

✅ **Avantages :**  
✔ Clés privées stockées hors ligne  
✔ Protection contre les malwares  

❌ **Inconvénients :**  
⚠ Payants  
⚠ Moins pratiques pour les transactions fréquentes  

---

### 🔐 Wallets Multisignature

Un wallet **multisignature** nécessite **plusieurs signatures** pour autoriser une transaction.  
Il est idéal pour les **entreprises** ou pour **renforcer la sécurité**.

#### ⚙ Exemple de configuration :
- **2 sur 3 signatures requises**  

✅ **Avantages :**  
✔ Réduit les risques de vol  
✔ Partage du contrôle sur les fonds  

❌ **Inconvénients :**  
⚠ Plus complexe à configurer  

---

### 📝 Paper Wallets et Cold Storage

Un **paper wallet** est un moyen de stocker des bitcoins **hors ligne** en imprimant la **clé privée sur papier**.

✅ **Avantages :**  
✔ Totalement hors ligne  
✔ Aucun risque de piratage informatique  

❌ **Inconvénients :**  
⚠ Si le papier est perdu ou endommagé, les fonds sont irrécupérables  
⚠ Moins pratique pour effectuer des transactions  

---

## ⚙ Configuration d'un Wallet Bitcoin

### 📥 Téléchargement et Installation

✔ **Toujours télécharger un wallet depuis son site officiel**.  
✔ Vérifier la **signature cryptographique** du fichier (*optionnel mais recommandé*).  

---

### 🔑 Génération de la Seed Phrase

Une **seed phrase** est une suite de **12 ou 24 mots** permettant de **restaurer un wallet**.  

✅ **À faire :**  
✔ L'écrire sur **papier** et la stocker en **lieu sûr**.  

❌ **À ne pas faire :**  
⚠ La stocker sur un appareil connecté à Internet (*fichier texte, capture d'écran, cloud*).  

---

### 🔒 Sécurisation du Wallet

✔ Activer l’**authentification à deux facteurs (2FA)** si disponible.  
✔ **Ne jamais partager** sa clé privée.  
✔ Faire des **sauvegardes régulières**.  

---

## 🔄 Fonctionnement d'un Wallet

Un wallet Bitcoin est un **logiciel ou un appareil** qui stocke et gère les **clés privées** permettant d’accéder à des bitcoins.  
Contrairement à un compte bancaire, un wallet **ne stocke pas les bitcoins eux-mêmes**, mais les **informations** permettant d’interagir avec la **blockchain Bitcoin**.

### 🌱 La Seed Phrase : La Racine de votre Wallet

Lors de la création d’un wallet Bitcoin, une **seed phrase** (ou phrase de récupération) de **12 ou 24 mots** est générée.  
Cette seed phrase est la **source de toutes les clés privées** et adresses associées à votre wallet.  

#### 🔑 Comment fonctionne la seed phrase ?
1. La **seed phrase** est générée aléatoirement par le wallet selon la norme **BIP-39**.
2. Cette seed phrase est utilisée pour dériver une **master key** à l’aide de **BIP-32**.
3. À partir de cette **master key**, le wallet génère **toutes les clés privées** et les **adresses Bitcoin** correspondantes.

✅ **Avantages de la seed phrase** :  
✔ Permet de restaurer un wallet sur n’importe quel appareil compatible.  
✔ Évite de devoir sauvegarder individuellement chaque clé privée.  

⚠ **Attention !**  
⚠ **Si vous perdez votre seed phrase, vous perdez définitivement l’accès à vos bitcoins.**  
⚠ **Ne la stockez jamais sur un appareil connecté à Internet !**  

---

### 📩 Création d’une Adresse Bitcoin

Une **adresse Bitcoin** est générée à partir de la **clé privée**, elle-même issue de la **seed phrase**.  

1. Le wallet génère une **seed phrase**.  
2. Cette seed est utilisée pour dériver une **clé privée principale**.  
3. La **clé privée principale** permet de générer plusieurs **clés privées** pour différentes adresses.  
4. À partir de chaque **clé privée**, une **clé publique** est dérivée.  
5. La **clé publique** est **hachée** et encodée pour créer une **adresse Bitcoin**.

![Screenshot6](https://raw.githubusercontent.com/BenBktech/Apprendre-Bitcoin/refs/heads/main/1.%20Introduction/images/screenshot6.png)

#### 🔢 Exemple :
- **Seed phrase** : `avocat vague tapis océan...`  
- **Clé privée dérivée** : `5J3mBbAH58...`  
- **Clé publique** : `03a34b4d...`  
- **Adresse Bitcoin** : `bc1qxy2kg...`  

Chaque transaction Bitcoin est envoyée à une adresse spécifique, et le propriétaire de la **clé privée associée** peut **dépenser ces fonds**.

---

### 🔎 Pourquoi est-ce important ?
Grâce à cette structure **hiérarchique et déterministe (HD Wallet, BIP-32)** :  
✔ Toutes les adresses d’un wallet peuvent être restaurées uniquement avec la **seed phrase**.  
✔ Un wallet peut générer **des milliers d’adresses Bitcoin** à partir d’une seule seed.  
✔ Les utilisateurs n’ont pas besoin de sauvegarder chaque clé privée, **seule la seed phrase est essentielle**.

💡 **Conseil** : Notez votre seed phrase sur **papier** ou **métal** et stockez-la en lieu sûr. Ne jamais la sauvegarder en ligne !  

---

## 🖥 Bitcoin Core : Une Alternative Complète

Bitcoin Core est le **wallet officiel de Bitcoin** et fonctionne comme un **nœud complet**.

✅ **Avantages :**  
✔ Autonomie totale (*vérification des transactions sans tiers*)  

❌ **Inconvénients :**  
⚠ Requiert de télécharger **toute la blockchain**  

---

## 🛡 Garde de ses Bitcoins : Pourquoi utiliser un Wallet ?

Laisser ses bitcoins sur un **exchange** présente des risques :  

⚠ **Risque de piratage**  
⚠ **Restrictions de retrait**  
⚠ **Possibilité de faillite de l’exchange**  

```
- Not your keys, not your coins. 🚀
```