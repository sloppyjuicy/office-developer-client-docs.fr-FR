---
title: Création d’un contact
TOCTitle: Create a Contact item
ms:assetid: b316294a-7f70-4e54-9375-4dc515e9fd11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184633(v=office.15)
ms:contentKeyID: 55119823
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 814885b209020fb37c84df2e88f04bb32ec5cd6c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407127"
---
# <a name="create-a-contact-item"></a><span data-ttu-id="8de9d-102">Création d’un contact</span><span class="sxs-lookup"><span data-stu-id="8de9d-102">Create a Contact item</span></span>

<span data-ttu-id="8de9d-103">Cet exemple montre comment créer un élément de contact et définir différentes propriétés pour le contact.</span><span class="sxs-lookup"><span data-stu-id="8de9d-103">This example shows how to create a contact item and set various properties for the contact.</span></span>

## <a name="example"></a><span data-ttu-id="8de9d-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="8de9d-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="8de9d-105">L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="8de9d-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="8de9d-106">Un objet [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) Outlook possède plus de 100 propriétés intégrées comme [Department](https://msdn.microsoft.com/library/bb610564\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)), [OfficeLocation](https://msdn.microsoft.com/library/bb647145\(v=office.15\)) et [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="8de9d-106">A Microsoft Outlook [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) object has more than 100 built-in properties such as [Department](https://msdn.microsoft.com/library/bb610564\(v=office.15\)) , [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)) , [OfficeLocation](https://msdn.microsoft.com/library/bb647145\(v=office.15\)) , and [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)) .</span></span> <span data-ttu-id="8de9d-107">Vous pouvez ajouter des propriétés personnalisées, si une propriété intégrée n’est pas disponible, à l’aide de la collection [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="8de9d-107">You can add custom properties, if a built-in property is not available, by using the [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) collection.</span></span> <span data-ttu-id="8de9d-108">Une fois que vous créez un objet **ContactItem**, vous pouvez définir ses propriétés.</span><span class="sxs-lookup"><span data-stu-id="8de9d-108">Once you create a **ContactItem**, you can set its properties.</span></span>

<span data-ttu-id="8de9d-109">Dans l’exemple de code suivant, la méthode CreateContactExample crée un objet **ContactItem** et définit les propriétés communément utilisées pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="8de9d-109">In the following code example,   creates a ContactItem and sets commonly used properties for that object.</span></span> <span data-ttu-id="8de9d-110">Elle appelle ensuite la méthode [ShowCheckPhoneDialog(OlContactPhoneNumber)](https://msdn.microsoft.com/library/bb646168\(v=office.15\)) sur l’objet **ContactItem**.</span><span class="sxs-lookup"><span data-stu-id="8de9d-110">It then calls the [ShowCheckPhoneDialog(OlContactPhoneNumber)](https://msdn.microsoft.com/library/bb646168\(v=office.15\)) method on the **ContactItem** object.</span></span> <span data-ttu-id="8de9d-111">La méthode **ShowCheckPhoneDialog** permet à l’utilisateur de résoudre un numéro de téléphone basé sur les conventions de numérotation locale.</span><span class="sxs-lookup"><span data-stu-id="8de9d-111">The **ShowCheckPhoneDialog** method allows the user to resolve a phone number based on local dialing conventions.</span></span>

<span data-ttu-id="8de9d-112">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="8de9d-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="8de9d-113">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="8de9d-113">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="8de9d-114">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="8de9d-114">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateContactExample()
{
    Outlook.ContactItem contact = Application.CreateItem(
        Outlook.OlItemType.olContactItem) as Outlook.ContactItem;
    contact.FirstName = "Mellissa";
    contact.LastName = "MacBeth";
    contact.JobTitle = "Account Representative";
    contact.CompanyName = "Contoso Ltd.";
    contact.OfficeLocation = "36/2529";
    contact.BusinessTelephoneNumber = "4255551212 x432";
    contact.WebPage = "https://www.contoso.com";
    contact.BusinessAddressStreet = "1 Microsoft Way";
    contact.BusinessAddressCity = "Redmond";
    contact.BusinessAddressState = "WA";
    contact.BusinessAddressPostalCode = "98052";
    contact.BusinessAddressCountry =
        "United States of America";
    contact.Email1Address = "melissa@contoso.com";
    contact.Email1AddressType = "SMTP";
    contact.Email1DisplayName =
        "Melissa MacBeth (mellissa@contoso.com)";
    contact.Display(false);
    contact.ShowCheckPhoneDialog(
        Outlook.OlContactPhoneNumber.
        olContactPhoneBusiness);
}
```

## <a name="see-also"></a><span data-ttu-id="8de9d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8de9d-115">See also</span></span>

- [<span data-ttu-id="8de9d-116">Contacts</span><span class="sxs-lookup"><span data-stu-id="8de9d-116">Contacts</span></span>](contacts.md)

