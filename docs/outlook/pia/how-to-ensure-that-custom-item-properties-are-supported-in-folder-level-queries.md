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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319088"
---
# <a name="ensure-that-custom-item-properties-are-supported-in-folder-level-queries"></a>Procédure pour vérifier la prise en charge des propriétés des éléments personnalisés dans les requêtes au niveau du dossier

Cet exemple montre comment vous assurer que lorsque vous ajoutez une propriété personnalisée à un type d'élément, vous ajoutez également la propriété au dossier afin de pouvoir effectuer une requête sur cette propriété personnalisée au niveau du dossier.

## <a name="example"></a>Exemple

Cet exemple de code illustre comment utiliser les objets [UserDefinedProperties](https://msdn.microsoft.com/library/bb643868\(v=office.15\)) et [UserDefinedProperty](https://msdn.microsoft.com/library/bb646064\(v=office.15\)) afin de vous assurer que lorsque vous ajoutez une propriété personnalisée à un type d'élément, vous ajoutez également la propriété au dossier afin de pouvoir effectuer une requête sur cette propriété personnalisée au niveau du dossier.

Lorsque vous utilisez la méthode [Add](https://msdn.microsoft.com/library/bb611522\(v=office.15\)) sur la collection [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) pour ajouter une propriété personnalisée à un élément, vous pouvez définir le paramètre *AddToFolderFields* sur **True** pour ajouter la propriété au dossier. Cependant, il se peut que la propriété personnalisée ne soit pas ajoutée au dossier souhaité en raison d'une erreur du développeur ou d'une action de l'utilisateur, par exemple en cas de suppression de la propriété personnalisée par le biais du Sélecteur de champs Outlook ou en cas de déplacement de l'élément vers un autre dossier. Dans ce cas de figure, les méthodes [Find](https://msdn.microsoft.com/library/bb646289\(v=office.15\))[Restrict](https://msdn.microsoft.com/library/bb612531\(v=office.15\)) de l'objet [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) qui utilise cette propriété personnalisée échouent. À l'aide de l'objet **UserDefinedProperties**, vous pouvez vérifier si vos propriétés personnalisées existent dans le dossier, et les ajouter si elles n'existent pas ou si elles ont été supprimées.

Pour conserver une propriété personnalisée représentée par un objet **UserDefinedProperty** dans un dossier, vous devez enregistrer la propriété personnalisée avec le même nom dans l'élément. Le stockage d'une valeur dans l'objet **UserDefinedProperty** pour le dossier n'a aucun effet. Vous devez configurer la collection **UserProperties** de l'élément de façon à accéder à l'objet [UserProperty](https://msdn.microsoft.com/library/bb623119\(v=office.15\)) que vous souhaitez définir, puis définir la valeur sur l'objet **UserProperty**. Assurez-vous d'appeler la méthode **Save** sur l'élément pour que vos modifications soient rendues persistantes.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.

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

## <a name="see-also"></a>Voir aussi

- [Dossiers](folders.md)

