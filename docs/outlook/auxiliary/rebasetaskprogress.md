---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Signale l’avancement de l’éumération et de la rebasation des rendez-vous.
ms.openlocfilehash: e5df0cd6df10ab86b1a125b9807637438976726f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326452"
---
# <a name="rebasetaskprogress"></a><span data-ttu-id="b69a4-103">RebaseTaskProgress</span><span class="sxs-lookup"><span data-stu-id="b69a4-103">RebaseTaskProgress</span></span>

<span data-ttu-id="b69a4-104">Signale l’avancement de l’éumération et de la rebasation des rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="b69a4-104">Reports progress for enumeration and rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b69a4-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="b69a4-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b69a4-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b69a4-106">Header file:</span></span>  <br/> |<span data-ttu-id="b69a4-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="b69a4-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="b69a4-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="b69a4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b69a4-109">Applications clientes MAPI</span><span class="sxs-lookup"><span data-stu-id="b69a4-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="b69a4-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="b69a4-110">Called by:</span></span>  <br/> |<span data-ttu-id="b69a4-111">Outlook de rebasing</span><span class="sxs-lookup"><span data-stu-id="b69a4-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="b69a4-112">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="b69a4-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="b69a4-113">**PFNREBASETASKPROGRESS** tel que défini dans tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="b69a4-113">**PFNREBASETASKPROGRESS** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a><span data-ttu-id="b69a4-114">Parameters</span><span class="sxs-lookup"><span data-stu-id="b69a4-114">Parameters</span></span>

<span data-ttu-id="b69a4-115">_ulMin_</span><span class="sxs-lookup"><span data-stu-id="b69a4-115">_ulMin_</span></span>
  
> <span data-ttu-id="b69a4-116">[in] Bas de la plage de rendez-vous en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="b69a4-116">[in] The low end of the range of appointments being processed.</span></span> <span data-ttu-id="b69a4-117">Il est généralement zéro.</span><span class="sxs-lookup"><span data-stu-id="b69a4-117">It is usually zero.</span></span>
    
<span data-ttu-id="b69a4-118">_ulMax_</span><span class="sxs-lookup"><span data-stu-id="b69a4-118">_ulMax_</span></span>
  
> <span data-ttu-id="b69a4-119">[in] Haut de la plage de rendez-vous en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="b69a4-119">[in] The high end of the range of appointments being processed.</span></span> <span data-ttu-id="b69a4-120">Il s’agit généralement du nombre d’éléments du dossier calendrier en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="b69a4-120">It is usually the number of items in the calendar folder being processed.</span></span>
    
<span data-ttu-id="b69a4-121">_ulCur_</span><span class="sxs-lookup"><span data-stu-id="b69a4-121">_ulCur_</span></span>
  
> <span data-ttu-id="b69a4-122">[in] Élément actuel en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="b69a4-122">[in] The current item being processed.</span></span>
    
<span data-ttu-id="b69a4-123">_État_</span><span class="sxs-lookup"><span data-stu-id="b69a4-123">_State_</span></span>
  
> <span data-ttu-id="b69a4-124">[in] Valeur qui indique l’état de l’élément en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="b69a4-124">[in] A value that indicates the status of the item being processed.</span></span> <span data-ttu-id="b69a4-125">L’REBASE_APPT_STATE **est** définie dans tzmovelib.h.</span><span class="sxs-lookup"><span data-stu-id="b69a4-125">The enumeration **REBASE_APPT_STATE** is defined in tzmovelib.h.</span></span>  <span data-ttu-id="b69a4-126">_State_ est l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="b69a4-126">_State_ is one of the following values:</span></span> 
    
   - <span data-ttu-id="b69a4-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** : analyse et examen d’un élément.</span><span class="sxs-lookup"><span data-stu-id="b69a4-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** —Scanning and examining an item.</span></span> 
    
   - <span data-ttu-id="b69a4-128">**REBASE_APPT_STATE_SCANNING_FOUND** : analyse et recherche d’un élément.</span><span class="sxs-lookup"><span data-stu-id="b69a4-128">**REBASE_APPT_STATE_SCANNING_FOUND** —Scanning and found an item.</span></span> 
    
   - <span data-ttu-id="b69a4-129">**REBASE_APPT_STATE_BEGIN** : correction et démarrage d’un élément.</span><span class="sxs-lookup"><span data-stu-id="b69a4-129">**REBASE_APPT_STATE_BEGIN** —Fixing and starting an item.</span></span> 
    
   - <span data-ttu-id="b69a4-130">**REBASE_APPT_STATE_REBASING** : correction et ajustement d’un élément.</span><span class="sxs-lookup"><span data-stu-id="b69a4-130">**REBASE_APPT_STATE_REBASING** —Fixing and adjusting an item.</span></span> 
    
   - <span data-ttu-id="b69a4-131">**REBASE_APPT_STATE_SENDING** : correction et envoi d’une mise à jour de réunion.</span><span class="sxs-lookup"><span data-stu-id="b69a4-131">**REBASE_APPT_STATE_SENDING** —Fixing and sending a meeting update.</span></span> 
    
   - <span data-ttu-id="b69a4-132">**REBASE_APPT_STATE_DONE** : correction et fin d’un élément.</span><span class="sxs-lookup"><span data-stu-id="b69a4-132">**REBASE_APPT_STATE_DONE** —Fixing and done with an item.</span></span> 
    
<span data-ttu-id="b69a4-133">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="b69a4-133">_pRowCur_</span></span>
  
> <span data-ttu-id="b69a4-134">[in] Pointeur vers une structure **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** qui décrit l’élément en cours d’analyse ou de correction.</span><span class="sxs-lookup"><span data-stu-id="b69a4-134">[in] A pointer to an **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure that describes the item being scanned or fixed.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="b69a4-135">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="b69a4-135">Return values</span></span>

<span data-ttu-id="b69a4-136">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="b69a4-136">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b69a4-137">Remarques</span><span class="sxs-lookup"><span data-stu-id="b69a4-137">Remarks</span></span>

<span data-ttu-id="b69a4-138">Les applications clientes MAPI qui utilisent [l’interface IOlkApptRebaser](iolkapptrebaser.md) implémentent cette fonction pour suivre le traitement des éléments.</span><span class="sxs-lookup"><span data-stu-id="b69a4-138">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track item processing.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b69a4-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b69a4-139">See also</span></span>

- [<span data-ttu-id="b69a4-140">À propos de la relocalisation des calendriers par programme à l'heure</span><span class="sxs-lookup"><span data-stu-id="b69a4-140">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

