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
# <a name="upmov"></a><span data-ttu-id="ad655-103">UPMOV</span><span class="sxs-lookup"><span data-stu-id="ad655-103">UPMOV</span></span>
 
<span data-ttu-id="ad655-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad655-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad655-105">Informations de téléchargement des éléments qui ont été déplacés.</span><span class="sxs-lookup"><span data-stu-id="ad655-105">Information for uploading items that have been moved.</span></span> <span data-ttu-id="ad655-106">Ces informations sont utilisées lors de l'état de la [suppression du chargement](upload-delete-status-state.md) et de l'état de la [table de chargement](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="ad655-106">This information is used during the [upload delete status state](upload-delete-status-state.md) and [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ad655-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="ad655-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="ad655-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ad655-108">Members</span></span>

<span data-ttu-id="ad655-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ad655-109">_ulFlags_</span></span>
  
> <span data-ttu-id="ad655-110">dans Indicateurs permettant de déterminer le comportement approprié pendant le chargement.</span><span class="sxs-lookup"><span data-stu-id="ad655-110">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="ad655-111">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="ad655-111">UPV_ERROR</span></span>
    
    - <span data-ttu-id="ad655-112">dans Problème lors de l'ouverture du dossier du serveur.</span><span class="sxs-lookup"><span data-stu-id="ad655-112">[in] Problem opening server folder.</span></span>
    
  - <span data-ttu-id="ad655-113">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="ad655-113">UPV_DIRTY</span></span>
    
    - <span data-ttu-id="ad655-114">dans L'état du chargement a changé.</span><span class="sxs-lookup"><span data-stu-id="ad655-114">[in] The upload state has changed.</span></span> <span data-ttu-id="ad655-115">Cette option est utilisée par le client pour effectuer le suivi de la modification de l'État pour le magasin local.</span><span class="sxs-lookup"><span data-stu-id="ad655-115">This is used by the client to track the change in state for the local store.</span></span>
    
  - <span data-ttu-id="ad655-116">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="ad655-116">UPV_COMMIT</span></span>
    
    - <span data-ttu-id="ad655-117">dans Valider l'état du chargement.</span><span class="sxs-lookup"><span data-stu-id="ad655-117">[in] Commit upload state.</span></span>
    
<span data-ttu-id="ad655-118">_Disparition_</span><span class="sxs-lookup"><span data-stu-id="ad655-118">_pReserved_</span></span>
  
>  <span data-ttu-id="ad655-119">[sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ad655-119">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="ad655-120">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="ad655-120">_pstmReserved_</span></span>
  
>  <span data-ttu-id="ad655-121">[sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ad655-121">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="ad655-122">_pszName_</span><span class="sxs-lookup"><span data-stu-id="ad655-122">_pszName_</span></span>
  
>  <span data-ttu-id="ad655-123">remarquer Nom du dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="ad655-123">[out] Name of the destination folder.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="ad655-124">Ce membre ne prend pas en charge UNICODE.</span><span class="sxs-lookup"><span data-stu-id="ad655-124">This member does not support UNICODE.</span></span> 
  
<span data-ttu-id="ad655-125">_feid_</span><span class="sxs-lookup"><span data-stu-id="ad655-125">_feid_</span></span>
  
>  <span data-ttu-id="ad655-126">remarquer ID d'entrée du dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="ad655-126">[out] Entry ID of destination folder.</span></span> 
    
<span data-ttu-id="ad655-127">_pfld_</span><span class="sxs-lookup"><span data-stu-id="ad655-127">_pfld_</span></span>
  
>  <span data-ttu-id="ad655-128">dans Pointeur vers le dossier du serveur.</span><span class="sxs-lookup"><span data-stu-id="ad655-128">[in] Pointer to server folder.</span></span> 
    
<span data-ttu-id="ad655-129">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="ad655-129">_pxicc_</span></span>
  
>  <span data-ttu-id="ad655-130">dans Pointeur vers l'interface de contenu **IExchangeImportContentsChanges** qui prend en charge le téléchargement de modifications de contenu lors de l'utilisation de la synchronisation des modifications incrémentielles (ICS).</span><span class="sxs-lookup"><span data-stu-id="ad655-130">[in] Pointer to the **IExchangeImportContentsChanges** contents interface that supports uploading content changes when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="ad655-131">Pour plus d'informations sur **IExchangeImportContentsChanges** et ICS, consultez la rubrique [critères d'évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ad655-131">For more information on **IExchangeImportContentsChanges** and ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="ad655-132">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="ad655-132">_dwReserved_</span></span>
  
>  <span data-ttu-id="ad655-133">[sortant] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ad655-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="ad655-134">_pupmovNext_</span><span class="sxs-lookup"><span data-stu-id="ad655-134">_pupmovNext_</span></span>
  
>  <span data-ttu-id="ad655-135">remarquer Contexte de déplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="ad655-135">[out] Next move context.</span></span> 
    
<span data-ttu-id="ad655-136">_cEntMov_</span><span class="sxs-lookup"><span data-stu-id="ad655-136">_cEntMov_</span></span>
  
>  <span data-ttu-id="ad655-137">dans Nombre d'éléments déplacés ici.</span><span class="sxs-lookup"><span data-stu-id="ad655-137">[in] Number of items moved here.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ad655-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad655-138">See also</span></span>

- [<span data-ttu-id="ad655-139">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="ad655-139">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="ad655-140">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="ad655-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="ad655-141">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="ad655-141">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="ad655-142">FEID</span><span class="sxs-lookup"><span data-stu-id="ad655-142">FEID</span></span>](feid.md)

