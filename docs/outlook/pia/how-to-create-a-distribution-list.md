---
title: Création d’une liste de distribution
TOCTitle: Create a distribution list
ms:assetid: c1fdbf3d-9669-4721-aabf-e8a332b82e0e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184637(v=office.15)
ms:contentKeyID: 55119841
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a83090f721d9afa9c1844f8e8aa828bec34e2d35
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623774"
---
# <a name="create-a-distribution-list"></a>Création d’une liste de distribution

Cet exemple montre comment créer une liste de distribution et la présenter à l’utilisateur.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Dans l’exemple de code suivant, CreateDistributionList crée une liste de distribution en appelant la méthode [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) pour créer un objet [DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\)). Il crée ensuite un objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) et appelle la méthode [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612189\(v=office.15\)) pour rechercher dans le dossier Contacts par défaut tous les contacts dont la valeur de la propriété [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) est « Top Customer » et dont la valeur de la propriété [Email1Address](https://msdn.microsoft.com/library/bb609902\(v=office.15\)) n’est pas vide. Une fois tous les contacts identifiés, le nom **Email1Address** est ajouté sous forme de colonne dans l’objet **Table**. CreateDistributionList crée ensuite un objet [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) en utilisant la méthode [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) de l’objet [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)). CreateDistributionList affiche enfin la liste de distribution « Top Customers » à l’utilisateur.

> [!NOTE] 
> Nous vous recommandons de transmettre un objet **Recipient** résolu en tant que paramètre à la méthode [AddMember(Recipient)](https://msdn.microsoft.com/library/bb612290(v=office.15)) de l’objet [DistListItem](https://msdn.microsoft.com/library/bb645382(v=office.15)). Pour résoudre un objet **Recipient**, utilisez la méthode [Resolve()](https://msdn.microsoft.com/library/bb624165(v=office.15)).

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateDistributionList()
{
    Outlook.DistListItem distList = Application.CreateItem(
        Outlook.OlItemType.olDistributionListItem)
        as Outlook.DistListItem;
    distList.Subject = "Top Customers";
    //Find top customer category in Contacts folder
    string filter = "[Categories] = 'Top Customer'"
        + " AND [Email1Address] <> ''";
    Outlook.Table table =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderContacts).
        GetTable(filter, Outlook.OlTableContents.olUserItems);
    table.Columns.Add("Email1Address");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Outlook.Recipient recip =
            Application.Session.CreateRecipient(
            nextRow["Email1Address"].ToString());
        //Resolve the Recipient before calling AddMember
        recip.Resolve();
        distList.AddMember(recip);
    }
    distList.Display(false);
}
```

## <a name="see-also"></a>Voir aussi

- [Utilisateurs Exchange](exchange-users.md)

