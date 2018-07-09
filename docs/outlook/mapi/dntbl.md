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
ms.openlocfilehash: 6096118d72dfc51fb60025a55f581ebf97b000a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783213"
---
# <a name="dntbl"></a><span data-ttu-id="7ab2b-103">DNTBL</span><span class="sxs-lookup"><span data-stu-id="7ab2b-103">DNTBL</span></span>
 
<span data-ttu-id="7ab2b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7ab2b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7ab2b-105">Informations pour le téléchargement du contenu d’un dossier à partir du serveur au cours de l' [état de la table du téléchargement](download-table-state.md), dans le cadre d’une synchronisation complète pour le contenu sur un magasin.</span><span class="sxs-lookup"><span data-stu-id="7ab2b-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md), as part of a full synchronization for contents on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7ab2b-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7ab2b-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="7ab2b-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7ab2b-107">Members</span></span>

<span data-ttu-id="7ab2b-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7ab2b-108">_ulFlags_</span></span>
  
> <span data-ttu-id="7ab2b-109">[in] Indicateurs pour modifier le comportement</span><span class="sxs-lookup"><span data-stu-id="7ab2b-109">[in] Flags to modify behavior</span></span> 
    
  - <span data-ttu-id="7ab2b-110">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="7ab2b-110">DNT_OK</span></span>
    
    - <span data-ttu-id="7ab2b-111">[in] Téléchargement a réussi.</span><span class="sxs-lookup"><span data-stu-id="7ab2b-111">[in] Download was successful.</span></span> <span data-ttu-id="7ab2b-112">Le client définit après le téléchargement des informations à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="7ab2b-112">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="7ab2b-113">_pstmReserved1_</span><span class="sxs-lookup"><span data-stu-id="7ab2b-113">_pstmReserved1_</span></span>
  
> <span data-ttu-id="7ab2b-114">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7ab2b-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="7ab2b-115">_pstmReserved2_</span><span class="sxs-lookup"><span data-stu-id="7ab2b-115">_pstmReserved2_</span></span>
  
> <span data-ttu-id="7ab2b-116">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7ab2b-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="7ab2b-117">_pstmReserved3_</span><span class="sxs-lookup"><span data-stu-id="7ab2b-117">_pstmReserved3_</span></span>
  
> <span data-ttu-id="7ab2b-118">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7ab2b-118">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="7ab2b-119">_pstmReserved4_</span><span class="sxs-lookup"><span data-stu-id="7ab2b-119">_pstmReserved4_</span></span>
  
> <span data-ttu-id="7ab2b-120">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7ab2b-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="7ab2b-121">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="7ab2b-121">_pxicc_</span></span>
  
>  <span data-ttu-id="7ab2b-122">[out] Pointeur vers l’interface de contenu **IExchangeImportContentsChanges** qui prend en charge le téléchargement des modifications de contenu.</span><span class="sxs-lookup"><span data-stu-id="7ab2b-122">[out] Pointer to the **IExchangeImportContentsChanges** contents interface that supports downloading content changes.</span></span> <span data-ttu-id="7ab2b-123">Pour plus d’informations sur **IExchangeImportContentsChanges**, voir [Critères d’évaluation de partage de connexion Internet](http://msdn.microsoft.com/fr-fr/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7ab2b-123">For more information on **IExchangeImportContentsChanges**, see [ICS Evaluation Criteria](http://msdn.microsoft.com/fr-fr/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="7ab2b-124">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="7ab2b-124">_pxihc_</span></span>
  
>  <span data-ttu-id="7ab2b-125">[out] Pointeur vers l’interface de hiérarchie **IExchangeImportHierarchyChanges** qui prend en charge le téléchargement des modifications incrémentielles de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="7ab2b-125">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="7ab2b-126">Pour plus d’informations sur **IExchangeImportHierarchyChanges**, voir [Critères d’évaluation de partage de connexion Internet](http://msdn.microsoft.com/fr-fr/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7ab2b-126">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](http://msdn.microsoft.com/fr-fr/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="7ab2b-127">_pszName_</span><span class="sxs-lookup"><span data-stu-id="7ab2b-127">_pszName_</span></span>
  
>  <span data-ttu-id="7ab2b-128">[out] Nom du dossier.</span><span class="sxs-lookup"><span data-stu-id="7ab2b-128">[out] Name of the folder.</span></span> 
    
<span data-ttu-id="7ab2b-129">_ftLastMod_</span><span class="sxs-lookup"><span data-stu-id="7ab2b-129">_ftLastMod_</span></span>
  
>  <span data-ttu-id="7ab2b-130">[out] Heure de dernière modification du dossier.</span><span class="sxs-lookup"><span data-stu-id="7ab2b-130">[out] Last modification time of the folder.</span></span> 
    
<span data-ttu-id="7ab2b-131">_ulRights_</span><span class="sxs-lookup"><span data-stu-id="7ab2b-131">_ulRights_</span></span>
  
>  <span data-ttu-id="7ab2b-132">[out] Valeur de la propriété **[PR_RIGHTS](http://msdn.microsoft.com/fr-fr/library/ee238052%28v=EXCHG.80%29.aspx)** du dossier.</span><span class="sxs-lookup"><span data-stu-id="7ab2b-132">[out] Value of the **[PR_RIGHTS](http://msdn.microsoft.com/fr-fr/library/ee238052%28v=EXCHG.80%29.aspx)** property of the folder.</span></span> 
    
<span data-ttu-id="7ab2b-133">_feid_</span><span class="sxs-lookup"><span data-stu-id="7ab2b-133">_feid_</span></span>
  
>  <span data-ttu-id="7ab2b-134">[out] ID d’entrée du dossier.</span><span class="sxs-lookup"><span data-stu-id="7ab2b-134">[out] Entry ID of the folder.</span></span> 
    
<span data-ttu-id="7ab2b-135">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="7ab2b-135">_uintReserved_</span></span>
  
>  <span data-ttu-id="7ab2b-136">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7ab2b-136">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="7ab2b-137">_rgte_</span><span class="sxs-lookup"><span data-stu-id="7ab2b-137">_rgte_</span></span>
  
> <span data-ttu-id="7ab2b-138">[out] Modifications normal (ou non masqués) et les éléments associés (ou masqués).</span><span class="sxs-lookup"><span data-stu-id="7ab2b-138">[out] Changes for normal (or non-hidden) and associated (or hidden) items.</span></span>  <span data-ttu-id="7ab2b-139">*rgte [0]* est pour les éléments normales et *rgte [1]* est des éléments associés.</span><span class="sxs-lookup"><span data-stu-id="7ab2b-139">*rgte[0]*  is for normal items, and  *rgte[1]*  is for associated items.</span></span> <span data-ttu-id="7ab2b-140">Outlook remplit ce membre pendant le téléchargement lors de l’utilisation de la synchronisation de modification incrémentielle (ICS).</span><span class="sxs-lookup"><span data-stu-id="7ab2b-140">Outlook populates this member during the downloading when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="7ab2b-141">Pour plus d’informations sur le partage de connexion Internet, voir [Critères d’évaluation de partage de connexion Internet](http://msdn.microsoft.com/fr-fr/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7ab2b-141">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/fr-fr/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="7ab2b-142">_lpsrReserved_</span><span class="sxs-lookup"><span data-stu-id="7ab2b-142">_lpsrReserved_</span></span>
  
>  <span data-ttu-id="7ab2b-143">[in] / [out] ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7ab2b-143">[in]/[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="7ab2b-144">_boReserved_</span><span class="sxs-lookup"><span data-stu-id="7ab2b-144">_boReserved_</span></span>
  
>  <span data-ttu-id="7ab2b-145">[in] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7ab2b-145">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="7ab2b-146">_pReserved1_</span><span class="sxs-lookup"><span data-stu-id="7ab2b-146">_pReserved1_</span></span>
  
>  <span data-ttu-id="7ab2b-147">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7ab2b-147">[out]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="7ab2b-148">_pReserved2_</span><span class="sxs-lookup"><span data-stu-id="7ab2b-148">_pReserved2_</span></span>
  
>  <span data-ttu-id="7ab2b-149">[in] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7ab2b-149">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7ab2b-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ab2b-150">See also</span></span>

- [<span data-ttu-id="7ab2b-151">Sur l’ordinateur de l’état de réplication</span><span class="sxs-lookup"><span data-stu-id="7ab2b-151">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)  
- [<span data-ttu-id="7ab2b-152">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="7ab2b-152">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="7ab2b-153">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="7ab2b-153">DNTBLE</span></span>](dntble.md)

