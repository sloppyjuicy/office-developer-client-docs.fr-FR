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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5380b6541e609c17a9005c3390c6d5db06155306
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567243"
---
# <a name="imapiformmgrcalcformpropset"></a><span data-ttu-id="c2264-103">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="c2264-103">IMAPIFormMgr::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="c2264-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2264-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2264-105">Renvoie un tableau des propriétés qui utilise un groupe de formulaires.</span><span class="sxs-lookup"><span data-stu-id="c2264-105">Returns an array of the properties that a group of forms uses.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="c2264-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2264-106">Parameters</span></span>

 <span data-ttu-id="c2264-107">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="c2264-107">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="c2264-108">[in] Pointeur vers un tableau d’objets d’informations de formulaire qui identifient les formulaires pour laquelle retourner les propriétés.</span><span class="sxs-lookup"><span data-stu-id="c2264-108">[in] A pointer to an array of form information objects that identify the forms for which to return properties.</span></span>
    
 <span data-ttu-id="c2264-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c2264-109">_ulFlags_</span></span>
  
> <span data-ttu-id="c2264-110">[in] Masque de bits d’indicateurs qui contrôle la façon dont le tableau de propriétés dans le paramètre _ppResults_ est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="c2264-110">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="c2264-111">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="c2264-111">The following flags can be set:</span></span> 
    
<span data-ttu-id="c2264-112">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="c2264-112">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="c2264-113">La matrice renvoyée contient l’intersection des propriétés du formulaire.</span><span class="sxs-lookup"><span data-stu-id="c2264-113">The returned array contains the intersection of the form's properties.</span></span>
    
<span data-ttu-id="c2264-114">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="c2264-114">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="c2264-115">Le tableau renvoyé contient l’union de propriétés du formulaire.</span><span class="sxs-lookup"><span data-stu-id="c2264-115">The returned array contains the union of the form's properties.</span></span>
    
<span data-ttu-id="c2264-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c2264-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c2264-117">Les chaînes renvoyées dans le tableau sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="c2264-117">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="c2264-118">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="c2264-118">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="c2264-119">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="c2264-119">_ppResults_</span></span>
  
> <span data-ttu-id="c2264-120">[out] Pointeur vers un pointeur vers la structure [SMAPIFormPropArray](smapiformproparray.md) renvoyée, qui contient les propriétés qui utilisent les formulaires.</span><span class="sxs-lookup"><span data-stu-id="c2264-120">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure, which contains the properties that the forms use.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c2264-121">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="c2264-121">Return value</span></span>

<span data-ttu-id="c2264-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="c2264-122">S_OK</span></span> 
  
> <span data-ttu-id="c2264-123">L’appel a réussi et renvoyé la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="c2264-123">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="c2264-124">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="c2264-124">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="c2264-125">Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="c2264-125">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c2264-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="c2264-126">Remarks</span></span>

<span data-ttu-id="c2264-127">Visionneuses de formulaire appeler la méthode **IMAPIFormMgr::CalcFormPropSet** pour obtenir un tableau des propriétés qui utilise un groupe de formulaires.</span><span class="sxs-lookup"><span data-stu-id="c2264-127">Form viewers call the **IMAPIFormMgr::CalcFormPropSet** method to obtain an array of the properties that a group of forms uses.</span></span> <span data-ttu-id="c2264-128">**CalcFormPropSet** accepte soit une intersection ou une union de propriété des formulaires définit, en fonction de l’indicateur défini dans le paramètre _ulFlags_ et elle renvoie une structure **SMAPIFormPropArray** qui contient le groupe résultant de Propriétés.</span><span class="sxs-lookup"><span data-stu-id="c2264-128">**CalcFormPropSet** takes either an intersection or a union of these forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c2264-129">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="c2264-129">Notes to implementers</span></span>

<span data-ttu-id="c2264-130">Si une visionneuse de formulaire transmet l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ , toutes les chaînes doivent être retournés en tant que chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="c2264-130">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings should be returned as Unicode strings.</span></span> <span data-ttu-id="c2264-131">Fournisseurs de bibliothèques de formulaires qui ne prennent pas en charge les chaînes Unicode doivent renvoyer MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE est passé.</span><span class="sxs-lookup"><span data-stu-id="c2264-131">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c2264-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2264-132">See also</span></span>



[<span data-ttu-id="c2264-133">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="c2264-133">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="c2264-134">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c2264-134">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

