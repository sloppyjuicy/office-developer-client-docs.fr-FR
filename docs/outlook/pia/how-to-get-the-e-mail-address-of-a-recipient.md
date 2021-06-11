---
title: Obtention de l’adresse e-mail du destinataire
TOCTitle: Get the email address of a recipient
ms:assetid: e585811b-a298-496f-ba79-df7d46526169
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-get-the-e-mail-address-of-a-recipient?redirectedfrom=MSDN
ms:contentKeyID: 55119879
ms.date: 12/03/2019
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8957cbc92414b0cdac442167a5c9ea025ce318cb
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819335"
---
# <a name="get-the-email-address-of-a-recipient"></a><span data-ttu-id="dc9c6-102">Obtention de l’adresse e-mail du destinataire</span><span class="sxs-lookup"><span data-stu-id="dc9c6-102">Get the email address of a recipient</span></span>

<span data-ttu-id="dc9c6-103">Cet exemple montre comment obtenir l’adresse SMTP d’un destinataire.</span><span class="sxs-lookup"><span data-stu-id="dc9c6-103">This example shows how to get the Simple Mail Transfer Protocol (SMTP) address of a recipient.</span></span>

## <a name="example"></a><span data-ttu-id="dc9c6-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="dc9c6-104">Example</span></span>

<span data-ttu-id="dc9c6-105">Dans l’exemple de code suivant, la méthode GetSMTPAddressForRecipients prend un objet [MailItem](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.mailitem?redirectedfrom=MSDN&view=outlook-pia) comme argument d’entrée, puis affiche l’adresse SMTP de chaque destinataire de cet élément de courrier.</span><span class="sxs-lookup"><span data-stu-id="dc9c6-105">In the following the code example, the GetSMTPAddressForRecipients method takes a [MailItem](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.mailitem?redirectedfrom=MSDN&view=outlook-pia) object as an input argument and then displays the SMTP address of each recipient for that mail item.</span></span> <span data-ttu-id="dc9c6-106">La méthode récupère d’abord la collection [Recipients](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipients?redirectedfrom=MSDN&view=outlook-pia) qui représente l’ensemble des destinataires indiqués pour l’élément de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="dc9c6-106">The method first retrieves the [Recipients](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipients?redirectedfrom=MSDN&view=outlook-pia) collection that represents the set of recipients specified for the mail item.</span></span> <span data-ttu-id="dc9c6-107">Pour chaque [destinataire](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipient?redirectedfrom=MSDN&view=outlook-pia) de cette collection **Recipients,** la méthode obtient ensuite l’objet [PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia)) qui correspond à cet **objet Recipient.**</span><span class="sxs-lookup"><span data-stu-id="dc9c6-107">For each [Recipient](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipient?redirectedfrom=MSDN&view=outlook-pia) in that **Recipients** collection, the method then obtains the [PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia)) object that corresponds to that **Recipient** object.</span></span> <span data-ttu-id="dc9c6-108">Enfin, la méthode utilise la propriété [PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipient.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_Recipient_PropertyAccessor) pour obtenir la valeur de la propriété MAPI , qui est mie à la propriété https://schemas.microsoft.com/mapi/proptag/0x39FE001E **PR \_ SMTP \_ ADDRESS**   ([PidTagSmtpAddress](https://docs.microsoft.com/office/client-developer/outlook/mapi/pidtagsmtpaddress-canonical-property?redirectedfrom=MSDN)) du destinataire.</span><span class="sxs-lookup"><span data-stu-id="dc9c6-108">Finally, the method uses the [PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipient.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_Recipient_PropertyAccessor) property to get the value of the MAPI property https://schemas.microsoft.com/mapi/proptag/0x39FE001E, which maps to the **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://docs.microsoft.com/office/client-developer/outlook/mapi/pidtagsmtpaddress-canonical-property?redirectedfrom=MSDN)) property of the recipient.</span></span>

<span data-ttu-id="dc9c6-109">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="dc9c6-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="dc9c6-110">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="dc9c6-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="dc9c6-111">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="dc9c6-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetSMTPAddressForRecipients(Outlook.MailItem mail)
{
    const string PR_SMTP_ADDRESS =
        "http://schemas.microsoft.com/mapi/proptag/0x39FE001E";
    Outlook.Recipients recips = mail.Recipients;
    foreach (Outlook.Recipient recip in recips)
    {
        Outlook.PropertyAccessor pa = recip.PropertyAccessor;
        string smtpAddress =
            pa.GetProperty(PR_SMTP_ADDRESS).ToString();
        Debug.WriteLine(recip.Name + " SMTP=" + smtpAddress);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="dc9c6-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc9c6-112">See also</span></span>

- [<span data-ttu-id="dc9c6-113">Destinataires</span><span class="sxs-lookup"><span data-stu-id="dc9c6-113">Recipients</span></span>](recipients.md)

