---
title: Suppression d’un service de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 27c20242417e51886ab184b1cc87d6ebb185e4bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428122"
---
# <a name="deleting-a-message-service"></a><span data-ttu-id="423ad-103">Suppression d’un service de message</span><span class="sxs-lookup"><span data-stu-id="423ad-103">Deleting a Message Service</span></span>

  
  
<span data-ttu-id="423ad-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="423ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="423ad-105">**Pour supprimer un service de message d’un profil**</span><span class="sxs-lookup"><span data-stu-id="423ad-105">**To delete a message service from a profile**</span></span>
  
1. <span data-ttu-id="423ad-106">Appelez **IMAPISession::GetMsgServiceTable** pour accéder à la table du service de message.</span><span class="sxs-lookup"><span data-stu-id="423ad-106">Call **IMAPISession::GetMsgServiceTable** to access the message service table.</span></span> 
    
2. <span data-ttu-id="423ad-107">Recherchez la ligne du service de message et passez sa colonne **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) dans le paramètre  _lpuid_ à [IMsgServiceAdmin::D eleteMsgService](imsgserviceadmin-deletemsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="423ad-107">Locate the row for the message service and pass its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column in the  _lpuid_ parameter to [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span></span> 
    
 <span data-ttu-id="423ad-108">**DeleteMsgService** appelle la fonction de point d’entrée du service de message avec le paramètre  _ulContext_ MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="423ad-108">**DeleteMsgService** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="423ad-109">Les services de messages effectuent actuellement des tâches de nettoyage avant qu’elles ne soient supprimées du profil.</span><span class="sxs-lookup"><span data-stu-id="423ad-109">Message services perform any clean up tasks at this time before they are removed from the profile.</span></span> 
  

