---
title: Suppression d’un service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f39f721d434f4e54cbfa5d25a3ba626858f2b13e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583567"
---
# <a name="deleting-a-message-service"></a><span data-ttu-id="e8b30-103">Suppression d’un service de messagerie</span><span class="sxs-lookup"><span data-stu-id="e8b30-103">Deleting a Message Service</span></span>

  
  
<span data-ttu-id="e8b30-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8b30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="e8b30-105">**Pour supprimer un service de message à partir d’un profil**</span><span class="sxs-lookup"><span data-stu-id="e8b30-105">**To delete a message service from a profile**</span></span>
  
1. <span data-ttu-id="e8b30-106">Appelez **IMAPISession::GetMsgServiceTable** pour accéder à la table de service de message.</span><span class="sxs-lookup"><span data-stu-id="e8b30-106">Call **IMAPISession::GetMsgServiceTable** to access the message service table.</span></span> 
    
2. <span data-ttu-id="e8b30-107">Localisez la ligne pour le service de message et le secret de sa colonne **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) dans le paramètre _lpuid_ à [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="e8b30-107">Locate the row for the message service and pass its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column in the  _lpuid_ parameter to [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span></span> 
    
 <span data-ttu-id="e8b30-108">**DeleteMsgService** appelle la fonction de point d’entrée du service de message avec le paramètre _ulContext_ défini sur MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="e8b30-108">**DeleteMsgService** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="e8b30-109">Services de messagerie effectuer l’une des tâches de nettoyage pour le moment où ils sont supprimés du profil.</span><span class="sxs-lookup"><span data-stu-id="e8b30-109">Message services perform any clean up tasks at this time before they are removed from the profile.</span></span> 
  

