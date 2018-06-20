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
ms.openlocfilehash: 43fd56932409861db86679eea6f1405dc4c37e62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787433"
---
# <a name="upmov"></a><span data-ttu-id="d7728-103">UPMOV</span><span class="sxs-lookup"><span data-stu-id="d7728-103">UPMOV</span></span>
 
<span data-ttu-id="d7728-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7728-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d7728-105">Informations de téléchargement des éléments qui ont été déplacés.</span><span class="sxs-lookup"><span data-stu-id="d7728-105">Information for uploading items that have been moved.</span></span> <span data-ttu-id="d7728-106">Ces informations sont utilisées lors du [téléchargement supprimer l’état](upload-delete-status-state.md) et [Télécharger l’état de la table](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="d7728-106">This information is used during the [upload delete status state](upload-delete-status-state.md) and [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d7728-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="d7728-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="d7728-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d7728-108">Members</span></span>

<span data-ttu-id="d7728-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d7728-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d7728-110">[in] Indicateurs pour déterminer le comportement approprié lors du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="d7728-110">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="d7728-111">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="d7728-111">UPV_ERROR</span></span>
    
    - <span data-ttu-id="d7728-112">[in] Problème d’ouverture de dossier du serveur.</span><span class="sxs-lookup"><span data-stu-id="d7728-112">[in] Problem opening server folder.</span></span>
    
  - <span data-ttu-id="d7728-113">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="d7728-113">UPV_DIRTY</span></span>
    
    - <span data-ttu-id="d7728-114">[in] L’état du téléchargement a changé.</span><span class="sxs-lookup"><span data-stu-id="d7728-114">[in] The upload state has changed.</span></span> <span data-ttu-id="d7728-115">Il est utilisé par le client pour effectuer le suivi de la modification de l’état pour le magasin local.</span><span class="sxs-lookup"><span data-stu-id="d7728-115">This is used by the client to track the change in state for the local store.</span></span>
    
  - <span data-ttu-id="d7728-116">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="d7728-116">UPV_COMMIT</span></span>
    
    - <span data-ttu-id="d7728-117">[in] Valider l’état du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="d7728-117">[in] Commit upload state.</span></span>
    
<span data-ttu-id="d7728-118">_Conservés_</span><span class="sxs-lookup"><span data-stu-id="d7728-118">_pReserved_</span></span>
  
>  <span data-ttu-id="d7728-119">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d7728-119">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="d7728-120">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="d7728-120">_pstmReserved_</span></span>
  
>  <span data-ttu-id="d7728-121">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d7728-121">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="d7728-122">_pszName_</span><span class="sxs-lookup"><span data-stu-id="d7728-122">_pszName_</span></span>
  
>  <span data-ttu-id="d7728-123">[out] Nom du dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="d7728-123">[out] Name of the destination folder.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="d7728-124">Ce membre ne prend pas en charge UNICODE.</span><span class="sxs-lookup"><span data-stu-id="d7728-124">This member does not support UNICODE.</span></span> 
  
<span data-ttu-id="d7728-125">_feid_</span><span class="sxs-lookup"><span data-stu-id="d7728-125">_feid_</span></span>
  
>  <span data-ttu-id="d7728-126">[out] ID d’entrée du dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="d7728-126">[out] Entry ID of destination folder.</span></span> 
    
<span data-ttu-id="d7728-127">_pfld_</span><span class="sxs-lookup"><span data-stu-id="d7728-127">_pfld_</span></span>
  
>  <span data-ttu-id="d7728-128">[in] Pointeur vers le dossier du serveur.</span><span class="sxs-lookup"><span data-stu-id="d7728-128">[in] Pointer to server folder.</span></span> 
    
<span data-ttu-id="d7728-129">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="d7728-129">_pxicc_</span></span>
  
>  <span data-ttu-id="d7728-130">[in] Pointeur vers l’interface de contenu **IExchangeImportContentsChanges** qui prend en charge le téléchargement des modifications du contenu lors de l’utilisation de la synchronisation de modification incrémentielle (ICS).</span><span class="sxs-lookup"><span data-stu-id="d7728-130">[in] Pointer to the **IExchangeImportContentsChanges** contents interface that supports uploading content changes when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="d7728-131">Pour plus d’informations sur **IExchangeImportContentsChanges** et partage de connexion Internet, voir [Critères d’évaluation de partage de connexion Internet](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d7728-131">For more information on **IExchangeImportContentsChanges** and ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="d7728-132">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="d7728-132">_dwReserved_</span></span>
  
>  <span data-ttu-id="d7728-133">[out] Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d7728-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="d7728-134">_pupmovNext_</span><span class="sxs-lookup"><span data-stu-id="d7728-134">_pupmovNext_</span></span>
  
>  <span data-ttu-id="d7728-135">[out] Déplacez ensuite le contexte.</span><span class="sxs-lookup"><span data-stu-id="d7728-135">[out] Next move context.</span></span> 
    
<span data-ttu-id="d7728-136">_cEntMov_</span><span class="sxs-lookup"><span data-stu-id="d7728-136">_cEntMov_</span></span>
  
>  <span data-ttu-id="d7728-137">[in] Nombre d’éléments déplacés ici.</span><span class="sxs-lookup"><span data-stu-id="d7728-137">[in] Number of items moved here.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d7728-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7728-138">See also</span></span>

- [<span data-ttu-id="d7728-139">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="d7728-139">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="d7728-140">Sur l’ordinateur de l’état de réplication</span><span class="sxs-lookup"><span data-stu-id="d7728-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="d7728-141">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="d7728-141">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="d7728-142">FEID</span><span class="sxs-lookup"><span data-stu-id="d7728-142">FEID</span></span>](feid.md)

