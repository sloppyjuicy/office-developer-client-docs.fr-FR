---
title: Exemples de solutions bac à sable (sandbox)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 415fa0fa-b7b7-4acb-a437-f54c34064004
description: Cette rubrique fournit deux exemples qui montrent le type de code que vous pouvez écrire dans un modèle de formulaire solution bac à sable InfoPath et comment publier ce modèle.
ms.openlocfilehash: 9bce60d1141b82343ab021b120ae804d404d6b13
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557420"
---
# <a name="sample-sandboxed-solutions"></a>Exemples de solutions bac à sable (sandbox)

Les formulaires InfoPath avec code managé peuvent être publiés sur l'infrastructure solution bac à sable SharePoint à partir du concepteur InfoPath. Cette rubrique fournit deux exemples qui montrent le type de code que vous pouvez écrire dans un modèle de formulaire solution bac à sable InfoPath et comment publier ce modèle.
  
## <a name="example-1-sorting-data-in-an-order-form"></a>Exemple 1 : tri des données dans un formulaire d’ordre

Une tâche utile, comme trier les données dans un tableau extensible, peut être effectuée à l'aide de code dans un formulaire InfoPath. Pour ce faire, le code réordonne les nœuds dans un document XML sous-jacent qui est affiché dans le formulaire InfoPath. Bien que le scénario décrit dans cette rubrique est conçu pour publier directement un formulaire InfoPath en tant que solution bac à sable, celui-ci peut également être déployé comme un modèle de formulaire approuvé par l'administrateur.
  
Avant de commencer, vérifiez que vous remplissez les conditions suivantes.
  
- Vous êtes administrateur de collection de sites sur le site SharePoint Server 2010 ou SharePoint Foundation 2010 sur lequel vous souhaitez publier le formulaire.
    
- Vérifiez auprès de l’administrateur de la batterie de serveurs que le service de code en bac à sable Microsoft SharePoint Foundation est en cours d’exécution sur le serveur. Pour plus d’informations, voir [Publication de formulaires avec code.](publishing-forms-with-code.md)
    
- Le langage de programmation que vous avez choisi pour le modèle de formulaire est **C#** ou **Visual Basic**, non suivi d'un nom de version antérieure. Les versions des langages de programmation et des modèles objet compatibles InfoPath 2007 ou InfoPath 2003 ne sont pas prises en charge pour solutions bac à sable. Pour plus d’informations sur la spécification du langage de programmation, voir [Développer avec Visual Studio](how-to-develop-with-visual-studio.md).
    
Pour créer un modèle de formulaire qui trie les données dans un contrôle **Tableau extensible** sur le formulaire, procédez comme suit. 
  
### <a name="to-create-a-form-template-that-programmatically-sorts-data-in-the-form"></a>Pour créer un modèle de formulaire qui trie les données dans le formulaire par programmation

1. Créez un modèle de formulaire dans le concepteur InfoPath, puis ajoutez un contrôle **Tableau extensible** sur ce formulaire. Le code de cet exemple trie les lignes en fonction de la première colonne du tableau, mais vous pouvez facilement le modifier afin d'utiliser une autre colonne. 
    
2. Ajoutez un contrôle **Bouton** au formulaire. Le code pour trier le tableau sera ajouté au gestionnaire d'événements pour l'événement **Clicked** du bouton, mais vous pouvez également utiliser un autre événement à cet effet. 
    
3. Sélectionnez le bouton, cliquez sur l'onglet **Propriétés**, puis cliquez sur **Code personnalisé**. Si vous n'avez pas encore enregistré votre formulaire, vous êtes invité à le faire, puis l'éditeur de code s'ouvre avec le curseur positionné sur le gestionnaire d'événements du bouton.
    
4. Collez le code suivant dans le gestionnaire d'événements du bouton. Ce code place les éléments de la première colonne dans un tableau, trie ce tableau, puis réorganise le tableau initial en se basant sur ce dernier. Ce code suppose que les données triées sont de type chaîne.
    
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

5. Publiez votre formulaire en suivant les étapes suivantes :
    
    1. Cliquez sur **SharePoint Server** sur l'onglet **Publier** dans Backstage. 
        
    2. Entrez l'URL du site SharePoint sur lequel publier, puis cliquez sur **Suivant**. 
        
       > [!IMPORTANT]
       > [!IMPORTANTE] Vous devez être administrateur de collection de sites sur ce site pour publier ce modèle de formulaire en tant que solution bac à sable. 
    
    3. Sélectionnez **Bibliothèque de formulaires**, puis cliquez sur **Suivant**.
        
    4. Sélectionnez **Créer une bibliothèque de formulaires**, puis cliquez sur **Suivant**.
        
    5. Entrez le nom et la description de votre bibliothèque de formulaires, puis cliquez sur **Suivant**.
        
    6. Cliquez sur **Publier**.
    
## <a name="example-2-managing-vendors-in-a-sharepoint-list"></a>Exemple 2 : Gestion des fournisseurs dans une SharePoint liste

Cet exemple comprend de la programmation par rapport au modèle objet Microsoft SharePoint Foundation 2010. Pour cela, vous devez établir une référence à l'assembly Microsoft.SharePoint.dll qui est installé avec une copie sous licence de SharePoint Server 2010.
  
La bibliothèque Microsoft.SharePoint.Server.dll est installée par défaut dans C:\Program Files\Common Files\Microsoft Shared\Web Server Extensions\14\ISAPI. Elle doit être incluse dans les projets où vous programmez en fonction du modèle objet SharePoint. Pour établir une référence à Microsoft.SharePoint.dll dans un projet Visual Studio 2012, ouvrez l' **Éditeur de code**, puis cliquez sur **Ajouter une référence** dans le menu **Outils**. Dans la boîte de dialogue **Ajouter une référence**, cliquez sur l'onglet **Parcourir**, spécifiez l'emplacement du fichier Microsoft.SharePoint.dll, puis cliquez sur **OK**. Cela copie Microsoft.SharePoint.dll dans le répertoire du projet afin que vous puissiez utiliser les membres du modèle objet SharePoint Foundation 2010 dans votre solution InfoPath.
  
### <a name="designing-the-form-and-developing-the-code"></a>Conception du formulaire et développement du code

À partir du code dans un formulaire InfoPath, vous pouvez utiliser le modèle objet SharePoint pour créer des éléments dans des listes de recherche. Cela est utile pour le remplissage d'une zone déroulante à partir d'une liste SharePoint, si vous souhaitez ajouter de nouvelles valeurs à cette zone sans créer de formulaire distinct. Cet exemple utilise une zone de liste déroulante pour afficher toutes les valeurs actuellement dans la liste et crée la logique de programmation pour ajouter la valeur à la liste si elle n'y figure pas encore.
  
### <a name="to-create-a-form-template-that-can-add-new-items-to-a-combo-box-based-on-a-sharepoint-list"></a>Pour créer un modèle de formulaire qui puisse ajouter de nouveaux éléments à une zone de liste déroulante basée sur une liste SharePoint

1. Créez une liste personnalisée simple sur un serveur SharePoint Server 2010 et nommez-la MyList. L’exemple suivant utilise une zone de liste **déroulante** liée au **champ Titre** de cette liste. 
    
2. Créez un **formulaire** vierge dans le Concepteur InfoPath, insérez un contrôle **Zone** de liste déroulante sur votre formulaire et renommez le champ lié à la zone de liste déroulante myCombo.
    
3. Créez la connexion de données à la liste qui sera utilisée pour remplir la zone de liste déroulante en suivant les étapes suivantes :
    
    1. Sur l'onglet **Données**, cliquez sur le bouton **À partir de la liste SharePoint** dans le groupe **Données externes**. 
        
    2. Entrez l'URL du site qui contient la liste, puis cliquez sur **Suivant**.
        
    3. Sélectionnez la liste, puis cliquez sur **Suivant**.
        
    4. Sélectionnez les champs que vous souhaitez inclure : pour cet exemple, sélectionnez Titre et ID. Titre contient les valeurs à rechercher. Cliquez sur **Suivant**.
        
    5. Cliquez sur **Suivant** dans l'écran suivant. 
        
    6. Nommez la connexion de données LookupList, puis cliquez sur **Terminer**.
    
4. Pour remplir les valeurs de la zone de liste déroulante à partir de la liste, utilisez les étapes suivantes :
    
    1. Sélectionnez la zone de liste déroulante que vous avez créée à l'étape 1.
        
    2. Cliquez sur **Modifier les choix** sur l'onglet **Propriétés Outils de contrôle** du ruban. 
        
    3. Sélectionnez **Rechercher des choix dans une source de données externe**.
        
    4. Vérifiez que la **Source de données** est définie sur la connexion que vous avez créée à l'étape 2. 
        
    5. Définissez la valeur et le nom complet pour Titre.
        
    6. Sous **l’onglet Formulaires** du navigateur, sélectionnez **Toujours** sous **Paramètres** de publication, puis cliquez sur **OK** pour fermer la boîte de dialogue des propriétés. 
    
5. Assurez-vous que la zone de liste déroulante est toujours sélectionnée, puis cliquez sur **Événement modifié** sous l’onglet Développeur du ruban.  
    
    Si vous n'avez pas encore enregistré votre formulaire, vous êtes invité à le faire. Ensuite, la fenêtre de l’éditeur de code s’ouvre avec le curseur dans le  `myCombo_Changed` handler d’événements. 
    
6. Ajoutez une référence à l'assembly Microsoft.SharePoint.dll comme décrit plus haut dans cette rubrique. Pour plus d’informations sur le référencement de Microsoft. SharePoint assembly, voir [Use SharePoint Object Model Members](how-to-use-sharepoint-object-model-members.md).
    
7. Collez le code suivant dans le  `myCombo_Changed` handler d’événements. 
    
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

8. L’exemple de code précédent dépend de la  `GetDomValue` fonction d’aide. Collez le code suivant pour la  `GetDomValue` fonction d’aide sous la  `myCombo_Changed` fonction de handler d’événements. 
    
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

9. Publiez votre formulaire en suivant les étapes suivantes :
    
    1. Cliquez sur **SharePoint Server** sur l'onglet **Publier** dans Backstage. 
        
    2. Entrez l'URL du site SharePoint sur lequel publier, puis cliquez sur **Suivant**. 
        
       > [!IMPORTANT]
       > [!IMPORTANTE] Vous devez être administrateur de collection de sites sur ce site pour publier ce modèle de formulaire en tant que solution bac à sable. 
    
    3. Sélectionnez **Bibliothèque de formulaires**, puis cliquez sur **Suivant**.
        
    4. Sélectionnez **Créer une bibliothèque de formulaires**, puis cliquez sur **Suivant**.
        
    5. Entrez le nom et la description de votre bibliothèque de formulaires, puis cliquez sur **Suivant**.
        
    6. Cliquez sur **Publier**.
        
    7. Une fois le formulaire publié, ouvrez-le à partir de la bibliothèque de formulaires et ajoutez une nouvelle valeur dans la zone de liste déroulante pour tester le code. Lorsque vous quittez le champ myCombo, la nouvelle valeur est écrite dans la SharePoint liste. 
    

