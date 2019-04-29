---
title: IPSTXGetSyncObject
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetSyncObject
api_type:
- COM
ms.assetid: b93dae79-4305-9a3a-7b93-42319f7e26ba
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 31ef1f5c6af498f042ab766ae90fcfbce805700a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407108"
---
# <a name="ipstxgetsyncobject"></a><span data-ttu-id="e93cf-103">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="e93cf-103">IPSTX::GetSyncObject</span></span>

  
  
<span data-ttu-id="e93cf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e93cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e93cf-105">Démarre une session de synchronisation et obtient l'interface **[IOSTX](iostxiunknown.md)** associée.</span><span class="sxs-lookup"><span data-stu-id="e93cf-105">Starts a synchronization session and gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a><span data-ttu-id="e93cf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e93cf-106">Parameters</span></span>

 <span data-ttu-id="e93cf-107">_ppostx_</span><span class="sxs-lookup"><span data-stu-id="e93cf-107">_ppostx_</span></span>
  
>  <span data-ttu-id="e93cf-108">remarquer Pointeur vers l'interface **IOSTX** à obtenir.</span><span class="sxs-lookup"><span data-stu-id="e93cf-108">[out] Pointer to the **IOSTX** interface to get.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e93cf-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="e93cf-109">Remarks</span></span>

<span data-ttu-id="e93cf-110">L'appelant doit s'assurer que le même dossier n'est pas synchronisé en même temps sur plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="e93cf-110">The caller must ensure that the same folder is not synchronized at the same time on more than one thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e93cf-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e93cf-111">See also</span></span>



[<span data-ttu-id="e93cf-112">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="e93cf-112">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="e93cf-113">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="e93cf-113">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)

