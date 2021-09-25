---
title: Création d’un contact
TOCTitle: Create a Contact item
ms:assetid: b316294a-7f70-4e54-9375-4dc515e9fd11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184633(v=office.15)
ms:contentKeyID: 55119823
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4c47111e0bf0358ae145996fe9d9b97cd0302cf3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609109"
---
# <a name="create-a-contact-item"></a>Création d’un contact

Cet exemple montre comment créer un élément de contact et définir différentes propriétés pour le contact.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Un objet [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) Outlook possède plus de 100 propriétés intégrées comme [Department](https://msdn.microsoft.com/library/bb610564\(v=office.15\)), [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)), [OfficeLocation](https://msdn.microsoft.com/library/bb647145\(v=office.15\)) et [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)). Vous pouvez ajouter des propriétés personnalisées, si une propriété intégrée n’est pas disponible, à l’aide de la collection [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)). Une fois que vous créez un objet **ContactItem**, vous pouvez définir ses propriétés.

Dans l’exemple de code suivant, la méthode CreateContactExample crée un objet **ContactItem** et définit les propriétés communément utilisées pour cet objet. Elle appelle ensuite la méthode [ShowCheckPhoneDialog(OlContactPhoneNumber)](https://msdn.microsoft.com/library/bb646168\(v=office.15\)) sur l’objet **ContactItem**. La méthode **ShowCheckPhoneDialog** permet à l’utilisateur de résoudre un numéro de téléphone basé sur les conventions de numérotation locale.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

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

## <a name="see-also"></a>Voir aussi

- [Contacts](contacts.md)

