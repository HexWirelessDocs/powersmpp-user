
## Webhooks: Notifications DLR/MO en temps réel

Les **Hooks Web** fonctionnalité dans iTextPro permet aux utilisateurs de recevoir **notifications en temps réel** des **DLR (Recueil de livraison)** et **MO (d'origine mobile)** messages via HTTP Web push.

![Webhooks](images/webhook1.png)

---

### Caractéristiques principales

- **Notifications en temps réel** 
 Recevez instantanément des copies des messages DLR/MO au fur et à mesure qu'ils se produisent.

- **Manipulation DLR/MO** 
 Choisissez le type de gestionnaire — si le webhook est destiné à **Pays** ou **DLR**.

- **Configuration flexible** 
 Définir un nom amical, définir l'URL de base du paramètre, sélectionner la méthode de requête (**Allez** ou **POSTE**) et assigner le gestionnaire approprié.

- **Sensibilisation au délai** 
 Webhook demandes ont un **délai par défaut de 10 secondes**. Le paramètre configuré doit renvoyer une **200 OK** réponse dans ce délai.

---

### Étapes pour configurer les hooks Web

1. **Accès aux sites Web** 
 Naviguez vers la **Hooks Web** dans iTextPro.

2. **Ajouter un nouveau Webhook** 
 Cliquez sur **"Ajouter un nouveau Webhook"** pour créer une nouvelle configuration.

3. **Préciser les détails** 
   - Nom amical 
   - URL de la base d'extrémité 
   - Méthode (**Allez** ou **POSTE**) 
   - Ouvrier (**Pays** ou **DLR**)

4. **Enregistrer la configuration** 
 Confirmez et enregistrez les détails du webhook.

---

Les **Hooks Web** la fonctionnalité assure **mises à jour instantanées, fiables et configurables des messages**, aidant les utilisateurs à maintenir un flux de communication efficace avec la livraison de données en temps réel.
