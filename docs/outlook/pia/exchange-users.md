---
title: Utilisateurs Exchange
TOCTitle: Exchange users
ms:assetid: 01802032-fd60-400b-ad83-1f4eefe596bd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184585(v=office.15)
ms:contentKeyID: 55119835
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 667f8a07477c527d251c4e50f35baa2da2e417ed
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703221"
---
# <a name="exchange-users"></a>Utilisateurs Exchange

Cette section fournit des exemples de tâches qui impliquent des utilisateurs de boîtes aux lettres Microsoft Exchange. Les utilisateurs d'Exchange sont connectés à un serveur Exchange et sont représentés par des objets [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) qui sont dérivés de l'objet [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) .

## <a name="in-this-section"></a>Dans cette section

|Rubrique|Description|
|:----|:----------|
|[Obtention des informations de l’utilisateur actuel](how-to-get-information-about-the-current-user.md)  |Récupère les informations de l’utilisateur actuel, par exemple, le nom, la fonction et le numéro de téléphone.|
|[Obtention des informations de toutes les listes de distribution dont l’utilisateur actuel est membre](how-to-get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member.md)  |Utilise la méthode [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) pour obtenir des informations sur toutes les listes de distribution dont l’utilisateur actuel est membre.|
|[Création d’une liste de distribution](how-to-create-a-distribution-list.md)  |Crée une liste de distribution et la présente à l’utilisateur.|
[Obtention des membres d’une liste de distribution Exchange](how-to-get-members-of-an-exchange-distribution-list.md)  |Invite l'utilisateur à sélectionner une liste de distribution Exchange dans la boîte de dialogue **Sélectionner des noms** et développe la liste de distribution pour afficher ses membres.|
[Obtention des informations du manager de l’utilisateur actuel](how-to-get-information-about-the-current-user-s-manager.md)  |Récupère les informations (par exemple, le nom, la fonction et les numéros de téléphone) du manager de l’utilisateur actuel.|
[Obtention des informations de disponibilité du manager d’un utilisateur Exchange](how-to-get-availability-information-for-an-exchange-user-s-manager.md) |  Affiche le prochain créneau de 60 minutes disponible du manager d’un utilisateur dans le calendrier.|
|[Vérification de la réponse d’un manager à une demande de réunion](how-to-check-a-manager-s-response-to-a-meeting-request.md) | Utilise la méthode [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) et [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) pour vérifier le statut de la réponse du manager de l’utilisateur actuel à une demande de réunion.|
|[Obtention des informations des collaborateurs directs du manager de l’utilisateur actuel](how-to-get-information-about-direct-reports-of-the-current-user-s-manager.md) | Obtient les collaborateurs directs du manager de l’utilisateur actuel, s’il en existe, puis affiche les informations de chaque collaborateur direct du manager.|

## <a name="see-also"></a>Voir aussi

- [Comptes](accounts.md)
- [Carnet d’adresses](address-book.md)
- [Banques](stores.md)
- [Procédure (Référence PIA Outlook 2013)](how-do-i-outlook-2013-pia-reference.md)

