---
title: Ajout ou suppression d’une banque
TOCTitle: Add or remove a store
ms:assetid: db2930ec-ef99-4e31-86c5-820e8368e05f
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612380(v=office.15)
ms:contentKeyID: 55119895
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4346f3bf1b7bba1f26a34e1562997b4d043c8d49
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359744"
---
# <a name="add-or-remove-a-store"></a>Ajouter ou supprimer un magasin

Cet exemple montre comment ajouter et supprimer un magasin dans un profil donné.

## <a name="example"></a>Exemple

Cet exemple de code montre comment ajouter et supprimer un magasin dans un profil spécifié en appelant respectivement la méthode [AddStoreEx](https://msdn.microsoft.com/library/bb623442\(v=office.15\)) et la méthode [RemoveStore](https://msdn.microsoft.com/library/bb610524\(v=office.15\)) sur l'objet [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) .

Dans Outlook, vous pouvez ajouter ou supprimer un magasin PST uniquement par programmation. L’exemple de code suivant ajoute un magasin Unicode et place le fichier .pst dans l’emplacement par défaut des fichiers .pst utilisateur : Documents and Settings\\\<UserName\>\\Local Settings\\Application Data\\Microsoft\\Outlook. L’exemple de code utilise Environment.SpecialFolder.LocalApplicationData pour récupérer le chemin d’accès au dossier Application Data sous le dossier Local Settings. Après avoir ajouté le magasin, l’exemple de code supprime le magasin. Dans la mesure où la méthode **RemoveStore** requiert un objet [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) pour supprimer l'objet [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) , elle énumère la collection [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) pour trouver l'objet **Store** qui vient d'être ajouté en fonction de la propriété [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) de l'objet **Store**.

**RemoveStore** supprime uniquement le magasin à partir du profil actif. Il ne supprime pas le fichier .pst du système de fichiers.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub CreateUnicodePST()
    Dim path As String = Environment.GetFolderPath( _
        Environment.SpecialFolder.LocalApplicationData) _
        & "\Microsoft\Outlook\MyUnicodeStore.pst"
    Try
        Application.Session.AddStoreEx( _
            path, Outlook.OlStoreType.olStoreUnicode)
        Dim stores As Outlook.Stores = Application.Session.Stores
        For Each store As Outlook.Store In stores
            If store.FilePath = path Then
                Dim folder As Outlook.Folder = _
                    CType(store.GetRootFolder(), Outlook.Folder)
                ' Remove the store
                Application.Session.RemoveStore(folder)
            End If
        Next
    Catch ex As Exception
        Debug.WriteLine(ex.Message)
    End Try
End Sub
```


```csharp
private void CreateUnicodePST()
{
    string path = Environment.GetFolderPath(
        Environment.SpecialFolder.LocalApplicationData)
        + @"\Microsoft\Outlook\MyUnicodeStore.pst";
    try
    {
        Application.Session.AddStoreEx(
            path, Outlook.OlStoreType.olStoreUnicode);
        Outlook.Stores stores = Application.Session.Stores;
        foreach (Outlook.Store store in stores)
        {
            if (store.FilePath == path)
            {
               Outlook.Folder folder =
                    store.GetRootFolder() as Outlook.Folder;
               // Remove the store
               Application.Session.RemoveStore(folder);
            }
        }
    }
    catch (Exception ex)
    {
        Debug.WriteLine(ex.Message);
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Magasins](stores.md)

