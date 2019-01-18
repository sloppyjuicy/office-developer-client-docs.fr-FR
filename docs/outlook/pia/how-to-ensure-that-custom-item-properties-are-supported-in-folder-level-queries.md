---
title: Procédure pour vérifier la prise en charge des propriétés des éléments personnalisés dans les requêtes au niveau du dossier
TOCTitle: Ensure that custom item properties are supported in folder-level queries
ms:assetid: 02cf14c6-ee1b-4e04-a865-32adaac13f9b
ms:mtpsurl: https://msdn.microsoft.com/library/Bb608929(v=office.15)
ms:contentKeyID: 55119863
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fcba2648988d2de3c208079d2845e2cb4c2f549
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722969"
---
# <a name="ensure-that-custom-item-properties-are-supported-in-folder-level-queries"></a><span data-ttu-id="6c6c7-102">Procédure pour vérifier la prise en charge des propriétés des éléments personnalisés dans les requêtes au niveau du dossier</span><span class="sxs-lookup"><span data-stu-id="6c6c7-102">Ensure that custom item properties are supported in folder-level queries</span></span>

<span data-ttu-id="6c6c7-103">Cet exemple montre comment vous assurer que lorsque vous ajoutez une propriété personnalisée à un type d'élément, vous ajoutez également la propriété au dossier afin de pouvoir effectuer une requête sur cette propriété personnalisée au niveau du dossier.</span><span class="sxs-lookup"><span data-stu-id="6c6c7-103">This example shows how to ensure that when you add a custom property to an item type, you also add the property to the folder so that you can query on that custom property at the folder level.</span></span>

## <a name="example"></a><span data-ttu-id="6c6c7-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="6c6c7-104">Example</span></span>

<span data-ttu-id="6c6c7-105">Cet exemple de code illustre comment utiliser les objets [UserDefinedProperties](https://msdn.microsoft.com/library/bb643868\(v=office.15\)) et [UserDefinedProperty](https://msdn.microsoft.com/library/bb646064\(v=office.15\)) afin de vous assurer que lorsque vous ajoutez une propriété personnalisée à un type d'élément, vous ajoutez également la propriété au dossier afin de pouvoir effectuer une requête sur cette propriété personnalisée au niveau du dossier.</span><span class="sxs-lookup"><span data-stu-id="6c6c7-105">This code sample shows how to use the [UserDefinedProperties](https://msdn.microsoft.com/library/bb643868\(v=office.15\)) object and the [UserDefinedProperty](https://msdn.microsoft.com/library/bb646064\(v=office.15\)) object to ensure that when you add a custom property to an item type, you also add the property to the folder so that you can query on that custom property at the folder level.</span></span>

<span data-ttu-id="6c6c7-106">Lorsque vous utilisez la méthode [Add](https://msdn.microsoft.com/library/bb611522\(v=office.15\)) sur la collection [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) pour ajouter une propriété personnalisée à un élément, vous pouvez définir le paramètre *AddToFolderFields* sur **True** pour ajouter la propriété au dossier.</span><span class="sxs-lookup"><span data-stu-id="6c6c7-106">When you use the [Add](https://msdn.microsoft.com/library/bb611522\(v=office.15\)) method on the [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) collection to add a custom property to an item, you can specify the *AddToFolderFields* parameter as **true** to add the property to the folder.</span></span> <span data-ttu-id="6c6c7-107">Cependant, il se peut que la propriété personnalisée ne soit pas ajoutée au dossier souhaité en raison d'une erreur du développeur ou d'une action de l'utilisateur, par exemple en cas de suppression de la propriété personnalisée par le biais du Sélecteur de champs Outlook ou en cas de déplacement de l'élément vers un autre dossier.</span><span class="sxs-lookup"><span data-stu-id="6c6c7-107">However, the custom property might not get added to the desired folderbecause of developer error or a user action, such as removing the custom property through the Outlook Field Chooser or moving the item to another folder.</span></span> <span data-ttu-id="6c6c7-108">Dans ce cas de figure, les méthodes [Find](https://msdn.microsoft.com/library/bb646289\(v=office.15\))[Restrict](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) de l'objet [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) qui utilise cette propriété personnalisée échouent.</span><span class="sxs-lookup"><span data-stu-id="6c6c7-108">Consequently, the [Find](https://msdn.microsoft.com/library/bb646289\(v=office.15\)) method and the [Restrict](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) method of the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) object that uses that custom property will fail.</span></span> <span data-ttu-id="6c6c7-109">À l'aide de l'objet **UserDefinedProperties**, vous pouvez vérifier si vos propriétés personnalisées existent dans le dossier, et les ajouter si elles n'existent pas ou si elles ont été supprimées.</span><span class="sxs-lookup"><span data-stu-id="6c6c7-109">By using the **UserDefinedProperties** object, you can test whether your custom properties exist in the folder, and add the custom properties if they do not exist or if they have been removed.</span></span>

<span data-ttu-id="6c6c7-p102">Pour conserver une propriété personnalisée représentée par un objet **UserDefinedProperty** dans un dossier, vous devez enregistrer la propriété personnalisée avec le même nom dans l'élément. Le stockage d'une valeur dans l'objet **UserDefinedProperty** pour le dossier n'a aucun effet. Vous devez configurer la collection **UserProperties** de l'élément de façon à accéder à l'objet [UserProperty](https://msdn.microsoft.com/library/bb623119\(v=office.15\)) que vous souhaitez définir, puis définir la valeur sur l'objet **UserProperty**. Assurez-vous d'appeler la méthode **Save** sur l'élément pour que vos modifications soient rendues persistantes.</span><span class="sxs-lookup"><span data-stu-id="6c6c7-p102">To persist a custom property represented by a **UserDefinedProperty** object in a folder, you must save the custom property with the same name in the item. Storing a value in the **UserDefinedProperty** object for the folder has no effect. You must se the item's **UserProperties** collection to access the [UserProperty](https://msdn.microsoft.com/library/bb623119\(v=office.15\)) object that you want to set, and then set the value on the **UserProperty** object. Be sure to call the **Save** method on the item to persist your changes.</span></span>

<span data-ttu-id="6c6c7-114">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="6c6c7-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="6c6c7-115">L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="6c6c7-115">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="6c6c7-116">Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.</span><span class="sxs-lookup"><span data-stu-id="6c6c7-116">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoUserDefinedProperty()
    Dim folder As Outlook.Folder = _
        CType(Application.ActiveExplorer().CurrentFolder(), _
        Outlook.Folder)
    Dim post As Outlook.PostItem = CType( _
        folder.Items.Add("IPM.Post"), Outlook.PostItem)
    ' Add UserProperty to PostItem
    post.UserProperties.Add("ColorID", _
        Outlook.OlUserPropertyType.olText, False)
    post.UserProperties("ColorID").Value = "Green"
    post.Subject = "UserProperty Example"
    post.Save()
    Dim findPost As Outlook.PostItem
    Try
        ' Items.Find will fail unless custom property
        ' is defined in the folder
        findPost = _
            CType(folder.Items.Find("[ColorID] = 'Green'"), _
            Outlook.PostItem)
        Catch ex As Exception
            Debug.WriteLine(ex.Message)
        End Try
        ' Add ColorID field to the folder
        folder.UserDefinedProperties.Add("ColorID", _
            Outlook.OlUserPropertyType.olText)
        ' Now the find works ok
        Dim findPostOK As Outlook.PostItem
        Try
            findPostOK = _
                CType(folder.Items.Find("[ColorID] = 'Green'"), _
                Outlook.PostItem)
            If Not (findPostOK Is Nothing) Then
                Debug.WriteLine("Found PostItem")
            End If
            ' Cleanup by deleting PostItem and ColorID
            findPostOK.Delete()
            Dim userProperty As Outlook.UserDefinedProperty = _
                folder.UserDefinedProperties("ColorID")
            userProperty.Delete()
        Catch ex As Exception
            Debug.WriteLine(ex.Message)
        End Try
End Sub
```


```csharp
private void DemoUserDefinedProperty()
{
    Outlook.Folder folder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.PostItem post = folder.Items.Add("IPM.Post")
        as Outlook.PostItem;
    // Add UserProperty to PostItem
    post.UserProperties.Add("ColorID",
        Outlook.OlUserPropertyType.olText,
        false, Type.Missing);
    post.UserProperties["ColorID"].Value = "Green";
    post.Subject = "UserProperty Example";
    post.Save();
    Outlook.PostItem findPost;
    try
    {
        // Items.Find will fail unless custom property
        // is defined in the folder
        findPost =
            folder.Items.Find("[ColorID] = 'Green'")
            as Outlook.PostItem;
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
     // Add ColorID field to the folder
    folder.UserDefinedProperties.Add("ColorID",
        Outlook.OlUserPropertyType.olText,
        Type.Missing, Type.Missing);
    // Now the find works ok
    Outlook.PostItem findPostOK;
    try
    {
        findPostOK =
            folder.Items.Find("[ColorID] = 'Green'")
            as Outlook.PostItem;
        if (findPostOK != null)
        {
            Debug.WriteLine("Found PostItem");
        }
        // Cleanup by deleting PostItem and ColorID
        findPostOK.Delete();
        Outlook.UserDefinedProperty userProperty =
            folder.UserDefinedProperties["ColorID"];
        userProperty.Delete();
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="6c6c7-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c6c7-117">See also</span></span>

- [<span data-ttu-id="6c6c7-118">Dossiers</span><span class="sxs-lookup"><span data-stu-id="6c6c7-118">Folders</span></span>](folders.md)

