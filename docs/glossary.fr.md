---
tags:
  - Reference
  - SMPP
  - Getting Started
---

# Glossaire

Un guide de référence rapide des termes communs utilisés dans la documentation Power SMPP.

---

## Termes de messagerie

| Durée | Formulaire complet | Désignation des marchandises |
|------|-----------|-------------|
| **SMS** | Service de messages courts | Protocole de messagerie texte standard pour les appareils mobiles |
| **Pays** | Mobile Terminé | Un message envoyé **à** un combiné mobile (extérieur) |
| **Pays** | Mobile d'origine | Un message envoyé **de** un combiné mobile (entrée) |
| **DLR** | Rapport d'exécution | Avis d'état confirmant si un message MT a été livré |
| **A2P** | Application à la personne | Messages automatisés envoyés par une application aux utilisateurs finaux |
| **P2P** | Personne à personne | Messages échangés entre utilisateurs individuels |

---

## Protocole SMPP

| Durée | Formulaire complet | Désignation des marchandises |
|------|-----------|-------------|
| **SMPP** | Message court de pair à pair | Protocole standard pour l'échange de SMS entre systèmes |
| **CSM** | Centre de service pour messages courts | Système central de stockage, d'acheminement et de livraison des SMS |
| **ESME** | Entité externe de messagerie courte | Une application externe qui se connecte au SMSC via SMPP |
| **PDU** | Groupe des données relatives au protocole | Un seul paquet de données SMPP échangé entre ESME et SMSC |
| **Reliure** | — | Le processus d'établissement d'une session SMPP entre ESME et SMSC |
| **Tx** | Émetteur | Une session SMPP qui ne peut que **envoyer** messages |
| **Rx** | Récepteur | Une session SMPP qui ne peut que **recevoir** messages |
| **TRx** | Émetteur-récepteur | Une session SMPP qui peut les deux **envoyer et recevoir** messages |
| **TPS** | Opérations par seconde | La capacité de débit d'une connexion SMPP |

---

## Adresse

| Durée | Formulaire complet | Désignation des marchandises |
|------|-----------|-------------|
| **TON** | Type de numéro | Définit le format de l'adresse (p. ex. international, alphanumérique) |
| **NPI** | Indicateur du plan de numérotation | Indique la norme de numérotation (par exemple, E.164, RNIS) |
| **OA** | Adresse | Adresse de l'expéditeur (source) d'un message |
| **DA** | Adresse de destination | Adresse du destinataire (destination) d'un message |
| **MCC** | Code pays mobile | Un code à 3 chiffres identifiant le pays d'un abonné mobile |
| **MNC** | Code réseau mobile | Un code à 2-3 chiffres identifiant un opérateur de réseau mobile |
| **MSISDN** | Mobile Station International Numéro de répertoire de l'abonné | Le numéro de téléphone international complet d'un abonné mobile |

---

## Caractéristiques de la plateforme

| Durée | Désignation des marchandises |
|------|-------------|
| **Régime des taux** | Modèle de prix qui définit les coûts par message pour différentes destinations |
| **Règle d'acheminement** | Une règle qui détermine quelle passerelle gère un message en fonction de critères comme destination, expéditeur ou contenu |
| **Passerelle** | Une connexion externe SMSC ou agrégator configurée dans iTextPRO |
| **Interface** | Un connecteur SMPP ou HTTP qui permet aux partenaires de se connecter à iTextPRO |
| **Routage aveugle** | Permet la soumission de messages à des destinations sans prix de revient prédéfinis |
| **Arrêter la perte** | Un seuil de coût maximal de la passerelle pour éviter les pertes sur les messages sans route |
| **Recherche HLR** | Accueil Localisation Enregistrer la requête pour valider un numéro mobile avant l'envoi |
| **DLT** | Distributed Ledger Technology — Le cadre réglementaire indien pour les SMS A2P exigeant l'enregistrement préalable des expéditeurs et des modèles |

---

## Facturation et affaires

| Durée | Désignation des marchandises |
|------|-------------|
| **Prépayé** | Mode de facturation où les utilisateurs doivent avoir un solde créditeur suffisant avant l'envoi |
| **Postes payés** | Mode de facturation où les utilisateurs sont facturés après consommation |
| **Monnaie de base** | La monnaie principale utilisée pour tous les calculs de facturation interne |
| **Facture récurrente** | Facture automatisée produite à intervalles réguliers (hebdomadaire, mensuelle, etc.) |

---

## Système et surveillance

| Durée | Désignation des marchandises |
|------|-------------|
| **Visionneur d'événements** | Un visionneur de journaux pour surveiller les événements, les erreurs et les avertissements du système |
| **Registre de vérification** | Un enregistrement chronologique de toutes les actions de l'utilisateur et du système pour la conformité |
| **Enregistreur PDU** | Un outil pour capturer et inspecter les paquets de données de protocole SMPP bruts |
| **Demande de lien** | Un paquet de conservation SMPP envoyé périodiquement pour maintenir des sessions actives |
| **QoS** | Qualité du service — mesures utilisées pour évaluer le rendement des passerelles |
