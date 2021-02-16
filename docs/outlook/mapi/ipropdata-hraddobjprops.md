---
title: IPropDataHrAddObjProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrAddObjProps
api_type:
- COM
ms.assetid: 683cf476-3c02-4b3b-939f-6fff6611f9aa
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: df63f08d3d453575816c4f7ab043f802023e21d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416383"
---
# <a name="ipropdatahraddobjprops"></a><span data-ttu-id="7465e-103">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="7465e-103">IPropData::HrAddObjProps</span></span>

  
  
<span data-ttu-id="7465e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7465e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7465e-105">Ajoute une ou plusieurs propriétés de type PT_OBJECT à l’objet.</span><span class="sxs-lookup"><span data-stu-id="7465e-105">Adds one or more properties of type PT_OBJECT to the object.</span></span>
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="7465e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7465e-106">Parameters</span></span>

 <span data-ttu-id="7465e-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="7465e-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="7465e-108">[in] Pointeur vers un tableau de balises de propriétés qui indiquent les propriétés à ajouter.</span><span class="sxs-lookup"><span data-stu-id="7465e-108">[in] A pointer to an array of property tags that indicate the properties to add.</span></span>
    
 <span data-ttu-id="7465e-109">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="7465e-109">_lppProblems_</span></span>
  
> <span data-ttu-id="7465e-110">[in, out] Lors de l’entrée, un pointeur valide vers une structure [SPropProblemArray](spropproblemarray.md) ou NULL.</span><span class="sxs-lookup"><span data-stu-id="7465e-110">[in, out] On input, a valid pointer to an [SPropProblemArray](spropproblemarray.md) structure, or NULL.</span></span> <span data-ttu-id="7465e-111">En sortie, un pointeur vers un pointeur vers une structure qui contient des informations sur les propriétés qui n’ont pas pu être ajoutées, ou NULL.</span><span class="sxs-lookup"><span data-stu-id="7465e-111">On output, a pointer to a pointer to a structure that contains information about properties that could not be added, or NULL.</span></span> <span data-ttu-id="7465e-112">Un pointeur vers une structure de tableau à problème de propriété est renvoyé uniquement si un pointeur valide est passé.</span><span class="sxs-lookup"><span data-stu-id="7465e-112">A pointer to a property problem array structure is returned only if a valid pointer is passed in.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7465e-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7465e-113">Return value</span></span>

<span data-ttu-id="7465e-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="7465e-114">S_OK</span></span> 
  
> <span data-ttu-id="7465e-115">Les propriétés ont été ajoutées avec succès.</span><span class="sxs-lookup"><span data-stu-id="7465e-115">The properties were successfully added.</span></span>
    
<span data-ttu-id="7465e-116">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="7465e-116">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="7465e-117">Un type de propriété autre que PT_OBJECT a été transmis dans le tableau vers qui pointe le paramètre _lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="7465e-117">A property type other than PT_OBJECT was passed in the array that the  _lpPropTagArray_ parameter points to.</span></span> 
    
<span data-ttu-id="7465e-118">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="7465e-118">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="7465e-119">L’objet a été définie pour ne pas autoriser l’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7465e-119">The object has been set not to allow read/write permission.</span></span>
    
<span data-ttu-id="7465e-120">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="7465e-120">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="7465e-121">Certaines des propriétés ont été ajoutées, mais pas toutes.</span><span class="sxs-lookup"><span data-stu-id="7465e-121">Some, but not all, of the properties were added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7465e-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="7465e-122">Remarks</span></span>

<span data-ttu-id="7465e-123">La **méthode IPropData::HrAddObjProps** ajoute une ou plusieurs propriétés de type PT_OBJECT à l’objet.</span><span class="sxs-lookup"><span data-stu-id="7465e-123">The **IPropData::HrAddObjProps** method adds one or more properties of type PT_OBJECT to the object.</span></span> <span data-ttu-id="7465e-124">**HrAddObjProps** fournit une alternative à la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) pour les propriétés d’objet, car les propriétés d’objet ne peuvent pas être créées en appelant **SetProps**.</span><span class="sxs-lookup"><span data-stu-id="7465e-124">**HrAddObjProps** provides an alternative to the [IMAPIProp::SetProps](imapiprop-setprops.md) method for object properties, because object properties cannot be created by calling **SetProps**.</span></span> <span data-ttu-id="7465e-125">L’ajout d’une propriété objet entraîne l’ajout de la balise de propriété dans la liste des balises de propriétés que la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) renvoie.</span><span class="sxs-lookup"><span data-stu-id="7465e-125">Adding an object property results in the property tag being included in the list of property tags that the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7465e-126">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="7465e-126">Notes to callers</span></span>

<span data-ttu-id="7465e-127">Si **HrAddObjProps** renvoie MAPI_W_PARTIAL_COMPLETION et que vous avez définie  _lppProblems_ sur un pointeur valide, vérifiez la structure [SPropProblemArray](spropproblemarray.md) renvoyée pour connaître les propriétés qui n’ont pas été ajoutées.</span><span class="sxs-lookup"><span data-stu-id="7465e-127">If **HrAddObjProps** returns MAPI_W_PARTIAL_COMPLETION and you have set  _lppProblems_ to a valid pointer, check the returned [SPropProblemArray](spropproblemarray.md) structure to find out which properties were not added.</span></span> <span data-ttu-id="7465e-128">En règle générale, le seul problème qui se produit est le manque de mémoire.</span><span class="sxs-lookup"><span data-stu-id="7465e-128">Typically, the only problem that occurs is lack of memory.</span></span> <span data-ttu-id="7465e-129">Libérez la structure **SPropProblemArray** en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) lorsque vous en avez terminé.</span><span class="sxs-lookup"><span data-stu-id="7465e-129">Free the **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished with it.</span></span> 
  
<span data-ttu-id="7465e-130">Pour ajouter une propriété, l’objet cible doit avoir une autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7465e-130">To add a property, the target object must have read/write permission.</span></span> <span data-ttu-id="7465e-131">Si **HrAddObjProps** renvoie MAPI_E_NO_ACCESS, vous ne pouvez pas ajouter de propriétés à l’objet, car il n’autorise pas la modification.</span><span class="sxs-lookup"><span data-stu-id="7465e-131">If **HrAddObjProps** returns MAPI_E_NO_ACCESS, you cannot add properties to the object because it does not permit modification.</span></span> <span data-ttu-id="7465e-132">Pour obtenir une autorisation de lecture/écriture sur un objet avant d’appeler **HrAddObjProps,** appelez [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) et définissez le paramètre  _ulAccess_ sur IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="7465e-132">To obtain read/write permission to an object prior to calling **HrAddObjProps**, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) and set the  _ulAccess_ parameter to IPROP_READWRITE.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7465e-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7465e-133">See also</span></span>



[<span data-ttu-id="7465e-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="7465e-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="7465e-135">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="7465e-135">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="7465e-136">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="7465e-136">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="7465e-137">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7465e-137">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

