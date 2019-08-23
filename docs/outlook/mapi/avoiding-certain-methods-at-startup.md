---
title: Éviter certaines méthodes au démarrage
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: 'Dernière modification : 07 décembre 2015'
ms.openlocfilehash: 21aafebefcb7e10e6ba432f2eb3cc5dc04978c20
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318087"
---
# <a name="avoiding-certain-methods-at-startup"></a><span data-ttu-id="76ae4-103">Éviter certaines méthodes au démarrage</span><span class="sxs-lookup"><span data-stu-id="76ae4-103">Avoiding Certain Methods at Startup</span></span>

 
  
<span data-ttu-id="76ae4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76ae4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76ae4-105">Pour améliorer les performances au moment du démarrage, évitez d’effectuer les appels suivants :</span><span class="sxs-lookup"><span data-stu-id="76ae4-105">To improve performance at startup time, avoid making the following calls:</span></span>
  
- [<span data-ttu-id="76ae4-106">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="76ae4-106">IMAPISession::EnumAdrTypes</span></span>](imapisession-enumadrtypes.md)
    
- [<span data-ttu-id="76ae4-107">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="76ae4-107">IMAPISession::GetStatusTable</span></span>](imapisession-getstatustable.md)
    
- [<span data-ttu-id="76ae4-108">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="76ae4-108">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
    
- [<span data-ttu-id="76ae4-109">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="76ae4-109">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
    
- [<span data-ttu-id="76ae4-110">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="76ae4-110">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
    
<span data-ttu-id="76ae4-111">L’appel à **IMAPIStatus::ValidateState** a une incidence sur les performances uniquement lorsqu’il est effectué sur le spouleur MAPI ou le sous-système MAPI.</span><span class="sxs-lookup"><span data-stu-id="76ae4-111">The call to **IMAPIStatus::ValidateState** affects performance only when made on either the MAPI spooler or the MAPI subsystem.</span></span> <span data-ttu-id="76ae4-112">Ces méthodes ralentissent le traitement du démarrage, car elles ne peuvent pas être effectuées tant que le spouleur MAPI n’a pas terminé ses tâches de démarrage.</span><span class="sxs-lookup"><span data-stu-id="76ae4-112">The reason that these methods slow startup processing is because they cannot complete until the MAPI spooler has finished its startup tasks.</span></span> 
  
<span data-ttu-id="76ae4-113">Vous devez également éviter d’effectuer une recherche dans la banque de messages lors du démarrage.</span><span class="sxs-lookup"><span data-stu-id="76ae4-113">You should also avoid searching the message store at startup time.</span></span> <span data-ttu-id="76ae4-114">Exécutez votre appel [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) une fois le traitement du démarrage terminé.</span><span class="sxs-lookup"><span data-stu-id="76ae4-114">Make your [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) call when startup processing has finished.</span></span> 
  

