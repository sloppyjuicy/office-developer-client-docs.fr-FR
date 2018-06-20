---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: 'Derni�re modification�: jeudi 5 juillet 2012'
ms.openlocfilehash: 3c7d59849fcd66a5fe90623b7bb8516d13b4a2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783214"
---
# <a name="dnhier"></a><span data-ttu-id="a7401-103">DNHIER</span><span class="sxs-lookup"><span data-stu-id="a7401-103">DNHIER</span></span>

<span data-ttu-id="a7401-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a7401-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a7401-105">Informations pour le téléchargement une hiérarchie à partir du serveur au cours de l' [état de la hiérarchie du téléchargement](download-hierarchy-state.md), qui fait partie d’une synchronisation complète de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="a7401-105">Information for downloading a hierarchy from the server during the [download hierarchy state](download-hierarchy-state.md), which is part of a full hierarchy synchronization.</span></span> <span data-ttu-id="a7401-106">Ce processus de téléchargement utilise la synchronisation modification incrémentielle (ICS) de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="a7401-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="a7401-107">Pour plus d’informations sur le partage de connexion Internet, voir [Critères d’évaluation de partage de connexion Internet](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a7401-107">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a7401-108">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="a7401-108">Quick info</span></span>

```cpp
struct DNHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    PXIHC pxihc; 
    UINT cEntNew; 
   UINT cEntMod; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="a7401-109">Membres</span><span class="sxs-lookup"><span data-stu-id="a7401-109">Members</span></span>

<span data-ttu-id="a7401-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a7401-110">_ulFlags_</span></span>
  
>  <span data-ttu-id="a7401-111">[in] Indicateurs pour déterminer le comportement approprié lors du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="a7401-111">[in] Flags to determine the appropriate behavior during the download.</span></span> 
    
   - <span data-ttu-id="a7401-112">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="a7401-112">DNH_OK</span></span>
    
   - <span data-ttu-id="a7401-113">[in] Téléchargement a réussi.</span><span class="sxs-lookup"><span data-stu-id="a7401-113">[in] Download was successful.</span></span> <span data-ttu-id="a7401-114">Le client définit après le téléchargement des informations à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="a7401-114">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="a7401-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="a7401-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="a7401-116">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a7401-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="a7401-117">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="a7401-117">_pxihc_</span></span>
  
>  <span data-ttu-id="a7401-118">[out] Pointeur vers l’interface de hiérarchie **IExchangeImportHierarchyChanges** qui prend en charge le téléchargement des modifications incrémentielles de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="a7401-118">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="a7401-119">Pour plus d’informations sur **IExchangeImportHierarchyChanges**, voir [Critères d’évaluation de partage de connexion Internet](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a7401-119">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="a7401-120">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="a7401-120">_cEntNew_</span></span>
  
> <span data-ttu-id="a7401-121">[out] Nombre de dossiers ajoutés dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="a7401-121">[out] Number of folders added to the local store.</span></span> <span data-ttu-id="a7401-122">Outlook remplit cette valeur pendant le téléchargement lors de l’utilisation du partage de connexion Internet.</span><span class="sxs-lookup"><span data-stu-id="a7401-122">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="a7401-123">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="a7401-123">_cEntMod_</span></span>
  
> <span data-ttu-id="a7401-124">[out] Nombre de dossiers à modifier dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="a7401-124">[out] Number of folders to be modified on the local store.</span></span> <span data-ttu-id="a7401-125">Outlook remplit cette valeur pendant le téléchargement lors de l’utilisation du partage de connexion Internet.</span><span class="sxs-lookup"><span data-stu-id="a7401-125">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="a7401-126">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="a7401-126">_cEntDel_</span></span>
  
> <span data-ttu-id="a7401-127">[out] Nombre de dossiers à supprimer dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="a7401-127">[out] Number of folders to be deleted on the local store.</span></span> <span data-ttu-id="a7401-128">Outlook remplit cette valeur pendant le téléchargement lors de l’utilisation du partage de connexion Internet.</span><span class="sxs-lookup"><span data-stu-id="a7401-128">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7401-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7401-129">See also</span></span>

- [<span data-ttu-id="a7401-130">Sur l’ordinateur de l’état de réplication</span><span class="sxs-lookup"><span data-stu-id="a7401-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md) 
- [<span data-ttu-id="a7401-131">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="a7401-131">MAPI Constants</span></span>](mapi-constants.md)

