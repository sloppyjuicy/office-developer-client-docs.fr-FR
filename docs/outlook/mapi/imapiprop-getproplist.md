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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f089fa2c608fb9fcb7deba2e061c5cf5886aa02f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316568"
---
# <a name="imapipropgetproplist"></a><span data-ttu-id="f8895-103">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="f8895-103">IMAPIProp::GetPropList</span></span>

  
  
<span data-ttu-id="f8895-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8895-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8895-105">Renvoie les balises de propriété pour toutes les propriétés.</span><span class="sxs-lookup"><span data-stu-id="f8895-105">Returns property tags for all properties.</span></span> 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a><span data-ttu-id="f8895-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8895-106">Parameters</span></span>

 <span data-ttu-id="f8895-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f8895-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f8895-108">dans Masque de des indicateurs qui contrôle le format des chaînes dans les balises de propriété renvoyées.</span><span class="sxs-lookup"><span data-stu-id="f8895-108">[in] A bitmask of flags that controls the format for the strings in the returned property tags.</span></span> <span data-ttu-id="f8895-109">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="f8895-109">The following flag can be set:</span></span>
    
<span data-ttu-id="f8895-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f8895-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f8895-111">Les chaînes renvoyées sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="f8895-111">The returned strings are in Unicode format.</span></span> <span data-ttu-id="f8895-112">Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="f8895-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="f8895-113">_lppPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="f8895-113">_lppPropTagArray_</span></span>
  
> <span data-ttu-id="f8895-114">remarquer Pointeur vers un pointeur vers le tableau de balises de propriété qui contient des balises pour toutes les propriétés de l'objet.</span><span class="sxs-lookup"><span data-stu-id="f8895-114">[out] A pointer to a pointer to the property tag array that contains tags for all of the object's properties.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f8895-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f8895-115">Return value</span></span>

<span data-ttu-id="f8895-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="f8895-116">S_OK</span></span> 
  
> <span data-ttu-id="f8895-117">Toutes les balises de propriété ont été renvoyées avec succès.</span><span class="sxs-lookup"><span data-stu-id="f8895-117">All of the property tags were returned successfully.</span></span>
    
<span data-ttu-id="f8895-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="f8895-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="f8895-119">L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.</span><span class="sxs-lookup"><span data-stu-id="f8895-119">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f8895-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="f8895-120">Remarks</span></span>

<span data-ttu-id="f8895-121">La méthode **IMAPIProp:: GetPropList** extrait la balise de propriété pour chaque propriété actuellement prise en charge par un objet.</span><span class="sxs-lookup"><span data-stu-id="f8895-121">The **IMAPIProp::GetPropList** method retrieves the property tag for each property currently supported by an object.</span></span> <span data-ttu-id="f8895-122">Si l'objet ne prend actuellement en charge aucune propriété, **GetPropList** renvoie un tableau de balises de propriété avec le membre **cValues** défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="f8895-122">If the object does not currently support any properties, **GetPropList** returns a property tag array with the **cValues** member set to 0.</span></span> 
  
<span data-ttu-id="f8895-123">L'étendue des propriétés retournées par **GetPropList** varie en fonction du fournisseur et du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f8895-123">The scope of properties returned by **GetPropList** varies from provider to provider.</span></span> <span data-ttu-id="f8895-124">Certains fournisseurs de services excluent les propriétés pour lesquelles l'appelant n'a pas accès.</span><span class="sxs-lookup"><span data-stu-id="f8895-124">Some service providers exclude those properties for which the caller does not have access.</span></span> <span data-ttu-id="f8895-125">Tous les fournisseurs renvoient les propriétés de type **PT_OBJECT**.</span><span class="sxs-lookup"><span data-stu-id="f8895-125">All providers return properties of type **PT_OBJECT**.</span></span>
  
<span data-ttu-id="f8895-126">Si l'objet ne prend pas en charge le format Unicode, **GetPropList** renvoie MAPI_E_BAD_CHARWIDTH, même s'il n'existe aucune propriété de chaîne définie pour l'objet.</span><span class="sxs-lookup"><span data-stu-id="f8895-126">If the object does not support Unicode, **GetPropList** returns MAPI_E_BAD_CHARWIDTH, even if there are no string properties defined for the object.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f8895-127">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="f8895-127">Notes to implementers</span></span>

<span data-ttu-id="f8895-128">Les fournisseurs de transport à distance implémentent **GetPropList** exactement comme spécifié ici.</span><span class="sxs-lookup"><span data-stu-id="f8895-128">Remote transport providers implement **GetPropList** exactly as specified here.</span></span> <span data-ttu-id="f8895-129">Il n'y a aucune préoccupation particulière.</span><span class="sxs-lookup"><span data-stu-id="f8895-129">There are no special concerns.</span></span> <span data-ttu-id="f8895-130">Votre implémentation doit, bien sûr, renvoyer la même liste de propriétés que celle prise en charge par la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="f8895-130">Your implementation should, of course, return the same list of properties as supported by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f8895-131">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="f8895-131">Notes to callers</span></span>

<span data-ttu-id="f8895-132">Appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer le tableau de balises de propriété pointé par _lppPropTagArray_.</span><span class="sxs-lookup"><span data-stu-id="f8895-132">Call the [MAPIFreeBuffer](mapifreebuffer.md) function to free the property tag array pointed to by  _lppPropTagArray_.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f8895-133">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f8895-133">MFCMAPI reference</span></span>

<span data-ttu-id="f8895-134">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f8895-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f8895-135">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="f8895-135">**File**</span></span>|<span data-ttu-id="f8895-136">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="f8895-136">**Function**</span></span>|<span data-ttu-id="f8895-137">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="f8895-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f8895-138">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="f8895-138">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="f8895-139">GetPropsNULL</span><span class="sxs-lookup"><span data-stu-id="f8895-139">GetPropsNULL</span></span>  <br/> |<span data-ttu-id="f8895-140">MFCMAPI utilise la méthode **IMAPIProp:: GetPropList** pour obtenir une liste de propriétés à transmettre à **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="f8895-140">MFCMAPI uses the **IMAPIProp::GetPropList** method to get a property list to pass to **GetProps**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f8895-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8895-141">See also</span></span>



[<span data-ttu-id="f8895-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="f8895-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="f8895-143">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f8895-143">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f8895-144">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f8895-144">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="f8895-145">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="f8895-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

