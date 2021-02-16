---
title: Gestion des notifications de la table
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6e6c24c3836f295054c1880dc506c5051078a9ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435893"
---
# <a name="handling-table-notification"></a><span data-ttu-id="a910f-103">Gestion des notifications de la table</span><span class="sxs-lookup"><span data-stu-id="a910f-103">Handling table notification</span></span>

<span data-ttu-id="a910f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a910f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a910f-105">Au lieu de s’inscrire directement avec un objet source de conseil, tel qu’un dossier ou un utilisateur de messagerie, un client peut s’inscrire pour les notifications dans un contenu ou une table hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="a910f-105">As an alternative to registering directly with an advise source object, such as a folder or a messaging user, a client can register for notifications on a contents or hierarchy table.</span></span> <span data-ttu-id="a910f-106">Le suivi des modifications apportées aux entrées, dossiers et messages du carnet d’adresses par le biais d’un contenu ou d’une table hiérarchique peut être plus simple et plus simple que par le biais d’objets individuels.</span><span class="sxs-lookup"><span data-stu-id="a910f-106">Tracking changes to address book entries, folders, and messages through a contents or hierarchy table can be simpler and more straightforward than through individual objects.</span></span> 

<span data-ttu-id="a910f-107">Par exemple, vous pouvez appeler [IMAPITable::Advise](imapitable-advise.md) on a folder’s hierarchy table to discover when changes occur to one of its subfolders.</span><span class="sxs-lookup"><span data-stu-id="a910f-107">For example, you can call [IMAPITable::Advise](imapitable-advise.md) on a folder's hierarchy table to discover when changes occur to one of its subfolders.</span></span> <span data-ttu-id="a910f-108">Si vous prendre en charge l’affichage des messages distants, inscrivez-vous dans la table d’état pour observer l’activité des fournisseurs de transport et dupooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="a910f-108">If you support the viewing of remote messages, register with the status table to observe activity by transport providers and the MAPI spooler.</span></span> 
  
<span data-ttu-id="a910f-109">Toutefois, il n’est pas toujours préférable d’utiliser des notifications de tableau plutôt que des notifications d’objet.</span><span class="sxs-lookup"><span data-stu-id="a910f-109">However, it is not always preferable to use table notifications instead of object notifications.</span></span> <span data-ttu-id="a910f-110">La surveillance des modifications apportées au nombre de messages dans un dossier est un exemple de cas où votre client peut avoir besoin de s’inscrire aux notifications d’objet sur un dossier plutôt que sur une table implémentée par le dossier.</span><span class="sxs-lookup"><span data-stu-id="a910f-110">Monitoring changes in the number of messages in a folder is an example of when your client might need to register for object notifications on a folder rather than on a table implemented by the folder.</span></span>
  

