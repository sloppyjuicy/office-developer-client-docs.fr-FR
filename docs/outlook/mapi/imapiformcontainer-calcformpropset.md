---
title: IMAPIFormContainerCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.CalcFormPropSet
api_type:
- COM
ms.assetid: 594e3aac-a00f-422e-8e7a-949e4c9a3f8d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ec1933f80f211c7c381f9de6b15d414932b9a78e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414913"
---
# <a name="imapiformcontainercalcformpropset"></a><span data-ttu-id="8e89b-103">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="8e89b-103">IMAPIFormContainer::CalcFormPropSet</span></span>

  
  
<span data-ttu-id="8e89b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e89b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e89b-105">Renvoie un tableau des propriétés utilisées par tous les formulaires installés dans un conteneur de formulaires.</span><span class="sxs-lookup"><span data-stu-id="8e89b-105">Returns an array of the properties used by all forms installed in a form container.</span></span>
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a><span data-ttu-id="8e89b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e89b-106">Parameters</span></span>

 <span data-ttu-id="8e89b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8e89b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8e89b-108">[in] Masque de bits d’indicateurs qui contrôle la façon dont le tableau de propriétés dans le  _paramètre ppResults_ est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="8e89b-108">[in] A bitmask of flags that controls how the property array in the  _ppResults_ parameter is returned.</span></span> <span data-ttu-id="8e89b-109">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="8e89b-109">The following flags can be set:</span></span> 
    
<span data-ttu-id="8e89b-110">FORMPROPSET_INTERSECTION</span><span class="sxs-lookup"><span data-stu-id="8e89b-110">FORMPROPSET_INTERSECTION</span></span> 
  
> <span data-ttu-id="8e89b-111">Le tableau renvoyé contient l’intersection des propriétés des formulaires.</span><span class="sxs-lookup"><span data-stu-id="8e89b-111">The returned array contains the intersection of the forms' properties.</span></span>
    
<span data-ttu-id="8e89b-112">FORMPROPSET_UNION</span><span class="sxs-lookup"><span data-stu-id="8e89b-112">FORMPROPSET_UNION</span></span> 
  
> <span data-ttu-id="8e89b-113">Le tableau renvoyé contient l’union des propriétés des formulaires.</span><span class="sxs-lookup"><span data-stu-id="8e89b-113">The returned array contains the union of the forms' properties.</span></span>
    
<span data-ttu-id="8e89b-114">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8e89b-114">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8e89b-115">Les chaînes renvoyées dans le tableau sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="8e89b-115">The strings returned in the array are in Unicode format.</span></span> <span data-ttu-id="8e89b-116">Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="8e89b-116">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="8e89b-117">_ppResults_</span><span class="sxs-lookup"><span data-stu-id="8e89b-117">_ppResults_</span></span>
  
> <span data-ttu-id="8e89b-118">[out] Pointeur vers un pointeur vers la structure [SMAPIFormPropArray](smapiformproparray.md) renvoyée.</span><span class="sxs-lookup"><span data-stu-id="8e89b-118">[out] A pointer to a pointer to the returned [SMAPIFormPropArray](smapiformproparray.md) structure.</span></span> <span data-ttu-id="8e89b-119">Cette structure contient toutes les propriétés utilisées par les formulaires installés.</span><span class="sxs-lookup"><span data-stu-id="8e89b-119">This structure contains all properties used by the installed forms.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8e89b-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8e89b-120">Return value</span></span>

<span data-ttu-id="8e89b-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="8e89b-121">S_OK</span></span> 
  
> <span data-ttu-id="8e89b-122">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="8e89b-122">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="8e89b-123">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="8e89b-123">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="8e89b-124">L’indicateur MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="8e89b-124">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8e89b-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="8e89b-125">Remarks</span></span>

<span data-ttu-id="8e89b-126">Les applications clientes appellent la méthode **IMAPIFormContainer::CalcFormPropSet** pour obtenir un tableau des propriétés utilisées par tous les formulaires installés dans un conteneur de formulaires.</span><span class="sxs-lookup"><span data-stu-id="8e89b-126">Client applications call the **IMAPIFormContainer::CalcFormPropSet** method to obtain an array of properties used by all forms installed in a form container.</span></span> <span data-ttu-id="8e89b-127">**IMAPIFormContainer::CalcFormPropSet** fonctionne comme la méthode [IMAPIFormMgr::CalcFormPropSet,](imapiformmgr-calcformpropset.md) sauf qu’elle fonctionne sur chaque formulaire enregistré dans un conteneur particulier.</span><span class="sxs-lookup"><span data-stu-id="8e89b-127">**IMAPIFormContainer::CalcFormPropSet** works like the [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) method, except that it operates on every form registered in a particular container.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8e89b-128">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="8e89b-128">Notes to implementers</span></span>

<span data-ttu-id="8e89b-129">Les fournisseurs de bibliothèques de formulaires qui ne prisent pas en charge les chaînes Unicode doivent MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE est passé.</span><span class="sxs-lookup"><span data-stu-id="8e89b-129">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="8e89b-130">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="8e89b-130">Notes to callers</span></span>

 <span data-ttu-id="8e89b-131">**IMAPIFormContainer::CalcFormPropSet** prend une intersection ou une union des jeux de propriétés des formulaires, en fonction de l’indicateur définie dans le paramètre  _ulFlags,_ et elle renvoie une structure **SMAPIFormPropArray** qui contient le groupe de propriétés résultant.</span><span class="sxs-lookup"><span data-stu-id="8e89b-131">**IMAPIFormContainer::CalcFormPropSet** takes either an intersection or a union of the forms' property sets, depending on the flag set in the  _ulFlags_ parameter, and it returns an **SMAPIFormPropArray** structure that contains the resulting group of properties.</span></span> 
  
<span data-ttu-id="8e89b-132">Si un client passe l’MAPI_UNICODE dans  _ulFlags,_ toutes les chaînes renvoyées sont Unicode.</span><span class="sxs-lookup"><span data-stu-id="8e89b-132">If a client passes the MAPI_UNICODE flag in  _ulFlags_, all returned strings are Unicode.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8e89b-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e89b-133">See also</span></span>



[<span data-ttu-id="8e89b-134">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="8e89b-134">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
  
[<span data-ttu-id="8e89b-135">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="8e89b-135">SMAPIFormPropArray</span></span>](smapiformproparray.md)
  
[<span data-ttu-id="8e89b-136">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e89b-136">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

