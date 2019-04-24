---
title: Gestion des notifications de la table
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 6e6c24c3836f295054c1880dc506c5051078a9ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299488"
---
# <a name="handling-table-notification"></a><span data-ttu-id="72f13-103">Gestion des notifications de la table</span><span class="sxs-lookup"><span data-stu-id="72f13-103">Handling table notification</span></span>

<span data-ttu-id="72f13-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72f13-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72f13-105">En guise d'alternative à l'inscription directe avec un objet de source de notification, tel qu'un dossier ou un utilisateur de messagerie, un client peut s'inscrire pour des notifications sur une table des matières ou une table de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="72f13-105">As an alternative to registering directly with an advise source object, such as a folder or a messaging user, a client can register for notifications on a contents or hierarchy table.</span></span> <span data-ttu-id="72f13-106">Le suivi des modifications apportées aux entrées de carnet d'adresses, aux dossiers et aux messages via un tableau de contenu ou de hiérarchie peut être plus simple et plus simple qu'avec des objets individuels.</span><span class="sxs-lookup"><span data-stu-id="72f13-106">Tracking changes to address book entries, folders, and messages through a contents or hierarchy table can be simpler and more straightforward than through individual objects.</span></span> 

<span data-ttu-id="72f13-107">Par exemple, vous pouvez appeler la fonction [IMAPITable:: Advise](imapitable-advise.md) sur la table de hiérarchie d'un dossier pour détecter les modifications apportées à l'un de ses sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="72f13-107">For example, you can call [IMAPITable::Advise](imapitable-advise.md) on a folder's hierarchy table to discover when changes occur to one of its subfolders.</span></span> <span data-ttu-id="72f13-108">Si vous prenez en charge l'affichage des messages distants, inscrivez-vous à l'aide de la table d'État pour observer l'activité par les fournisseurs de transport et le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="72f13-108">If you support the viewing of remote messages, register with the status table to observe activity by transport providers and the MAPI spooler.</span></span> 
  
<span data-ttu-id="72f13-109">Toutefois, il n'est pas toujours préférable d'utiliser des notifications de table au lieu de notifications d'objet.</span><span class="sxs-lookup"><span data-stu-id="72f13-109">However, it is not always preferable to use table notifications instead of object notifications.</span></span> <span data-ttu-id="72f13-110">Le suivi des modifications apportées au nombre de messages dans un dossier est un exemple de la nécessité pour votre client d'inscrire des notifications d'objet sur un dossier plutôt que sur une table implémentée par le dossier.</span><span class="sxs-lookup"><span data-stu-id="72f13-110">Monitoring changes in the number of messages in a folder is an example of when your client might need to register for object notifications on a folder rather than on a table implemented by the folder.</span></span>
  

