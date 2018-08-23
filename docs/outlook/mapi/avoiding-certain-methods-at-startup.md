---
title: Éviter certaines méthodes au démarrage
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: 5d26583ad7ad3b4a200daf321a8994e302b75a79
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580634"
---
# <a name="avoiding-certain-methods-at-startup"></a><span data-ttu-id="7bbdf-103">Éviter certaines méthodes au démarrage</span><span class="sxs-lookup"><span data-stu-id="7bbdf-103">Avoiding Certain Methods at Startup</span></span>

 
  
<span data-ttu-id="7bbdf-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7bbdf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7bbdf-105">Pour améliorer les performances lors du démarrage, évitez les appels suivants :</span><span class="sxs-lookup"><span data-stu-id="7bbdf-105">To improve performance at startup time, avoid making the following calls:</span></span>
  
- [<span data-ttu-id="7bbdf-106">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="7bbdf-106">IMAPISession::EnumAdrTypes</span></span>](imapisession-enumadrtypes.md)
    
- [<span data-ttu-id="7bbdf-107">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="7bbdf-107">IMAPISession::GetStatusTable</span></span>](imapisession-getstatustable.md)
    
- [<span data-ttu-id="7bbdf-108">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="7bbdf-108">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
    
- [<span data-ttu-id="7bbdf-109">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="7bbdf-109">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
    
- [<span data-ttu-id="7bbdf-110">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="7bbdf-110">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
    
<span data-ttu-id="7bbdf-111">L’appel vers **IMAPIStatus::ValidateState** affecte les performances que s’il fait sur le spouleur MAPI ou le sous-système MAPI.</span><span class="sxs-lookup"><span data-stu-id="7bbdf-111">The call to **IMAPIStatus::ValidateState** affects performance only when made on either the MAPI spooler or the MAPI subsystem.</span></span> <span data-ttu-id="7bbdf-112">Que ces méthodes ralentissent le traitement de démarrage est, car ils ne peuvent pas effectuer jusqu'à ce que le spouleur MAPI a terminé ses tâches de démarrage.</span><span class="sxs-lookup"><span data-stu-id="7bbdf-112">The reason that these methods slow startup processing is because they cannot complete until the MAPI spooler has finished its startup tasks.</span></span> 
  
<span data-ttu-id="7bbdf-113">Vous devez également éviter de recherche dans la banque de messages au démarrage.</span><span class="sxs-lookup"><span data-stu-id="7bbdf-113">You should also avoid searching the message store at startup time.</span></span> <span data-ttu-id="7bbdf-114">Appelez votre [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) de traitement de démarrage est terminée.</span><span class="sxs-lookup"><span data-stu-id="7bbdf-114">Make your [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) call when startup processing has finished.</span></span> 
  

