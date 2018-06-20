---
title: IOSTXSyncEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncEnd
api_type:
- COM
ms.assetid: da9de705-bdab-6cb8-35ea-61f03cdc4ff5
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 66542d2cc7600ecbcd8de9043b6b40559744c2ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784341"
---
# <a name="iostxsyncend"></a><span data-ttu-id="33e8c-103">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="33e8c-103">IOSTX::SyncEnd</span></span>

  
  
<span data-ttu-id="33e8c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="33e8c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="33e8c-105">Met fin à la synchronisation dans l’état actuel et quitte cet état.</span><span class="sxs-lookup"><span data-stu-id="33e8c-105">Ends synchronization in the current state and exits that state.</span></span>
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a><span data-ttu-id="33e8c-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="33e8c-106">Remarks</span></span>

<span data-ttu-id="33e8c-107">Le client doit appeler **IOSTX::SyncEnd** pour chaque appel à [IOSTX::SyncBeg](iostx-syncbeg.md).</span><span class="sxs-lookup"><span data-stu-id="33e8c-107">The client must call **IOSTX::SyncEnd** for each call to [IOSTX::SyncBeg](iostx-syncbeg.md).</span></span> <span data-ttu-id="33e8c-108">La structure de données correspondante conserve des informations pour indiquer si le client a terminé l’état actuel afin qu’Outlook peut nettoyer son état interne.</span><span class="sxs-lookup"><span data-stu-id="33e8c-108">The corresponding data structure holds information to indicate whether the client has successfully completed the current state so that Outlook can clean up its internal state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="33e8c-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33e8c-109">See also</span></span>



[<span data-ttu-id="33e8c-110">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="33e8c-110">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="33e8c-111">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="33e8c-111">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="33e8c-112">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="33e8c-112">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="33e8c-113">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="33e8c-113">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="33e8c-114">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="33e8c-114">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="33e8c-115">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="33e8c-115">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="33e8c-116">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="33e8c-116">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="33e8c-117">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="33e8c-117">MAPI Constants</span></span>](mapi-constants.md)

