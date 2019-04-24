---
title: Accounts
TOCTitle: Accounts
ms:assetid: 28df6dbd-4d24-42f3-91c1-fd8b3a4ea722
ms:mtpsurl: https://msdn.microsoft.com/library/office/ff184597(v=office.15)
ms:contentKeyID: 55119790
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d539f38419a8eaac60cd3054da6283a49bf4cc00
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331184"
---
# <a name="accounts"></a>Comptes 

Cette section fournit des exemples de tâches qui impliquent des comptes de messagerie. Microsoft Exchange Server, POP3 (Post Office Protocol 3), IMAP (Internet Message Access Protocol) et les comptes HTTP sont des exemples de compte de messagerie. Le compte du profil actuel est représenté par un objet [Account](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.account?view=outlook-pia).


|Rubrique|Description|
|:----|:----------|
|[Obtention des informations du compte](how-to-get-account-information.md) | Prend comme argument d'entrée un objet Microsoft Outlook [Application](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.application?view=outlook-pia) approuvé, et utilise l'objet **Account** pour afficher les détails de chaque compte disponible pour le profil Outlook actuel.|
|[Création d’un élément à envoyer pour un compte spécifique basé sur le dossier actuel](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md) | Contient deux exemples de code qui montrent comment créer un élément de messagerie à envoyer et une demande de réunion, et comment les envoyer en utilisant un compte spécifique basé sur le dossier actuel.|
|[Obtention du compte lié à un dossier](how-to-get-the-account-for-a-folder.md) | Obtient le compte associé à un dossier dans la session actuelle.|
|[Obtention des informations de plusieurs comptes](how-to-get-information-about-multiple-accounts.md) | Obtient et affiche des informations diverses sur chaque compte dans le profil actuel.|
|[Envoi d’un élément de courrier électronique avec un compte Hotmail](how-to-send-a-mail-item-by-using-a-hotmail-account.md) | Utilise la propriété [SendUsingAccount](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._mailitem.sendusingaccount?view=outlook-pia) pour envoyer un message en utilisant un compte Windows Live Hotmail.|

## <a name="see-also"></a>Voir aussi

- [Utilisateurs Exchange](exchange-users.md)
- [Courrier](mail.md)
- [Destinataires](recipients.md)
- [Procédure (Référence PIA Outlook 2013)](how-do-i-outlook-2013-pia-reference.md)

