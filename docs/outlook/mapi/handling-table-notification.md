---
title: Gestion de notification de la table
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: edc9bc71-4885-4783-b465-0bafa20eff73
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b36e4697bfd4360f4ea6ea47c70eaaae434696d8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595131"
---
# <a name="handling-table-notification"></a><span data-ttu-id="16869-103">Gestion de notification de la table</span><span class="sxs-lookup"><span data-stu-id="16869-103">Handling table notification</span></span>

<span data-ttu-id="16869-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16869-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16869-105">En guise d’alternative à l’enregistrement directement avec un objet source advise, par exemple un dossier ou un utilisateur de messagerie, un client peut s’inscrire pour les notifications sur un contenu ou une table de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="16869-105">As an alternative to registering directly with an advise source object, such as a folder or a messaging user, a client can register for notifications on a contents or hierarchy table.</span></span> <span data-ttu-id="16869-106">Suivi des modifications à l’adresse carnet d’entrées, dossiers et messages via un contenu ou table de hiérarchie peut être plus simple et plus simple que par le biais des objets individuels.</span><span class="sxs-lookup"><span data-stu-id="16869-106">Tracking changes to address book entries, folders, and messages through a contents or hierarchy table can be simpler and more straightforward than through individual objects.</span></span> 

<span data-ttu-id="16869-107">Par exemple, vous pouvez appeler [IMAPITable::Advise](imapitable-advise.md) sur la table de hiérarchie d’un dossier pour découvrir les modifications sont apportées à un de ses sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="16869-107">For example, you can call [IMAPITable::Advise](imapitable-advise.md) on a folder's hierarchy table to discover when changes occur to one of its subfolders.</span></span> <span data-ttu-id="16869-108">Si vous prenez en charge l’affichage des messages à distance, enregistrez la table d’état à respecter le spouleur MAPI et l’activité par les fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="16869-108">If you support the viewing of remote messages, register with the status table to observe activity by transport providers and the MAPI spooler.</span></span> 
  
<span data-ttu-id="16869-109">Toutefois, il n’est pas toujours préférable d’utiliser des notifications de table au lieu des notifications de l’objet.</span><span class="sxs-lookup"><span data-stu-id="16869-109">However, it is not always preferable to use table notifications instead of object notifications.</span></span> <span data-ttu-id="16869-110">Suivi des modifications dans le nombre de messages dans un dossier est un exemple de lorsque votre client peut être nécessaire d’enregistrer les notifications d’objet dans un dossier, plutôt que sur une table implémentée par le dossier.</span><span class="sxs-lookup"><span data-stu-id="16869-110">Monitoring changes in the number of messages in a folder is an example of when your client might need to register for object notifications on a folder rather than on a table implemented by the folder.</span></span>
  

