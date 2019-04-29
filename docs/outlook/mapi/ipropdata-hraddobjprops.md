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
# <a name="ipropdatahraddobjprops"></a><span data-ttu-id="0975f-103">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="0975f-103">IPropData::HrAddObjProps</span></span>

  
  
<span data-ttu-id="0975f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0975f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0975f-105">Ajoute une ou plusieurs propriétés de type PT_OBJECT à l'objet.</span><span class="sxs-lookup"><span data-stu-id="0975f-105">Adds one or more properties of type PT_OBJECT to the object.</span></span>
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="0975f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0975f-106">Parameters</span></span>

 <span data-ttu-id="0975f-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="0975f-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="0975f-108">dans Pointeur vers un tableau de balises de propriété qui indiquent les propriétés à ajouter.</span><span class="sxs-lookup"><span data-stu-id="0975f-108">[in] A pointer to an array of property tags that indicate the properties to add.</span></span>
    
 <span data-ttu-id="0975f-109">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="0975f-109">_lppProblems_</span></span>
  
> <span data-ttu-id="0975f-110">[in, out] Lors de l'entrée, pointeur valide vers une structure [SPropProblemArray](spropproblemarray.md) ou valeur null.</span><span class="sxs-lookup"><span data-stu-id="0975f-110">[in, out] On input, a valid pointer to an [SPropProblemArray](spropproblemarray.md) structure, or NULL.</span></span> <span data-ttu-id="0975f-111">En sortie, pointeur vers un pointeur vers une structure qui contient des informations sur les propriétés qui n'ont pas pu être ajoutées, ou NULL.</span><span class="sxs-lookup"><span data-stu-id="0975f-111">On output, a pointer to a pointer to a structure that contains information about properties that could not be added, or NULL.</span></span> <span data-ttu-id="0975f-112">Un pointeur vers une structure de tableau de problèmes de propriété n'est renvoyé qu'en cas de transmission d'un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="0975f-112">A pointer to a property problem array structure is returned only if a valid pointer is passed in.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0975f-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0975f-113">Return value</span></span>

<span data-ttu-id="0975f-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="0975f-114">S_OK</span></span> 
  
> <span data-ttu-id="0975f-115">Les propriétés ont été correctement ajoutées.</span><span class="sxs-lookup"><span data-stu-id="0975f-115">The properties were successfully added.</span></span>
    
<span data-ttu-id="0975f-116">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="0975f-116">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="0975f-117">Un type de propriété autre que PT_OBJECT a été transmis dans le tableau vers lequel pointe le paramètre _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="0975f-117">A property type other than PT_OBJECT was passed in the array that the  _lpPropTagArray_ parameter points to.</span></span> 
    
<span data-ttu-id="0975f-118">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="0975f-118">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="0975f-119">L'objet a été défini pour ne pas autoriser les autorisations en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0975f-119">The object has been set not to allow read/write permission.</span></span>
    
<span data-ttu-id="0975f-120">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="0975f-120">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="0975f-121">Certaines propriétés ont été ajoutées, mais pas toutes.</span><span class="sxs-lookup"><span data-stu-id="0975f-121">Some, but not all, of the properties were added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0975f-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="0975f-122">Remarks</span></span>

<span data-ttu-id="0975f-123">La méthode **IPropData:: HrAddObjProps** ajoute une ou plusieurs propriétés de type PT_OBJECT à l'objet.</span><span class="sxs-lookup"><span data-stu-id="0975f-123">The **IPropData::HrAddObjProps** method adds one or more properties of type PT_OBJECT to the object.</span></span> <span data-ttu-id="0975f-124">**HrAddObjProps** fournit une alternative à la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) pour les propriétés de l'objet, car les propriétés de l'objet ne peuvent pas être créées en appelant **SetProps**.</span><span class="sxs-lookup"><span data-stu-id="0975f-124">**HrAddObjProps** provides an alternative to the [IMAPIProp::SetProps](imapiprop-setprops.md) method for object properties, because object properties cannot be created by calling **SetProps**.</span></span> <span data-ttu-id="0975f-125">L'ajout d'une propriété d'objet entraîne l'inclusion de la balise de propriété dans la liste des balises de propriété renvoyées par la méthode [IMAPIProp:: GetPropList](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="0975f-125">Adding an object property results in the property tag being included in the list of property tags that the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0975f-126">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="0975f-126">Notes to callers</span></span>

<span data-ttu-id="0975f-127">Si **HrAddObjProps** renvoie MAPI_W_PARTIAL_COMPLETION et que vous avez défini _lppProblems_ sur un pointeur valide, vérifiez la structure [SPropProblemArray](spropproblemarray.md) renvoyée pour savoir quelles propriétés n'ont pas été ajoutées.</span><span class="sxs-lookup"><span data-stu-id="0975f-127">If **HrAddObjProps** returns MAPI_W_PARTIAL_COMPLETION and you have set  _lppProblems_ to a valid pointer, check the returned [SPropProblemArray](spropproblemarray.md) structure to find out which properties were not added.</span></span> <span data-ttu-id="0975f-128">En règle générale, le seul problème qui se produit est le manque de mémoire.</span><span class="sxs-lookup"><span data-stu-id="0975f-128">Typically, the only problem that occurs is lack of memory.</span></span> <span data-ttu-id="0975f-129">Libérez la structure **SPropProblemArray** en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) une fois que vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="0975f-129">Free the **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished with it.</span></span> 
  
<span data-ttu-id="0975f-130">Pour ajouter une propriété, l'objet cible doit disposer d'une autorisation en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0975f-130">To add a property, the target object must have read/write permission.</span></span> <span data-ttu-id="0975f-131">Si **HrAddObjProps** renvoie MAPI_E_NO_ACCESS, vous ne pouvez pas ajouter de propriétés à l'objet car il n'autorise pas la modification.</span><span class="sxs-lookup"><span data-stu-id="0975f-131">If **HrAddObjProps** returns MAPI_E_NO_ACCESS, you cannot add properties to the object because it does not permit modification.</span></span> <span data-ttu-id="0975f-132">Pour obtenir l'autorisation de lecture/écriture sur un objet avant d'appeler **HrAddObjProps**, appelez [IPropData:: HrSetObjAccess](ipropdata-hrsetobjaccess.md) et définissez le paramètre _ulAccess_ sur IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="0975f-132">To obtain read/write permission to an object prior to calling **HrAddObjProps**, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) and set the  _ulAccess_ parameter to IPROP_READWRITE.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0975f-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0975f-133">See also</span></span>



[<span data-ttu-id="0975f-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="0975f-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="0975f-135">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="0975f-135">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="0975f-136">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="0975f-136">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="0975f-137">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0975f-137">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

