---
title: Création d’une liste de distribution
TOCTitle: Create a distribution list
ms:assetid: c1fdbf3d-9669-4721-aabf-e8a332b82e0e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184637(v=office.15)
ms:contentKeyID: 55119841
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f37338209ea468d0143dfd1063c3c57216bc13ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359653"
---
# <a name="create-a-distribution-list"></a><span data-ttu-id="9f8a9-102">Création d’une liste de distribution</span><span class="sxs-lookup"><span data-stu-id="9f8a9-102">Create a distribution list</span></span>

<span data-ttu-id="9f8a9-103">Cet exemple montre comment créer une liste de distribution et la présenter à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9f8a9-103">This example shows how to create a distribution list and display it to the user.</span></span>

## <a name="example"></a><span data-ttu-id="9f8a9-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="9f8a9-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="9f8a9-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="9f8a9-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="9f8a9-106">Dans l’exemple de code suivant, CreateDistributionList crée une liste de distribution en appelant la méthode [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) pour créer un objet [DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="9f8a9-106">In the following code example, CreateDistributionList creates a distribution list by calling the [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) method to create a [DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\)) object.</span></span> <span data-ttu-id="9f8a9-107">Il crée ensuite un objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) et appelle la méthode [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612189\(v=office.15\)) pour rechercher dans le dossier Contacts par défaut tous les contacts dont la valeur de la propriété [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) est « Top Customer » et dont la valeur de la propriété [Email1Address](https://msdn.microsoft.com/library/bb609902\(v=office.15\)) n’est pas vide.</span><span class="sxs-lookup"><span data-stu-id="9f8a9-107">Next it creates a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, and calls the [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612189\(v=office.15\)) method to find all contacts in the default Contacts folder for which the [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) property value is “Top Customer” and the [Email1Address](https://msdn.microsoft.com/library/bb609902\(v=office.15\)) property value is not empty.</span></span> <span data-ttu-id="9f8a9-108">Une fois tous les contacts identifiés, le nom **Email1Address** est ajouté sous forme de colonne dans l’objet **Table**.</span><span class="sxs-lookup"><span data-stu-id="9f8a9-108">Once all contacts are identified, the **Email1Address** name is added as a column to the **Table**.</span></span> <span data-ttu-id="9f8a9-109">CreateDistributionList crée ensuite un objet [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) en utilisant la méthode [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) de l’objet [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="9f8a9-109">CreateDistributionList then creates a [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object by using the [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) method from the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span> <span data-ttu-id="9f8a9-110">CreateDistributionList affiche enfin la liste de distribution « Top Customers » à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9f8a9-110">CreateDistributionList finally displays the “Top Customers” distribution list to the user.</span></span>

> [!NOTE] 
> <span data-ttu-id="9f8a9-111">Nous vous recommandons de transmettre un objet **Recipient** résolu en tant que paramètre à la méthode [AddMember(Recipient)](https://msdn.microsoft.com/library/bb612290(v=office.15)) de l’objet [DistListItem](https://msdn.microsoft.com/library/bb645382(v=office.15)).</span><span class="sxs-lookup"><span data-stu-id="9f8a9-111">You must pass a resolved **Recipient** object as a parameter to the [AddMember(Recipient)](https://msdn.microsoft.com/library/bb612290(v=office.15)) method of the [DistListItem](https://msdn.microsoft.com/library/bb645382(v=office.15)) object.</span></span> <span data-ttu-id="9f8a9-112">Pour résoudre un objet **Recipient**, utilisez la méthode [Resolve()](https://msdn.microsoft.com/library/bb624165(v=office.15)).</span><span class="sxs-lookup"><span data-stu-id="9f8a9-112">To resolve a **Recipient** object, use the [Resolve()](https://msdn.microsoft.com/library/bb624165(v=office.15)) method.</span></span>

<span data-ttu-id="9f8a9-113">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="9f8a9-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="9f8a9-114">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="9f8a9-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="9f8a9-115">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="9f8a9-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="9f8a9-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f8a9-116">See also</span></span>

- [<span data-ttu-id="9f8a9-117">Utilisateurs Exchange</span><span class="sxs-lookup"><span data-stu-id="9f8a9-117">Exchange users</span></span>](exchange-users.md)

