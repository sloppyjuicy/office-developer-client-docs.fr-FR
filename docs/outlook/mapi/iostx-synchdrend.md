---
title: IOSTXSyncHdrEnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrEnd
api_type:
- COM
ms.assetid: a0beb6eb-7978-c64e-dba1-89f0caf2090e
description: 'Dernière modification : 03 juillet 2012'
ms.openlocfilehash: a40d4e62a930219a738c7b431f3d2192007c3d9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591330"
---
# <a name="iostxsynchdrend"></a><span data-ttu-id="a5aac-103">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="a5aac-103">IOSTX::SyncHdrEnd</span></span>

 
  
<span data-ttu-id="a5aac-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5aac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5aac-105">Fin de la synchronisation pour un en-tête de message.</span><span class="sxs-lookup"><span data-stu-id="a5aac-105">Ends synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a><span data-ttu-id="a5aac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5aac-106">Parameters</span></span>

 <span data-ttu-id="a5aac-107">_pprog_</span><span class="sxs-lookup"><span data-stu-id="a5aac-107">_pprog_</span></span>
  
> <span data-ttu-id="a5aac-108">[in] Interface **[IMAPIProgress](imapiprogressiunknown.md)** pour la synchronisation de déplacé ou copié des messages.</span><span class="sxs-lookup"><span data-stu-id="a5aac-108">[in] **[IMAPIProgress](imapiprogressiunknown.md)** interface for synchronization of moved or copied messages.</span></span> <span data-ttu-id="a5aac-109">Voir mapidefs.h pour la définition du type de **LPMAPIPROGRESS**.</span><span class="sxs-lookup"><span data-stu-id="a5aac-109">See mapidefs.h for the type definition of **LPMAPIPROGRESS**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a5aac-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="a5aac-110">Remarks</span></span>

<span data-ttu-id="a5aac-111">Lors de l' **[IOSTX::SyncBeg](iostx-syncbeg.md)**, du stockage local passe l' [état d’en-tête de message du téléchargement](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="a5aac-111">Upon **[IOSTX::SyncBeg](iostx-syncbeg.md)**, the local store enters the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="a5aac-112">Le client télécharge un élément de message complète (comme *pmsgFull* dans **[HDRSYNC](hdrsync.md)** ).</span><span class="sxs-lookup"><span data-stu-id="a5aac-112">The client downloads a full message item (as  *pmsgFull*  in **[HDRSYNC](hdrsync.md)** ).</span></span> <span data-ttu-id="a5aac-113">Si l’opération réussit, le client définit également *ulFlags* **HDRSYNC** en tant que **HSF_OK**.</span><span class="sxs-lookup"><span data-stu-id="a5aac-113">If this is successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="a5aac-114">Fonction **IOSTX::SyncHdrEnd**, Outlook vérifie le résultat dans **HDRSYNC** et utilise *pprog* et les informations **HDRSYNC** pour mettre à jour l’en-tête de message local.</span><span class="sxs-lookup"><span data-stu-id="a5aac-114">Upon **IOSTX::SyncHdrEnd**, Outlook checks the result in **HDRSYNC** and uses  *pprog*  and the information in **HDRSYNC** to update the local message header.</span></span> 
  
<span data-ttu-id="a5aac-115">Le magasin local renvoie à l’état, qu'il se trouvait avant précédente **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span><span class="sxs-lookup"><span data-stu-id="a5aac-115">The local store returns to the state it was in before the preceding **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a5aac-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5aac-116">See also</span></span>



[<span data-ttu-id="a5aac-117">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="a5aac-117">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="a5aac-118">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="a5aac-118">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="a5aac-119">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="a5aac-119">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="a5aac-120">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="a5aac-120">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="a5aac-121">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="a5aac-121">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="a5aac-122">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="a5aac-122">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="a5aac-123">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a5aac-123">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="a5aac-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="a5aac-124">MAPI Constants</span></span>](mapi-constants.md)

