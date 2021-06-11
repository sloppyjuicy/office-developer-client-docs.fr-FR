---
title: UPMOV
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 098743a5-f265-639a-8ba6-1412705bee0a
description: 'Derni�re modification�: jeudi 5 juillet 2012'
ms.openlocfilehash: a7588d5fed2e059be7e628d8a76a12f76aea734d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339185"
---
# <a name="upmov"></a><span data-ttu-id="e3f8d-103">UPMOV</span><span class="sxs-lookup"><span data-stu-id="e3f8d-103">UPMOV</span></span>
 
<span data-ttu-id="e3f8d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3f8d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3f8d-105">Informations pour le chargement d’éléments qui ont été déplacés.</span><span class="sxs-lookup"><span data-stu-id="e3f8d-105">Information for uploading items that have been moved.</span></span> <span data-ttu-id="e3f8d-106">Ces informations sont utilisées pendant l’état de suppression de [téléchargement et](upload-delete-status-state.md) [l’état de la table de chargement.](upload-table-state.md)</span><span class="sxs-lookup"><span data-stu-id="e3f8d-106">This information is used during the [upload delete status state](upload-delete-status-state.md) and [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e3f8d-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="e3f8d-107">Quick info</span></span>

```cpp
struct UPMOV 
{ 
      ULONG          ulFlags; 
      LPVOID         pReserved; 
      LPSTREAM       pstmReserved; 
      LPSTR          pszName; 
      FEID           feid; 
      LPMAPIFOLDER   pfld; 
      PXICC          pxicc; 
      DWORD          dwReserved; 
      PUPMOV         pupmovNext; 
      UINT           cEntMov; 
};
```

## <a name="members"></a><span data-ttu-id="e3f8d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e3f8d-108">Members</span></span>

<span data-ttu-id="e3f8d-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e3f8d-109">_ulFlags_</span></span>
  
> <span data-ttu-id="e3f8d-110">[in] Indicateurs pour déterminer le comportement approprié pendant le chargement.</span><span class="sxs-lookup"><span data-stu-id="e3f8d-110">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="e3f8d-111">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="e3f8d-111">UPV_ERROR</span></span>
    
    - <span data-ttu-id="e3f8d-112">[in] Problème d’ouverture du dossier serveur.</span><span class="sxs-lookup"><span data-stu-id="e3f8d-112">[in] Problem opening server folder.</span></span>
    
  - <span data-ttu-id="e3f8d-113">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="e3f8d-113">UPV_DIRTY</span></span>
    
    - <span data-ttu-id="e3f8d-114">[in] L’état de chargement a changé.</span><span class="sxs-lookup"><span data-stu-id="e3f8d-114">[in] The upload state has changed.</span></span> <span data-ttu-id="e3f8d-115">Il est utilisé par le client pour suivre la modification de l’état du magasin local.</span><span class="sxs-lookup"><span data-stu-id="e3f8d-115">This is used by the client to track the change in state for the local store.</span></span>
    
  - <span data-ttu-id="e3f8d-116">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="e3f8d-116">UPV_COMMIT</span></span>
    
    - <span data-ttu-id="e3f8d-117">[in] Valider l’état de chargement.</span><span class="sxs-lookup"><span data-stu-id="e3f8d-117">[in] Commit upload state.</span></span>
    
<span data-ttu-id="e3f8d-118">_pReserved_</span><span class="sxs-lookup"><span data-stu-id="e3f8d-118">_pReserved_</span></span>
  
>  <span data-ttu-id="e3f8d-119">[sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e3f8d-119">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="e3f8d-120">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="e3f8d-120">_pstmReserved_</span></span>
  
>  <span data-ttu-id="e3f8d-121">[sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e3f8d-121">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="e3f8d-122">_pszName_</span><span class="sxs-lookup"><span data-stu-id="e3f8d-122">_pszName_</span></span>
  
>  <span data-ttu-id="e3f8d-123">[out] Nom du dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="e3f8d-123">[out] Name of the destination folder.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="e3f8d-124">Ce membre ne prend pas en charge UNICODE.</span><span class="sxs-lookup"><span data-stu-id="e3f8d-124">This member does not support UNICODE.</span></span> 
  
<span data-ttu-id="e3f8d-125">_feid_</span><span class="sxs-lookup"><span data-stu-id="e3f8d-125">_feid_</span></span>
  
>  <span data-ttu-id="e3f8d-126">[out] ID d’entrée du dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="e3f8d-126">[out] Entry ID of destination folder.</span></span> 
    
<span data-ttu-id="e3f8d-127">_pfld_</span><span class="sxs-lookup"><span data-stu-id="e3f8d-127">_pfld_</span></span>
  
>  <span data-ttu-id="e3f8d-128">[in] Pointeur vers le dossier du serveur.</span><span class="sxs-lookup"><span data-stu-id="e3f8d-128">[in] Pointer to server folder.</span></span> 
    
<span data-ttu-id="e3f8d-129">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="e3f8d-129">_pxicc_</span></span>
  
>  <span data-ttu-id="e3f8d-130">[in] Pointeur vers l’interface de contenu **IExchangeImportContentsChanges** qui prend en charge le chargement des modifications de contenu lors de l’utilisation de la synchronisation incrémentielle des modifications (ICS).</span><span class="sxs-lookup"><span data-stu-id="e3f8d-130">[in] Pointer to the **IExchangeImportContentsChanges** contents interface that supports uploading content changes when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="e3f8d-131">Pour plus d’informations **sur IExchangeImportContentsChanges** et ICS, voir Critères d’évaluation [ICS.](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3f8d-131">For more information on **IExchangeImportContentsChanges** and ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="e3f8d-132">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="e3f8d-132">_dwReserved_</span></span>
  
>  <span data-ttu-id="e3f8d-133">[sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e3f8d-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="e3f8d-134">_movNext_</span><span class="sxs-lookup"><span data-stu-id="e3f8d-134">_pupmovNext_</span></span>
  
>  <span data-ttu-id="e3f8d-135">[out] Contexte de déplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="e3f8d-135">[out] Next move context.</span></span> 
    
<span data-ttu-id="e3f8d-136">_cEntMov_</span><span class="sxs-lookup"><span data-stu-id="e3f8d-136">_cEntMov_</span></span>
  
>  <span data-ttu-id="e3f8d-137">[in] Nombre d’éléments déplacés ici.</span><span class="sxs-lookup"><span data-stu-id="e3f8d-137">[in] Number of items moved here.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e3f8d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3f8d-138">See also</span></span>

- [<span data-ttu-id="e3f8d-139">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="e3f8d-139">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="e3f8d-140">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="e3f8d-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="e3f8d-141">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="e3f8d-141">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="e3f8d-142">FEID</span><span class="sxs-lookup"><span data-stu-id="e3f8d-142">FEID</span></span>](feid.md)

