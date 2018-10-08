---
title: Créer un élément à envoyer pour un compte spécifique basé sur le dossier actif
TOCTitle: Create a sendable item for a specific account based on the current folder
ms:assetid: 665ebdc5-2912-4d85-ac40-835c9ef9a439
ms:contentKeyID: 55119796
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 076677ed2eeedb269ddddc3bee201a162196db0c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405762"
---
# <a name="create-a-sendable-item-for-a-specific-account-based-on-the-current-folder"></a><span data-ttu-id="f7d29-102">Créer un élément à envoyer pour un compte spécifique basé sur le dossier actif</span><span class="sxs-lookup"><span data-stu-id="f7d29-102">Create a Sendable Item for a Specific Account Based on the Current Folder</span></span>

<span data-ttu-id="f7d29-103">Cette rubrique contient deux exemples de code montrant comment créer un élément de courrier et une demande de réunion prêts à l'envoi, puis comment les envoyer en utilisant un compte spécifique déterminé en fonction du dossier actif.</span><span class="sxs-lookup"><span data-stu-id="f7d29-103">This topic contains two code examples that show how to create a sendable e-mail item and meeting request, and then how to send them by using a specific account that is based on the current folder.</span></span>

## <a name="example"></a><span data-ttu-id="f7d29-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="f7d29-104">Example</span></span>

<span data-ttu-id="f7d29-105">Lorsque vous utilisez la méthode [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) de l'objet[Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) pour créer un élément Microsoft Outlook, cet élément est créé pour le compte principal de la session active.</span><span class="sxs-lookup"><span data-stu-id="f7d29-105">When you use the [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) method of the [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object to create a Microsoft Outlook item, the item is created for the primary account for that session.</span></span> <span data-ttu-id="f7d29-106">Dans une session pour laquelle plusieurs comptes sont définis dans le profil, vous pouvez créer un élément pour un compte IMAP, POP ou Microsoft Exchange spécifique.</span><span class="sxs-lookup"><span data-stu-id="f7d29-106">In a session where multiple accounts are defined in the profile, you can create an item for a specific IMAP, POP, or Microsoft Exchange account.</span></span> 

<span data-ttu-id="f7d29-107">Si le profil actif contient plusieurs comptes et que vous créez un élément prêt à l'envoi dans l'interface utilisateur, par exemple, en cliquant sur **Nouveau message électronique** ou sur **Nouvelle réunion**, un inspecteur affiche un nouvel élément de courrier ou une demande de réunion en mode composition, et il ne vous reste plus qu'à sélectionner le compte depuis lequel envoyer l'élément.</span><span class="sxs-lookup"><span data-stu-id="f7d29-107">If there are multiple accounts in the current profile and you create a sendable item in the user interface, for example, by clicking **New E-mail** or **New Meeting**, an inspector displays a new mail item or meeting request in compose mode, and then you can select the account from which to send the item.</span></span> 

<span data-ttu-id="f7d29-108">Cette rubrique explique comment créer un élément à envoyer avec un programme et l’envoyer à l’aide d’un compte d’envoi spécifique.</span><span class="sxs-lookup"><span data-stu-id="f7d29-108">This topic shows how to programmatically create a sendable item and send it by using a specific sending account.</span></span> <span data-ttu-id="f7d29-109">Cette rubrique contient deux exemples de code qui montrent comment créer un objet [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) et un objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) pour un compte spécifique qui est déterminé par le dossier actif dans l'explorateur actif.</span><span class="sxs-lookup"><span data-stu-id="f7d29-109">The topic has two code examples that show how to create a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) and an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) for a specific account that is determined by the current folder in the active explorer.</span></span>

<span data-ttu-id="f7d29-110">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d'abord ajouter une référence au composant Bibliothèque d'objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l'espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="f7d29-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="f7d29-111">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="f7d29-111">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="f7d29-112">La ligne de code suivante montre comment effectuer l'importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="f7d29-112">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

<span data-ttu-id="f7d29-113">Dans la première méthode, CreateMailItemFromAccount identifie d’abord le compte concerné en mettant en correspondance la banque du dossier actif (obtenue à partir de la propriété [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) et la banque de remise par défaut de chaque compte (obtenue à partir de la propriété [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))) qui est définie dans la collection [comptes](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) de la session.</span><span class="sxs-lookup"><span data-stu-id="f7d29-113"> matches the store of the current folder (obtained from the Store property) with the default delivery store of each account (obtained with the DeliveryStore property) that is defined in the Accounts collection for the session.</span></span> <span data-ttu-id="f7d29-114">CreateMailItemFromAccount crée ensuite le **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="f7d29-114">CreateMailItemFromAccount then creates the **MailItem**.</span></span> 

<span data-ttu-id="f7d29-115">Pour associer l’élément avec le compte, CreateMailItemFromAccount affecte l’utilisateur du compte en tant qu’expéditeur de l’élément en configurant le compte account.CurrentUser.AddressEntry au compte[expéditeur](https://msdn.microsoft.com/library/ff184720\(v=office.15\))  du **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="f7d29-115">To associate the item with the account, CreateMailItemFromAccount assigns the user of the account as the sender of the item by setting the account.CurrentUser.AddressEntry property to the [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) property of the **MailItem**.</span></span> <span data-ttu-id="f7d29-116">Assigner la propriété à l’expéditeur est une étape importante ; si vous ne spécifiez pas l’expéditeur, le**MailItem** est créé pour le compte principal par défaut.</span><span class="sxs-lookup"><span data-stu-id="f7d29-116">Assigning the Sender property is the important step; if you do not specify the sender, the **MailItem** is created for the primary account by default.</span></span> <span data-ttu-id="f7d29-117">À la fin de la méthode, CreateMailItemFromAccount affiche le**MailItem**.</span><span class="sxs-lookup"><span data-stu-id="f7d29-117">At the end of the method, CreateMailItemFromAccount displays the **MailItem**.</span></span> <span data-ttu-id="f7d29-118">Notez que si le dossier actif ne se trouve pas sur un magasin de livraison, CreateMailItemFromAccount crée le **MailItem** pour le compte principal de la session.</span><span class="sxs-lookup"><span data-stu-id="f7d29-118">Note that if the current folder is not on a delivery store, CreateMailItemFromAccount creates the **MailItem** for the primary account for the session.</span></span>

```csharp
private void CreateMailItemFromAccount()
{
    Outlook.AddressEntry addrEntry = null;
    // Get the Store for CurrentFolder.
    Outlook.Folder folder =
        Application.ActiveExplorer().CurrentFolder 
        as Outlook.Folder;
    Outlook.Store store = folder.Store;
    Outlook.Accounts accounts =
        Application.Session.Accounts;
    // Enumerate accounts to find
    // account.DeliveryStore for store.
    foreach (Outlook.Account account in accounts)
    {
        if (account.DeliveryStore.StoreID == 
            store.StoreID)
        {
            addrEntry =
                account.CurrentUser.AddressEntry;
            break;
        }
    }
    // Create MailItem.
    Outlook.MailItem mail =
        Application.CreateItem(
        Outlook.OlItemType.olMailItem)
        as Outlook.MailItem;
    if (addrEntry != null)
    {
        // Set Sender property.
        mail.Sender = addrEntry;
        mail.Display(false);
    }
}
```

<span data-ttu-id="f7d29-119">La méthode suivante, CreateMeetingRequestFromAccount, ressemble à CreateMailItemFromAccount sauf qu’elle crée un AppointmentItem au lieu d’un objet MailItem.</span><span class="sxs-lookup"><span data-stu-id="f7d29-119">The next method, CreateMeetingRequestFromAccount, is similar to CreateMailItemFromAccount except that it creates an AppointmentItem instead of a MailItem.</span></span> <span data-ttu-id="f7d29-120">CreateMeetingRequestFromAccount identifie d’abord le compte concerné en mettant en correspondance la banque du dossier actif (obtenue à partir de la propriété [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))  ) et la banque de remise par défaut de chaque compte (obtenue à partir de la propriété [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\)) ) qui est définie dans la collection comptes de la session.</span><span class="sxs-lookup"><span data-stu-id="f7d29-120"> matches the store of the current folder (obtained from the Store property) with the default delivery store of each account (obtained with the DeliveryStore property) that is defined in the Accounts collection for the session.</span></span> <span data-ttu-id="f7d29-121">CreateMeetingRequestFromAccount crée ensuite l’objet AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="f7d29-121">CreateMeetingRequestFromAccount then creates the AppointmentItem.</span></span> 

<span data-ttu-id="f7d29-122">Pour associer l’élément avec le compte, CreateMeetingRequestFromAccount définit ce compte en tant que compte expéditeur de l’élément en définissant l’objet du [compte](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) vers la propriété [SendUsingAccount](https://msdn.microsoft.com/library/bb610680\(v=office.15\)) du AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="f7d29-122">To associate the item with the account, CreateMeetingRequestFromAccount assigns that account as the item's sending account by setting the [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object to the [SendUsingAccount](https://msdn.microsoft.com/library/bb610680\(v=office.15\)) property of the AppointmentItem.</span></span> <span data-ttu-id="f7d29-123">Assigner la propriété à l’expéditeur est une étape importante ; si vous ne spécifiez pas l’expéditeur, le AppointmentItem est créé pour le compte principal par défaut.</span><span class="sxs-lookup"><span data-stu-id="f7d29-123">Assigning the SendUsingAccount property is the important step; if you do not specify the account, the AppointmentItem is created for the primary account by default.</span></span> <span data-ttu-id="f7d29-124">À la fin de la méthode, CreateMeetingRequestFromAccount affiche l’objet AppointmentItem.</span><span class="sxs-lookup"><span data-stu-id="f7d29-124">At the end of the method, CreateMeetingRequestFromAccount displays the AppointmentItem.</span></span> <span data-ttu-id="f7d29-125">Notez que si le dossier actif ne se trouve pas sur un magasin de livraison, CreateMeetingRequestFromAccount crée le AppointmentItem pour le compte principal de la session.</span><span class="sxs-lookup"><span data-stu-id="f7d29-125">Note that if the current folder is not on a delivery store, CreateMeetingRequestFromAccount creates the AppointmentItem for the primary account for the session.</span></span>

```csharp
private void CreateMeetingRequestFromAccount()
{
    Outlook.Account acct = null;
    Outlook.Folder folder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.Store store = folder.Store;
    Outlook.Accounts accounts =
        Application.Session.Accounts;
    foreach (Outlook.Account account in accounts)
    {
        if (account.DeliveryStore.StoreID ==
            store.StoreID)
        {
            acct = account;
            break;
        }
    }
    Outlook.AppointmentItem appt =
        Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.MeetingStatus = 
        Outlook.OlMeetingStatus.olMeeting;
    if (acct != null)
    {
        // Set SendUsingAccount property.
        appt.SendUsingAccount=acct;
        appt.Display(false);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="f7d29-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7d29-126">See also</span></span>

- [<span data-ttu-id="f7d29-127">Comptes</span><span class="sxs-lookup"><span data-stu-id="f7d29-127">Accounts</span></span>](accounts.md)

