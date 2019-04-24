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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 364914df1c5897241dfeb89cce2cc3c62018ce24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332150"
---
# <a name="iostxsyncend"></a><span data-ttu-id="268e9-103">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="268e9-103">IOSTX::SyncEnd</span></span>

  
  
<span data-ttu-id="268e9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="268e9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="268e9-105">Termine la synchronisation à l'état actuel et quitte cet État.</span><span class="sxs-lookup"><span data-stu-id="268e9-105">Ends synchronization in the current state and exits that state.</span></span>
  
```cpp
HRESULT SyncEnd();
```

## <a name="remarks"></a><span data-ttu-id="268e9-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="268e9-106">Remarks</span></span>

<span data-ttu-id="268e9-107">Le client doit appeler **IOSTX:: SyncEnd,** pour chaque appel à [IOSTX:: SyncBeg](iostx-syncbeg.md).</span><span class="sxs-lookup"><span data-stu-id="268e9-107">The client must call **IOSTX::SyncEnd** for each call to [IOSTX::SyncBeg](iostx-syncbeg.md).</span></span> <span data-ttu-id="268e9-108">La structure de données correspondante contient des informations qui indiquent si le client a réussi l'état actuel afin qu'Outlook puisse nettoyer son état interne.</span><span class="sxs-lookup"><span data-stu-id="268e9-108">The corresponding data structure holds information to indicate whether the client has successfully completed the current state so that Outlook can clean up its internal state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="268e9-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="268e9-109">See also</span></span>



[<span data-ttu-id="268e9-110">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="268e9-110">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="268e9-111">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="268e9-111">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="268e9-112">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="268e9-112">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="268e9-113">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="268e9-113">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="268e9-114">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="268e9-114">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="268e9-115">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="268e9-115">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="268e9-116">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="268e9-116">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="268e9-117">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="268e9-117">MAPI Constants</span></span>](mapi-constants.md)

