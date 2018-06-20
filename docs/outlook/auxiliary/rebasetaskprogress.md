---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Indique la progression de l’énumération et redéfinition de rendez-vous.
ms.openlocfilehash: 4219ab1d59b596bebbe3ced03651716b04b51f81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782831"
---
# <a name="rebasetaskprogress"></a><span data-ttu-id="ffd4f-103">RebaseTaskProgress</span><span class="sxs-lookup"><span data-stu-id="ffd4f-103">RebaseTaskProgress</span></span>

<span data-ttu-id="ffd4f-104">Indique la progression de l’énumération et redéfinition de rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="ffd4f-104">Reports progress for enumeration and rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ffd4f-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="ffd4f-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ffd4f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="ffd4f-106">Header file:</span></span>  <br/> |<span data-ttu-id="ffd4f-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="ffd4f-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="ffd4f-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="ffd4f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ffd4f-109">Applications clientes MAPI</span><span class="sxs-lookup"><span data-stu-id="ffd4f-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="ffd4f-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="ffd4f-110">Called by:</span></span>  <br/> |<span data-ttu-id="ffd4f-111">Objet redéfinition Outlook</span><span class="sxs-lookup"><span data-stu-id="ffd4f-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="ffd4f-112">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="ffd4f-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="ffd4f-113">**PFNREBASETASKPROGRESS** comme défini dans tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="ffd4f-113">**PFNREBASETASKPROGRESS** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a><span data-ttu-id="ffd4f-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ffd4f-114">Parameters</span></span>

<span data-ttu-id="ffd4f-115">_ulMin_</span><span class="sxs-lookup"><span data-stu-id="ffd4f-115">_ulMin_</span></span>
  
> <span data-ttu-id="ffd4f-116">[in] Le début de la plage de rendez-vous en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="ffd4f-116">[in] The low end of the range of appointments being processed.</span></span> <span data-ttu-id="ffd4f-117">Il est généralement égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="ffd4f-117">It is usually zero.</span></span>
    
<span data-ttu-id="ffd4f-118">_ulMax_</span><span class="sxs-lookup"><span data-stu-id="ffd4f-118">_ulMax_</span></span>
  
> <span data-ttu-id="ffd4f-119">[in] Haut de gamme de la plage de rendez-vous en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="ffd4f-119">[in] The high end of the range of appointments being processed.</span></span> <span data-ttu-id="ffd4f-120">Il est généralement le nombre d’éléments dans le dossier de calendrier en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="ffd4f-120">It is usually the number of items in the calendar folder being processed.</span></span>
    
<span data-ttu-id="ffd4f-121">_ulCur_</span><span class="sxs-lookup"><span data-stu-id="ffd4f-121">_ulCur_</span></span>
  
> <span data-ttu-id="ffd4f-122">[in] L’élément actuel en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="ffd4f-122">[in] The current item being processed.</span></span>
    
<span data-ttu-id="ffd4f-123">_State_</span><span class="sxs-lookup"><span data-stu-id="ffd4f-123">_State_</span></span>
  
> <span data-ttu-id="ffd4f-124">[in] Une valeur qui indique l’état de l’élément en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="ffd4f-124">[in] A value that indicates the status of the item being processed.</span></span> <span data-ttu-id="ffd4f-125">L’énumération **REBASE_APPT_STATE** est définie dans tzmovelib.h.</span><span class="sxs-lookup"><span data-stu-id="ffd4f-125">The enumeration **REBASE_APPT_STATE** is defined in tzmovelib.h.</span></span>  <span data-ttu-id="ffd4f-126">_État_ est une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ffd4f-126">_State_ is one of the following values:</span></span> 
    
   - <span data-ttu-id="ffd4f-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** — analyse et en examinant un élément.</span><span class="sxs-lookup"><span data-stu-id="ffd4f-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** —Scanning and examining an item.</span></span> 
    
   - <span data-ttu-id="ffd4f-128">**REBASE_APPT_STATE_SCANNING_FOUND** — analyse et a trouvé un élément.</span><span class="sxs-lookup"><span data-stu-id="ffd4f-128">**REBASE_APPT_STATE_SCANNING_FOUND** —Scanning and found an item.</span></span> 
    
   - <span data-ttu-id="ffd4f-129">**REBASE_APPT_STATE_BEGIN** — fixation et démarrage d’un élément.</span><span class="sxs-lookup"><span data-stu-id="ffd4f-129">**REBASE_APPT_STATE_BEGIN** —Fixing and starting an item.</span></span> 
    
   - <span data-ttu-id="ffd4f-130">**REBASE_APPT_STATE_REBASING** — fixation et ajustement d’un élément.</span><span class="sxs-lookup"><span data-stu-id="ffd4f-130">**REBASE_APPT_STATE_REBASING** —Fixing and adjusting an item.</span></span> 
    
   - <span data-ttu-id="ffd4f-131">**REBASE_APPT_STATE_SENDING** — fixation et l’envoi d’une mise à jour de réunion.</span><span class="sxs-lookup"><span data-stu-id="ffd4f-131">**REBASE_APPT_STATE_SENDING** —Fixing and sending a meeting update.</span></span> 
    
   - <span data-ttu-id="ffd4f-132">**REBASE_APPT_STATE_DONE** — fixation et terminé avec un élément.</span><span class="sxs-lookup"><span data-stu-id="ffd4f-132">**REBASE_APPT_STATE_DONE** —Fixing and done with an item.</span></span> 
    
<span data-ttu-id="ffd4f-133">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="ffd4f-133">_pRowCur_</span></span>
  
> <span data-ttu-id="ffd4f-134">[in] Pointeur vers une structure **[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** qui décrit l’élément en cours d’analyse ou fixe.</span><span class="sxs-lookup"><span data-stu-id="ffd4f-134">[in] A pointer to an **[SRow](http://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure that describes the item being scanned or fixed.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="ffd4f-135">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="ffd4f-135">Return values</span></span>

<span data-ttu-id="ffd4f-136">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="ffd4f-136">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ffd4f-137">Note</span><span class="sxs-lookup"><span data-stu-id="ffd4f-137">Remarks</span></span>

<span data-ttu-id="ffd4f-138">Les applications clientes MAPI qui utilisent l’interface [IOlkApptRebaser](iolkapptrebaser.md) implémentent cette fonction pour effectuer le suivi du traitement de l’élément.</span><span class="sxs-lookup"><span data-stu-id="ffd4f-138">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track item processing.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ffd4f-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffd4f-139">See also</span></span>

- [<span data-ttu-id="ffd4f-140">À propos de la relocalisation des calendriers par programme à l'heure</span><span class="sxs-lookup"><span data-stu-id="ffd4f-140">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

