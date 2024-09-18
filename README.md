# CryptComC

# Mini-Projet de Messagerie Chiffrée en C

Messagerie très simple en C qui permet à deux machines de communiquer de manière chiffrée.

## Architecture du Système
Le système est composé de deux programmes :
1. **Serveur** : Attend les messages chiffrés des clients et les déchiffre.
2. **Client** : Chiffre les messages et les envoie au serveur.

## Étapes du Projet

### Étape 1 : Mise en Place de la Communication Réseau
#### Sous-étape 1.1 : Créer le Serveur de Base
- Créer un socket serveur.
- Lier (`bind`) le socket à une adresse IP et à un port spécifique.
- Mettre le serveur en écoute (`listen`) des connexions entrantes.
- Accepter (`accept`) une connexion d'un client.

#### Sous-étape 1.2 : Créer le Client de Base
- Créer un socket client.
- Se connecter (`connect`) au serveur en utilisant l'adresse IP du serveur et le port choisi.

### Étape 2 : Échange de Messages en Texte Clair
#### Sous-étape 2.1 : Échange de Messages
- Serveur : Recevoir un message du client (`recv`).
- Client : Envoyer un message au serveur (`send`).
- Tester que la communication fonctionne sans chiffrement pour l'instant.

### Étape 3 : Ajouter le Chiffrement
#### Sous-étape 3.1 : Implémenter un Algorithme de Chiffrement Simple
- Choisir un algorithme de chiffrement simple (par exemple, le chiffrement de César ou XOR).
- Ajouter une fonction pour chiffrer les messages avant de les envoyer.
- Ajouter une fonction pour déchiffrer les messages à la réception.

#### Sous-étape 3.2 : Intégrer le Chiffrement dans la Communication
- Client : Chiffrer le message avant de l'envoyer.
- Serveur : Déchiffrer le message reçu et l'afficher.

### Étape 4 : Améliorations et Gestion des Erreurs
#### Sous-étape 4.1 : Gérer les Erreurs Réseau
- Ajouter une gestion des erreurs pour les fonctions de sockets (`socket`, `bind`, `listen`, `accept`, `send`, `recv`).

#### Sous-étape 4.2 : Sécurité Supplémentaire (Optionnelle)
- Si vous vous sentez à l'aise, implémenter un chiffrement plus sécurisé comme AES.
- Ajouter une fonctionnalité pour échanger des clés de chiffrement de manière sécurisée.

### Étape 5 : Test et Validation
#### Sous-étape 5.1 : Tester sur Deux Machines
- Lancer le serveur sur une machine.
- Lancer le client sur une autre machine.
- Tester l'envoi et la réception de messages chiffrés.

## Résumé de l'Architecture
1. **Serveur**
   - Crée un socket.
   - Accepte les connexions.
   - Reçoit et déchiffre les messages.
2. **Client**
   - Crée un socket.
   - Se connecte au serveur.
   - Chiffre et envoie les messages.


