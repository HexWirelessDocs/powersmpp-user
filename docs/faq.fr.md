---
tags:
  - FAQ
  - Help
---

# Foire aux questions

Trouvez des réponses rapides aux questions courantes sur Power SMPP.

---

## Commencer

??? question "Comment puis-je me connecter au panneau utilisateur ?"
 Naviguez sur votre URL d'instance Power SMPP fournie par votre administrateur. Entrez votre **Nom d'utilisateur** et **Mot de passe** pour accéder au tableau de bord utilisateur iText Hub.

 Si vous avez oublié vos identifiants, contactez votre administrateur système pour réinitialiser votre mot de passe. Pour la sécurité, il est recommandé de changer votre mot de passe après votre premier login via **Paramètres > Modifier le mot de passe**.

??? question "Que montre le tableau de bord ?"
 Le tableau de bord (iText Hub) fournit un aperçu en temps réel de votre activité de messagerie avec quatre paramètres clés:

    - **SMS envoyé aujourd'hui** — Total des messages SMS envoyés depuis toutes les interfaces le jour actuel
    - **Livré aujourd'hui** — Nombre total de SMS livrés avec succès le jour actuel
    - **SMS envoyé hier** — Messages envoyés la veille
    - **Livré hier** — Messages de la veille

 Il affiche également des cartes interactives de surveillance du trafic pour les deux **MT (Mobile Terminé / sortant)** et **MO (d'origine mobile / entrant)** messages. Depuis le tableau de bord, vous pouvez accéder rapidement à la création de campagne, à la gestion des contacts, à la visualisation du trafic, aux téléchargements de rapports et aux paramètres de profil. Voir [Tableau de bord](user/dashboard/dashboard.md) pour plus de détails.

??? question "Comment puis-je changer mon mot de passe?"
    1. Allez à **Paramètres > Modifier le mot de passe**
    2. Entrez votre **mot de passe actuel** pour la vérification
    3. Entrez votre **nouveau mot de passe** (doit répondre aux exigences de sécurité définies par votre administrateur)
    4. **Confirmer** le nouveau mot de passe
    5. Cliquez sur **Enregistrer**

 Des mises à jour régulières des mots de passe sont recommandées pour maintenir la sécurité des comptes et s'aligner sur les pratiques exemplaires. Votre administrateur peut également appliquer une politique de changement de mot de passe nécessitant des mises à jour périodiques. Voir [Modifier le mot de passe](user/settings/changepassword.md).

??? question "Comment mettre à jour les informations de mon profil?"
 Allez à **Paramètres > Mon profil** où vous pouvez mettre à jour les champs suivants:

    - **Prénom** — Référencé par votre compte parent pour la facturation
    - **Numéro mobile** — utilisés pour les communications et la vérification des comptes
    - **Code pays** — Peut être appliqué automatiquement aux numéros de campagne via l'option « Auto-add country code »
    - **Adresse électronique** — Utilisé pour les communications, les alertes, le BTP et la transmission des notifications
    - **Pays/État** — à des fins de facturation et de référence
    - **Fuseau horaire** — affecte tous les affichages de date/heure sur la plateforme, y compris le calendrier et les rapports de campagne

 Cliquez sur **Enregistrer** après avoir apporté des changements. Voir [Mon profil](user/settings/myprofile.md).

??? question "Quel fuseau horaire utilise la plateforme ?"
 La plateforme utilise le fuseau horaire configuré dans votre **Mon profil** paramètres. Ce fuseau horaire affecte:

    - Affichage des paramètres du tableau de bord
    - Calendrier des campagnes
    - Date/heure du rapport
    - Rapports de comptage des messages

 Vérifiez toujours que votre fuseau horaire est correct avant de programmer les campagnes pour s'assurer qu'elles sont envoyées à l'heure prévue pour vos destinataires.

??? question "Quelle est la différence entre les messages MT et MO?"
    - **MT (Mobile Terminé)** — Messages envoyés **à** un combiné mobile. Ce sont vos messages sortants (p. ex. campagnes, notifications, PAO).
    - **MO (d'origine mobile)** — Messages envoyés **de** un combiné mobile. Il s'agit de messages entrants ou entrants reçus de vos destinataires (p. ex. réponses, demandes de refus).

 Le trafic MT et MO sont affichés sur vos tableaux de bord.

---

## Envoi de SMS

??? question "Comment composer et envoyer une campagne SMS ?"
 Suivez ces étapes pour créer et envoyer une campagne SMS :

    1. Cliquez sur **Autres** pour ouvrir la page Compose SMS
    2. Entrez un **Nom de la campagne** (auto-généré avec préfixe "Camp " et date-heure, ou saisissez un nom personnalisé)
    3. Sélectionner un **ID de l'expéditeur** de la liste approuvée (ou entrez une dynamique si "Open Sender ID" est activé par votre administrateur)
    4. **Ajouter des destinataires** utilisant l'une des quatre méthodes:
        - **Groupes stockés** — Sélectionner parmi les groupes de contact précréés
        - **Fichier local** — Télécharger un fichier Excel/CSV avec les numéros de téléphone
        - **Entrée manuelle** — Numéros de type directement (comma-séparé avec code pays, n° + symbole)
        - **Copier-coller** — Coller les numéros d'une autre source
    5. **Composez votre message** dans la zone de texte (ou sélectionner parmi les projets/templates)
    6. Activer en option **Flash SMS** pour l'écran instantané
    7. Le système **auto-détecte Unicode** si des caractères spéciaux sont utilisés
    8. Choisir **Envoyer maintenant** ou **Tableau** pour plus tard
    9. Cliquez sur **Envoyer un SMS** — un aperçu des coûts est affiché avant la confirmation finale

    !!! tip
 Toujours tester le contenu de votre message sur quelques numéros avant d'exécuter des campagnes à grande échelle, car les compteurs de caractères sont approximatifs en raison des variations de navigateur/encodage.

 Voir [Compose SMS](user/smsmt/compose.md) pour le guide complet.

??? question "Comment puis-je envoyer des SMS personnalisés à partir d'un fichier Excel?"
 La fonction SMS From Excel vous permet d'envoyer des messages personnalisés en utilisant les données de votre tableur:

    1. Ouvrez la **SMS depuis Excel** onglet
    2. Téléchargez le **exemple de fichier** via l'onglet "Voir l'échantillon" pour voir le format requis
    3. Préparer votre fichier Excel avec des numéros mobiles dans une colonne et des données de personnalisation (noms, montants, dates, etc.) dans d'autres colonnes
    4. **Envoi** le fichier Excel — les 5 premières lignes sont affichées pour vérification
    5. **Sélectionnez la colonne** contenant des numéros mobiles
    6. Entrez un **ID de l'expéditeur**
    7. Composez votre message et cliquez **"Insert Placeholder"** pour ajouter des variables dynamiques à partir de vos colonnes de tableur (p. ex., <span data-ph="0"></span>, <span data-ph="1"></span>)
    8. Cliquez sur **Aperçu** pour voir le top 5 des messages personnalisés avec le nombre de caractères
    9. Choisir **Tableau** ou **Envoyer maintenant**
    10. Revoir **écran d'aperçu final** montrant la ventilation des coûts par pays
    11. Cliquez sur **Envoyer**

 Ceci est idéal pour des contenus personnalisés comme des rappels de rendez-vous, des confirmations de commande ou des notifications de paiement. Voir [SMS d'Excel](user/smsmt/smsfromexcel.md).

??? question "Quels formats de fichiers sont pris en charge pour les téléchargements de contact?"
 Power SMPP prend en charge les formats de fichiers suivants pour les téléchargements de contacts :

    | Présentation | Prolongation | Cas d'utilisation |
    |--------|-----------|----------|
    | Excel | .xls, .xlsx | Le plus courant, supporte plusieurs colonnes |
    | CSV | .csv | Compatibilité légère et universelle |
    | Texte | .txt | Listes de numéros simples |

 **Exigences:**

    - Les numéros de téléphone doivent inclure les **code pays** (par exemple, 919909945175, pas +919909945175)
    - Faites **pas** utiliser les <span data-ph="0"></span> symbole avant le code de pays
    - Des colonnes supplémentaires peuvent contenir des données de personnalisation (noms, montants, etc.)
    - Le système détecte automatiquement les colonnes après le téléchargement

??? question "Qu'est-ce que Flash SMS et quand dois-je l'utiliser?"
 Flash SMS est un type de message spécial qui **apparaît directement sur l'écran du destinataire immédiatement** sans être stockés dans leur boîte de réception. Le message s'affiche comme une superposition popup sur le combiné.

 **Quand utiliser Flash SMS:**

    - Alertes urgentes et notifications d'urgence
    - Information rapide nécessitant une attention immédiate
    - Codes OTP qui n'ont pas besoin d'être enregistrés
    - Notifications des systèmes critiques

 **Comment activer :** Vérifiez **Flash SMS** case à cocher lors de la composition de votre message dans la page Compose SMS. Notez que le comportement SMS Flash peut varier selon le combiné et le support du destinataire.

??? question "Comment fonctionne Unicode / détection de caractères spéciaux?"
 Puissance SMPP **détecte automatiquement** lorsque votre message contient des caractères Unicode. Voici comment ça marche :

    - **Encodage 7 bits GSM** (par défaut) : prend en charge les lettres, numéros et symboles anglais standard. Limite: **160 caractères** par segment SMS.
    - **Encodage Unicode** (auto-détecté) : activé lorsque des scripts non latins (arabes, hindis, chinois, etc.), des emojis ou des caractères spéciaux sont détectés. Limite: **70 caractères** par segment SMS.

 **Important:** Lorsque Unicode est détecté, le compteur de caractères se met à jour automatiquement. Un seul emoji ou caractère spécial commutera l'ensemble du message en encodage Unicode, réduisant ainsi les caractères disponibles par segment.

    !!! warning
 Les compteurs de messages et de caractères affichés sont **indicatif seulement** en raison de variations de navigateur et de codage. Toujours tester sur un petit lot avant de grandes campagnes.

??? question "Quelle est la limite de caractères par SMS et comment fonctionne la concaténation?"
 **Limites de caractères par segment SMS:**

    | Codage | Un seul SMS | SMS concaténé (par segment) |
    |----------|-----------|-------------------------------|
    | GSM 7 bits (standard) | 160 caractères | 153 caractères |
    | Unicode | 70 caractères | 67 caractères |

 Lorsqu'un message dépasse la limite du SMS, il est automatiquement divisé en **SMS concaténé (multi-partie)**. Chaque segment supplémentaire utilise un peu moins de caractères (153 ou 67) parce que certains octets sont réservés à l'en-tête de concaténation qui indique au combiné comment remonter les pièces.

 **Exemple :** Un message GSM de 320 caractères = 3 segments SMS (153 + 153 + 14 caractères). Vous êtes facturé par segment.

??? question "Comment programmer une campagne pour plus tard?"
    1. Lors de la composition de votre SMS (Compose SMS ou SMS d'Excel), sélectionnez le **Tableau** option
    2. Choisissez votre choix **date et heure**
    3. Sélectionner le bon **fuseau horaire** (par défaut sur votre fuseau horaire)
    4. Remplissez le reste de la configuration de la campagne et cliquez **Envoyer**
    5. La campagne sera en attente et envoyée automatiquement à l'heure prévue.

 **Gestion des campagnes programmées :**

    - Allez à **Rapport > Mes horaires** pour voir toutes les campagnes programmées
    - Vous pouvez **rééchelonnement** une campagne en attente en cliquant sur **Modifier** bouton dans l'onglet Action
    - Vérifiez toujours que le fuseau horaire sélectionné correspond à votre délai de livraison prévu

 Voir [Mes horaires](user/report/schedule.md).

??? question "Quelle est la différence entre les ébauches et les modèles?"
    | Fonctionnalité | Projets | Modèles |
    |---------|--------|-----------|
    | **Édition** | Entièrement modifiable — vous pouvez modifier l'ensemble du contenu | Seuls les emplacements peuvent être modifiés; le contenu statique est verrouillé |
    | **Approbation** | Aucune homologation requise | Peut exiger l'approbation de l'administration avant utilisation |
    | **Cas d'utilisation** | Enregistrement de messages de travail en cours | Formats de message réutilisables et approuvés |
    | **Conformité** | Aucune exécution | Conformité aux DLT (pour l ' Inde) |

 **Projets** sont idéales pour enregistrer les messages sur lesquels vous travaillez encore. **Modèles** sont idéales pour les messages normalisés et préapprouvés qui doivent maintenir un formatage cohérent.

    !!! warning "Utilisateurs de l' API"
 Lorsque vous utilisez des modèles via l'API, assurez-vous que l'espacement exact, les virgules et la ponctuation correspondent au modèle approuvé. Toute différence de formatage peut entraîner le rejet du modèle comme étant invalide.

??? question "Puis-je ajouter un code de pays automatiquement à tous les numéros?"
 Oui. Il y a deux façons :

    1. **Pendant la composition de la campagne** — Vérifiez **"Ajouter le code du pays"** case à cocher lors de l'ajout de destinataires. Le système prépendra le code pays configuré à tous les numéros.
    2. **Dans votre profil** — Allez à **Paramètres > Mon profil** et configurer votre par défaut **Code pays**. Ce paramètre est utilisé lorsque l'option d'ajout automatique est activée.

 Ceci est utile lorsque votre liste de contacts contient des numéros locaux sans préfixe pays.

---

## ID de l'expéditeur et modèles

??? question "Comment puis-je demander un nouvel ID d'expéditeur ?"
    1. Allez à **SMS MT > Gérer l'identifiant de l'expéditeur**
    2. Cliquez sur **"Ajouter l'identifiant de l'expéditeur"** onglet
    3. Un popup de configuration apparaît — saisissez les détails de l'ID de l'expéditeur souhaité suivant les directives de votre administrateur
    4. Cliquez sur **Enregistrer**
    5. L'identifiant de l'expéditeur entre un **en attente d ' approbation** État
    6. Votre administrateur examine et approuve/rejette la demande
    7. Une fois approuvé, l'identifiant de l'expéditeur apparaît dans votre menu déroulant lors de la composition des campagnes

 Vous pouvez voir la **État d ' homologation** de tous vos identifiants d'expéditeur dans la liste d'identifiant de gestion de l'expéditeur. Si votre compte a **"Open Sender ID"** activé par l'administrateur, vous pouvez sauter cette étape et taper n'importe quel Sender ID directement lors de la composition. Voir [Numéro d'expéditeur de gestion](user/smsmt/managesenderid.md).

??? question "Comment créer et gérer des modèles de messages ?"
    1. Allez à **SMS MT > Modèle de gestion**
    2. Cliquez sur **"Ajouter un modèle"** onglet
    3. Saisissez le nom du modèle et composez le contenu
    4. Cliquez sur **"Insert Placeholder"** ajouter des variables dynamiques pour la personnalisation (p. ex. <span data-ph="0"></span>, <span data-ph="1"></span>)
    5. Cliquez sur **Enregistrer** — le modèle peut exiger une approbation administrative

 **Après homologation:**

    - **Contenu statique** (Tout sauf les places) est verrouillé et ne peut pas être changé
    - Seulement **valeurs du détenteur de place** peut être modifié lors de l'utilisation du modèle dans les campagnes
    - Vous pouvez voir le statut d'approbation de tous les modèles dans la vue liste

    !!! warning "Important pour les utilisateurs de l'API"
 Lorsque vous envoyez via API en utilisant des modèles, assurez-vous **exact** l'espacement, les virgules, la ponctuation et le formatage correspondent au modèle approuvé. Même une divergence mineure peut faire que le modèle est considéré comme invalide et le message peut être rejeté.

 Si votre compte a **"Ouvrir le modèle"** activé, vous pouvez sauter la configuration du modèle. Voir [Management Template](user/smsmt/managetemplate.md).

??? question "Qu'est-ce que le DLT et pourquoi l'approbation du modèle/de l'identificateur d'appel d'offres est-elle requise?"
 **DLT (Technologie du grand livre distribué)** est un cadre réglementaire prescrit par **TRAI (Autorité de régulation de télécom de l'Inde)** pour tous les messages Application-to-Person (A2P) en Inde.

 **Principales exigences:**

    - Tous **IDs de l'expéditeur** doit être enregistré sur la plateforme DLT
    - Tous **modèles de message** doivent être pré-approuvés sur DLT avant utilisation
    - Les messages qui ne correspondent pas aux modèles approuvés peuvent être bloqués par les opérateurs
    - Cela vaut pour tous les SMS commerciaux et transactionnels envoyés en Inde

 **Pourquoi il existe:**

    - Réduit les communications commerciales non sollicitées (spam)
    - Protège les consommateurs des messages frauduleux
    - Crée une piste auditable pour toutes les messageries A2P
    - Assurer la conformité réglementaire des opérateurs de télécommunications

 Si vous opérez en dehors de l'Inde, le DLT peut ne pas s'appliquer, mais votre administrateur peut quand même imposer l'approbation de modèle pour le contrôle de la qualité.

??? question "Que se passe-t-il si mon ID d'expéditeur ou mon modèle est rejeté?"
 Si votre ID d'expéditeur ou modèle est rejeté par votre administrateur :

    - L'état s'affichera comme **Rejeté** dans la page de gestion correspondante
    - Vous devrez créer une **nouvelle demande** avec des précisions corrigées
    - Les raisons courantes de rejet comprennent : le contenu non conforme, le formatage incorrect, les entrées en double ou les violations de la politique
    - Contactez votre administrateur pour des raisons et des lignes directrices précises en matière de rejet

---

## Personnes-ressources

??? question "Comment créer et gérer des groupes de contact?"
 **Création d'un groupe :**

    1. Allez à **Personnes-ressources > Gérer les groupes**
    2. Cliquez sur **Ajouter un groupe**
    3. Saisissez un nom de groupe et enregistrez

 **Gestion des groupes existants — actions disponibles:**

    | Décision | Désignation des marchandises |
    |--------|-------------|
    | **Modifier le nom du groupe** | Renommer un groupe existant |
    | **Contacts pour l'importation en vrac** | Ajouter plusieurs contacts à partir d'un fichier |
    | **Groupe vide** | Supprimer tous les contacts mais garder le groupe |
    | **Supprimer le groupe** | Supprimer définitivement le groupe et tous les contacts |

 Les groupes facilitent l'organisation des bénéficiaires et les sélectionnent rapidement lors de la composition des campagnes. Voir [Gérer les groupes](user/contacts/managegroups.md).

??? question "Comment importer des contacts?"
 Les offres de SMPP de puissance **trois méthodes d'importation**:

 **Méthode 1: Importer à partir d'un fichier**

    - Meilleur pour les grands ensembles de données
    - Appui **.xls**, **.csv**et **.txt** formats
    - Sélectionnez le groupe cible, téléchargez le fichier et validez

 **Méthode 2: Copier et coller**

    - Rapide et flexible
    - Copier les contacts directement depuis une feuille Excel ou une autre source
    - Coller dans la zone d'entrée

 **Méthode 3 : Entrée manuelle**

    - Ajouter des contacts un par un
    - Meilleur pour un petit nombre de contacts

 **Étapes :**

    1. Sélectionnez la **groupe cible** de la liste déroulante
    2. Choisissez votre méthode d'importation
    3. Ajouter vos contacts
    4. Cliquez sur **Fait** pour confirmer l'importation

 Voir [Personnes-ressources pour l'importation](user/contacts/importcontacts.md).

??? question "Comment puis-je exporter des contacts?"
    1. Allez à **Personnes-ressources > Personnes-ressources pour l'exportation**
    2. Sélectionnez la **Groupe(s)** vous voulez exporter en utilisant des cases à cocher
    3. Cliquez sur **Exportation**
    4. Choisissez votre format préféré:
        - **.xls** — Format Excel
        - **.csv** — Valeurs séparées par des virgules
        - **.txt** — Texte simple
    5. Télécharger le fichier exporté

    !!! tip
 Exportez seulement les groupes dont vous avez besoin pour gérer les tailles de fichiers. Utiliser les exportations à des fins de sauvegarde ou de migration des contacts entre les systèmes.

 Voir [Personnes-ressources pour l'exportation](user/contacts/exportcontacts.md).

---

## Rapports

??? question "Comment puis-je consulter les rapports de campagne?"
 Allez à **Rapport > Rapport de campagne** où vous avez plusieurs vues:

 **Vue de campagne :**

    - Liste récapitulative de toutes les campagnes
    - Affiche l'état de la campagne, les taux de livraison, les dates d'exécution et les statistiques clés
    - Cliquez sur une campagne pour en savoir plus

 **Affichage de la liste :**

    - Rapport DLR (Recueil de livraison) avec détails au niveau du message
    - Affiche l'état de livraison des messages individuels

 **État de la campagne :**

    - Suivi de la file de messages en temps réel
    - Vue terminée et en attente de livraison

 **Onglet Actions :**

    - Nombre de messages délivrés
    - Nombre de messages en attente
    - Nombre de messages ayant échoué
    - Autres catégories de statut

 Filtrer par **date** trouver des campagnes spécifiques. Voir [Rapport de campagne](user/report/campaign.md).

??? question "Que signifie le statut de DLR?"
 Les états d'avancement du DLR (rapport de livraison) indiquent le résultat de chaque message :

    | État | Signification | Décision |
    |--------|---------|--------|
    | **Livraison** | Message livré avec succès au combiné du destinataire | Aucune action nécessaire |
    | **Échec** | Le message n'a pas pu être livré (numéro invalide, problème de réseau, bloqué, ou MDN) | Vérifier la validité du numéro; envisager de supprimer de la liste |
    | **En attente** | Message envoyé à l'opérateur mais confirmation de livraison non encore reçu | Attendre — le statut peut être mis à jour; certains opérateurs retardent les DLR |
    | **Saisie** | Le message attend dans le système pour être traité et envoyé | Attendre le traitement |
    | **Rejeté** | Le message a été rejeté par l'opérateur ou la passerelle | Vérifier la conformité du modèle, l'identifiant de l'expéditeur ou les restrictions de contenu |

    !!! tip
 Utilisez la **Nombre de messages** rapporter pour obtenir un résumé du statut sur une plage de dates, et utiliser **Télécharger le rapport** pour les exportations Excel détaillées.

??? question "Comment puis-je voir les rapports de comptage des messages?"
    1. Allez à **Rapport > Compte de messages**
    2. Sélectionner un **date** ou spécifiques **mois**
    3. Afficher les nombres de messages ventilés par état (livré, en attente, échoué, etc.)
    4. Cliquez sur **Lien hypertexte** un mois pour forer **Répartition au jour le jour**

 Le rapport affiche des comptes selon votre fuseau horaire configuré. Utiliser ensemble la plage de dates et les filtres d'état pour l'analyse ciblée du trafic. Voir [Compte des messages](user/report/messagecount.md).

??? question "Comment puis-je télécharger des rapports en format Excel?"
    1. Allez à **Rapport > Télécharger le rapport**
    2. Afficher la liste des **précédents rapports demandés** (le cas échéant)
    3. Cliquez sur **Rapport de demande** générer un nouveau rapport
    4. Le rapport entre **En attente** statut pendant que le système récupère les données
    5. Une fois le traitement terminé, l'état change **Prêt**
    6. Cliquez sur le rapport pour **télécharger** en format Excel (.xls)

 Les rapports comprennent des données détaillées au niveau du message : numéro du destinataire, état, horodatage, coût, numéro d'expéditeur, et plus encore. Voir [Télécharger le rapport](user/report/downloadreport.md).

??? question "Puis-je renvoyer des messages ratés d'une campagne?"
 Oui, mais avec conditions:

    1. Ouvrir la campagne **Rapport de campagne**
    2. Allez au **Renvoyer** onglet
    3. Sélectionnez les messages échoués ou en attente à renvoyer

 **Résoudre les règles d'admissibilité :**

    | Scénario | Resend Disponible ? |
    |----------|-------------------|
    | Campagne exécutée (achevée) | Oui |
    | Campagne toujours en attente | Numéro |
    | Les messages longs sont encore traités | Numéro |

    !!! tip
 Télécharger le rapport **avant la reprise** pour valider votre liste cible et éviter les livraisons en double à des numéros qui ont déjà reçu le message.

??? question "Comment arrêter une campagne de course ?"
    1. Allez à **Rapport > Rapport de campagne**
    2. Trouvez la campagne active
    3. Cliquez sur **Arrête** bouton

 **Important:**

    - Messages **déjà envoyé** ne peut être rappelé
    - Seulement **Autres messages en attente** sera annulé
    - Cette action est immédiate et ne peut être annulée
    - Utilisez ceci lorsque vous découvrez une erreur dans votre contenu de campagne ou que vous devez arrêter la livraison d'urgence

??? question "Comment reporter une campagne en attente?"
    1. Allez à **Rapport > Mes horaires**
    2. Trouvez la campagne que vous voulez programmer
    3. Cliquez sur **Modifier** bouton dans l'onglet Action
    4. Sélectionnez la nouvelle **fuseau horaire**
    5. Définir le nouveau **date et heure du calendrier**
    6. Cliquez sur **Enregistrer**

 Vérifiez toujours le fuseau horaire sélectionné pour vous assurer que la campagne est envoyée à l'heure locale correcte pour vos destinataires. Voir [Mes horaires](user/report/schedule.md).

---

## WhatsApp

??? question "Comment connecter mon compte WhatsApp Business ?"
 **Préalables:**

    - A vérifié **Entreprises Facebook** compte
    - A **Profil d'entreprise WhatsApp** lié à votre compte Facebook

 **Étapes :**

    1. Naviguez vers la section WhatsApp
    2. Cliquez sur **"Connect en utilisant Facebook"**
    3. Une boîte de dialogue apparaît — enregistrez votre compte Facebook avec iTextPro
    4. Créez ou liez votre **Profil d'entreprise WhatsApp** (ceci agit comme le pont entre Meta et iTextPro)
    5. Configurer les paramètres de messagerie de WhatsApp dans iTextPro

 Une fois connecté, vous pouvez commencer à créer des modèles, des campagnes et utiliser Team Inbox pour le support client. Voir [Pour commencer](plugins/whatsapp/whatsappuser/overview.md).

??? question "Comment créer une campagne WhatsApp ?"
    1. Cliquez sur **Campagne** bouton dans la section WhatsApp
    2. **Sélectionner le nom de l'expéditeur** depuis la liste déroulante (par défaut vers le nom du connecteur)
    3. **Ajouter des destinataires** utilisant l'une des trois méthodes suivantes:
        - **Entrée manuelle** — Tapez directement des numéros mobiles
        - **Importer des contacts** — Télécharger un fichier Excel/CSV
        - **Utiliser les groupes existants** — Sélectionner les groupes de contact précréés
    4. Cliquez sur **"Sélectionner le modèle"** et choisir un modèle préapprouvé
    5. **Personnaliser le message :**
        - Modifier l'en-tête si nécessaire
        - Remplacer les variables dynamiques ({{1}}, {{2}}, etc.) avec valeurs réelles
        - A **prévisualisation en temps réel** apparaît sur le côté droit
    6. Choisir **Tableau** (cochez la case et fixez la date/heure) ou **Envoyer maintenant**
    7. Cliquez sur **Envoyer**

 Seulement **Modèles Méta-approuvés** peut être utilisé, assurant la conformité réglementaire. Voir [Campagne](plugins/whatsapp/whatsappuser/campaign.md).

??? question "Quelles sont les catégories de modèles WhatsApp et comment en créer une ?"
 Les modèles WhatsApp sont classés par Meta en trois types :

    | Catégorie | Objet | Exemples |
    |----------|---------|---------|
    | **Commercialisation** | Messages promotionnels à plusieurs destinataires | Offres, lancements de produits, newsletters |
    | **Utilité** | Mises à jour en temps opportun concernant les achats/voyage du client | Confirmations de commande, mises à jour d'expédition, rappels de rendez-vous |
    | **Authentification** | OTP et messages de vérification | Codes de connexion, vérification de compte |

 **Création d'un modèle :**

    1. Allez à **WhatsApp > Modèle**
    2. Sélectionnez la **catégorie** (Marchés, services publics ou authentification)
    3. Sélectionnez la **langue** (Meta prend en charge plusieurs langues)
    4. **Ajouter un en-tête** (facultatif): Aucun, texte ou média (image, vidéo, document, emplacement)
    5. **Ajouter le corps**: Contenu principal du message avec variables via le bouton Variable (format: {{1}}, {{2}}, {{3}})
    6. Fournir **exemples** pour chaque variable (aide Meta à comprendre et à approuver plus rapidement)
    7. **Ajouter un pied de page** (facultatif): texte de marque ou avertissement
    8. **Ajouter des boutons** (facultatif):
        - **Bouton Opt-Out** — Option de désabonnement
        - **Boutons CTA** — Visitez le site Web (jusqu'à 2) ou appelez le numéro de téléphone
    9. Cliquez sur **Enregistrer sous forme d'ébauche** ou **Enregistrer et soumettre** pour l'approbation du Méta

 L'approbation prend généralement une **quelques secondes**. Une fois approuvé, vous pouvez prévisualiser, modifier (exige une nouvelle approbation), supprimer, ou lancer directement une campagne à partir du modèle. Voir [Template](plugins/whatsapp/whatsappuser/template.md).

??? question "Comment utiliser Team Inbox pour le support client ?"
 Team Inbox est une plateforme centralisée pour gérer les conversations avec WhatsApp :

 **Pour les administrateurs :**

    - Pleine visibilité **Toutes les conversations** (conversations d'agents humains et de chatbots)
    - **Prise de contrôle instantanée** de toute conversation en cours pour une résolution rapide des problèmes
    - Rechercher et filtrer les conversations

 **Pour les agents:**

    - Connexion unique pour chaque agent
    - Accès limité à **Chats attribués** seulement
    - Répondre aux clients en temps réel

 **Principales caractéristiques:**

    - Surveillance centralisée de toutes les interactions de WhatsApp en un seul endroit
    - Capacité de prise en charge administrative pour les problèmes exacerbés
    - Accès sécurisé avec des connexions uniques assurant la protection de la vie privée et des données
    - Rechercher et filtrer la recherche de conversation rapide

 Voir [Boîte de réception de l'équipe](plugins/whatsapp/whatsappuser/teaminbox.md).

??? question "Comment créer et gérer des comptes d'agents?"
 Les comptes d'agents permettent aux membres de votre équipe de soutien d'accéder à une connexion individuelle :

    1. Allez à **WhatsApp > Équipe avec les comptes d'agents**
    2. Cliquez sur **Ajouter un nouvel agent**
    3. Remplir les détails requis
    4. Cliquez sur **Enregistrer** — le compte agent est créé instantanément

 **Avantages des comptes d'agents individuels :**

    - **Gestion d'équipe améliorée** — Créer des groupes spécialisés pour différents sujets ou segments de clients
    - **Amélioration de la sécurité** — Restreindre l'accès aux agents autorisés seulement
    - **Responsabilité accrue** — Surveiller les performances de chaque agent et les temps de réponse
    - **Programme de poste flexible** — comptes séparés pour différents postes ou fuseaux horaires

 Voir [Agent d'équipe](plugins/whatsapp/whatsappuser/teamagent.md).

??? question "Comment configurer les règles de routage avancées pour WhatsApp ?"
 Le routage avancé dirige automatiquement les messages WhatsApp entrants vers le bon agent ou chatbot :

    1. Allez à **WhatsApp > Règles d'acheminement avancées**
    2. Cliquez sur **"Ajouter une nouvelle règle"**
    3. Configurez la règle avec ces paramètres :

    | Paramètres | Désignation des marchandises |
    |-----------|-------------|
    | **Nom de la règle** | Nom descriptif clair pour faciliter l'identification |
    | **Portée - Connecteur** | Sélectionnez le connecteur webchat spécifique |
    | **Portée - Calendrier** | Définit quand la règle est active |
    | **Logique - Type de charge utile** | Itinéraire par type de contenu (texte, image, etc.) |
    | **Logique - Texte de la charge utile** | Route par mots-clés ou phrases spécifiques |
    | **Logique - Caption de charge utile** | Route par image/titre vidéo |
    | **Logique - Sender Info** | Itinéraire par les coordonnées de l'expéditeur (nom, téléphone) |
    | **Les opérateurs logiques** | Combiner les conditions avec la logique ET/OU |
    | **Exécution** | Route vers un itinéraire spécifique **Agent** ou **Bot** |

 Voir [Avanced Routing](plugins/whatsapp/whatsappuser/advancerouting.md) et [Configuration des règles](plugins/whatsapp/whatsappuser/ruleconfiguration.md).

??? question "Comment créer des flux de chatbot automatisés ?"
    1. Allez à **WhatsApp > Gérer le flux**
    2. Choisir : **Utiliser un modèle pré-construit** (réglage rapide) ou **Construire à partir de Scratch** (entièrement coutume)
    3. Configurer la **Déclencheur de bot** — un texte/phrase spécifique qui active le chatbot
    4. Définissez la **Mécanisme de réessayer** pour tentative de déclenchement ratée
    5. Configuration **Temps d'arrêt de la poche** pour un suivi automatique lorsque l'utilisateur cesse de répondre

 **Éléments de construction disponibles:**

    | Bloc | Désignation des marchandises |
    |-------|-------------|
    | **Envoyer un message** | Envoyer un message texte à l'utilisateur |
    | **Collecte des données** | Affiche une invite et capture la réponse de l'utilisateur dans une variable |
    | **Option** | Présentez jusqu'à 3 options (limite Meta) avec une image en option; le flux continue selon la sélection |
    | **Secteur** | Créer des chemins conditionnels basés sur des entrées précédemment collectées |
    | **Envoyer la pièce jointe** | Envoyer des documents, des photos ou des vidéos |

 Combinez ces blocs pour créer des conversations automatisées qui traitent des FAQ, collectent des informations, qualifient les pistes et les itinéraires vers les agents humains au besoin. Voir [Gérer le flux](plugins/whatsapp/whatsappuser/manageflow.md).

??? question "Comment puis-je surveiller les journaux de communication WhatsApp?"
 Allez à **WhatsApp > Surveillance** pour consulter les dossiers de transaction détaillés:

    - Chaque interaction entre votre application et Meta (WhatsApp) est enregistrée
    - Les deux **requêtes** et **Réponses** sont enregistrées
    - Utile pour résoudre les problèmes de livraison et diagnostiquer les problèmes techniques

    !!! warning
 Les registres de surveillance sont conservés pour **3 derniers jours** Seulement. Vérifiez les journaux rapidement si vous devez enquêter sur un problème.

 Voir [Surveiller](plugins/whatsapp/whatsappuser/monitoring.md).

??? question "Comment puis-je consulter les rapports de campagne de WhatsApp?"
 Allez à **WhatsApp > Rapports** pour plusieurs types de rapports:

 **Rapport de campagne :**

    - **Affichage de la campagne** — Aperçu du nom de la campagne, de l'expéditeur, du contenu, du total des messages, du statut et des coûts
    - **Affichage de la liste** — Renseignements sur le niveau de message, y compris le numéro du destinataire, le modèle utilisé, la date de soumission, la date de livraison, l'état et les codes d'erreur

 **Rapport de compte de message :**

    - Aperçu rapide du total des messages envoyés dans une plage de dates sélectionnée

 **Mon horaire :**

    - Voir toutes les campagnes de WhatsApp programmées avec état et nombre de messages

 **Télécharger le rapport :**

    - Exporter des rapports de campagne WhatsApp détaillés pour une analyse hors ligne
    - Séparé des rapports SMS pour une meilleure organisation

 Voir [Rapport de campagne](plugins/whatsapp/whatsappuser/reports/campaignreport.md).

---

## API développeur

??? question "Comment puis-je accéder à la documentation API?"
    1. Allez à **API développeur > Document API**
    2. Cliquez sur **Afficher le document de l'API**
    3. Le système redirige vers le **Swagger** outil d'API interactif
    4. Parcourir les paramètres, afficher les formats de demande/réponse et tester les appels d'API directement

 La documentation comprend les formats de charge utile, les structures de réponse, les détails d'authentification, le traitement des erreurs et les meilleures pratiques d'intégration. Voir [document API](user/apidocument/document.md).

??? question "Comment générer des identifiants d'API et commencer?"
 L'accès à l'API est fourni par votre administrateur :

    1. Votre administrateur active **Accès à l'API HTTP** pour votre compte
    2. Vous recevez **Nom d'utilisateur** et **Clé API** pour l'authentification
    3. Allez à **API développeur > API développeur** pour voir vos références
    4. Cliquez sur **Afficher le document de l'API** pour accéder à l'outil Swagger pour tester

 Utilisez ces identifiants dans l'en-tête d'autorisation de vos requêtes API. L'outil Swagger vous permet de tester tous les paramètres de l'API de manière interactive avant de vous intégrer à votre application. Voir [API Developer](user/apidocument/developerapi.md).

??? question "Quels sont les paramètres de l'API disponibles?"
 Power SMPP fournit des API REST complètes pour:

    - **Envoi de SMS** — Présentation de messages uniques et en vrac
    - **Vérification de l'état de livraison** — Demander le statut de DLR pour les messages envoyés
    - **Gestion des contacts** — Créer, mettre à jour et supprimer des contacts/groupes
    - **Récupération de rapports** — Tirer les rapports de campagne et de message programmatiquement

 Tous les paramètres acceptent la norme **Méthodes HTTP** (GET, POST) et retour **Réponses de JSON**. La liste complète des paramètres, des exemples et des codes de réponse est disponible dans le [document API](user/apidocument/document.md).

??? question "Puis-je intégrer Power SMPP à ma propre application?"
 Oui. Power SMPP prend en charge l'intégration de tiers par:

    - **API REST** — API HTTP complète pour l'accès programmatique
    - **Hooks Web** — Appels en temps réel pour les notifications DLR et MO
    - **Protocole SMPP** — Connectivité directe SMPP v3.4 pour les intégrations à haut volume (configuré par admin)

 La documentation Swagger fournit des exemples de demandes/réponses et des pratiques exemplaires pour une intégration transparente. Contactez votre administrateur pour les détails de connexion SMPP.

---

## Compte & facturation

??? question "Comment puis-je visualiser mon plan tarifaire?"
 Allez à **Barre d'application > Mon plan de taux** pour voir votre prix actuel:

    - Les prix sont affichés par **Pays** et **réseau**
    - Les tarifs sont fixés par votre compte parent/administrateur
    - Ils déterminent **Coût par message** pour chaque destination
    - Utilisez ceci pour estimer les coûts de campagne avant d'envoyer

 L'aperçu des coûts montré lors de la composition de la campagne utilise ces taux. Voir [Mon plan tarifaire](user/applicationbar/rateplan.md).

??? question "Quelle est la différence entre la facturation prépayée et Postpayée?"
    | Fonctionnalité | Prépayé | Postes payés |
    |---------|---------|----------|
    | **Solde** | Doit avoir suffisamment de crédits avant d'envoyer | Facturation après consommation |
    | **Vérification du crédit** | Le système vérifie l'équilibre avant traitement | Aucune vérification préalable requise |
    | **Dépenses excessives** | Impossible — la campagne s'arrête lorsque les crédits s'épuisent | Possibilité — suivi de la facturation |
    | **Cas d'utilisation** | Le plus fréquent pour les utilisateurs finaux | Généralement pour les comptes de confiance/entreprise |

 Votre mode de facturation est configuré par votre administrateur. Vérification **Barre d'application > Mes transactions** pour visualiser votre solde actuel et l'historique des transactions.

??? question "Comment puis-je vérifier mon historique de transaction?"
 Allez à **Barre d'application > Mes transactions** pour voir:

    - Historique complet des transactions entre votre compte et votre compte parent
    - Crédits supplémentaires
    - Déductions de crédit (frais de campagne)
    - Une piste d'audit complète pour la transparence

 Cela vous aide à suivre les dépenses, vérifier les suppléments et gérer votre budget de messagerie. Voir [Mes opérations](user/applicationbar/transaction.md).

??? question "Comment configurer les webhooks pour les notifications en temps réel ?"
 Webhooks pousser en temps réel les notifications DLR et MO à votre application:

    1. Allez à **Barre d'application > WebHooks**
    2. Cliquez sur **"Ajouter un nouveau Webhook"**
    3. Configurer le webhook :

    | Champ | Désignation des marchandises |
    |-------|-------------|
    | **Nom amical** | Un nom descriptif pour le webhook |
    | **URL de la base d'extrémité** | URL de rappel de votre serveur |
    | **Méthode** | GET ou POST |
    | **Maître** | MO (messages entrants) ou DLR (reçus de livraison) |

 **Prescriptions techniques:**

    - Votre paramètre doit revenir **HTTP 200 OK** dans le délai imparti
    - Le délai par défaut est **10 secondes**
    - Si votre serveur ne répond pas à temps, la notification peut être réétudiée ou abandonnée.

 Voir [WebHooks](user/applicationbar/webhook.md).

??? question "Comment configurer les courriels de notification ?"
 Allez à **Barre d'application > Courriels de notification** pour configurer les alertes email:

    - Par défaut, les notifications sont envoyées à votre **courriel enregistré** Adresse
    - Vous pouvez ajouter **autres adresses électroniques des parties prenantes** pour recevoir des alertes
    - Configurer lequel **événements** déclencher des notifications par courriel

 Les notifications par courriel sont utilisées pour les communications par compte, les alertes de campagne, la livraison par le BTP et les notifications système. Voir [Email de notification](user/applicationbar/notificationemail.md).

---

## Dépannage

??? question "Pourquoi mes messages sont-ils affichés pendant longtemps ?"
 Plusieurs raisons peuvent causer une prolongation du statut :

    - **Délais des opérateurs** — Certains opérateurs mobiles prennent plus de temps pour retourner les confirmations de livraison
    - **Téléphone du bénéficiaire éteint** — Le message est en attente à l'opérateur jusqu'à ce que le téléphone soit accessible
    - **Engorgement des réseaux** — Des périodes de trafic élevé peuvent retarder le traitement des DLR
    - **Questions relatives à la passerelle** — La passerelle en amont peut connaître des retards

 **Que faire:** Attendre un délai raisonnable (varie selon le pays/l'exploitant). Si les messages demeurent en attente après 24 à 48 heures, il est peu probable qu'ils soient livrés. Vérifiez auprès de votre administrateur si le problème persiste.

??? question "Pourquoi mon message a-t-il été rejeté ou échoué?"
 Raisons communes de l'échec du message:

    | Motifs | Solution |
    |--------|----------|
    | Numéro de téléphone non valide | Vérifier le format du numéro inclut le code du pays correct |
    | MDN/Ne dérangez pas | Le bénéficiaire s'est retiré des messages publicitaires |
    | Incohérence du modèle | S'assurer que le message correspond exactement au modèle approuvé |
    | ID de l'expéditeur non approuvé | Utiliser un ID d'expéditeur approuvé ou demander l'approbation |
    | Nombre insuffisant de crédits | Remplir votre solde de compte (prépayé) |
    | Numéro sur la liste noire | Vérifiez auprès de votre administrateur |
    | Contenu bloqué | Examiner le contenu du message pour les mots-clés restreints |

??? question "Pourquoi mon coût de campagne diffère-t-il de ce que j'attendais?"
 Les coûts de la campagne dépendent :

    - **Nombre de bénéficiaires** — Chaque numéro unique est facturé
    - **segments de messages** — Les messages longs sont divisés en plusieurs segments, chacun facturé séparément
    - **Unicode vs GSM** — Les messages Unicode ont des limites de caractères inférieures, ce qui donne lieu à davantage de segments
    - **Tarifs de destination** — Différents pays/réseaux ont des coûts de permestage différents
    - **Indemnisation des DLR** — Certaines configurations peuvent ajuster les coûts en fonction de l'état de livraison

 Toujours vérifier **Aperçu des coûts** avant de confirmer une campagne, et de revoir votre [Plan de taux](user/applicationbar/rateplan.md) pour les prix spécifiques à la destination.

??? question "J'ai oublié mon mot de passe. Comment le réinitialiser ?"
 Les réinitialisations de mot de passe sont gérées par votre **administrateur système**. Contactez-les directement pour demander une réinitialisation. Une fois réinitialisé, connectez-vous avec le mot de passe temporaire et changez-le immédiatement via **Paramètres > Modifier le mot de passe**.

 Votre administrateur peut également avoir une option de réinitialisation du mot de passe en libre-service configurée — vérifiez avec eux pour le processus spécifique.
