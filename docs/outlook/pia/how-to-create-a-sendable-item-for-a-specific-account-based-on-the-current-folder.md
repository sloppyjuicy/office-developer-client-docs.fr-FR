---
title: Créer un élément à envoyer pour un compte spécifique basé sur le dossier actif
TOCTitle: Create a sendable item for a specific account based on the current folder
ms:assetid: 665ebdc5-2912-4d85-ac40-835c9ef9a439
ms:contentKeyID: 55119796
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 82d8fc7dc40a70eedc3fa9fd0deeb4e005ad1756
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590773"
---
# <a name="create-a-sendable-item-for-a-specific-account-based-on-the-current-folder"></a>Créer un élément à envoyer pour un compte spécifique basé sur le dossier actif

Cette rubrique contient deux exemples de code montrant comment créer un élément de courrier et une demande de réunion prêts à l'envoi, puis comment les envoyer en utilisant un compte spécifique déterminé en fonction du dossier actif.

## <a name="example"></a>Exemple

Lorsque vous utilisez la méthode [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) de l'objet[Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) pour créer un élément Microsoft Outlook, cet élément est créé pour le compte principal de la session active. Dans une session pour laquelle plusieurs comptes sont définis dans le profil, vous pouvez créer un élément pour un compte IMAP, POP ou Microsoft Exchange spécifique. 

Si le profil actif contient plusieurs comptes et que vous créez un élément prêt à l'envoi dans l'interface utilisateur, par exemple, en cliquant sur **Nouveau message électronique** ou sur **Nouvelle réunion**, un inspecteur affiche un nouvel élément de courrier ou une demande de réunion en mode composition, et il ne vous reste plus qu'à sélectionner le compte depuis lequel envoyer l'élément. 

Cette rubrique explique comment créer un élément à envoyer avec un programme et l’envoyer à l’aide d’un compte d’envoi spécifique. Cette rubrique contient deux exemples de code qui montrent comment créer un objet [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) et un objet [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) pour un compte spécifique qui est déterminé par le dossier actif dans l'explorateur actif.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

Dans la première méthode, CreateMailItemFromAccount identifie d’abord le compte concerné en mettant en correspondance la banque du dossier actif (obtenue à partir de la propriété [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))) et la banque de remise par défaut de chaque compte (obtenue à partir de la propriété [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\))) qui est définie dans la collection [comptes](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) de la session. CreateMailItemFromAccount crée ensuite le **MailItem**. 

Pour associer l’élément avec le compte, CreateMailItemFromAccount affecte l’utilisateur du compte en tant qu’expéditeur de l’élément en configurant le compte account.CurrentUser.AddressEntry au compte [expéditeur](https://msdn.microsoft.com/library/ff184720\(v=office.15\))  du **MailItem**. Assigner la propriété à l’expéditeur est une étape importante ; si vous ne spécifiez pas l’expéditeur, le **MailItem** est créé pour le compte principal par défaut. À la fin de la méthode, CreateMailItemFromAccount affiche le **MailItem**. Notez que si le dossier actif ne se trouve pas sur un magasin de livraison, CreateMailItemFromAccount crée le **MailItem** pour le compte principal de la session.

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

La méthode suivante, CreateMeetingRequestFromAccount, ressemble à CreateMailItemFromAccount sauf qu’elle crée un AppointmentItem au lieu d’un objet MailItem. CreateMeetingRequestFromAccount identifie d’abord le compte concerné en mettant en correspondance la banque du dossier actif (obtenue à partir de la propriété [Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\))  ) et la banque de remise par défaut de chaque compte (obtenue à partir de la propriété [DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\)) ) qui est définie dans la collection comptes de la session. CreateMeetingRequestFromAccount crée ensuite l’objet AppointmentItem. 

Pour associer l’élément avec le compte, CreateMeetingRequestFromAccount définit ce compte en tant que compte expéditeur de l’élément en définissant l’objet du [compte](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) vers la propriété [SendUsingAccount](https://msdn.microsoft.com/library/bb610680\(v=office.15\)) du AppointmentItem. Assigner la propriété à l’expéditeur est une étape importante ; si vous ne spécifiez pas l’expéditeur, le AppointmentItem est créé pour le compte principal par défaut. À la fin de la méthode, CreateMeetingRequestFromAccount affiche l’objet AppointmentItem. Notez que si le dossier actif ne se trouve pas sur un magasin de livraison, CreateMeetingRequestFromAccount crée le AppointmentItem pour le compte principal de la session.

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

## <a name="see-also"></a>Voir aussi

- [Comptes](accounts.md)

