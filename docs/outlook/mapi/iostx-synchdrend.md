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
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: 864c2d2dfd17c285b0d8a401d59ce5b7d0463864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432771"
---
# <a name="iostxsynchdrend"></a><span data-ttu-id="44164-103">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="44164-103">IOSTX::SyncHdrEnd</span></span>

 
  
<span data-ttu-id="44164-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44164-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44164-105">Met fin à la synchronisation d’un en-tête de message.</span><span class="sxs-lookup"><span data-stu-id="44164-105">Ends synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrEnd( 
    LPMAPIPROGRESS pprog 
);
```

## <a name="parameters"></a><span data-ttu-id="44164-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="44164-106">Parameters</span></span>

 <span data-ttu-id="44164-107">_pprog_</span><span class="sxs-lookup"><span data-stu-id="44164-107">_pprog_</span></span>
  
> <span data-ttu-id="44164-108">[in] **[Interface IMAPIProgress pour](imapiprogressiunknown.md)** la synchronisation des messages déplacés ou copiés.</span><span class="sxs-lookup"><span data-stu-id="44164-108">[in] **[IMAPIProgress](imapiprogressiunknown.md)** interface for synchronization of moved or copied messages.</span></span> <span data-ttu-id="44164-109">Voir mapidefs.h pour la définition de type **de LPMAPIPROGRESS**.</span><span class="sxs-lookup"><span data-stu-id="44164-109">See mapidefs.h for the type definition of **LPMAPIPROGRESS**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="44164-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="44164-110">Remarks</span></span>

<span data-ttu-id="44164-111">Sur **[IOSTX::SyncBeg](iostx-syncbeg.md)**, la boutique locale entre dans l’état d’en-tête [du message de téléchargement.](download-message-header-state.md)</span><span class="sxs-lookup"><span data-stu-id="44164-111">Upon **[IOSTX::SyncBeg](iostx-syncbeg.md)**, the local store enters the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="44164-112">Le client télécharge un élément de message complet (comme *pmsgFull* dans **[HDRSYNC).](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="44164-112">The client downloads a full message item (as  *pmsgFull*  in **[HDRSYNC](hdrsync.md)** ).</span></span> <span data-ttu-id="44164-113">Si cela réussit, le client définit également  *ulFlags*  dans **HDRSYNC** comme **HSF_OK**.</span><span class="sxs-lookup"><span data-stu-id="44164-113">If this is successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="44164-114">Sur **IOSTX::SyncHdrEnd**, Outlook vérifie le résultat dans **HDRSYNC** et utilise *pprog* et les informations dans **HDRSYNC** pour mettre à jour l’en-tête de message local.</span><span class="sxs-lookup"><span data-stu-id="44164-114">Upon **IOSTX::SyncHdrEnd**, Outlook checks the result in **HDRSYNC** and uses  *pprog*  and the information in **HDRSYNC** to update the local message header.</span></span> 
  
<span data-ttu-id="44164-115">Le magasin local revient à l’état dans le précédent **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span><span class="sxs-lookup"><span data-stu-id="44164-115">The local store returns to the state it was in before the preceding **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="44164-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44164-116">See also</span></span>



[<span data-ttu-id="44164-117">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="44164-117">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="44164-118">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="44164-118">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="44164-119">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="44164-119">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="44164-120">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="44164-120">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="44164-121">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="44164-121">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="44164-122">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="44164-122">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="44164-123">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="44164-123">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="44164-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="44164-124">MAPI Constants</span></span>](mapi-constants.md)

