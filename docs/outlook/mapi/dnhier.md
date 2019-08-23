---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: 'Dernière modification : 05 juillet 2012'
ms.openlocfilehash: 06f30b4856fc10127aec99975652e28a5e8dda30
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337099"
---
# <a name="dnhier"></a><span data-ttu-id="57800-103">DNHIER</span><span class="sxs-lookup"><span data-stu-id="57800-103">DNHIER</span></span>

<span data-ttu-id="57800-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57800-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57800-105">Informations relatives au téléchargement d’une hiérarchie à partir du serveur pendant le [téléchargement de l’état de la hiérarchie](download-hierarchy-state.md), qui fait partie d’une synchronisation de la hiérarchie complète.</span><span class="sxs-lookup"><span data-stu-id="57800-105">Information for downloading a hierarchy from the server during the [download hierarchy state](download-hierarchy-state.md), which is part of a full hierarchy synchronization.</span></span> <span data-ttu-id="57800-106">Ce processus de téléchargement utilise une méthode de synchronisation des modifications incrémentielle (ICS) de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="57800-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="57800-107">Pour plus d’informations sur ICS, reportez-vous à [Critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="57800-107">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="57800-108">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="57800-108">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="57800-109">Membres</span><span class="sxs-lookup"><span data-stu-id="57800-109">Members</span></span>

<span data-ttu-id="57800-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="57800-110">_ulFlags_</span></span>
  
>  <span data-ttu-id="57800-111">[entrant] Indicateurs permettant de déterminer le comportement approprié pendant le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="57800-111">[in] Flags to determine the appropriate behavior during the download.</span></span> 
    
   - <span data-ttu-id="57800-112">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="57800-112">DNH_OK</span></span>
    
   - <span data-ttu-id="57800-113">[entrant] Téléchargement réussi.</span><span class="sxs-lookup"><span data-stu-id="57800-113">[in] Download was successful.</span></span> <span data-ttu-id="57800-114">Le client définit cet élément après avoir téléchargé des informations à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="57800-114">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="57800-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="57800-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="57800-116">[sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="57800-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="57800-117">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="57800-117">_pxihc_</span></span>
  
>  <span data-ttu-id="57800-118">[sortant] Pointeur vers l’interface de hiérarchie **IExchangeImportHierarchyChanges** qui prend en charge le téléchargement des modifications de hiérarchie incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="57800-118">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="57800-119">Pour plus d’informations sur **IExchangeImportHierarchyChanges**, reportez-vous à [Critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="57800-119">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="57800-120">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="57800-120">_cEntNew_</span></span>
  
> <span data-ttu-id="57800-121">[sortant] Nombre de dossiers ajoutés à la banque locale.</span><span class="sxs-lookup"><span data-stu-id="57800-121">[out] Number of folders added to the local store.</span></span> <span data-ttu-id="57800-122">Outlook renseigne cette valeur pendant le téléchargement lors de l’utilisation d’ICS.</span><span class="sxs-lookup"><span data-stu-id="57800-122">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="57800-123">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="57800-123">_cEntMod_</span></span>
  
> <span data-ttu-id="57800-124">[sortant] Nombre de dossiers à modifier dans la banque locale.</span><span class="sxs-lookup"><span data-stu-id="57800-124">[out] Number of folders to be modified on the local store.</span></span> <span data-ttu-id="57800-125">Outlook renseigne cette valeur pendant le téléchargement lors de l’utilisation d’ICS.</span><span class="sxs-lookup"><span data-stu-id="57800-125">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="57800-126">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="57800-126">_cEntDel_</span></span>
  
> <span data-ttu-id="57800-127">[sortant] Nombre de dossiers à supprimer de la banque locale.</span><span class="sxs-lookup"><span data-stu-id="57800-127">[out] Number of folders to be deleted on the local store.</span></span> <span data-ttu-id="57800-128">Outlook renseigne cette valeur pendant le téléchargement lors de l’utilisation d’ICS.</span><span class="sxs-lookup"><span data-stu-id="57800-128">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="57800-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57800-129">See also</span></span>

- [<span data-ttu-id="57800-130">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="57800-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md) 
- [<span data-ttu-id="57800-131">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="57800-131">MAPI Constants</span></span>](mapi-constants.md)

