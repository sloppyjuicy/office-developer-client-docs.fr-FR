---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: 'Derni�re modification�: jeudi 5 juillet 2012'
ms.openlocfilehash: 4716a6f42968d7451a5db36173c4e6a9e843c08e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398121"
---
# <a name="dntbl"></a><span data-ttu-id="c5a16-103">DNTBL</span><span class="sxs-lookup"><span data-stu-id="c5a16-103">DNTBL</span></span>
 
<span data-ttu-id="c5a16-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5a16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5a16-105">Informations pour le téléchargement du contenu d’un dossier à partir du serveur au cours de l' [état de la table du téléchargement](download-table-state.md), dans le cadre d’une synchronisation complète pour le contenu sur un magasin.</span><span class="sxs-lookup"><span data-stu-id="c5a16-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md), as part of a full synchronization for contents on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c5a16-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="c5a16-106">Quick info</span></span>

```cpp
struct DNTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved1; 
    LPSTREAM pstmReserved2; 
    LPSTREAM pstmReserved3; 
    LPSTREAM pstmReserved4; 
    PXICC pxicc; 
    PXIHC pxihc; 
    LPSTR pszName; 
    FILETIME ftLastMod; 
    ULONG ulRights; 
    FEID feid; 
    UINT uintReserved; 
    DNTBLE rgte[2]; 
    LPSRestriction psrReserved; 
    BOOL boReserved; 
    void* pReserved1; 
    void* pReserved2; 
};

```

## <a name="members"></a><span data-ttu-id="c5a16-107">Members</span><span class="sxs-lookup"><span data-stu-id="c5a16-107">Members</span></span>

<span data-ttu-id="c5a16-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c5a16-108">_ulFlags_</span></span>
  
> <span data-ttu-id="c5a16-109">[in] Indicateurs pour modifier le comportement</span><span class="sxs-lookup"><span data-stu-id="c5a16-109">[in] Flags to modify behavior</span></span> 
    
  - <span data-ttu-id="c5a16-110">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="c5a16-110">DNT_OK</span></span>
    
    - <span data-ttu-id="c5a16-111">[in] Téléchargement a réussi.</span><span class="sxs-lookup"><span data-stu-id="c5a16-111">[in] Download was successful.</span></span> <span data-ttu-id="c5a16-112">Le client définit après le téléchargement des informations à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="c5a16-112">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="c5a16-113">_pstmReserved1_</span><span class="sxs-lookup"><span data-stu-id="c5a16-113">_pstmReserved1_</span></span>
  
> <span data-ttu-id="c5a16-114">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c5a16-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="c5a16-115">_pstmReserved2_</span><span class="sxs-lookup"><span data-stu-id="c5a16-115">_pstmReserved2_</span></span>
  
> <span data-ttu-id="c5a16-116">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c5a16-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="c5a16-117">_pstmReserved3_</span><span class="sxs-lookup"><span data-stu-id="c5a16-117">_pstmReserved3_</span></span>
  
> <span data-ttu-id="c5a16-118">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c5a16-118">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="c5a16-119">_pstmReserved4_</span><span class="sxs-lookup"><span data-stu-id="c5a16-119">_pstmReserved4_</span></span>
  
> <span data-ttu-id="c5a16-120">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c5a16-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="c5a16-121">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="c5a16-121">_pxicc_</span></span>
  
>  <span data-ttu-id="c5a16-122">[out] Pointeur vers l’interface de contenu **IExchangeImportContentsChanges** qui prend en charge le téléchargement des modifications de contenu.</span><span class="sxs-lookup"><span data-stu-id="c5a16-122">[out] Pointer to the **IExchangeImportContentsChanges** contents interface that supports downloading content changes.</span></span> <span data-ttu-id="c5a16-123">Pour plus d’informations sur **IExchangeImportContentsChanges**, voir [Critères d’évaluation de partage de connexion Internet](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c5a16-123">For more information on **IExchangeImportContentsChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="c5a16-124">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="c5a16-124">_pxihc_</span></span>
  
>  <span data-ttu-id="c5a16-125">[out] Pointeur vers l’interface de hiérarchie **IExchangeImportHierarchyChanges** qui prend en charge le téléchargement des modifications incrémentielles de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="c5a16-125">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="c5a16-126">Pour plus d’informations sur **IExchangeImportHierarchyChanges**, voir [Critères d’évaluation de partage de connexion Internet](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c5a16-126">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="c5a16-127">_pszName_</span><span class="sxs-lookup"><span data-stu-id="c5a16-127">_pszName_</span></span>
  
>  <span data-ttu-id="c5a16-128">[out] Nom du dossier.</span><span class="sxs-lookup"><span data-stu-id="c5a16-128">[out] Name of the folder.</span></span> 
    
<span data-ttu-id="c5a16-129">_ftLastMod_</span><span class="sxs-lookup"><span data-stu-id="c5a16-129">_ftLastMod_</span></span>
  
>  <span data-ttu-id="c5a16-130">[out] Heure de dernière modification du dossier.</span><span class="sxs-lookup"><span data-stu-id="c5a16-130">[out] Last modification time of the folder.</span></span> 
    
<span data-ttu-id="c5a16-131">_ulRights_</span><span class="sxs-lookup"><span data-stu-id="c5a16-131">_ulRights_</span></span>
  
>  <span data-ttu-id="c5a16-132">[out] Valeur de la propriété **[PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx)** du dossier.</span><span class="sxs-lookup"><span data-stu-id="c5a16-132">[out] Value of the **[PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx)** property of the folder.</span></span> 
    
<span data-ttu-id="c5a16-133">_feid_</span><span class="sxs-lookup"><span data-stu-id="c5a16-133">_feid_</span></span>
  
>  <span data-ttu-id="c5a16-134">[out] ID d’entrée du dossier.</span><span class="sxs-lookup"><span data-stu-id="c5a16-134">[out] Entry ID of the folder.</span></span> 
    
<span data-ttu-id="c5a16-135">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="c5a16-135">_uintReserved_</span></span>
  
>  <span data-ttu-id="c5a16-136">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c5a16-136">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="c5a16-137">_rgte_</span><span class="sxs-lookup"><span data-stu-id="c5a16-137">_rgte_</span></span>
  
> <span data-ttu-id="c5a16-138">[out] Modifications normal (ou non masqués) et les éléments associés (ou masqués).</span><span class="sxs-lookup"><span data-stu-id="c5a16-138">[out] Changes for normal (or non-hidden) and associated (or hidden) items.</span></span>  <span data-ttu-id="c5a16-139">*rgte [0]* est pour les éléments normales et *rgte [1]* est des éléments associés.</span><span class="sxs-lookup"><span data-stu-id="c5a16-139">*rgte[0]*  is for normal items, and  *rgte[1]*  is for associated items.</span></span> <span data-ttu-id="c5a16-140">Outlook remplit ce membre pendant le téléchargement lors de l’utilisation de la synchronisation de modification incrémentielle (ICS).</span><span class="sxs-lookup"><span data-stu-id="c5a16-140">Outlook populates this member during the downloading when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="c5a16-141">Pour plus d’informations sur le partage de connexion Internet, voir [Critères d’évaluation de partage de connexion Internet](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="c5a16-141">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="c5a16-142">_lpsrReserved_</span><span class="sxs-lookup"><span data-stu-id="c5a16-142">_lpsrReserved_</span></span>
  
>  <span data-ttu-id="c5a16-143">[in] / [out] ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c5a16-143">[in]/[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="c5a16-144">_boReserved_</span><span class="sxs-lookup"><span data-stu-id="c5a16-144">_boReserved_</span></span>
  
>  <span data-ttu-id="c5a16-145">[in] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c5a16-145">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="c5a16-146">_pReserved1_</span><span class="sxs-lookup"><span data-stu-id="c5a16-146">_pReserved1_</span></span>
  
>  <span data-ttu-id="c5a16-147">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c5a16-147">[out]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="c5a16-148">_pReserved2_</span><span class="sxs-lookup"><span data-stu-id="c5a16-148">_pReserved2_</span></span>
  
>  <span data-ttu-id="c5a16-149">[in] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c5a16-149">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c5a16-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5a16-150">See also</span></span>

- [<span data-ttu-id="c5a16-151">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="c5a16-151">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)  
- [<span data-ttu-id="c5a16-152">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="c5a16-152">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="c5a16-153">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="c5a16-153">DNTBLE</span></span>](dntble.md)

