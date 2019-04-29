---
title: IOSTXSyncHdrBeg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrBeg
api_type:
- COM
ms.assetid: 7f8ca7cf-ac0b-9b77-c1dd-9f1d0871d603
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 49ef9862d5156a1bed242652df32baab9a0123fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405092"
---
# <a name="iostxsynchdrbeg"></a><span data-ttu-id="890e4-103">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="890e4-103">IOSTX::SyncHdrBeg</span></span>

  
  
<span data-ttu-id="890e4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="890e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="890e4-105">Démarre la synchronisation pour un en-tête de message.</span><span class="sxs-lookup"><span data-stu-id="890e4-105">Starts synchronization for a message header.</span></span>
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a><span data-ttu-id="890e4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="890e4-106">Parameters</span></span>

 <span data-ttu-id="890e4-107">_cbeid_</span><span class="sxs-lookup"><span data-stu-id="890e4-107">_cbeid_</span></span>
  
> <span data-ttu-id="890e4-108">dans Nombre d'octets dans l'ID d'entrée du message.</span><span class="sxs-lookup"><span data-stu-id="890e4-108">[in] The number of bytes in the entry ID for the message.</span></span>
    
 <span data-ttu-id="890e4-109">_lpeid_</span><span class="sxs-lookup"><span data-stu-id="890e4-109">_lpeid_</span></span>
  
> <span data-ttu-id="890e4-110">dans ID d'entrée du message.</span><span class="sxs-lookup"><span data-stu-id="890e4-110">[in] The entry ID for the message.</span></span>
    
 <span data-ttu-id="890e4-111">_PPV_</span><span class="sxs-lookup"><span data-stu-id="890e4-111">_ppv_</span></span>
  
>  <span data-ttu-id="890e4-112">[in]/[out] pointeur vers la structure **[HDRSYNC](hdrsync.md)** pour l'en-tête de message.</span><span class="sxs-lookup"><span data-stu-id="890e4-112">[in]/[out] Pointer to the **[HDRSYNC](hdrsync.md)** structure for the message header.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="890e4-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="890e4-113">Remarks</span></span>

<span data-ttu-id="890e4-114">Sur **IOSTX:: SyncHdrBeg**, le magasin local passe à l' [État d'en-tête du message de téléchargement](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="890e4-114">Upon **IOSTX::SyncHdrBeg**, the local store transitions to the [download message header state](download-message-header-state.md).</span></span> <span data-ttu-id="890e4-115">Outlook initialise pour le client la structure **HDRSYNC** avec la représentation actuelle de l'en-tête du message dans le magasin et le dossier parent.</span><span class="sxs-lookup"><span data-stu-id="890e4-115">Outlook initializes for the client the **HDRSYNC** structure with the current representation of the message header in the store and the parent folder.</span></span> <span data-ttu-id="890e4-116">Le client doit ensuite télécharger un élément de message complet (en tant que *pmsgFull* dans **HDRSYNC** ).</span><span class="sxs-lookup"><span data-stu-id="890e4-116">The client must then download a full message item (as  *pmsgFull*  in **HDRSYNC** ).</span></span> <span data-ttu-id="890e4-117">Si cette opération réussit, le client définit également *ulFlags* dans **HDRSYNC** en tant que **HSF_OK**.</span><span class="sxs-lookup"><span data-stu-id="890e4-117">If this was successful, the client also sets  *ulFlags*  in **HDRSYNC** as **HSF_OK**.</span></span> <span data-ttu-id="890e4-118">Sur **[IOSTX:: SyncHdrEnd](iostx-synchdrend.md)**, Outlook vérifie le résultat dans **HDRSYNC** et utilise les informations de **HDRSYNC** pour mettre à jour l'en-tête de message local.</span><span class="sxs-lookup"><span data-stu-id="890e4-118">Upon **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)**, Outlook checks the result in **HDRSYNC** and uses the information in **HDRSYNC** to update the local message header.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="890e4-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="890e4-119">See also</span></span>



[<span data-ttu-id="890e4-120">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="890e4-120">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="890e4-121">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="890e4-121">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="890e4-122">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="890e4-122">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="890e4-123">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="890e4-123">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="890e4-124">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="890e4-124">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="890e4-125">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="890e4-125">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="890e4-126">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="890e4-126">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="890e4-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="890e4-127">MAPI Constants</span></span>](mapi-constants.md)

