---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Signale l’achèvement du rebasage des rendez-vous.
ms.openlocfilehash: 9fab0d06bf0b9856b9a968f5c0db1bb15b0fe0bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328321"
---
# <a name="rebasetaskcomplete"></a><span data-ttu-id="3005a-103">RebaseTaskComplete</span><span class="sxs-lookup"><span data-stu-id="3005a-103">RebaseTaskComplete</span></span>

<span data-ttu-id="3005a-104">Signale l’achèvement du rebasage des rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="3005a-104">Reports completion for rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3005a-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="3005a-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3005a-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="3005a-106">Header file:</span></span>  <br/> |<span data-ttu-id="3005a-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="3005a-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="3005a-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="3005a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3005a-109">Applications clientes MAPI</span><span class="sxs-lookup"><span data-stu-id="3005a-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="3005a-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="3005a-110">Called by:</span></span>  <br/> |<span data-ttu-id="3005a-111">Outlook de rebasing</span><span class="sxs-lookup"><span data-stu-id="3005a-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="3005a-112">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="3005a-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="3005a-113">**PFNREBASETASKCOMPLETE** tel que défini dans tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="3005a-113">**PFNREBASETASKCOMPLETE** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskComplete(  
    ULONG ulRowIndex, 
    const SRow* pRowCur, 
    HRESULT hrResult, 
    BOOL fModified, 
    BOOL fSentUpdate, 
    const MAPIERROR* pError); 

```

## <a name="parameters"></a><span data-ttu-id="3005a-114">Parameters</span><span class="sxs-lookup"><span data-stu-id="3005a-114">Parameters</span></span>

<span data-ttu-id="3005a-115">_ulRowIndex_</span><span class="sxs-lookup"><span data-stu-id="3005a-115">_ulRowIndex_</span></span>
  
> <span data-ttu-id="3005a-116">[in] Ligne qui a été traitée.</span><span class="sxs-lookup"><span data-stu-id="3005a-116">[in] The row that was processed.</span></span> <span data-ttu-id="3005a-117">Cet index fait référence à la structure **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** transmise à [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="3005a-117">This index refers to the **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** structure passed to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
<span data-ttu-id="3005a-118">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="3005a-118">_pRowCur_</span></span>
  
> <span data-ttu-id="3005a-119">in] Pointeur vers une structure **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** décrivant l’élément qui a été traitée.</span><span class="sxs-lookup"><span data-stu-id="3005a-119">in] A pointer to an **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure describing the item that was processed.</span></span> 
    
<span data-ttu-id="3005a-120">_hrResult_</span><span class="sxs-lookup"><span data-stu-id="3005a-120">_hrResult_</span></span>
  
> <span data-ttu-id="3005a-121">[in] **HRESULT** indiquant le résultat de l’opération de rebasing.</span><span class="sxs-lookup"><span data-stu-id="3005a-121">[in] An **HRESULT** indicating the result of the rebasing operation.</span></span> 
    
<span data-ttu-id="3005a-122">_fModified_</span><span class="sxs-lookup"><span data-stu-id="3005a-122">_fModified_</span></span>
  
> <span data-ttu-id="3005a-123">[in] Spécifie si l’élément a été modifié.</span><span class="sxs-lookup"><span data-stu-id="3005a-123">[in] Specifies whether the item was modified.</span></span>
    
<span data-ttu-id="3005a-124">_fSentUpdate_</span><span class="sxs-lookup"><span data-stu-id="3005a-124">_fSentUpdate_</span></span>
  
> <span data-ttu-id="3005a-125">[in] Spécifie si un message de mise à jour de réunion a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="3005a-125">[in] Specifies whether a meeting update message was sent.</span></span> 
    
<span data-ttu-id="3005a-126">_pError_</span><span class="sxs-lookup"><span data-stu-id="3005a-126">_pError_</span></span>
  
> <span data-ttu-id="3005a-127">[in] Pointeur vers une structure **MAPIERROR** avec des informations d’erreur étendues.</span><span class="sxs-lookup"><span data-stu-id="3005a-127">[in] A pointer to a **MAPIERROR** structure with extended error information.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="3005a-128">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="3005a-128">Return values</span></span>

<span data-ttu-id="3005a-129">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="3005a-129">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3005a-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="3005a-130">Remarks</span></span>

<span data-ttu-id="3005a-131">Les applications clientes MAPI qui utilisent l’interface [IOlkApptRebaser](iolkapptrebaser.md) implémentent cette fonction pour suivre la fin des mises à jour des éléments.</span><span class="sxs-lookup"><span data-stu-id="3005a-131">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track completion of item updates.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3005a-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3005a-132">See also</span></span>

- [<span data-ttu-id="3005a-133">À propos de la relocalisation des calendriers par programme à l'heure</span><span class="sxs-lookup"><span data-stu-id="3005a-133">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

