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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: fd5b2ed23eba30cbe861a20c4fd100cb8ea1aeb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568839"
---
# <a name="iostxsyncend"></a><span data-ttu-id="9510d-103">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="9510d-103">IOSTX::SyncEnd</span></span>

  
  
<span data-ttu-id="9510d-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9510d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9510d-105">Met fin à la synchronisation dans l’état actuel et quitte cet état.</span><span class="sxs-lookup"><span data-stu-id="9510d-105">Ends synchronization in the current state and exits that state.</span></span>
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a><span data-ttu-id="9510d-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="9510d-106">Remarks</span></span>

<span data-ttu-id="9510d-107">Le client doit appeler **IOSTX::SyncEnd** pour chaque appel à [IOSTX::SyncBeg](iostx-syncbeg.md).</span><span class="sxs-lookup"><span data-stu-id="9510d-107">The client must call **IOSTX::SyncEnd** for each call to [IOSTX::SyncBeg](iostx-syncbeg.md).</span></span> <span data-ttu-id="9510d-108">La structure de données correspondante conserve des informations pour indiquer si le client a terminé l’état actuel afin qu’Outlook peut nettoyer son état interne.</span><span class="sxs-lookup"><span data-stu-id="9510d-108">The corresponding data structure holds information to indicate whether the client has successfully completed the current state so that Outlook can clean up its internal state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9510d-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9510d-109">See also</span></span>



[<span data-ttu-id="9510d-110">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="9510d-110">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="9510d-111">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="9510d-111">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="9510d-112">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="9510d-112">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="9510d-113">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="9510d-113">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="9510d-114">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="9510d-114">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="9510d-115">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="9510d-115">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="9510d-116">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9510d-116">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="9510d-117">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="9510d-117">MAPI Constants</span></span>](mapi-constants.md)

