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
ms.openlocfilehash: ab149b488d2b2df1e91ba2cb435960c6749ecefb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574558"
---
# <a name="work-with-offline-solutions"></a><span data-ttu-id="d8a60-105">Travailler avec des solutions en mode hors connexion</span><span class="sxs-lookup"><span data-stu-id="d8a60-105">Work with offline solutions</span></span>

<span data-ttu-id="d8a60-p102">Le modèle objet InfoPath fournit la propriété [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) de la classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) qui active votre code de formulaire pour déterminer si l'ordinateur de l'utilisateur est connecté au réseau. En vérifiant la valeur de la propriété **MachineOnlineState**, votre code de formulaire peut effectuer différentes actions, selon l'état de la connexion.</span><span class="sxs-lookup"><span data-stu-id="d8a60-p102">The InfoPath object model provides the [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.MachineOnlineState.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class that enables your form code to check whether the user's computer is connected to the network. By checking the value of **MachineOnlineState** property, your form code can perform different actions depending on the state of the connection.</span></span> 
  
## <a name="using-the-machineonlinestate-property"></a><span data-ttu-id="d8a60-108">À l’aide de la propriété MachineOnlineState</span><span class="sxs-lookup"><span data-stu-id="d8a60-108">Using the MachineOnlineState property</span></span>

<span data-ttu-id="d8a60-109">L'exemple suivant vous montre comment ajouter une logique au code de votre formulaire afin de déterminer comment le formulaire doit être envoyé, selon que l'ordinateur de l'utilisateur est connecté ou non.</span><span class="sxs-lookup"><span data-stu-id="d8a60-109">The following example shows how you can add logic to your form code that determines how to submit a form based on whether the user's computer is online or offline.</span></span>
  
<span data-ttu-id="d8a60-p103">Cet exemple suppose que vous avez créé un formulaire permettant d'envoyer un rapport des ventes qui contient un champ intitulé période qui spécifie le mois et l'année concernés par le rapport. Il part également du principe que vous avez défini une connexion de données et la logique d'envoi du rapport lorsque l'utilisateur est connecté.</span><span class="sxs-lookup"><span data-stu-id="d8a60-p103">This example assumes that you have created a form for submitting a sales report that contains a field named period that specifies the month and year covered in the report. It also assumes that you have already defined a data connection and the logic for submitting the report when the user is online.</span></span> 
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a><span data-ttu-id="d8a60-112">Ajouter une connexion de données qui envoie le formulaire en tant que pièce jointe à un message électronique</span><span class="sxs-lookup"><span data-stu-id="d8a60-112">Add a data connection that submits the form as an attachment to an email message</span></span>

1. <span data-ttu-id="d8a60-113">Créez un modèle de formulaire InfoPath avec le modèle **Vide (éditeur InfoPath)**.</span><span class="sxs-lookup"><span data-stu-id="d8a60-113">Create an InfoPath form template using the **Blank (InfoPath Editor)** template.</span></span> 
    
2. <span data-ttu-id="d8a60-114">Dans InfoPath, en mode Création, cliquez sur **Connexions de données** sous l'onglet **Données**.</span><span class="sxs-lookup"><span data-stu-id="d8a60-114">In InfoPath design mode, click **Data Connections** on the **Data** tab.</span></span> 
    
3. <span data-ttu-id="d8a60-115">Dans la boîte de dialogue **Connexions de données**, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="d8a60-115">In the **Data Connections** dialog box, click **Add**.</span></span>
    
4. <span data-ttu-id="d8a60-116">Dans l' **Assistant Connexion de données**, cliquez sur **Envoi des données**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="d8a60-116">In the **Data Connection Wizard**, click **Submit data**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="d8a60-117">Dans la page suivante de l’Assistant, cliquez sur **en tant qu’un message électronique**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="d8a60-117">On the next page of the wizard, click **As an email message**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="d8a60-118">Dans la page suivante de l’Assistant, tapez votre adresse de messagerie dans **la zone** .</span><span class="sxs-lookup"><span data-stu-id="d8a60-118">On the next page of the wizard, type your email address in the **To** box.</span></span> 
    
7. <span data-ttu-id="d8a60-119">Dans la zone de texte **Objet**, effectuez les opérations suivantes pour combiner la période de ventes avec le texte « Rapport de ventes » :</span><span class="sxs-lookup"><span data-stu-id="d8a60-119">In the **Subject** box, do the following to combine the sales period with the text Sales Report:</span></span> 
    
   1. <span data-ttu-id="d8a60-120">Cliquez sur le bouton **Formule** en regard de la zone de texte **Objet**.</span><span class="sxs-lookup"><span data-stu-id="d8a60-120">Click the **Formula** button next to the **Subject** box.</span></span> 
      
   2. <span data-ttu-id="d8a60-121">Dans la boîte de dialogue **Insérer une formule**, cliquez sur **Insérer une fonction**.</span><span class="sxs-lookup"><span data-stu-id="d8a60-121">In the **Insert Formula** dialog box, click **Insert Function**.</span></span>
      
   3. <span data-ttu-id="d8a60-122">Dans la boîte de dialogue **Insérer une fonction**, cliquez sur **Texte** dans la liste **Catégories**, puis double-cliquez sur **concat** dans la liste **Fonctions**.</span><span class="sxs-lookup"><span data-stu-id="d8a60-122">In the **Insert Function** dialog box, click **Text** in the **Categories** list, and then double-click **concat** in the **Functions** list.</span></span> 
      
   4. <span data-ttu-id="d8a60-123">Remplacez la première instance de **double-cliquer pour insérer un champ** par 'Rapport de ventes : ' (avec des guillemets simples).</span><span class="sxs-lookup"><span data-stu-id="d8a60-123">Replace the first instance of **double click to insert field** with the following (include the single quotes): 'Sales Report: '</span></span> 
      
   5. <span data-ttu-id="d8a60-124">Double-cliquez sur la deuxième instance de **double-cliquer pour insérer un champ**.</span><span class="sxs-lookup"><span data-stu-id="d8a60-124">Double-click the second instance of **double click to insert field**.</span></span>
      
   6. <span data-ttu-id="d8a60-125">Dans la boîte de dialogue **Sélectionner un champ ou un groupe**, sélectionnez le champ période.</span><span class="sxs-lookup"><span data-stu-id="d8a60-125">In the **Select a Field or Group** dialog box, select the period field.</span></span> 
      
   7. <span data-ttu-id="d8a60-126">Supprimez la dernière instance de **double-cliquer pour insérer un champ**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="d8a60-126">Delete the final instance of **double click to insert field**, and then click **OK**.</span></span>
    
8. <span data-ttu-id="d8a60-127">Dans l'Assistant, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="d8a60-127">In the wizard, click **Next**.</span></span>
    
9. <span data-ttu-id="d8a60-128">Dans la page suivante de l'Assistant, cliquez sur le bouton **Formule** en regard de la zone **Nom de la pièce jointe**, puis répétez les étapes ci-dessus pour créer la formule concat("Rapport de ventes - ", période), puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="d8a60-128">On the next page of the wizard, click the **Formula** button next to the **Attachment Name** box, and then repeat the steps above to create the formula concat("Sales Report - ", period), and then click **Next**.</span></span>
    
10. <span data-ttu-id="d8a60-129">Dans la dernière page de l’Assistant, tapez envoyer du courrier électronique dans la zone **Entrez un nom pour cette connexion de données** , puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="d8a60-129">On the last page of the wizard, type Email Submit in the **Enter a name for this data connection** box, and then click **Finish**.</span></span>
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a><span data-ttu-id="d8a60-130">Ajout de la logique d'envoi du formulaire en fonction de l'état de la connexion de l'ordinateur de l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="d8a60-130">Add logic for submitting the form depending on the connected state of a user's computer</span></span>

1. <span data-ttu-id="d8a60-131">Dans InfoPath, en mode Création, cliquez sur **Options d'envoi** sous l'onglet **Données**.</span><span class="sxs-lookup"><span data-stu-id="d8a60-131">In InfoPath design mode, click **Submit Options** on the **Data** tab.</span></span> 
    
2. <span data-ttu-id="d8a60-132">Dans la boîte de dialogue **Options d'envoi**, cliquez sur **Autoriser les utilisateurs à envoyer ce formulaire**, sélectionnez **Effectuer une action personnalisée à l'aide du code**, cliquez sur **Modifier le code**.</span><span class="sxs-lookup"><span data-stu-id="d8a60-132">In the **Submit Options** dialog box, click **Allow users to submit this form**, select **Perform custom action using Code**, click **Edit Code**.</span></span>
    
3. <span data-ttu-id="d8a60-133">Ajoutez les deux fonctions suivantes en dessous du gestionnaire d'événements [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) :</span><span class="sxs-lookup"><span data-stu-id="d8a60-133">Add the following two functions below the [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) event handler:</span></span> 
    
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

4. <span data-ttu-id="d8a60-134">Ajoutez l'instruction **if** suivante à la fonction du gestionnaire d'événements [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d8a60-134">Add the following **if** statement to the [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) event handler function.</span></span> 
    
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

### <a name="test-the-code"></a><span data-ttu-id="d8a60-135">Test du code</span><span class="sxs-lookup"><span data-stu-id="d8a60-135">Test the code</span></span>

1. <span data-ttu-id="d8a60-136">Dans le menu **Déboguer**, cliquez sur **Démarrer le débogage**.</span><span class="sxs-lookup"><span data-stu-id="d8a60-136">On the **Debug** menu, click **Start Debugging**.</span></span>
    
2. <span data-ttu-id="d8a60-137">Remplissez le formulaire.</span><span class="sxs-lookup"><span data-stu-id="d8a60-137">Fill out the form.</span></span>
    
3. <span data-ttu-id="d8a60-138">Lancez Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="d8a60-138">Start Microsoft Internet Explorer.</span></span>
    
4. <span data-ttu-id="d8a60-139">Dans Internet Explorer, cliquez sur **Travailler hors connexion** dans le menu **Fichier**.</span><span class="sxs-lookup"><span data-stu-id="d8a60-139">In Internet Explorer, click **Work offline** on the **File** menu.</span></span> 
    
5. <span data-ttu-id="d8a60-140">Dans InfoPath, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="d8a60-140">In InfoPath, click **Submit**.</span></span> <span data-ttu-id="d8a60-141">Vous devriez voir un message que le formulaire sera envoyé dans un message électronique.</span><span class="sxs-lookup"><span data-stu-id="d8a60-141">You should see a message that the form will be submitted as an email message.</span></span>
    
6. <span data-ttu-id="d8a60-p105">Cliquez sur **Envoyer**. Vous devez voir apparaître un message indiquant que le formulaire a été soumis hors connexion et qu'il sera envoyé dès que vous vous connecterez au réseau.</span><span class="sxs-lookup"><span data-stu-id="d8a60-p105">Click **Send**. You should see a message stating that the form has been submitted offline and will be submitted when you connect to the network.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d8a60-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8a60-144">See also</span></span>

- [<span data-ttu-id="d8a60-145">Concevoir un modèle de formulaire pour une utilisation hors connexion</span><span class="sxs-lookup"><span data-stu-id="d8a60-145">Design a form template for offline use</span></span>](https://support.office.com/en-us/article/design-a-form-template-for-offline-use-3ab8de84-babc-4bd7-9215-66d308546be4)

