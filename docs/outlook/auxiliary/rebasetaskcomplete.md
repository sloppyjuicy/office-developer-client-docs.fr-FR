---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Signale la fin de la relocalisation des rendez-vous.
ms.openlocfilehash: 9fab0d06bf0b9856b9a968f5c0db1bb15b0fe0bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328321"
---
# <a name="rebasetaskcomplete"></a><span data-ttu-id="5e8c0-103">RebaseTaskComplete</span><span class="sxs-lookup"><span data-stu-id="5e8c0-103">RebaseTaskComplete</span></span>

<span data-ttu-id="5e8c0-104">Signale la fin de la relocalisation des rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-104">Reports completion for rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5e8c0-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="5e8c0-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5e8c0-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="5e8c0-106">Header file:</span></span>  <br/> |<span data-ttu-id="5e8c0-107">tzmovelib. h</span><span class="sxs-lookup"><span data-stu-id="5e8c0-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="5e8c0-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="5e8c0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5e8c0-109">Applications clientes MAPI</span><span class="sxs-lookup"><span data-stu-id="5e8c0-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="5e8c0-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="5e8c0-110">Called by:</span></span>  <br/> |<span data-ttu-id="5e8c0-111">Objet de relocalisation Outlook</span><span class="sxs-lookup"><span data-stu-id="5e8c0-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="5e8c0-112">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="5e8c0-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="5e8c0-113">**PFNREBASETASKCOMPLETE** tel que défini dans tzmovelib. h</span><span class="sxs-lookup"><span data-stu-id="5e8c0-113">**PFNREBASETASKCOMPLETE** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskComplete(  
    ULONG ulRowIndex, 
    const SRow* pRowCur, 
    HRESULT hrResult, 
    BOOL fModified, 
    BOOL fSentUpdate, 
    const MAPIERROR* pError); 

```

## <a name="parameters"></a><span data-ttu-id="5e8c0-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e8c0-114">Parameters</span></span>

<span data-ttu-id="5e8c0-115">_ulRowIndex_</span><span class="sxs-lookup"><span data-stu-id="5e8c0-115">_ulRowIndex_</span></span>
  
> <span data-ttu-id="5e8c0-116">dans Ligne traitée.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-116">[in] The row that was processed.</span></span> <span data-ttu-id="5e8c0-117">Cet index fait référence à la structure **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** passée à [IOlkApptRebaser:: BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="5e8c0-117">This index refers to the **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** structure passed to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
<span data-ttu-id="5e8c0-118">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="5e8c0-118">_pRowCur_</span></span>
  
> <span data-ttu-id="5e8c0-119">in] pointeur vers une structure **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** décrivant l'élément qui a été traité.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-119">in] A pointer to an **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure describing the item that was processed.</span></span> 
    
<span data-ttu-id="5e8c0-120">_hrResult_</span><span class="sxs-lookup"><span data-stu-id="5e8c0-120">_hrResult_</span></span>
  
> <span data-ttu-id="5e8c0-121">dans **HRESULT** indiquant le résultat de l'opération de relocalisation.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-121">[in] An **HRESULT** indicating the result of the rebasing operation.</span></span> 
    
<span data-ttu-id="5e8c0-122">_fModified_</span><span class="sxs-lookup"><span data-stu-id="5e8c0-122">_fModified_</span></span>
  
> <span data-ttu-id="5e8c0-123">dans Indique si l'élément a été modifié.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-123">[in] Specifies whether the item was modified.</span></span>
    
<span data-ttu-id="5e8c0-124">_fSentUpdate_</span><span class="sxs-lookup"><span data-stu-id="5e8c0-124">_fSentUpdate_</span></span>
  
> <span data-ttu-id="5e8c0-125">dans Indique si un message de mise à jour de réunion a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-125">[in] Specifies whether a meeting update message was sent.</span></span> 
    
<span data-ttu-id="5e8c0-126">_pError_</span><span class="sxs-lookup"><span data-stu-id="5e8c0-126">_pError_</span></span>
  
> <span data-ttu-id="5e8c0-127">dans Pointeur vers une structure **MAPIERROR** avec des informations d'erreur étendues.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-127">[in] A pointer to a **MAPIERROR** structure with extended error information.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="5e8c0-128">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="5e8c0-128">Return values</span></span>

<span data-ttu-id="5e8c0-129">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-129">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5e8c0-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="5e8c0-130">Remarks</span></span>

<span data-ttu-id="5e8c0-131">Les applications clientes MAPI qui utilisent l'interface [IOlkApptRebaser](iolkapptrebaser.md) implémentent cette fonction pour effectuer le suivi des mises à jour des éléments.</span><span class="sxs-lookup"><span data-stu-id="5e8c0-131">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track completion of item updates.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5e8c0-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e8c0-132">See also</span></span>

- [<span data-ttu-id="5e8c0-133">À propos de la relocalisation des calendriers par programme à l'heure</span><span class="sxs-lookup"><span data-stu-id="5e8c0-133">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

