---
title: Travailler avec des solutions en mode hors connexion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- offline solutions [infopath 2007],solutions [InfoPath 2007], offline,InfoPath 2007, offline solutions
localization_priority: Normal
ms.assetid: 108f9bd0-c80f-4790-a572-da2f571a7d85
description: Le modèle objet InfoPath fournit la propriété MachineOnlineState de la classe Application qui active votre code de formulaire pour déterminer si l'ordinateur de l'utilisateur est connecté au réseau. En vérifiant la valeur de la propriété MachineOnlineState, votre code de formulaire peut effectuer différentes actions, selon l'état de la connexion.
ms.openlocfilehash: fcdaae31dd6a0c76cf1c453f267be430a2b34bba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782370"
---
# <a name="work-with-offline-solutions"></a>Travailler avec des solutions en mode hors connexion

Le modèle objet InfoPath fournit la propriété [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) de la classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) qui active votre code de formulaire pour déterminer si l'ordinateur de l'utilisateur est connecté au réseau. En vérifiant la valeur de la propriété **MachineOnlineState**, votre code de formulaire peut effectuer différentes actions, selon l'état de la connexion. 
  
## <a name="using-the-machineonlinestate-property"></a>À l’aide de la propriété MachineOnlineState

L'exemple suivant vous montre comment ajouter une logique au code de votre formulaire afin de déterminer comment le formulaire doit être envoyé, selon que l'ordinateur de l'utilisateur est connecté ou non.
  
Cet exemple suppose que vous avez créé un formulaire permettant d'envoyer un rapport des ventes qui contient un champ intitulé période qui spécifie le mois et l'année concernés par le rapport. Il part également du principe que vous avez défini une connexion de données et la logique d'envoi du rapport lorsque l'utilisateur est connecté. 
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a>Ajouter une connexion de données qui envoie le formulaire en tant que pièce jointe à un message électronique

1. Créez un modèle de formulaire InfoPath avec le modèle **Vide (éditeur InfoPath)**. 
    
2. Dans InfoPath, en mode Création, cliquez sur **Connexions de données** sous l'onglet **Données**. 
    
3. Dans la boîte de dialogue **Connexions de données**, cliquez sur **Ajouter**.
    
4. Dans l' **Assistant Connexion de données**, cliquez sur **Envoi des données**, puis sur **Suivant**.
    
5. Dans la page suivante de l’Assistant, cliquez sur **en tant qu’un message électronique**, puis cliquez sur **suivant**.
    
6. Dans la page suivante de l’Assistant, tapez votre adresse de messagerie dans **la zone** . 
    
7. Dans la zone de texte **Objet**, effectuez les opérations suivantes pour combiner la période de ventes avec le texte « Rapport de ventes » : 
    
   1. Cliquez sur le bouton **Formule** en regard de la zone de texte **Objet**. 
      
   2. Dans la boîte de dialogue **Insérer une formule**, cliquez sur **Insérer une fonction**.
      
   3. Dans la boîte de dialogue **Insérer une fonction**, cliquez sur **Texte** dans la liste **Catégories**, puis double-cliquez sur **concat** dans la liste **Fonctions**. 
      
   4. Remplacez la première instance de **double-cliquer pour insérer un champ** par 'Rapport de ventes : ' (avec des guillemets simples). 
      
   5. Double-cliquez sur la deuxième instance de **double-cliquer pour insérer un champ**.
      
   6. Dans la boîte de dialogue **Sélectionner un champ ou un groupe**, sélectionnez le champ période. 
      
   7. Supprimez la dernière instance de **double-cliquer pour insérer un champ**, puis cliquez sur **OK**.
    
8. Dans l'Assistant, cliquez sur **Suivant**.
    
9. Dans la page suivante de l'Assistant, cliquez sur le bouton **Formule** en regard de la zone **Nom de la pièce jointe**, puis répétez les étapes ci-dessus pour créer la formule concat("Rapport de ventes - ", période), puis cliquez sur **Suivant**.
    
10. Dans la dernière page de l’Assistant, tapez envoyer du courrier électronique dans la zone **Entrez un nom pour cette connexion de données** , puis cliquez sur **Terminer**.
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a>Ajout de la logique d'envoi du formulaire en fonction de l'état de la connexion de l'ordinateur de l'utilisateur

1. Dans InfoPath, en mode Création, cliquez sur **Options d'envoi** sous l'onglet **Données**. 
    
2. Dans la boîte de dialogue **Options d'envoi**, cliquez sur **Autoriser les utilisateurs à envoyer ce formulaire**, sélectionnez **Effectuer une action personnalisée à l'aide du code**, cliquez sur **Modifier le code**.
    
3. Ajoutez les deux fonctions suivantes en dessous du gestionnaire d'événements [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) : 
    
   ```cs
    public void OnlineSubmit(SubmitEventArgs e)
    {
      // Logic for submitting online goes here.
    }
    public void OfflineSubmit(SubmitEventArgs e)
    {
      // Access and submit to the email connection.
      DataConnectionCollection myDataConnections =
          this.DataConnections;
      EmailSubmitConnection submitConnection =
          (EmailSubmitConnection)myDataConnections["Email Submit"];
      submitConnection.Execute();
      // Notify the user that the form was submitted offline.
      System.Text.StringBuilder myMessage = 
          new System.Text.StringBuilder();
      myMessage.Append("You submitted your Sales Report offline. ");
      myMessage.Append("Your Sales Report is in your outbox ");
      myMessage.Append("and will be submitted when you connect to ");
      myMessage.Append("the network.");
        MessageBox.Show(myMessage.ToString());
      // The submission was successful.
      e.CancelableArgs.Cancel = false;
    }
   ```

   ```vb
    Public Sub OnlineSubmit(ByVal e As SubmitEventArgs)
      ' Logic for submitting online goes here.
    End Sub
    Public Sub OfflineSubmit(ByVal e As SubmitEventArgs)
      ' Access and submit to the email connection.
      Dim myDataConnections As DataConnectionCollection = _
          Me.DataConnections
      Dim submitConnection As EmailSubmitConnection = _
          DirectCast(myDataConnections("Email Submit"), _
          EmailSubmitConnection)
      submitConnection.Execute
      ' Notify the user that the form was submitted offline.
      Dim myMessage As System.Text.StringBuilder = _
          New System.Text.StringBuilder()
      myMessage.Append("You submitted your Sales Report offline. ")
      myMessage.Append("Your Sales Report is in your outbox ")
      myMessage.Append("and will be submitted when you connect to ")
      myMessage.Append("the network.")
        MessageBox.Show(myMessage.ToString())
      ' The submission was successful.
      e.CancelableArgs.Cancel = False
    End Sub
   ```

4. Ajoutez l'instruction **if** suivante à la fonction du gestionnaire d'événements [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) . 
    
   ```cs
    // Check the computer's connection state.
    if (this.Application.MachineOnlineState == MachineState.Online)
    {
      OnlineSubmit(e);
    }
    else
    {
      OfflineSubmit(e);
    }
   ```

   ```vb
    ' Check the computer's connection state.
    If (Me.Application.MachineOnlineState = MachineState.Online) Then
      OnlineSubmit(e)
    Else
    {
      OfflineSubmit(e)
    End If
   ```

### <a name="test-the-code"></a>Test du code

1. Dans le menu **Déboguer**, cliquez sur **Démarrer le débogage**.
    
2. Remplissez le formulaire.
    
3. Lancez Microsoft Internet Explorer.
    
4. Dans Internet Explorer, cliquez sur **Travailler hors connexion** dans le menu **Fichier**. 
    
5. Dans InfoPath, cliquez sur **Envoyer**. Vous devriez voir un message que le formulaire sera envoyé dans un message électronique.
    
6. Cliquez sur **Envoyer**. Vous devez voir apparaître un message indiquant que le formulaire a été soumis hors connexion et qu'il sera envoyé dès que vous vous connecterez au réseau.
    
## <a name="see-also"></a>Voir aussi

- [Concevoir un modèle de formulaire pour une utilisation hors connexion](http://office.microsoft.com/en-us/infopath/HA102117391033.aspx?pid=CH100341121033)

