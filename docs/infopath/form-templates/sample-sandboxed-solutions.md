---
title: Exemples de solutions en bac à sable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 415fa0fa-b7b7-4acb-a437-f54c34064004
description: Cette rubrique fournit deux exemples qui montrent le type de code que vous pouvez écrire dans un modèle de formulaire solution bac à sable InfoPath et comment publier ce modèle.
ms.openlocfilehash: b0874e34d843850df55eee87d689ce0d01112635
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782460"
---
# <a name="sample-sandboxed-solutions"></a><span data-ttu-id="aad37-103">Exemples de solutions en bac à sable</span><span class="sxs-lookup"><span data-stu-id="aad37-103">Sample sandboxed solutions</span></span>

<span data-ttu-id="aad37-p101">Les formulaires InfoPath avec code managé peuvent être publiés sur l'infrastructure solution bac à sable SharePoint à partir du concepteur InfoPath. Cette rubrique fournit deux exemples qui montrent le type de code que vous pouvez écrire dans un modèle de formulaire solution bac à sable InfoPath et comment publier ce modèle.</span><span class="sxs-lookup"><span data-stu-id="aad37-p101">InfoPath forms with managed code can be published to the SharePoint sandboxed solution infrastructure from the InfoPath Designer. This topic provides two examples that show the kind of code that you can write in an InfoPath sandboxed solution, and how to publish the form template.</span></span>
  
## <a name="example-1-sorting-data-in-an-order-form"></a><span data-ttu-id="aad37-106">L’exemple 1 : Tri des données dans un formulaire de commande</span><span class="sxs-lookup"><span data-stu-id="aad37-106">Example 1: Sorting data in an order form</span></span>

<span data-ttu-id="aad37-p102">Une tâche utile, comme trier les données dans un tableau extensible, peut être effectuée à l'aide de code dans un formulaire InfoPath. Pour ce faire, le code réordonne les nœuds dans un document XML sous-jacent qui est affiché dans le formulaire InfoPath. Bien que le scénario décrit dans cette rubrique est conçu pour publier directement un formulaire InfoPath en tant que solution bac à sable, celui-ci peut également être déployé comme un modèle de formulaire approuvé par l'administrateur.</span><span class="sxs-lookup"><span data-stu-id="aad37-p102">A useful task that you can perform by using code in an InfoPath form is to sort data in a repeating table. To do this, the code reorders the nodes in underlying XML document that is displayed in the InfoPath form. Although the scenario described in this topic is targeted for publishing directly from InfoPath as a sandboxed solution, it can also be deployed as an administrator-approved form template.</span></span>
  
<span data-ttu-id="aad37-110">Avant de commencer, vérifiez que vous remplissez les conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="aad37-110">Before you start, make sure that you meet the following requirements.</span></span>
  
- <span data-ttu-id="aad37-111">Vous êtes administrateur de collection de sites sur le site SharePoint Server 2010 ou SharePoint Foundation 2010 sur lequel vous souhaitez publier le formulaire.</span><span class="sxs-lookup"><span data-stu-id="aad37-111">You are a site collection administrator on the SharePoint Server 2010 or SharePoint Foundation 2010 site where you want to publish the form.</span></span>
    
- <span data-ttu-id="aad37-112">Contactez l’administrateur de batterie de serveurs pour vous assurer que le Service de Code en bac à sable Microsoft SharePoint Foundation est en cours d’exécution sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="aad37-112">Check with the farm administrator to make sure that the Microsoft SharePoint Foundation Sandboxed Code Service is running on the server.</span></span> <span data-ttu-id="aad37-113">Pour plus d’informations, voir [Publication de formulaires avec Code](publishing-forms-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="aad37-113">For more information, see [Publishing Forms with Code](publishing-forms-with-code.md).</span></span>
    
- <span data-ttu-id="aad37-114">Le langage de programmation que vous avez choisi pour le modèle de formulaire est **C#** ou **Visual Basic**, non suivi d'un nom de version antérieure.</span><span class="sxs-lookup"><span data-stu-id="aad37-114">The programming language that you have selected for the form template is either **C#** or **Visual Basic** without any earlier version name after it.</span></span> <span data-ttu-id="aad37-115">Les versions des langages de programmation et des modèles objet compatibles InfoPath 2007 ou InfoPath 2003 ne sont pas prises en charge pour solutions bac à sable.</span><span class="sxs-lookup"><span data-stu-id="aad37-115">The InfoPath 2007-compatible and InfoPath 2003-compatible versions of the programming languages and object models are not supported for sandboxed solutions.</span></span> <span data-ttu-id="aad37-116">Pour plus d’informations sur la façon de spécifier le langage de programmation, voir [Develop avec Visual Studio](how-to-develop-with-visual-studio.md).</span><span class="sxs-lookup"><span data-stu-id="aad37-116">For more information about how to specify the programming language, see [Develop with Visual Studio](how-to-develop-with-visual-studio.md).</span></span>
    
<span data-ttu-id="aad37-117">Pour créer un modèle de formulaire qui trie les données dans un contrôle **Tableau extensible** sur le formulaire, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="aad37-117">Perform the following steps to create a form template that sorts the data in a **Repeating Table** control on the form.</span></span> 
  
### <a name="to-create-a-form-template-that-programmatically-sorts-data-in-the-form"></a><span data-ttu-id="aad37-118">Pour créer un modèle de formulaire qui trie les données dans le formulaire par programmation</span><span class="sxs-lookup"><span data-stu-id="aad37-118">To create a form template that programmatically sorts data in the form</span></span>

1. <span data-ttu-id="aad37-p105">Créez un modèle de formulaire dans le concepteur InfoPath, puis ajoutez un contrôle **Tableau extensible** sur ce formulaire. Le code de cet exemple trie les lignes en fonction de la première colonne du tableau, mais vous pouvez facilement le modifier afin d'utiliser une autre colonne.</span><span class="sxs-lookup"><span data-stu-id="aad37-p105">Create a new form template in the InfoPath designer, and add a **Repeating Table** control to the form. The sample code for this example sorts the rows based on the first column in the table, but you can easily modify the code to work with any column.</span></span> 
    
2. <span data-ttu-id="aad37-p106">Ajoutez un contrôle **Bouton** au formulaire. Le code pour trier le tableau sera ajouté au gestionnaire d'événements pour l'événement **Clicked** du bouton, mais vous pouvez également utiliser un autre événement à cet effet.</span><span class="sxs-lookup"><span data-stu-id="aad37-p106">Add a **Button** control to the form. The code to sort the table will be added to the event handler for the button's **Clicked** event, but you could also use another event for this purpose.</span></span> 
    
3. <span data-ttu-id="aad37-p107">Sélectionnez le bouton, cliquez sur l'onglet **Propriétés**, puis cliquez sur **Code personnalisé**. Si vous n'avez pas encore enregistré votre formulaire, vous êtes invité à le faire, puis l'éditeur de code s'ouvre avec le curseur positionné sur le gestionnaire d'événements du bouton.</span><span class="sxs-lookup"><span data-stu-id="aad37-p107">Select the button, click the **Properties** tab, and then click **Custom Code**. If your form hasn't been saved yet, you are prompted to save it, and then the Code Editor will open with the cursor in the button's event handler.</span></span>
    
4. <span data-ttu-id="aad37-p108">Collez le code suivant dans le gestionnaire d'événements du bouton. Ce code place les éléments de la première colonne dans un tableau, trie ce tableau, puis réorganise le tableau initial en se basant sur ce dernier. Ce code suppose que les données triées sont de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="aad37-p108">Paste the following code into the button's event handler. The code puts the elements from the first column into an array, sorts the array, and then reorders the table based on the sorted array. This code assumes that the data being sorted is string data.</span></span>
    
   ```cs
    // Put the elements from the first column into an array.
    XPathNavigator root = this.CreateNavigator();
        
    // Create a node iterator which contains only the values that you want to sort.
    // For this form, the entire table is in "group1", each row is a "group2"
    // and the rows are "field1", "field2" and "field3" respectively.
    XPathNodeIterator nodeIterator = root.Select(
        "/my:myFields/my:group1/my:group2/my:field1", this.NamespaceManager);
        
    // Create arrays to use for sorting.
    string[] sortArrayWords = new string[nodeIterator.Count + 1];
    int[] sortArrayKeys = new int[nodeIterator.Count + 1];
    int arrayPosition = 1;
        
    // Populate the arrays for sorting.
    while (nodeIterator.MoveNext()) 
    {
        // Loop until there are no more elements
        sortArrayWords[arrayPosition] = nodeIterator.Current.Value;
        sortArrayKeys[arrayPosition] = arrayPosition;
        arrayPosition += 1;
    }
        
    // Sort the array.
    Array.Sort(sortArrayWords, sortArrayKeys);
    arrayPosition = 0;
        
    // Create new XML to update the table.
    string newTableXML = "";
    // Iterate through the sorted array of keys.
    for (int i = 1; i <= sortArrayWords.Length - 1; i++) 
    {
        nodeIterator = root.Select(
            "/my:myFields/my:group1/my:group2", this.NamespaceManager);
            
        // Go to the right position in the table.
        for (int j = 1; j <= sortArrayKeys[i]; j++) 
        {
            nodeIterator.MoveNext();
        }
            
        // Add the row to the XML.
        newTableXML += nodeIterator.Current.OuterXml;
    }
        
    // Set the table to use the new XML.
    root.SelectSingleNode(
        "/my:myFields/my:group1", this.NamespaceManager).InnerXml = newTableXML;
    
   ```

   ```vb
    ' Put the elements from the first column into an array.
    Dim root As XPathNavigator = Me.CreateNavigator
    ' Create a node iterator which contains only the values that you want to sort
    ' For this form, the entire table is in "group1",
    ' each row is a "group2"
    ' and the rows are "field1", "field2" and "field3" respectively.
    Dim nodeIterator As XPathNodeIterator = root.Select( _
        "/my:myFields/my:group1/my:group2/my:field1", Me.NamespaceManager)
    ' Create arrays to use for sorting.
    Dim sortArrayWords(nodeIterator.Count) As String
    Dim sortArrayKeys(nodeIterator.Count) As Integer
    Dim arrayPosition As Integer = 1
    ' Populate the arrays for sorting.
    While nodeIterator.MoveNext() ' Loop until there are no more elements
        sortArrayWords(arrayPosition) = nodeIterator.Current.Value
        sortArrayKeys(arrayPosition) = arrayPosition
        arrayPosition += 1
    End While
    ' Sort the array.
    Array.Sort(sortArrayWords, sortArrayKeys)
    arrayPosition = 0
    ' Create new XML to update the table.
    Dim newTableXML As String = ""
    ' Iterate through the sorted array of keys.
    For i As Integer = 1 To sortArrayWords.Length - 1
        nodeIterator = root.Select( _
            "/my:myFields/my:group1/my:group2", Me.NamespaceManager)
        ' Go to the right position in the table.
        For j As Integer = 1 To sortArrayKeys(i)
        nodeIterator.MoveNext()
        Next
    ' Add the row to the XML.
    newTableXML &amp;= nodeIterator.Current.OuterXml
    Next
    ' Set the table to use the new XML.
    root.SelectSingleNode("/my:myFields/my:group1", _
        Me.NamespaceManager).InnerXml = newTableXML
   ```

5. <span data-ttu-id="aad37-128">Publier votre formulaire à l’aide de la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="aad37-128">Publish your form by using the following steps:</span></span>
    
    1. <span data-ttu-id="aad37-129">Cliquez sur **SharePoint Server** sur l'onglet **Publier** dans Backstage.</span><span class="sxs-lookup"><span data-stu-id="aad37-129">Click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
        
    2. <span data-ttu-id="aad37-130">Entrez l'URL du site SharePoint sur lequel publier, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="aad37-130">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
        
       > [!IMPORTANT]
       > <span data-ttu-id="aad37-131">Vous devez être administrateur de collection de sites sur ce site pour publier ce modèle de formulaire en tant que solution bac à sable.</span><span class="sxs-lookup"><span data-stu-id="aad37-131">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
    
    3. <span data-ttu-id="aad37-132">Sélectionnez **Bibliothèque de formulaires**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="aad37-132">Select **Form Library**, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="aad37-133">Sélectionnez **Créer une bibliothèque de formulaires**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="aad37-133">Select **Create a new form library**, and then click **Next**.</span></span>
        
    5. <span data-ttu-id="aad37-134">Entrez le nom et la description de votre bibliothèque de formulaires, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="aad37-134">Enter the name and descriptions for your form library, and then click **Next**.</span></span>
        
    6. <span data-ttu-id="aad37-135">Cliquez sur **Publier**.</span><span class="sxs-lookup"><span data-stu-id="aad37-135">Click **Publish**.</span></span>
    
## <a name="example-2-managing-vendors-in-a-sharepoint-list"></a><span data-ttu-id="aad37-136">L’exemple 2 : Gestion des fournisseurs dans une liste SharePoint</span><span class="sxs-lookup"><span data-stu-id="aad37-136">Example 2: Managing vendors in a SharePoint list</span></span>

<span data-ttu-id="aad37-p109">Cet exemple comprend de la programmation par rapport au modèle objet Microsoft SharePoint Foundation 2010. Pour cela, vous devez établir une référence à l'assembly Microsoft.SharePoint.dll qui est installé avec une copie sous licence de SharePoint Server 2010.</span><span class="sxs-lookup"><span data-stu-id="aad37-p109">This example involves programming against the Microsoft SharePoint Foundation 2010 object model. To do that, you must establish a reference to the Microsoft.SharePoint.dll assembly which is installed with a licensed copy of SharePoint Server 2010.</span></span>
  
<span data-ttu-id="aad37-p110">La bibliothèque Microsoft.SharePoint.Server.dll est installée par défaut dans C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI. Elle doit être incluse dans les projets où vous programmez en fonction du modèle objet SharePoint. Pour établir une référence à Microsoft.SharePoint.dll dans un projet Visual Studio 2012, ouvrez l' **Éditeur de code**, puis cliquez sur **Ajouter une référence** dans le menu **Outils**. Dans la boîte de dialogue **Ajouter une référence**, cliquez sur l'onglet **Parcourir**, spécifiez l'emplacement du fichier Microsoft.SharePoint.dll, puis cliquez sur **OK**. Cela copie Microsoft.SharePoint.dll dans le répertoire du projet afin que vous puissiez utiliser les membres du modèle objet SharePoint Foundation 2010 dans votre solution InfoPath.</span><span class="sxs-lookup"><span data-stu-id="aad37-p110">Microsoft.SharePoint.Server.dll is installed in C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI by default. This DLL must be included in projects where you program against the SharePoint object model. To establish a reference to the Microsoft.SharePoint.dll in a Visual Studio 2012 project, open the **Code Editor**, and then click **Add Reference** on the **Tools** menu. In the **Add Reference** dialog box, click the **Browse** tab, specify the location of the Microsoft.SharePoint.dll file, and then click **OK**. This will copy the Microsoft.SharePoint.dll into the project directory so that you can use SharePoint Foundation 2010 object model members in your InfoPath solution.</span></span>
  
### <a name="designing-the-form-and-developing-the-code"></a><span data-ttu-id="aad37-144">Création du formulaire et développement du code</span><span class="sxs-lookup"><span data-stu-id="aad37-144">Designing the form and developing the code</span></span>

<span data-ttu-id="aad37-p111">À partir du code dans un formulaire InfoPath, vous pouvez utiliser le modèle objet SharePoint pour créer des éléments dans des listes de recherche. Cela est utile pour le remplissage d'une zone déroulante à partir d'une liste SharePoint, si vous souhaitez ajouter de nouvelles valeurs à cette zone sans créer de formulaire distinct. Cet exemple utilise une zone de liste déroulante pour afficher toutes les valeurs actuellement dans la liste et crée la logique de programmation pour ajouter la valeur à la liste si elle n'y figure pas encore.</span><span class="sxs-lookup"><span data-stu-id="aad37-p111">From code in an InfoPath form, you can use the SharePoint object model to create items in lookup lists. This is useful when you populate a drop-down box from a SharePoint list and want to add new values to it without creating a separate form. This example uses a combo box to show all the values currently in the list and creates programming logic to add the value to the list if it does not already exist.</span></span>
  
### <a name="to-create-a-form-template-that-can-add-new-items-to-a-combo-box-based-on-a-sharepoint-list"></a><span data-ttu-id="aad37-148">Pour créer un modèle de formulaire qui puisse ajouter de nouveaux éléments à une zone de liste déroulante basée sur une liste SharePoint</span><span class="sxs-lookup"><span data-stu-id="aad37-148">To create a form template that can add new items to a combo box based on a SharePoint list</span></span>

1. <span data-ttu-id="aad37-149">Créer une liste personnalisée simple sur un serveur SharePoint Server 2010 et nommez-le MyList.</span><span class="sxs-lookup"><span data-stu-id="aad37-149">Create a simple custom list on a SharePoint Server 2010 server, and name it MyList.</span></span> <span data-ttu-id="aad37-150">L’exemple suivant utilise une **Zone de liste déroulante** lié au champ de **titre** de cette liste.</span><span class="sxs-lookup"><span data-stu-id="aad37-150">The following example uses a **Combo Box** bound to the **Title** field of this list.</span></span> 
    
2. <span data-ttu-id="aad37-151">Créer un nouveau **Formulaire vierge** dans InfoPath Designer, insérer un contrôle de **Zone de liste déroulante** sur votre formulaire et renommez le champ lié à la zone de liste déroulante myCombo.</span><span class="sxs-lookup"><span data-stu-id="aad37-151">Create a new **Blank Form** in InfoPath Designer, insert a **Combo Box** control on your form, and rename the field bound to the combo box to myCombo.</span></span>
    
3. <span data-ttu-id="aad37-152">Créer la connexion de données à la liste qui sera utilisée pour remplir la zone de liste déroulante en suivant les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="aad37-152">Create the data connection to the list that will be used to populate the combo box by using the following steps:</span></span>
    
    1. <span data-ttu-id="aad37-153">Sur l'onglet **Données**, cliquez sur le bouton **À partir de la liste SharePoint** dans le groupe **Données externes**.</span><span class="sxs-lookup"><span data-stu-id="aad37-153">On the **Data** tab, click **From SharePoint List** button in the **Get External Data** group.</span></span> 
        
    2. <span data-ttu-id="aad37-154">Entrez l'URL du site qui contient la liste, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="aad37-154">Enter the URL for the site that contains the list, and then click **Next**.</span></span>
        
    3. <span data-ttu-id="aad37-155">Sélectionnez la liste, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="aad37-155">Select the list, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="aad37-p113">Sélectionnez les champs que vous souhaitez inclure : pour cet exemple, sélectionnez Titre et ID. Titre contient les valeurs à rechercher. Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="aad37-p113">Select the fields that you want to include, for this example, select Title and ID. Title contains the values for lookup. Click **Next**.</span></span>
        
    5. <span data-ttu-id="aad37-159">Cliquez sur **Suivant** dans l'écran suivant.</span><span class="sxs-lookup"><span data-stu-id="aad37-159">Click **Next** on the following screen.</span></span> 
        
    6. <span data-ttu-id="aad37-160">Nommez la connexion de données LookupList, puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="aad37-160">Name the data connection LookupList, and then click **Finish**.</span></span>
    
4. <span data-ttu-id="aad37-161">Pour remplir la zone de liste déroulante dans la liste à l’aide de la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="aad37-161">Populate the values in the combo box from the list by using the following steps:</span></span>
    
    1. <span data-ttu-id="aad37-162">Sélectionnez la zone de liste déroulante que vous avez créée à l'étape 1.</span><span class="sxs-lookup"><span data-stu-id="aad37-162">Select the combo box that you created in step 1.</span></span>
        
    2. <span data-ttu-id="aad37-163">Cliquez sur **Modifier les choix** sur l'onglet **Propriétés Outils de contrôle** du ruban.</span><span class="sxs-lookup"><span data-stu-id="aad37-163">Click **Edit Choices** on the **Control Tools Properties** tab of the ribbon.</span></span> 
        
    3. <span data-ttu-id="aad37-164">Sélectionnez **Rechercher des choix dans une source de données externe**.</span><span class="sxs-lookup"><span data-stu-id="aad37-164">Select **Get choices from an external data source**.</span></span>
        
    4. <span data-ttu-id="aad37-165">Vérifiez que la **Source de données** est définie sur la connexion que vous avez créée à l'étape 2.</span><span class="sxs-lookup"><span data-stu-id="aad37-165">Make sure that **Data source** is set to the data connection that you created in step 2.</span></span> 
        
    5. <span data-ttu-id="aad37-166">Définissez la valeur et le nom complet pour Titre.</span><span class="sxs-lookup"><span data-stu-id="aad37-166">Set the value and display name to Title.</span></span>
        
    6. <span data-ttu-id="aad37-167">Sous l’onglet **formulaires du navigateur** , sélectionnez **toujours** sous **paramètres de publication (postback)**, puis cliquez sur **OK** pour fermer la boîte de dialogue Propriétés.</span><span class="sxs-lookup"><span data-stu-id="aad37-167">On the **Browser forms** tab, select **Always** under **Postback settings**, and then click **OK** to close the properties dialog box.</span></span> 
    
5. <span data-ttu-id="aad37-168">Assurez-vous que la zone de liste modifiable est toujours sélectionnée, puis cliquez sur **Événement de modification de** l’onglet **développeur** du ruban.</span><span class="sxs-lookup"><span data-stu-id="aad37-168">Make sure the combo box is still selected, and then click **Changed Event** on the **Developer** tab of the ribbon.</span></span> 
    
    <span data-ttu-id="aad37-169">Si vous n'avez pas encore enregistré votre formulaire, vous êtes invité à le faire.</span><span class="sxs-lookup"><span data-stu-id="aad37-169">If your form is not saved yet, you are prompted to save it.</span></span> <span data-ttu-id="aad37-170">Puis, la fenêtre de l’éditeur de code ouvre le curseur dans le `myCombo_Changed` Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="aad37-170">And then, the code editor window opens with the cursor in the  `myCombo_Changed` event handler.</span></span> 
    
6. <span data-ttu-id="aad37-171">Ajoutez une référence à l'assembly Microsoft.SharePoint.dll comme décrit plus haut dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="aad37-171">Add a reference to the Microsoft.SharePoint.dll assembly as described earlier in this topic.</span></span> <span data-ttu-id="aad37-172">Pour plus d’informations sur la référence à l’assembly Microsoft.SharePoint, voir [Membres du modèle objet utiliser SharePoint](how-to-use-sharepoint-object-model-members.md).</span><span class="sxs-lookup"><span data-stu-id="aad37-172">For more information about referencing the Microsoft.SharePoint assembly, see [Use SharePoint Object Model Members](how-to-use-sharepoint-object-model-members.md).</span></span>
    
7. <span data-ttu-id="aad37-173">Collez le code suivant dans le `myCombo_Changed` Gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="aad37-173">Paste the following code into the  `myCombo_Changed` event handler.</span></span> 
    
   ```cs
    // Use InfoPath OM's ServerInfo.SharePointSiteUrl property to programmatically
    // specify the site where the form is published.
    using (SPSite FormSite = new SPSite(ServerInfo.SharePointSiteUrl.ToString()))
    {
        using (SPWeb FormWeb = FormSite.OpenWeb())
        {
            // Get the SharePoint list.
            SPList LookupList = FormWeb.Lists["MyList"];
            // Query for the item.
            SPQuery MyQuery = new SPQuery();
            // "Title" is the field (column) to search in the SharePoint list.
            // /my:myFields/my:myCombo is the xpath to the field bound to the Combo Box in the form.
            MyQuery.Query = "<Where><Eq><FieldRef Name='Title' /><Value Type='Text'>" + 
                GetDomValue("/my:myFields/my:myCombo") + "</Value></Eq></Where>";
            SPListItemCollection ReturnedItems = LookupList.GetItems(MyQuery);
            // Add the item to the SharePoint list if no items were returned in the query.
            if (ReturnedItems.Count == 0)
            {
                SPListItem NewItem = LookupList.Items.Add();
                // Set the value of the Title field in the list to the value in Combo Box on the form.
                NewItem["Title"] = GetDomValue("/my:myFields/my:myCombo");
                // Set AllowUnsafeUpdates to 'true' to temporarily allow updates to the database.
                FormWeb.AllowUnsafeUpdates = true;
                NewItem.Update();
                // Set AllowUnsafeUpdates back to 'false' to prevent further updates to the database.
                FormWeb.AllowUnsafeUpdates = false;
            }
        }
    }
   ```

   ```vb
    ' Use InfoPath OM's ServerInfo.SharePointSiteUrl property to specify the site where the form is published.
    Using FormSite As New SPSite(ServerInfo.SharePointSiteUrl.ToString())
        Using FormWeb As SPWeb = FormSite.OpenWeb()
            ' Get the SharePoint list.
            Dim LookupList As SPList = FormWeb.Lists("MyList")
            ' Query for the item.
            Dim MyQuery As New SPQuery()
            ' "Title" is the field (column) to search in the SharePoint list.
            ' my:myFields/my:myCombo is the xpath to the field bound to the Combo Box in the form.
            MyQuery.Query = "<Where><Eq><FieldRef Name='Title' /><Value Type='Text'>" &amp; _
                GetDomValue("/my:myFields/my:myCombo") &amp; "</Value></Eq></Where>"
            Dim ReturnedItems As SPListItemCollection = LookupList.GetItems(MyQuery)
            ' Add the item to the lookup list if no items were returned in the query.
            If ReturnedItems.Count = 0 Then
                Dim NewItem As SPListItem = LookupList.Items.Add()
                ' Set the value of the Title field in the list to the value in Combo Box on the form.
                NewItem("Title") = GetDomValue("/my:myFields/my:myCombo")
                ' Set AllowUnsafeUpdates to 'true' to temporarily allow updates to the database.
                FormWeb.AllowUnsafeUpdates = True
                NewItem.Update()
                ' Set AllowUnsafeUpdates back to 'false' to prevent further updates to the database.
                FormWeb.AllowUnsafeUpdates = False
            End If
        End Using
    End Using
   ```

8. <span data-ttu-id="aad37-174">L’exemple de code précédent dépend du `GetDomValue` fonction d’assistance.</span><span class="sxs-lookup"><span data-stu-id="aad37-174">The preceding code example depends on the  `GetDomValue` helper function.</span></span> <span data-ttu-id="aad37-175">Collez le code suivant pour le `GetDomValue` fonction d’assistance ci-dessous les `myCombo_Changed` fonction de gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="aad37-175">Paste the following code for the  `GetDomValue` helper function below the  `myCombo_Changed` event handler function.</span></span> 
    
   ```cs
    private string GetDomValue(string XpathToGet)
    {
        return this.CreateNavigator().SelectSingleNode(XpathToGet, this.NamespaceManager).Value;
    }
   ```

   ```vb
    Private Function GetDomValue(XpathToGet As String) As String
        Return Me.CreateNavigator().SelectSingleNode(XpathToGet, Me.NamespaceManager).Value
    End Function
   ```

9. <span data-ttu-id="aad37-176">Publier votre formulaire à l’aide de la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="aad37-176">Publish your form by using the following steps:</span></span>
    
    1. <span data-ttu-id="aad37-177">Cliquez sur **SharePoint Server** sur l'onglet **Publier** dans Backstage.</span><span class="sxs-lookup"><span data-stu-id="aad37-177">Click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
        
    2. <span data-ttu-id="aad37-178">Entrez l'URL du site SharePoint sur lequel publier, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="aad37-178">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
        
       > [!IMPORTANT]
       > <span data-ttu-id="aad37-179">Vous devez être administrateur de collection de sites sur ce site pour publier ce modèle de formulaire en tant que solution bac à sable.</span><span class="sxs-lookup"><span data-stu-id="aad37-179">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
    
    3. <span data-ttu-id="aad37-180">Sélectionnez **Bibliothèque de formulaires**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="aad37-180">Select **Form Library**, and then click **Next**.</span></span>
        
    4. <span data-ttu-id="aad37-181">Sélectionnez **Créer une bibliothèque de formulaires**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="aad37-181">Select **Create a new form library**, and then click **Next**.</span></span>
        
    5. <span data-ttu-id="aad37-182">Entrez le nom et la description de votre bibliothèque de formulaires, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="aad37-182">Enter the name and description for your form library, and then click **Next**.</span></span>
        
    6. <span data-ttu-id="aad37-183">Cliquez sur **Publier**.</span><span class="sxs-lookup"><span data-stu-id="aad37-183">Click **Publish**.</span></span>
        
    7. <span data-ttu-id="aad37-184">Une fois que le formulaire est correctement publié, ouvrez le formulaire à partir de la bibliothèque de formulaires et ajouter une nouvelle valeur dans la zone de liste déroulante pour tester le code.</span><span class="sxs-lookup"><span data-stu-id="aad37-184">After the form is successfully published, open the form from the form library and add a new value into the combo box to test the code.</span></span> <span data-ttu-id="aad37-185">Lorsque vous quittez le champ myCombo, la nouvelle valeur est écrit à la liste SharePoint.</span><span class="sxs-lookup"><span data-stu-id="aad37-185">When you exit the myCombo field, the new value will be written to the SharePoint list.</span></span> 
    

