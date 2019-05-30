---
title: Obtention de l’adresse SMTP de l’expéditeur d’un élément de courrier
TOCTitle: Get the SMTP address of the sender of a mail item
ms:assetid: 86e0c0aa-1696-4415-b25f-f9c1c29d88a9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184624(v=office.15)
ms:contentKeyID: 55119869
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 05d52f24262f08a6326d464a2dc0d57d6d0510d7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542547"
---
# <a name="get-the-smtp-address-of-the-sender-of-a-mail-item"></a><span data-ttu-id="53c72-102">Obtention de l’adresse SMTP de l’expéditeur d’un élément de courrier</span><span class="sxs-lookup"><span data-stu-id="53c72-102">Get the SMTP address of the sender of a mail item</span></span>

<span data-ttu-id="53c72-103">Cet exemple obtient l’adresse SMTP (Simple Mail Transfer Protocol) de l’expéditeur d’un élément de courrier.</span><span class="sxs-lookup"><span data-stu-id="53c72-103">This example gets the sender’s Simple Mail Transfer Protocol (SMTP) address for a mail item.</span></span>

## <a name="example"></a><span data-ttu-id="53c72-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="53c72-104">Example</span></span>

<span data-ttu-id="53c72-105">Pour déterminer l’adresse SMTP pour un élément de courrier électronique reçu, utilisez la propriété [SenderEmailAddress](https://msdn.microsoft.com/library/bb622746\(v=office.15\)) de l’objet [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="53c72-105">To determine the SMTP address for a received mail item, use the [SenderEmailAddress](https://msdn.microsoft.com/library/bb622746\(v=office.15\)) property of the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object.</span></span> <span data-ttu-id="53c72-106">Cependant, si l’expéditeur est interne à votre organisation, **SenderEmailAddress** ne renvoie pas une adresse SMTP, et vous devez utiliser l’objet [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) pour renvoyer l’adresse SMTP de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="53c72-106">However, if the sender is internal to your organization, **SenderEmailAddress** does not return an SMTP address, and you must use the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object to return the sender’s SMTP address.</span></span>

<span data-ttu-id="53c72-107">Dans l’exemple de code suivant, GetSenderSMTPAddress utilise l’objet **PropertyAccessor** pour obtenir des valeurs qui ne sont pas exposées directement dans le modèle objet Outlook.</span><span class="sxs-lookup"><span data-stu-id="53c72-107">In the following code example, GetSenderSMTPAddress uses the **PropertyAccessor** object to obtain values that are not exposed directly in the Outlook object model.</span></span> <span data-ttu-id="53c72-108">GetSenderSMTPAddress prend un objet un **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="53c72-108">GetSenderSMTPAddress takes in a **MailItem**.</span></span> <span data-ttu-id="53c72-109">Si la valeur de la propriété [SenderEmailType](https://msdn.microsoft.com/library/bb624136\(v=office.15\)) de l'élément **MailItem** reçu est « EX », c'est que l'expéditeur se trouve sur un serveur Exchange dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="53c72-109">If the value of the [SenderEmailType](https://msdn.microsoft.com/library/bb624136\(v=office.15\)) property of the received **MailItem** is "EX", the sender of the message resides on an Exchange server in your organization.</span></span> <span data-ttu-id="53c72-110">GetSenderSMTPAddres utilise la propriété [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) de l’objet **MailItem** pour obtenir l’expéditeur, représenté par l’objet [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="53c72-110">GetSenderSMTPAddress uses the [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) property of the **MailItem** object to get the sender, represented by the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object.</span></span> <span data-ttu-id="53c72-111">Si l'objet **AddressEntry** représente un utilisateur Exchange, l'exemple appelle la méthode [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) pour retourner l'objet [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) de l'objet **AddressEntry**.</span><span class="sxs-lookup"><span data-stu-id="53c72-111">If the **AddressEntry** object represents an Exchange user, the example calls the [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) method to return the [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object of the **AddressEntry** object.</span></span> <span data-ttu-id="53c72-112">GetSenderSMTPAddress utilise ensuite la propriété [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) de l’objet **ExchangeUser** pour renvoyer l’adresse SMTP de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="53c72-112">GetSenderSMTPAddress then uses the [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) property of the **ExchangeUser** object to return the SMTP address of the sender.</span></span> <span data-ttu-id="53c72-113">Si l’objet **AddressEntry** pour l’expéditeur ne représente pas un objet **ExchangeUser**, la méthode [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) de l’objet **PropertyAccessor** est utilisée, avec **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) comme argument, pour renvoyer l’adresse SMTP de l’expéditeur.</span><span class="sxs-lookup"><span data-stu-id="53c72-113">If the **AddressEntry** object for the sender does not represent an **ExchangeUser** object, the [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) method of the **PropertyAccessor** object is used, with **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) as the argument, to return the sender’s SMTP address.</span></span>

<span data-ttu-id="53c72-114">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="53c72-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="53c72-115">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="53c72-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="53c72-116">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="53c72-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private string GetSenderSMTPAddress(Outlook.MailItem mail)
{
    string PR_SMTP_ADDRESS =
        @"http://schemas.microsoft.com/mapi/proptag/0x39FE001E";
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

## <a name="see-also"></a><span data-ttu-id="53c72-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53c72-117">See also</span></span>

- [<span data-ttu-id="53c72-118">Courrier</span><span class="sxs-lookup"><span data-stu-id="53c72-118">Mail</span></span>](mail.md)

