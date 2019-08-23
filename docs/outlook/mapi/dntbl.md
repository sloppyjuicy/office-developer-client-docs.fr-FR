---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: 'Dernière modification : 05 juillet 2012'
ms.openlocfilehash: 4716a6f42968d7451a5db36173c4e6a9e843c08e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337001"
---
# <a name="dntbl"></a><span data-ttu-id="3bb82-103">DNTBL</span><span class="sxs-lookup"><span data-stu-id="3bb82-103">DNTBL</span></span>
 
<span data-ttu-id="3bb82-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3bb82-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3bb82-105">Informations relatives au téléchargement du contenu d’un dossier à partir du serveur pendant le [téléchargement de l’état de la table](download-table-state.md), dans le cadre d’une synchronisation complète du contenu dans une banque.</span><span class="sxs-lookup"><span data-stu-id="3bb82-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md), as part of a full synchronization for contents on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3bb82-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="3bb82-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="3bb82-107">Membres</span><span class="sxs-lookup"><span data-stu-id="3bb82-107">Members</span></span>

<span data-ttu-id="3bb82-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3bb82-108">_ulFlags_</span></span>
  
> <span data-ttu-id="3bb82-109">[entrant] Indicateurs permettant de modifier le comportement</span><span class="sxs-lookup"><span data-stu-id="3bb82-109">[in] Flags to modify behavior</span></span> 
    
  - <span data-ttu-id="3bb82-110">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="3bb82-110">DNT_OK</span></span>
    
    - <span data-ttu-id="3bb82-111">[entrant] Téléchargement réussi.</span><span class="sxs-lookup"><span data-stu-id="3bb82-111">[in] Download was successful.</span></span> <span data-ttu-id="3bb82-112">Le client définit cet élément après avoir téléchargé des informations à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="3bb82-112">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="3bb82-113">_pstmReserved1_</span><span class="sxs-lookup"><span data-stu-id="3bb82-113">_pstmReserved1_</span></span>
  
> <span data-ttu-id="3bb82-114">[sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3bb82-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="3bb82-115">_pstmReserved2_</span><span class="sxs-lookup"><span data-stu-id="3bb82-115">_pstmReserved2_</span></span>
  
> <span data-ttu-id="3bb82-116">[sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3bb82-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="3bb82-117">_pstmReserved3_</span><span class="sxs-lookup"><span data-stu-id="3bb82-117">_pstmReserved3_</span></span>
  
> <span data-ttu-id="3bb82-118">[sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3bb82-118">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="3bb82-119">_pstmReserved4_</span><span class="sxs-lookup"><span data-stu-id="3bb82-119">_pstmReserved4_</span></span>
  
> <span data-ttu-id="3bb82-120">[sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3bb82-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="3bb82-121">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="3bb82-121">_pxicc_</span></span>
  
>  <span data-ttu-id="3bb82-122">[sortant] Pointeur vers l’interface de contenu **IExchangeImportContentsChanges** prenant en charge le téléchargement des modifications de contenu.</span><span class="sxs-lookup"><span data-stu-id="3bb82-122">[out] Pointer to the **IExchangeImportContentsChanges** contents interface that supports downloading content changes.</span></span> <span data-ttu-id="3bb82-123">Pour plus d’informations sur **IExchangeImportContentsChanges**, reportez-vous à [Critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3bb82-123">For more information on **IExchangeImportContentsChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="3bb82-124">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="3bb82-124">_pxihc_</span></span>
  
>  <span data-ttu-id="3bb82-125">[sortant] Pointeur vers l’interface de hiérarchie **IExchangeImportHierarchyChanges** qui prend en charge le téléchargement des modifications de hiérarchie incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="3bb82-125">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="3bb82-126">Pour plus d’informations sur **IExchangeImportHierarchyChanges**, reportez-vous à [Critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3bb82-126">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="3bb82-127">_pszName_</span><span class="sxs-lookup"><span data-stu-id="3bb82-127">_pszName_</span></span>
  
>  <span data-ttu-id="3bb82-128">[sortant] Nom du dossier.</span><span class="sxs-lookup"><span data-stu-id="3bb82-128">[out] Name of the folder.</span></span> 
    
<span data-ttu-id="3bb82-129">_ftLastMod_</span><span class="sxs-lookup"><span data-stu-id="3bb82-129">_ftLastMod_</span></span>
  
>  <span data-ttu-id="3bb82-130">[sortant] Heure de la dernière modification du dossier.</span><span class="sxs-lookup"><span data-stu-id="3bb82-130">[out] Last modification time of the folder.</span></span> 
    
<span data-ttu-id="3bb82-131">_ulRights_</span><span class="sxs-lookup"><span data-stu-id="3bb82-131">_ulRights_</span></span>
  
>  <span data-ttu-id="3bb82-132">[sortant] Valeur de la propriété **[PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx)** du dossier.</span><span class="sxs-lookup"><span data-stu-id="3bb82-132">[out] Value of the **[PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx)** property of the folder.</span></span> 
    
<span data-ttu-id="3bb82-133">_feid_</span><span class="sxs-lookup"><span data-stu-id="3bb82-133">_feid_</span></span>
  
>  <span data-ttu-id="3bb82-134">[sortant] ID d’entrée du dossier.</span><span class="sxs-lookup"><span data-stu-id="3bb82-134">[out] Entry ID of the folder.</span></span> 
    
<span data-ttu-id="3bb82-135">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="3bb82-135">_uintReserved_</span></span>
  
>  <span data-ttu-id="3bb82-136">[sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3bb82-136">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="3bb82-137">_rgte_</span><span class="sxs-lookup"><span data-stu-id="3bb82-137">_rgte_</span></span>
  
> <span data-ttu-id="3bb82-138">[sortant] Modifications pour les éléments normaux (ou non masqués) et les éléments associés (ou masqués).</span><span class="sxs-lookup"><span data-stu-id="3bb82-138">[out] Changes for normal (or non-hidden) and associated (or hidden) items.</span></span>  <span data-ttu-id="3bb82-139">*rgte[0]* concerne les éléments normaux et *rgte[1]* concerne les éléments associés.</span><span class="sxs-lookup"><span data-stu-id="3bb82-139">*rgte[0]*  is for normal items, and  *rgte[1]*  is for associated items.</span></span> <span data-ttu-id="3bb82-140">Outlook renseigne ce membre pendant le téléchargement lors de l’utilisation de la synchronisation des modifications incrémentielle (ICS).</span><span class="sxs-lookup"><span data-stu-id="3bb82-140">Outlook populates this member during the downloading when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="3bb82-141">Pour plus d’informations sur ICS, reportez-vous à [Critères d’évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3bb82-141">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="3bb82-142">_lpsrReserved_</span><span class="sxs-lookup"><span data-stu-id="3bb82-142">_lpsrReserved_</span></span>
  
>  <span data-ttu-id="3bb82-143">[entrant]/[sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3bb82-143">[in]/[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="3bb82-144">_boReserved_</span><span class="sxs-lookup"><span data-stu-id="3bb82-144">_boReserved_</span></span>
  
>  <span data-ttu-id="3bb82-145">[entrant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3bb82-145">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="3bb82-146">_pReserved1_</span><span class="sxs-lookup"><span data-stu-id="3bb82-146">_pReserved1_</span></span>
  
>  <span data-ttu-id="3bb82-147">[sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3bb82-147">[out]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="3bb82-148">_pReserved2_</span><span class="sxs-lookup"><span data-stu-id="3bb82-148">_pReserved2_</span></span>
  
>  <span data-ttu-id="3bb82-149">[entrant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3bb82-149">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3bb82-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bb82-150">See also</span></span>

- [<span data-ttu-id="3bb82-151">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="3bb82-151">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)  
- [<span data-ttu-id="3bb82-152">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="3bb82-152">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="3bb82-153">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="3bb82-153">DNTBLE</span></span>](dntble.md)

