---
title: Utiliser des solutions hors ligne à l'aide du modèle objet InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- solutions [infopath 2007], offline,offline solutions [InfoPath 2007], InfoPath 2003-compatible form templates,InfoPath 2003-compatible form templates, offline solutions
localization_priority: Normal
ms.assetid: 634ccd8c-0b5f-4161-875c-0e546a517377
description: Le modèle objet compatible InfoPath 2003 contient la propriété MachineOnlineState de l'objet Application qui permet au code de votre formulaire de vérifier si l'ordinateur de l'utilisateur est connecté au réseau. Le code de formulaire peut effectuer différentes actions en fonction de l'état de la connexion.
ms.openlocfilehash: 452eb0d92b09dc0c3f9b2c247f7cda243dc8eb13
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429242"
---
# <a name="work-with-offline-solutions-using-the-infopath-object-model"></a><span data-ttu-id="04e15-105">Utiliser des solutions hors ligne à l'aide du modèle objet InfoPath</span><span class="sxs-lookup"><span data-stu-id="04e15-105">Work with offline solutions using the InfoPath object model</span></span>

<span data-ttu-id="04e15-p102">Le modèle objet compatible InfoPath 2003 contient la propriété [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) de l'objet [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) qui permet au code de votre formulaire de vérifier si l'ordinateur de l'utilisateur est connecté au réseau. Le code de formulaire peut effectuer différentes actions en fonction de l'état de la connexion.</span><span class="sxs-lookup"><span data-stu-id="04e15-p102">The InfoPath 2003-compatible object model provides the [MachineOnlineState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.MachineOnlineState.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) object which enables your form code to check whether the user's computer is connected to the network. Your form code can perform different actions depending on the state of the connection.</span></span> 
  
## <a name="using-the-machineonlinestate-property"></a><span data-ttu-id="04e15-108">Utilisation de la propriété MachineOnlineState</span><span class="sxs-lookup"><span data-stu-id="04e15-108">Using the MachineOnlineState property</span></span>

<span data-ttu-id="04e15-109">L'exemple qui suit vous présente comment ajouter une logique au code de votre formulaire afin de déterminer comment le formulaire doit être envoyé, en fonction de l'état connecté ou hors connexion de l'ordinateur.</span><span class="sxs-lookup"><span data-stu-id="04e15-109">The following example shows how you can add logic to your form code that determines how to submit a form based on whether the user's computer is online or offline.</span></span>
  
<span data-ttu-id="04e15-p103">Cet exemple part du principe que vous avez créé un formulaire de rapports de ventes qui contient un champ « période » qui spécifie le mois et l'année concernés par le rapport. Il part également du principe que vous avez défini une connexion de données et la logique d'envoi du rapport lorsque l'utilisateur est connecté.</span><span class="sxs-lookup"><span data-stu-id="04e15-p103">This example assumes that you have created a form for submitting a sales report that contains a field named "period" that specifies the month and year covered in the report. It also assumes that you have already defined a data connection and the logic for submitting the report when the user is online.</span></span>
  
### <a name="add-a-data-connection-that-submits-the-form-as-an-attachment-to-an-email-message"></a><span data-ttu-id="04e15-112">Ajouter une connexion de données qui envoie le formulaire en tant que pièce jointe à un message électronique</span><span class="sxs-lookup"><span data-stu-id="04e15-112">Add a data connection that submits the form as an attachment to an email message</span></span>

1. <span data-ttu-id="04e15-113">Créez ou ouvrez un modèle de formulaire InfoPath avec code managé.</span><span class="sxs-lookup"><span data-stu-id="04e15-113">Create or open an InfoPath managed-code form template.</span></span>
    
2. <span data-ttu-id="04e15-114">Dans InfoPath, en mode Création, cliquez sur **Connexions de données** sous l'onglet **Données**.</span><span class="sxs-lookup"><span data-stu-id="04e15-114">In InfoPath design mode, on the **Data** tab, click **Data Connections**.</span></span>
    
3. <span data-ttu-id="04e15-115">Dans la boîte de dialogue **Connexions de données**, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="04e15-115">In the **Data Connections** dialog box, click **Add**.</span></span>
    
4. <span data-ttu-id="04e15-116">Dans l' **Assistant Connexion de données**, cliquez sur **Envoi des données**, puis sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="04e15-116">In the **Data Connection Wizard**, click **Submit data**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="04e15-117">Sur la page suivante de l'Assistant, cliquez sur **en tant que message électronique**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="04e15-117">On the next page of the wizard, click **As an email message**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="04e15-118">Sur la page suivante de l'Assistant, tapez votre adresse de messagerie dans la zone **à** .</span><span class="sxs-lookup"><span data-stu-id="04e15-118">On the next page of the wizard, type your email address in the **To** box.</span></span> 
    
7. <span data-ttu-id="04e15-119">Dans la zone de texte **Objet**, effectuez les opérations suivantes pour combiner la période de ventes avec le texte « Rapport de ventes » :</span><span class="sxs-lookup"><span data-stu-id="04e15-119">In the **Subject** box, do the following to combine the sales period with the text Sales Report:</span></span> 
    
   1. <span data-ttu-id="04e15-120">Cliquez sur le bouton **Formule** en regard de la zone de texte **Objet**.</span><span class="sxs-lookup"><span data-stu-id="04e15-120">Click the **Formula** button next to the **Subject** box.</span></span> 
      
   2. <span data-ttu-id="04e15-121">Dans la boîte de dialogue **Insérer une formule**, cliquez sur **Insérer une fonction**.</span><span class="sxs-lookup"><span data-stu-id="04e15-121">In the **Insert Formula** dialog box, click **Insert Function**.</span></span>
      
   3. <span data-ttu-id="04e15-122">Dans la boîte de dialogue **Insérer une fonction**, cliquez sur **Texte** dans la liste **Catégories**, puis double-cliquez sur **concat** dans la liste **Fonctions**.</span><span class="sxs-lookup"><span data-stu-id="04e15-122">In the **Insert Function** dialog box, click **Text** in the **Categories** list, and then double-click **concat** in the **Functions** list.</span></span> 
      
   4. <span data-ttu-id="04e15-123">Remplacez la première instance de **double-cliquer pour insérer un champ** par 'Rapport de ventes : ' (avec des guillemets simples).</span><span class="sxs-lookup"><span data-stu-id="04e15-123">Replace the first instance of **double click to insert field** with the following (include the single quotes): 'Sales Report: '</span></span> 
      
   5. <span data-ttu-id="04e15-124">Double-cliquez sur la deuxième instance de **double-cliquer pour insérer un champ**.</span><span class="sxs-lookup"><span data-stu-id="04e15-124">Double-click the second instance of **double click to insert field**.</span></span>
      
   6. <span data-ttu-id="04e15-125">Dans la boîte de dialogue **Sélectionner un champ ou un groupe**, sélectionnez le champ période.</span><span class="sxs-lookup"><span data-stu-id="04e15-125">In the **Select a Field or Group** dialog box, select the period field.</span></span> 
      
   7. <span data-ttu-id="04e15-126">Supprimez la dernière instance de **double-cliquer pour insérer un champ**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="04e15-126">Delete the final instance of **double click to insert field**, and then click **OK**.</span></span>
    
8. <span data-ttu-id="04e15-127">Dans l'Assistant, cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="04e15-127">In the wizard, click **Next**.</span></span>
    
9. <span data-ttu-id="04e15-128">Sur la page suivante de l'Assistant, tapez «envoi par courrier électronique» dans la zone **Entrez un nom pour cette connexion de données** , puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="04e15-128">On the next page of the wizard, type 'Email Submit' in the **Enter a name for this data connection** box, and then click **Finish**.</span></span>
    
### <a name="add-logic-for-submitting-the-form-depending-on-the-connected-state-of-a-users-computer"></a><span data-ttu-id="04e15-129">Ajouter une logique d'envoi du formulaire en fonction de l'état de la connexion de l'ordinateur de l'utilisateur</span><span class="sxs-lookup"><span data-stu-id="04e15-129">Add logic for submitting the form depending on the connected state of a user's computer</span></span>

1. <span data-ttu-id="04e15-130">Dans InfoPath, en mode Création, cliquez sur **Options d'envoi** sous l'onglet **Données**.</span><span class="sxs-lookup"><span data-stu-id="04e15-130">In InfoPath design mode, on the **Data** tab, click **Submit Options**.</span></span>
    
2. <span data-ttu-id="04e15-131">Dans la boîte de dialogue **Options d'envoi**, cliquez sur **Autoriser les utilisateurs à envoyer ce formulaire**, puis sélectionnez **Effectuer une action personnalisée à l'aide du code**.</span><span class="sxs-lookup"><span data-stu-id="04e15-131">In the **Submit Options** dialog box, click **Allow users to submit this form**, and then select **Perform custom action using Code**.</span></span>
    
3. <span data-ttu-id="04e15-132">Cliquez sur le bouton **Modifier le code**.</span><span class="sxs-lookup"><span data-stu-id="04e15-132">Click the **Edit Code** button.</span></span> 
    
4. <span data-ttu-id="04e15-133">Ajoutez les deux fonctions qui suivent sous le gestionnaire d'événements [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) :</span><span class="sxs-lookup"><span data-stu-id="04e15-133">Add the following two functions below the [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) event handler:</span></span> 
    
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

5. <span data-ttu-id="04e15-134">Ajoutez l'instruction **if** qui suit à la fonction de gestionnaire d'événements **OnSubmitRequest**.</span><span class="sxs-lookup"><span data-stu-id="04e15-134">Add the following **if** statement to the **OnSubmitRequest** event handler function.</span></span> 
    
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

### <a name="test-the-code"></a><span data-ttu-id="04e15-135">Test du code</span><span class="sxs-lookup"><span data-stu-id="04e15-135">Test the code</span></span>

1. <span data-ttu-id="04e15-136">Dans le Concepteur InfoPath, cliquez sur **Aperçu** sous l'onglet **Accueil**.</span><span class="sxs-lookup"><span data-stu-id="04e15-136">In the InfoPath designer, click **Preview** on the **Home** tab.</span></span> 
    
2. <span data-ttu-id="04e15-137">Remplissez le formulaire.</span><span class="sxs-lookup"><span data-stu-id="04e15-137">Fill out the form.</span></span>
    
3. <span data-ttu-id="04e15-138">Lancez Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="04e15-138">Start Microsoft Internet Explorer.</span></span>
    
4. <span data-ttu-id="04e15-139">Dans Internet Explorer, cliquez sur **Travailler hors connexion** dans le menu **Fichier**.</span><span class="sxs-lookup"><span data-stu-id="04e15-139">In Internet Explorer, click **Work offline** on the **File** menu.</span></span> 
    
5. <span data-ttu-id="04e15-140">Dans InfoPath, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="04e15-140">In InfoPath, click **Submit**.</span></span> <span data-ttu-id="04e15-141">Vous devez voir apparaître un message indiquant que le formulaire sera envoyé sous forme de message électronique.</span><span class="sxs-lookup"><span data-stu-id="04e15-141">You should see a message that the form will be submitted as an email message.</span></span>
    
6. <span data-ttu-id="04e15-p105">Cliquez sur **Envoyer**. Vous devez voir apparaître un message indiquant que le formulaire a été envoyé hors connexion.</span><span class="sxs-lookup"><span data-stu-id="04e15-p105">Click **Send**. You should see a message stating that the form has been submitted offline.</span></span>
    

