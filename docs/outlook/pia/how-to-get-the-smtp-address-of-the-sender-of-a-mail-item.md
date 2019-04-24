---
title: Obtention de l’adresse SMTP de l’expéditeur d’un élément de courrier
TOCTitle: Get the SMTP address of the sender of a mail item
ms:assetid: 86e0c0aa-1696-4415-b25f-f9c1c29d88a9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184624(v=office.15)
ms:contentKeyID: 55119869
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 74adbf02180e0e993b22e35481f51d304b14e7d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320082"
---
# <a name="get-the-smtp-address-of-the-sender-of-a-mail-item"></a>Obtention de l’adresse SMTP de l’expéditeur d’un élément de courrier

Cet exemple obtient l’adresse SMTP (Simple Mail Transfer Protocol) de l’expéditeur d’un élément de courrier.

## <a name="example"></a>Exemple

Pour déterminer l’adresse SMTP pour un élément de courrier électronique reçu, utilisez la propriété [SenderEmailAddress](https://msdn.microsoft.com/library/bb622746\(v=office.15\)) de l’objet [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)). Cependant, si l’expéditeur est interne à votre organisation, **SenderEmailAddress** ne renvoie pas une adresse SMTP, et vous devez utiliser l’objet [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) pour renvoyer l’adresse SMTP de l’expéditeur.

Dans l’exemple de code suivant, GetSenderSMTPAddress utilise l’objet **PropertyAccessor** pour obtenir des valeurs qui ne sont pas exposées directement dans le modèle objet Outlook. GetSenderSMTPAddress prend un objet un **MailItem**. Si la valeur de la propriété [SenderEmailType](https://msdn.microsoft.com/library/bb624136\(v=office.15\)) de l'élément **MailItem** reçu est « EX », c'est que l'expéditeur se trouve sur un serveur Exchange dans votre organisation. GetSenderSMTPAddres utilise la propriété [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) de l’objet **MailItem** pour obtenir l’expéditeur, représenté par l’objet [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)). Si l'objet **AddressEntry** représente un utilisateur Exchange, l'exemple appelle la méthode [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) pour retourner l'objet [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) de l'objet **AddressEntry**. GetSenderSMTPAddress utilise ensuite la propriété [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) de l’objet **ExchangeUser** pour renvoyer l’adresse SMTP de l’expéditeur. Si l’objet **AddressEntry** pour l’expéditeur ne représente pas un objet **ExchangeUser**, la méthode [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) de l’objet **PropertyAccessor** est utilisée, avec **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) comme argument, pour renvoyer l’adresse SMTP de l’expéditeur.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private string GetSenderSMTPAddress(Outlook.MailItem mail)
{
    string PR_SMTP_ADDRESS =
        @"https://schemas.microsoft.com/mapi/proptag/0x39FE001E";
    if (mail == null)
    {
        throw new ArgumentNullException();
    }
    if (mail.SenderEmailType == "EX")
    {
        Outlook.AddressEntry sender =
            mail.Sender;
        if (sender != null)
        {
            //Now we have an AddressEntry representing the Sender
            if (sender.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeUserAddressEntry
                || sender.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeRemoteUserAddressEntry)
            {
                //Use the ExchangeUser object PrimarySMTPAddress
                Outlook.ExchangeUser exchUser =
                    sender.GetExchangeUser();
                if (exchUser != null)
                {
                    return exchUser.PrimarySmtpAddress;
                }
                else
                {
                    return null;
                }
            }
            else
            {
                return sender.PropertyAccessor.GetProperty(
                    PR_SMTP_ADDRESS) as string;
            }
        }
        else
        {
            return null;
        }
    }
    else
    {
        return mail.SenderEmailAddress;
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Courrier](mail.md)

