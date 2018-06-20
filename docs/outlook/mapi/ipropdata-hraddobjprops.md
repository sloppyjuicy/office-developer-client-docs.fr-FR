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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 985b763ade9670c064c6c338953debf7beaa2783
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784394"
---
# <a name="ipropdatahraddobjprops"></a><span data-ttu-id="266db-103">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="266db-103">IPropData::HrAddObjProps</span></span>

  
  
<span data-ttu-id="266db-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="266db-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="266db-105">Ajoute une ou plusieurs propriétés de type PT_OBJECT à l’objet.</span><span class="sxs-lookup"><span data-stu-id="266db-105">Adds one or more properties of type PT_OBJECT to the object.</span></span>
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="266db-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="266db-106">Parameters</span></span>

 <span data-ttu-id="266db-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="266db-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="266db-108">[in] Pointeur vers un tableau de balises de propriété qui indiquent les propriétés à ajouter.</span><span class="sxs-lookup"><span data-stu-id="266db-108">[in] A pointer to an array of property tags that indicate the properties to add.</span></span>
    
 <span data-ttu-id="266db-109">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="266db-109">_lppProblems_</span></span>
  
> <span data-ttu-id="266db-110">[entrée, sortie] Sur entrée, un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) valide ou valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="266db-110">[in, out] On input, a valid pointer to an [SPropProblemArray](spropproblemarray.md) structure, or NULL.</span></span> <span data-ttu-id="266db-111">Dans la sortie, un pointeur vers un pointeur vers une structure qui contient des informations sur les propriétés qui ne peut pas être ajouté ou NULL.</span><span class="sxs-lookup"><span data-stu-id="266db-111">On output, a pointer to a pointer to a structure that contains information about properties that could not be added, or NULL.</span></span> <span data-ttu-id="266db-112">Un pointeur vers une structure de tableau de problème de propriété est renvoyé uniquement si un pointeur valide est passé.</span><span class="sxs-lookup"><span data-stu-id="266db-112">A pointer to a property problem array structure is returned only if a valid pointer is passed in.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="266db-113">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="266db-113">Return value</span></span>

<span data-ttu-id="266db-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="266db-114">S_OK</span></span> 
  
> <span data-ttu-id="266db-115">Les propriétés ont été ajoutées.</span><span class="sxs-lookup"><span data-stu-id="266db-115">The properties were successfully added.</span></span>
    
<span data-ttu-id="266db-116">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="266db-116">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="266db-117">Une propriété de type autre que PT_OBJECT a été passée dans le paramètre _lpPropTagArray_ pointe vers le tableau.</span><span class="sxs-lookup"><span data-stu-id="266db-117">A property type other than PT_OBJECT was passed in the array that the  _lpPropTagArray_ parameter points to.</span></span> 
    
<span data-ttu-id="266db-118">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="266db-118">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="266db-119">L’objet a été défini ne pas pour accorder l’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="266db-119">The object has been set not to allow read/write permission.</span></span>
    
<span data-ttu-id="266db-120">MAPI_W_PARTIAL_COMPLETION SE PRODUIT</span><span class="sxs-lookup"><span data-stu-id="266db-120">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="266db-121">Certains, mais pas toutes les propriétés ont été ajoutés.</span><span class="sxs-lookup"><span data-stu-id="266db-121">Some, but not all, of the properties were added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="266db-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="266db-122">Remarks</span></span>

<span data-ttu-id="266db-123">La méthode **IPropData::HrAddObjProps** ajoute une ou plusieurs propriétés de type PT_OBJECT à l’objet.</span><span class="sxs-lookup"><span data-stu-id="266db-123">The **IPropData::HrAddObjProps** method adds one or more properties of type PT_OBJECT to the object.</span></span> <span data-ttu-id="266db-124">**HrAddObjProps** propose une alternative à la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) pour les propriétés de l’objet, car les propriétés de l’objet ne peut pas être créées en appelant **SetProps**.</span><span class="sxs-lookup"><span data-stu-id="266db-124">**HrAddObjProps** provides an alternative to the [IMAPIProp::SetProps](imapiprop-setprops.md) method for object properties, because object properties cannot be created by calling **SetProps**.</span></span> <span data-ttu-id="266db-125">Ajout d’un objet entraîne de propriété dans la balise de propriété soient incluse dans la liste des balises de propriété retournée par la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="266db-125">Adding an object property results in the property tag being included in the list of property tags that the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="266db-126">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="266db-126">Notes to callers</span></span>

<span data-ttu-id="266db-127">Si **HrAddObjProps** renvoie MAPI_W_PARTIAL_COMPLETION se produit et que vous avez défini un pointeur valide _lppProblems_ , vérifiez la structure [SPropProblemArray](spropproblemarray.md) retournée permettant de savoir quelles propriétés n’ont pas été ajoutées.</span><span class="sxs-lookup"><span data-stu-id="266db-127">If **HrAddObjProps** returns MAPI_W_PARTIAL_COMPLETION and you have set  _lppProblems_ to a valid pointer, check the returned [SPropProblemArray](spropproblemarray.md) structure to find out which properties were not added.</span></span> <span data-ttu-id="266db-128">En règle générale, le seul problème qui se produit est manque de mémoire.</span><span class="sxs-lookup"><span data-stu-id="266db-128">Typically, the only problem that occurs is lack of memory.</span></span> <span data-ttu-id="266db-129">Libérer la structure **SPropProblemArray** en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) lorsque vous avez terminé avec lui.</span><span class="sxs-lookup"><span data-stu-id="266db-129">Free the **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished with it.</span></span> 
  
<span data-ttu-id="266db-130">Pour ajouter une propriété, l’objet de cible doit avoir des autorisations en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="266db-130">To add a property, the target object must have read/write permission.</span></span> <span data-ttu-id="266db-131">Si **HrAddObjProps** renvoie MAPI_E_NO_ACCESS, vous ne pouvez pas ajouter des propriétés à l’objet car il ne permet pas de modification.</span><span class="sxs-lookup"><span data-stu-id="266db-131">If **HrAddObjProps** returns MAPI_E_NO_ACCESS, you cannot add properties to the object because it does not permit modification.</span></span> <span data-ttu-id="266db-132">Pour obtenir l’autorisation de lecture/écriture à un objet avant d’appeler **HrAddObjProps**, appelez [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) et définissez le paramètre _ulAccess_ IPROP_READWRITE.</span><span class="sxs-lookup"><span data-stu-id="266db-132">To obtain read/write permission to an object prior to calling **HrAddObjProps**, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) and set the  _ulAccess_ parameter to IPROP_READWRITE.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="266db-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="266db-133">See also</span></span>



[<span data-ttu-id="266db-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="266db-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="266db-135">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="266db-135">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="266db-136">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="266db-136">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="266db-137">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="266db-137">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

