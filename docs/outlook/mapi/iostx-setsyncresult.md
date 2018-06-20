---
title: IOSTXSetSyncResult
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SetSyncResult
api_type:
- COM
ms.assetid: 7f083ee0-bf36-0059-1589-66e454fe0098
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 74a4e299da6c0637c3da70c329569266d43dbd9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784332"
---
# <a name="iostxsetsyncresult"></a><span data-ttu-id="a7fa1-103">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="a7fa1-103">IOSTX::SetSyncResult</span></span>

  
  
<span data-ttu-id="a7fa1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a7fa1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a7fa1-105">Définit le résultat de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="a7fa1-105">Sets the result of the synchronization.</span></span>
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a><span data-ttu-id="a7fa1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7fa1-106">Parameters</span></span>

 <span data-ttu-id="a7fa1-107">_hrSync_</span><span class="sxs-lookup"><span data-stu-id="a7fa1-107">_hrSync_</span></span>
  
>  <span data-ttu-id="a7fa1-108">[in] Le résultat de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="a7fa1-108">[in] The result of the synchronization.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a7fa1-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="a7fa1-109">Remarks</span></span>

<span data-ttu-id="a7fa1-110">Appelez **IOSTX::SetSyncResult** avant d’appeler **IOSTX::SyncEnd** pour informer le magasin local du résultat de la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="a7fa1-110">Call **IOSTX::SetSyncResult** before calling **IOSTX::SyncEnd** to inform the local store of the result of synchronization.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a7fa1-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7fa1-111">See also</span></span>



[<span data-ttu-id="a7fa1-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a7fa1-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="a7fa1-113">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="a7fa1-113">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="a7fa1-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="a7fa1-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="a7fa1-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="a7fa1-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="a7fa1-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="a7fa1-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="a7fa1-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="a7fa1-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)


[<span data-ttu-id="a7fa1-118">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="a7fa1-118">MAPI Constants</span></span>](mapi-constants.md)

