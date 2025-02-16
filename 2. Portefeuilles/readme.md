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

### 📩 Création d’une Adresse Bitcoin

1. Le wallet génère une **clé privée aléatoire**.  
2. À partir de cette clé privée, une **clé publique** est dérivée.  
3. La clé publique est **hachée** et encodée pour créer une **adresse Bitcoin**.  

#### 🔢 Exemple :
- **Clé privée** : `5J3mBbAH58...`  
- **Clé publique** : `03a34b4d...`  
- **Adresse Bitcoin** : `bc1qxy2kg...`  

Chaque transaction Bitcoin est envoyée à une adresse spécifique, et le propriétaire de la **clé privée associée** peut **dépenser ces fonds**.

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