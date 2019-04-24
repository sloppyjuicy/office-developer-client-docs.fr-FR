---
title: IMAPIFormMgrCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CalcFormPropSet
api_type:
- COM
ms.assetid: ab302bfd-5cff-49b4-b0d2-308ae5af478d
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: bf072aba27c90b7cea80c464e17fafb47524b695
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342083"
---
# <a name="imapiformmgrcalcformpropset"></a><span data-ttu-id="91dde-103">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="91dde-103">IMAPIFormMgr::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="91dde-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91dde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91dde-105">Renvoie un tableau des propriétés utilisées par un groupe de formulaires.</span><span class="sxs-lookup"><span data-stu-id="91dde-105">Returns an array of the properties that a group of forms uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="91dde-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91dde-106">Parameters</span></span>

 <span data-ttu-id="91dde-107">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="91dde-107">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="91dde-108">dans Pointeur vers un tableau d'objets d'informations de formulaire qui identifient les formulaires pour lesquels renvoyer des propriétés.</span><span class="sxs-lookup"><span data-stu-id="91dde-108">[in] A pointer to an array of form information objects that identify the forms for which to return properties.</span></span>
    
 <span data-ttu-id="91dde-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="91dde-109">_ulFlags_</span></span>
  
> <span data-ttu-id="91dde-110">dans Masque de des indicateurs qui contrôle la manière dont le tableau de propriétés dans le paramètre _ppResults_ est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="91dde-110">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="91dde-111">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="91dde-111">The following flags can be set:</span></span> 
    
<span data-ttu-id="91dde-112">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="91dde-112">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="91dde-113">Le tableau renvoyé contient l'intersection des propriétés du formulaire.</span><span class="sxs-lookup"><span data-stu-id="91dde-113">The returned array contains the intersection of the form's properties.</span></span>
    
<span data-ttu-id="91dde-114">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="91dde-114">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="91dde-115">Le tableau renvoyé contient l'Union des propriétés du formulaire.</span><span class="sxs-lookup"><span data-stu-id="91dde-115">The returned array contains the union of the form's properties.</span></span>
    
<span data-ttu-id="91dde-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="91dde-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="91dde-117">Les chaînes renvoyées dans le tableau sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="91dde-117">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="91dde-118">Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="91dde-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="91dde-119">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="91dde-119">_ppResults_</span></span>
  
> <span data-ttu-id="91dde-120">remarquer Pointeur vers un pointeur vers la structure [SMAPIFormPropArray](smapiformproparray.md) renvoyée, qui contient les propriétés utilisées par les formulaires.</span><span class="sxs-lookup"><span data-stu-id="91dde-120">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure, which contains the properties that the forms use.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="91dde-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="91dde-121">Return value</span></span>

<span data-ttu-id="91dde-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="91dde-122">S_OK</span></span> 
  
> <span data-ttu-id="91dde-123">L'appel a réussi et a renvoyé la ou les valeurs attendues.</span><span class="sxs-lookup"><span data-stu-id="91dde-123">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="91dde-124">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="91dde-124">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="91dde-125">L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.</span><span class="sxs-lookup"><span data-stu-id="91dde-125">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="91dde-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="91dde-126">Remarks</span></span>

<span data-ttu-id="91dde-127">Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr:: CalcFormPropSet** pour obtenir un tableau des propriétés utilisées par un groupe de formulaires.</span><span class="sxs-lookup"><span data-stu-id="91dde-127">Form viewers call the **IMAPIFormMgr::CalcFormPropSet** method to obtain an array of the properties that a group of forms uses.</span></span> <span data-ttu-id="91dde-128">**CalcFormPropSet** prend une intersection ou une Union des jeux de propriétés de ces formulaires, en fonction de l'indicateur défini dans le paramètre _ulFlags_ , et renvoie une structure **SMAPIFormPropArray** qui contient le groupe résultant de Propriétés.</span><span class="sxs-lookup"><span data-stu-id="91dde-128">**CalcFormPropSet** takes either an intersection or a union of these forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="91dde-129">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="91dde-129">Notes to implementers</span></span>

<span data-ttu-id="91dde-130">Si une visionneuse de formulaires transmet l'indicateur MAPI_UNICODE dans le paramètre _ulFlags_ , toutes les chaînes doivent être renvoyées en tant que chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="91dde-130">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings should be returned as Unicode strings.</span></span> <span data-ttu-id="91dde-131">Les fournisseurs de bibliothèques de formulaires qui ne prennent pas en charge les chaînes Unicode doivent renvoyer MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE est transmis.</span><span class="sxs-lookup"><span data-stu-id="91dde-131">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="91dde-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91dde-132">See also</span></span>



[<span data-ttu-id="91dde-133">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="91dde-133">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="91dde-134">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="91dde-134">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

