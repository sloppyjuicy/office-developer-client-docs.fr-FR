---
title: IMAPIPropGetPropList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetPropList
api_type:
- COM
ms.assetid: 0069c223-32bb-4286-b763-39fd45dc263b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5417853dbb1fa87d2beead2f73ca57329e17b044
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571121"
---
# <a name="imapipropgetproplist"></a><span data-ttu-id="0183c-103">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="0183c-103">IMAPIProp::GetPropList</span></span>

  
  
<span data-ttu-id="0183c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0183c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0183c-105">Renvoie les balises de propriété pour toutes les propriétés.</span><span class="sxs-lookup"><span data-stu-id="0183c-105">Returns property tags for all properties.</span></span> 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="0183c-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="0183c-106">Parameters</span></span>

 <span data-ttu-id="0183c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0183c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0183c-108">[in] Masque de bits d’indicateurs qui contrôle le format des chaînes dans les balises de propriété renvoyées.</span><span class="sxs-lookup"><span data-stu-id="0183c-108">[in] A bitmask of flags that controls the format for the strings in the returned property tags.</span></span> <span data-ttu-id="0183c-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="0183c-109">The following flag can be set:</span></span>
    
<span data-ttu-id="0183c-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0183c-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0183c-111">Les chaînes retournées sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="0183c-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="0183c-112">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="0183c-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="0183c-113">_lppPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="0183c-113">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="0183c-114">[out] Pointeur vers un pointeur vers le tableau de balise de propriété qui contient des balises pour toutes les propriétés de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0183c-114">[out] A pointer to a pointer to the property tag array that contains tags for all of the object's properties.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0183c-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0183c-115">Return value</span></span>

<span data-ttu-id="0183c-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="0183c-116">S_OK</span></span> 
  
> <span data-ttu-id="0183c-117">Toutes les balises de propriété ont été renvoyées.</span><span class="sxs-lookup"><span data-stu-id="0183c-117">All of the property tags were returned successfully.</span></span>
    
<span data-ttu-id="0183c-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="0183c-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="0183c-119">Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="0183c-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0183c-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="0183c-120">Remarks</span></span>

<span data-ttu-id="0183c-121">La méthode **IMAPIProp::GetPropList** récupère la balise de propriété pour chaque propriété actuellement pris en charge par un objet.</span><span class="sxs-lookup"><span data-stu-id="0183c-121">The **IMAPIProp::GetPropList** method retrieves the property tag for each property currently supported by an object.</span></span> <span data-ttu-id="0183c-122">Si l’objet ne prend pas en charge toutes les propriétés, **GetPropList** renvoie un tableau de balise de propriété avec le membre **cValues** défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="0183c-122">If the object does not currently support any properties, **GetPropList** returns a property tag array with the **cValues** member set to 0.</span></span> 
  
<span data-ttu-id="0183c-123">La portée des propriétés retournées par **GetPropList** varie d’un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0183c-123">The scope of properties returned by **GetPropList** varies from provider to provider.</span></span> <span data-ttu-id="0183c-124">Certains fournisseurs de services excluent les propriétés pour lesquelles l’appelant n’a pas accès.</span><span class="sxs-lookup"><span data-stu-id="0183c-124">Some service providers exclude those properties for which the caller does not have access.</span></span> <span data-ttu-id="0183c-125">Tous les fournisseurs de renvoient les propriétés de type **PT_OBJECT**.</span><span class="sxs-lookup"><span data-stu-id="0183c-125">All providers return properties of type **PT_OBJECT**.</span></span>
  
<span data-ttu-id="0183c-126">Si l’objet ne prend pas en charge Unicode, **GetPropList** renvoie MAPI_E_BAD_CHARWIDTH, même si aucune propriété de chaîne définis pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="0183c-126">If the object does not support Unicode, **GetPropList** returns MAPI_E_BAD_CHARWIDTH, even if there are no string properties defined for the object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0183c-127">Remarques à l’attention des responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="0183c-127">Notes to implementers</span></span>

<span data-ttu-id="0183c-128">Fournisseurs de transport à distance implémentent **GetPropList** exactement comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="0183c-128">Remote transport providers implement **GetPropList** exactly as specified here.</span></span> <span data-ttu-id="0183c-129">Il n’existe aucune problèmes spéciaux.</span><span class="sxs-lookup"><span data-stu-id="0183c-129">There are no special concerns.</span></span> <span data-ttu-id="0183c-130">Votre implémentation doit retourner bien sûr, la même liste des propriétés de prise en charge par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="0183c-130">Your implementation should, of course, return the same list of properties as supported by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0183c-131">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="0183c-131">Notes to callers</span></span>

<span data-ttu-id="0183c-132">Appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer le tableau de balise de propriété désigné par _lppPropTagArray_.</span><span class="sxs-lookup"><span data-stu-id="0183c-132">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the property tag array pointed to by  _lppPropTagArray_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0183c-133">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0183c-133">MFCMAPI reference</span></span>

<span data-ttu-id="0183c-134">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0183c-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0183c-135">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="0183c-135">**File**</span></span>|<span data-ttu-id="0183c-136">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="0183c-136">**Function**</span></span>|<span data-ttu-id="0183c-137">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="0183c-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0183c-138">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="0183c-138">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="0183c-139">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="0183c-139">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="0183c-140">MFCMAPI utilise la méthode **IMAPIProp::GetPropList** pour obtenir une liste de propriétés à transmettre à **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="0183c-140">MFCMAPI uses the **IMAPIProp::GetPropList** method to get a property list to pass to **GetProps**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0183c-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0183c-141">See also</span></span>



[<span data-ttu-id="0183c-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="0183c-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="0183c-143">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="0183c-143">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="0183c-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0183c-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="0183c-145">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="0183c-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

