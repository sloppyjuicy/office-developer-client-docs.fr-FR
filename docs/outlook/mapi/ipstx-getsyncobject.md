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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 31ef1f5c6af498f042ab766ae90fcfbce805700a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315084"
---
# <a name="ipstxgetsyncobject"></a><span data-ttu-id="40fc8-103">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="40fc8-103">IPSTX::GetSyncObject</span></span>

  
  
<span data-ttu-id="40fc8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40fc8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="40fc8-105">Démarre une session de synchronisation et obtient l'interface **[IOSTX](iostxiunknown.md)** associée.</span><span class="sxs-lookup"><span data-stu-id="40fc8-105">Starts a synchronization session and gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a><span data-ttu-id="40fc8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40fc8-106">Parameters</span></span>

 <span data-ttu-id="40fc8-107">_ppostx_</span><span class="sxs-lookup"><span data-stu-id="40fc8-107">_ppostx_</span></span>
  
>  <span data-ttu-id="40fc8-108">remarquer Pointeur vers l'interface **IOSTX** à obtenir.</span><span class="sxs-lookup"><span data-stu-id="40fc8-108">[out] Pointer to the **IOSTX** interface to get.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="40fc8-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="40fc8-109">Remarks</span></span>

<span data-ttu-id="40fc8-110">L'appelant doit s'assurer que le même dossier n'est pas synchronisé en même temps sur plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="40fc8-110">The caller must ensure that the same folder is not synchronized at the same time on more than one thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="40fc8-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40fc8-111">See also</span></span>



[<span data-ttu-id="40fc8-112">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="40fc8-112">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="40fc8-113">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="40fc8-113">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)

