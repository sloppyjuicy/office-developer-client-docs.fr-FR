---
title: Suppression d'un service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 27c20242417e51886ab184b1cc87d6ebb185e4bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316862"
---
# <a name="deleting-a-message-service"></a><span data-ttu-id="aeb6b-103">Suppression d'un service de messagerie</span><span class="sxs-lookup"><span data-stu-id="aeb6b-103">Deleting a Message Service</span></span>

  
  
<span data-ttu-id="aeb6b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aeb6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="aeb6b-105">**Pour supprimer un service de messagerie d'un profil**</span><span class="sxs-lookup"><span data-stu-id="aeb6b-105">**To delete a message service from a profile**</span></span>
  
1. <span data-ttu-id="aeb6b-106">Appelez **IMAPISession:: GetMsgServiceTable** pour accéder à la table des services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="aeb6b-106">Call **IMAPISession::GetMsgServiceTable** to access the message service table.</span></span> 
    
2. <span data-ttu-id="aeb6b-107">Localisez la ligne du service de messagerie et transmettez sa colonne **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) dans le paramètre _Lpuid_ à [IMsgServiceAdmin::D eletemsgservice](imsgserviceadmin-deletemsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="aeb6b-107">Locate the row for the message service and pass its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column in the  _lpuid_ parameter to [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span></span> 
    
 <span data-ttu-id="aeb6b-108">**DeleteMsgService** appelle la fonction de point d'entrée du service de messagerie avec le paramètre _ULCONTEXT_ défini sur MSG_SERVICE_DELETE.</span><span class="sxs-lookup"><span data-stu-id="aeb6b-108">**DeleteMsgService** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="aeb6b-109">Les services de messagerie effectuent toutes les tâches de nettoyage pour le moment précédant leur suppression du profil.</span><span class="sxs-lookup"><span data-stu-id="aeb6b-109">Message services perform any clean up tasks at this time before they are removed from the profile.</span></span> 
  

