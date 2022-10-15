---
title: Obtention de l’adresse e-mail du destinataire
TOCTitle: Get the email address of a recipient
ms:assetid: e585811b-a298-496f-ba79-df7d46526169
ms:mtpsurl: https://learn.microsoft.com/office/client-developer/outlook/pia/how-to-get-the-e-mail-address-of-a-recipient?redirectedfrom=MSDN
ms:contentKeyID: 55119879
ms.date: 12/03/2019
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2e3824969d13fa9cfacd8ea475bcd43f75657468
ms.sourcegitcommit: b6d8fc4db483ecd1a3247a6cb3377f5b52c44cfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2022
ms.locfileid: "68574349"
---
# <a name="get-the-email-address-of-a-recipient"></a>Obtention de l’adresse e-mail du destinataire

Cet exemple montre comment obtenir l’adresse SMTP d’un destinataire.

## <a name="example"></a>Exemple

Dans l’exemple de code suivant, la méthode GetSMTPAddressForRecipients prend un objet [MailItem](/dotnet/api/microsoft.office.interop.outlook.mailitem) comme argument d’entrée, puis affiche l’adresse SMTP de chaque destinataire de cet élément de courrier. La méthode récupère d’abord la collection [Recipients](/dotnet/api/microsoft.office.interop.outlook.recipients) qui représente l’ensemble des destinataires indiqués pour l’élément de courrier électronique. Pour chaque [destinataire](/dotnet/api/microsoft.office.interop.outlook.recipient) de cette collection **Recipients** , la méthode obtient ensuite l’objet [PropertyAccessor](/dotnet/api/microsoft.office.interop.outlook.propertyaccessor)) qui correspond à cet objet **Recipient** . Enfin, la méthode utilise la propriété [PropertyAccessor](/dotnet/api/microsoft.office.interop.outlook.recipient.propertyaccessor) pour obtenir la valeur de la propriété MAPI `https://schemas.microsoft.com/mapi/proptag/0x39FE001E`, laquelle est mappée à la propriété **PR\_SMTP\_ADDRESS**([PidTagSmtpAddress](/office/client-developer/outlook/mapi/pidtagsmtpaddress-canonical-property?redirectedfrom=MSDN)) du destinataire.

If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace. The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration. The following line of code shows how to do the import and assignment in C\#.

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

## <a name="see-also"></a>Voir aussi

- [Destinataires](recipients.md)
