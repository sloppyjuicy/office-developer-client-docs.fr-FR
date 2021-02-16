---
title: Création d’un contact personnalisé
TOCTitle: Create a custom Contact item
ms:assetid: 24b2a104-a0a7-469b-9676-a07cab613f59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184596(v=office.15)
ms:contentKeyID: 55119831
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4261fffef0934e01cbfbcc7068377cc392af178c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361053"
---
# <a name="create-a-custom-contact-item"></a><span data-ttu-id="1c3ec-102">Création d’un contact personnalisé</span><span class="sxs-lookup"><span data-stu-id="1c3ec-102">Create a custom Contact item</span></span>

<span data-ttu-id="1c3ec-103">Cet exemple montre comment créer un élément de contact personnalisé et définir les propriétés prédéfinies et définies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-103">This example shows how to create a custom contact item and set both predefined and user-defined properties.</span></span>

## <a name="example"></a><span data-ttu-id="1c3ec-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="1c3ec-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="1c3ec-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="1c3ec-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="1c3ec-106">Un objet [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) représente un contact dans le dossier Contacts et comporte plus de 100 propriétés intégrées, dont [FirstName](https://msdn.microsoft.com/library/bb652965\(v=office.15\)) et [LastName](https://msdn.microsoft.com/library/bb609750\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="1c3ec-106">A [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) object represents a contact in the Contacts folder, and has more than 100 built-in properties such as [FirstName](https://msdn.microsoft.com/library/bb652965\(v=office.15\)) and [LastName](https://msdn.microsoft.com/library/bb609750\(v=office.15\)).</span></span> <span data-ttu-id="1c3ec-107">Parfois, les propriétés intégrées ne sont pas suffisantes. Il faut alors ajouter des propriétés personnalisées, en utilisant la collection [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="1c3ec-107">Sometimes, the built-in properties are not sufficient and you need to add custom properties, which you can do by using the [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) collection.</span></span>

<span data-ttu-id="1c3ec-108">Dans l’exemple de code suivant, CreateCustomItem crée un objet **ContactItem** personnalisé, le nomme « Shoe Store », et appelle la méthode [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) pour l’ajouter à un dossier nommé « Shoe Store ».</span><span class="sxs-lookup"><span data-stu-id="1c3ec-108">In the following code example, CreateCustomItem creates a custom **ContactItem** object, names it "Shoe Store", and calls the [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\)) method to add it to a folder named "Shoe Store".</span></span> <span data-ttu-id="1c3ec-109">CreateCustomItem obtient d’abord le dossier « Shoe Store » en utilisant la méthode [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="1c3ec-109">CreateCustomItem first gets the "Shoe Store" folder by using the [GetDefaultFolder(OlDefaultFolders)](https://msdn.microsoft.com/library/bb646473\(v=office.15\)) method.</span></span> <span data-ttu-id="1c3ec-110">Le dossier « Shoe Store » est un sous-dossier du dossier Contacts par défaut.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-110">The "Shoe Store" folder is a subfolder of the default Contacts folder.</span></span> <span data-ttu-id="1c3ec-111">CreateCustomItem définit ensuite les propriétés **FirstName** et **LastName**, puis crée une propriété définie par l’utilisateur (« Shoe Size ») en utilisant la collection **UserProperties**.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-111">CreateCustomItem then sets the **FirstName** and **LastName** properties, and creates a user-defined property ("Shoe Size") by using the **UserProperties** collection.</span></span>

<span data-ttu-id="1c3ec-112">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="1c3ec-113">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="1c3ec-114">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="1c3ec-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateCustomItem()
{
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Folders[
        "Shoe Store"] as Outlook.Folder;
    Outlook.ContactItem contact =
        folder.Items.Add(
        "IPM.Contact.Shoe Store") as Outlook.ContactItem;
    contact.FirstName = "Michael";
    contact.LastName = "Affronti";
    contact.UserProperties["Shoe Size"].Value = "9";
    contact.Save();
}
```

## <a name="see-also"></a><span data-ttu-id="1c3ec-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c3ec-115">See also</span></span>

- [<span data-ttu-id="1c3ec-116">Contacts</span><span class="sxs-lookup"><span data-stu-id="1c3ec-116">Contacts</span></span>](contacts.md)

