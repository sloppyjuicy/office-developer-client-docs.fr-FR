---
title: Utiliser des solutions hors connexion à l’aide du modèle objet InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- solutions [infopath 2007], offline,offline solutions [InfoPath 2007], InfoPath 2003-compatible form templates,InfoPath 2003-compatible form templates, offline solutions
ms.localizationpriority: medium
ms.assetid: 634ccd8c-0b5f-4161-875c-0e546a517377
description: Le modèle objet compatible InfoPath 2003 contient la propriété MachineOnlineState de l'objet Application qui permet au code de votre formulaire de vérifier si l'ordinateur de l'utilisateur est connecté au réseau. Le code de formulaire peut effectuer différentes actions en fonction de l'état de la connexion.
ms.openlocfilehash: 5ac33120d3f88cdff0a0aa3eb8bdffe81962d095
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580572"
---
# <a name="work-with-offline-solutions-using-the-infopath-object-model"></a>Utiliser des solutions hors connexion à l’aide du modèle objet InfoPath

Le modèle objet compatible InfoPath 2003 contient la propriété [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) de l'objet [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) qui permet au code de votre formulaire de vérifier si l'ordinateur de l'utilisateur est connecté au réseau. Le code de formulaire peut effectuer différentes actions en fonction de l'état de la connexion. 
  
## <a name="using-the-machineonlinestate-property"></a>Utilisation de la propriété MachineOnlineState

L'exemple qui suit vous présente comment ajouter une logique au code de votre formulaire afin de déterminer comment le formulaire doit être envoyé, en fonction de l'état connecté ou hors connexion de l'ordinateur.
  
Cet exemple part du principe que vous avez créé un formulaire de rapports de ventes qui contient un champ « période » qui spécifie le mois et l'année concernés par le rapport. Il part également du principe que vous avez défini une connexion de données et la logique d'envoi du rapport lorsque l'utilisateur est connecté.
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a>Ajouter une connexion de données qui envoie le formulaire en tant que pièce jointe à un message électronique

1. Créez ou ouvrez un modèle de formulaire InfoPath avec code managé.
    
2. Dans InfoPath, en mode Création, cliquez sur **Connexions de données** sous l'onglet **Données**.
    
3. Dans la boîte de dialogue **Connexions de données**, cliquez sur **Ajouter**.
    
4. Dans l' **Assistant Connexion de données**, cliquez sur **Envoi des données**, puis sur **Suivant**.
    
5. Sur la page suivante de l’Assistant, cliquez sur En tant **que message électronique,** puis sur **Suivant**.
    
6. Sur la page suivante de l’Assistant, tapez votre adresse de messagerie dans la **zone À.** 
    
7. Dans la zone de texte **Objet**, effectuez les opérations suivantes pour combiner la période de ventes avec le texte « Rapport de ventes » : 
    
   1. Cliquez sur le bouton **Formule** en regard de la zone de texte **Objet**. 
      
   2. Dans la boîte de dialogue **Insérer une formule**, cliquez sur **Insérer une fonction**.
      
   3. Dans la boîte de dialogue **Insérer une fonction**, cliquez sur **Texte** dans la liste **Catégories**, puis double-cliquez sur **concat** dans la liste **Fonctions**. 
      
   4. Remplacez la première instance de **double-cliquer pour insérer un champ** par 'Rapport de ventes : ' (avec des guillemets simples). 
      
   5. Double-cliquez sur la deuxième instance de **double-cliquer pour insérer un champ**.
      
   6. Dans la boîte de dialogue **Sélectionner un champ ou un groupe**, sélectionnez le champ période. 
      
   7. Supprimez la dernière instance de **double-cliquer pour insérer un champ**, puis cliquez sur **OK**.
    
8. Dans l'Assistant, cliquez sur **Suivant**.
    
9. Sur la page suivante de l’Assistant,  tapez « Envoyer un courrier électronique » dans la zone Entrez un nom pour cette connexion de données, puis cliquez sur **Terminer.**
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a>Ajouter une logique d'envoi du formulaire en fonction de l'état de la connexion de l'ordinateur de l'utilisateur

1. Dans InfoPath, en mode Création, cliquez sur **Options d'envoi** sous l'onglet **Données**.
    
2. Dans la boîte de dialogue **Options d'envoi**, cliquez sur **Autoriser les utilisateurs à envoyer ce formulaire**, puis sélectionnez **Effectuer une action personnalisée à l'aide du code**.
    
3. Cliquez sur le bouton **Modifier le code**. 
    
4. Ajoutez les deux fonctions qui suivent sous le gestionnaire d'événements [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) : 
    
   ```cs
    public void OnlineSubmit(DocReturnEvent e)
    {
      // Logic for submitting online goes here.
    }
    public void OfflineSubmitX(DocReturnEvent e)
    {
      // Access and submit to the email adapter.
      DataAdaptersCollection myDataAdapters = 
          thisXDocument.DataAdapters;
      EmailAdapterObject submitAdapter = 
          (EmailAdapterObject) myDataAdapters["Email Submit"];
      submitAdapter.Submit();
      // Notify the user that the form was submitted offline.
      System.Text.StringBuilder message = 
      new System.Text.StringBuilder();
      message.Append("You submitted your Sales Report offline. ");
      message.Append("Your Sales Report is in your outbox ");
      message.Append("and will be submitted when you connect to ");
      message.Append("the network.");
        thisXDocument.UI.Alert(message.ToString());
      // The submission was successful.
      e.ReturnStatus = true;
    }
   ```

5. Ajoutez l'instruction **if** qui suit à la fonction de gestionnaire d'événements **OnSubmitRequest**. 
    
   ```cs
    // Check the computer's connection state.
    if (thisApplication.MachineOnlineState==XdMachineOnlineState.xdOnline)
    {
        OnlineSubmit(e);
    }
    else
    {
        OfflineSubmit(e);
    }
   ```

### <a name="test-the-code"></a>Test du code

1. Dans le Concepteur InfoPath, cliquez sur **Aperçu** sous l'onglet **Accueil**. 
    
2. Remplissez le formulaire.
    
3. Lancez Microsoft Internet Explorer.
    
4. Dans Internet Explorer, cliquez sur **Travailler hors connexion** dans le menu **Fichier**. 
    
5. Dans InfoPath, cliquez sur **Envoyer**. Vous devriez voir un message vous messageant que le formulaire sera envoyé sous la forme d’un message électronique.
    
6. Cliquez sur **Envoyer**. Vous devez voir apparaître un message indiquant que le formulaire a été envoyé hors connexion.
    

