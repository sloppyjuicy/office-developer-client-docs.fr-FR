---
title: IOSTXInitSync
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.InitSync
api_type:
- COM
ms.assetid: e22244a2-ac5f-910a-501f-4483ea0667c2
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b9086383b45d40d5839284ac785d72438be60e00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413352"
---
# <a name="iostxinitsync"></a><span data-ttu-id="7dedf-103">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="7dedf-103">IOSTX::InitSync</span></span>

  
  
<span data-ttu-id="7dedf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7dedf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7dedf-105">Informe la Banque de messages locale que la synchronisation est sur le début.</span><span class="sxs-lookup"><span data-stu-id="7dedf-105">Informs the local message store that synchronization is about to start.</span></span>
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="7dedf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7dedf-106">Parameters</span></span>

 <span data-ttu-id="7dedf-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7dedf-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7dedf-108">dans Indicateurs permettant de déterminer le comportement approprié lors de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="7dedf-108">[in] Flags to determine appropriate behavior during synchronization.</span></span> <span data-ttu-id="7dedf-109">Outlook utilise ces indicateurs dans chaque État de la machine à États de réplication pour déterminer les informations qu'il doit fournir pour le client.</span><span class="sxs-lookup"><span data-stu-id="7dedf-109">Outlook uses these flags in each state of the replication state machine to determine the information that it should provide for the client.</span></span> <span data-ttu-id="7dedf-110">Par exemple, si le client transmet **SYNC_ONLY_ASSOCIATED**, Outlook renverra uniquement les informations relatives aux éléments associés (ou masqués).</span><span class="sxs-lookup"><span data-stu-id="7dedf-110">For example, if the client passes **SYNC_ONLY_ASSOCIATED**, Outlook will only return information related to associated (or hidden) items.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7dedf-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7dedf-111">See also</span></span>



[<span data-ttu-id="7dedf-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="7dedf-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="7dedf-113">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="7dedf-113">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="7dedf-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="7dedf-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="7dedf-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="7dedf-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="7dedf-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="7dedf-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="7dedf-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="7dedf-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="7dedf-118">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7dedf-118">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="7dedf-119">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="7dedf-119">MAPI Constants</span></span>](mapi-constants.md)

