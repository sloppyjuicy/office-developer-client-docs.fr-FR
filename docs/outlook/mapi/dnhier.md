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
ms.openlocfilehash: 06f30b4856fc10127aec99975652e28a5e8dda30
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389084"
---
# <a name="dnhier"></a><span data-ttu-id="f5d18-103">DNHIER</span><span class="sxs-lookup"><span data-stu-id="f5d18-103">DNHIER</span></span>

<span data-ttu-id="f5d18-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5d18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5d18-105">Informations pour le téléchargement une hiérarchie à partir du serveur au cours de l' [état de la hiérarchie du téléchargement](download-hierarchy-state.md), qui fait partie d’une synchronisation complète de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="f5d18-105">Information for downloading a hierarchy from the server during the [download hierarchy state](download-hierarchy-state.md), which is part of a full hierarchy synchronization.</span></span> <span data-ttu-id="f5d18-106">Ce processus de téléchargement utilise la synchronisation modification incrémentielle (ICS) de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="f5d18-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="f5d18-107">Pour plus d’informations sur le partage de connexion Internet, voir [Critères d’évaluation de partage de connexion Internet](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5d18-107">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f5d18-108">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="f5d18-108">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="f5d18-109">Members</span><span class="sxs-lookup"><span data-stu-id="f5d18-109">Members</span></span>

<span data-ttu-id="f5d18-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f5d18-110">_ulFlags_</span></span>
  
>  <span data-ttu-id="f5d18-111">[in] Indicateurs pour déterminer le comportement approprié lors du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="f5d18-111">[in] Flags to determine the appropriate behavior during the download.</span></span> 
    
   - <span data-ttu-id="f5d18-112">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="f5d18-112">DNH_OK</span></span>
    
   - <span data-ttu-id="f5d18-113">[in] Téléchargement a réussi.</span><span class="sxs-lookup"><span data-stu-id="f5d18-113">[in] Download was successful.</span></span> <span data-ttu-id="f5d18-114">Le client définit après le téléchargement des informations à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="f5d18-114">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="f5d18-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="f5d18-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="f5d18-116">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f5d18-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="f5d18-117">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="f5d18-117">_pxihc_</span></span>
  
>  <span data-ttu-id="f5d18-118">[out] Pointeur vers l’interface de hiérarchie **IExchangeImportHierarchyChanges** qui prend en charge le téléchargement des modifications incrémentielles de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="f5d18-118">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="f5d18-119">Pour plus d’informations sur **IExchangeImportHierarchyChanges**, voir [Critères d’évaluation de partage de connexion Internet](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5d18-119">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="f5d18-120">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="f5d18-120">_cEntNew_</span></span>
  
> <span data-ttu-id="f5d18-121">[out] Nombre de dossiers ajoutés dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="f5d18-121">[out] Number of folders added to the local store.</span></span> <span data-ttu-id="f5d18-122">Outlook remplit cette valeur pendant le téléchargement lors de l’utilisation du partage de connexion Internet.</span><span class="sxs-lookup"><span data-stu-id="f5d18-122">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="f5d18-123">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="f5d18-123">_cEntMod_</span></span>
  
> <span data-ttu-id="f5d18-124">[out] Nombre de dossiers à modifier dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="f5d18-124">[out] Number of folders to be modified on the local store.</span></span> <span data-ttu-id="f5d18-125">Outlook remplit cette valeur pendant le téléchargement lors de l’utilisation du partage de connexion Internet.</span><span class="sxs-lookup"><span data-stu-id="f5d18-125">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="f5d18-126">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="f5d18-126">_cEntDel_</span></span>
  
> <span data-ttu-id="f5d18-127">[out] Nombre de dossiers à supprimer dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="f5d18-127">[out] Number of folders to be deleted on the local store.</span></span> <span data-ttu-id="f5d18-128">Outlook remplit cette valeur pendant le téléchargement lors de l’utilisation du partage de connexion Internet.</span><span class="sxs-lookup"><span data-stu-id="f5d18-128">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5d18-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5d18-129">See also</span></span>

- [<span data-ttu-id="f5d18-130">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="f5d18-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md) 
- [<span data-ttu-id="f5d18-131">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="f5d18-131">MAPI Constants</span></span>](mapi-constants.md)

