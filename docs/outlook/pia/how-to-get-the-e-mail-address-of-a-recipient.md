---
title: Obtention de l’adresse e-mail du destinataire
TOCTitle: Get the email address of a recipient
ms:assetid: e585811b-a298-496f-ba79-df7d46526169
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-get-the-e-mail-address-of-a-recipient?redirectedfrom=MSDN
ms:contentKeyID: 55119879
ms.date: 12/03/2019
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5ea54fcf21eaae78b65a83cc661ef27fec62eea5
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894060"
---
# <a name="get-the-email-address-of-a-recipient"></a>Obtention de l’adresse e-mail du destinataire

Cet exemple montre comment obtenir l’adresse SMTP d’un destinataire.

## <a name="example"></a>Exemple

Dans l’exemple de code suivant, la méthode GetSMTPAddressForRecipients prend un objet [MailItem](/dotnet/api/microsoft.office.interop.outlook.mailitem) comme argument d’entrée, puis affiche l’adresse SMTP de chaque destinataire de cet élément de courrier. La méthode récupère d’abord la collection [Recipients](/dotnet/api/microsoft.office.interop.outlook.recipients) qui représente l’ensemble des destinataires indiqués pour l’élément de courrier électronique. Pour chaque [destinataire](/dotnet/api/microsoft.office.interop.outlook.recipient) de cette collection **Recipients** , la méthode obtient ensuite l’objet [PropertyAccessor](/dotnet/api/microsoft.office.interop.outlook.propertyaccessor)) qui correspond à cet objet **Recipient** . Enfin, la méthode utilise la propriété [PropertyAccessor](/dotnet/api/microsoft.office.interop.outlook.recipient.propertyaccessor) pour obtenir la valeur de la propriété MAPI https://schemas.microsoft.com/mapi/proptag/0x39FE001E, laquelle est mappée à la propriété **PR\_SMTP\_ADDRESS**([PidTagSmtpAddress](/office/client-developer/outlook/mapi/pidtagsmtpaddress-canonical-property?redirectedfrom=MSDN)) du destinataire.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d'objets Microsoft Outlook 15.0 et spécifier la variable Outlook lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration Class publique. La ligne de code suivante montre comment effectuer l’importation et l’affectation dans C \#.

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

