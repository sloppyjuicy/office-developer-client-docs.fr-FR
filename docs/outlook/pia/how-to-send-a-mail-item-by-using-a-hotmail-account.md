---
title: Envoi d’un élément de courrier électronique avec un compte Hotmail
TOCTitle: Send a mail item by using a Hotmail account
ms:assetid: f25853a7-67c0-46a3-a298-5cdf72ebc53f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184652(v=office.15)
ms:contentKeyID: 55119797
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 008f66ff1a43f90e756900c467ba6c086829b769
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331163"
---
# <a name="send-a-mail-item-by-using-a-hotmail-account"></a><span data-ttu-id="0e5c9-102">Envoi d’un élément de courrier électronique avec un compte Hotmail</span><span class="sxs-lookup"><span data-stu-id="0e5c9-102">Send a mail item by using a Hotmail account</span></span>

<span data-ttu-id="0e5c9-103">Cet exemple utilise la propriété [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) pour envoyer un message en utilisant un compte Windows Live Hotmail.</span><span class="sxs-lookup"><span data-stu-id="0e5c9-103">This example uses the [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) property to send a mail item by using a Windows Live Hotmail account.</span></span>

## <a name="example"></a><span data-ttu-id="0e5c9-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="0e5c9-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="0e5c9-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="0e5c9-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="0e5c9-106">Un profil définit un ou plusieurs comptes de messagerie et chaque compte est associé à un serveur d’un type spécifique, comme Microsoft Exchange Server ou POP3 (Post Office Protocol 3).</span><span class="sxs-lookup"><span data-stu-id="0e5c9-106">A profile defines one or more email accounts, and each email account is associated with a server of a specific type, such as Microsoft Exchange Server or Post Office Protocol 3 (POP3).</span></span> <span data-ttu-id="0e5c9-107">Dans la mesure où votre profil peut inclure plusieurs comptes, indiquez le compte à utiliser pour envoyer l’élément, puis obtenez un objet [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) pour le représenter.</span><span class="sxs-lookup"><span data-stu-id="0e5c9-107">Because you may have multiple accounts in your profile, you must specify which email account you want to use to send the item, and then obtain an [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object to represent it.</span></span>

<span data-ttu-id="0e5c9-108">Dans l’exemple de code suivant, un message est créé avec un itinéraire joint, puis il est envoyé à l’aide d’un compte Windows Live Hotmail.</span><span class="sxs-lookup"><span data-stu-id="0e5c9-108">In the following code example, a message is created with an attached itinerary and then sent by using a Windows Live Hotmail account.</span></span> <span data-ttu-id="0e5c9-109">Le compte de messagerie Hotmail est utilisé comme objet **Account** dans le profil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0e5c9-109">The Hotmail email account is used as the **Account** object in the user’s profile.</span></span> <span data-ttu-id="0e5c9-110">L’exemple de code définit ensuite la propriété SendUsingAccount sur ce compte et appelle la méthode [Send()](https://msdn.microsoft.com/library/bb644139\(v=office.15\)) à partir de l’objet [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="0e5c9-110">The code example then sets the SendUsingAccount property to that Account and calls the [Send()](https://msdn.microsoft.com/library/bb644139\(v=office.15\)) method from the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object.</span></span>

<span data-ttu-id="0e5c9-111">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="0e5c9-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="0e5c9-112">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="0e5c9-112">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="0e5c9-113">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="0e5c9-113">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void SendUsingAccountExample()
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.Subject = "Our itinerary";
    mail.Attachments.Add(@"c:\travel\itinerary.doc",
        Outlook.OlAttachmentType.olByValue,
        Type.Missing, Type.Missing);
    Outlook.Account account =
        Application.Session.Accounts["Hotmail"];
    mail.SendUsingAccount = account;
    mail.Send();
}
```

## <a name="see-also"></a><span data-ttu-id="0e5c9-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e5c9-114">See also</span></span>

- [<span data-ttu-id="0e5c9-115">Comptes</span><span class="sxs-lookup"><span data-stu-id="0e5c9-115">Accounts</span></span>](accounts.md)

