---
title: HrGetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetOneProp
api_type:
- HeaderDef
ms.assetid: 8d0a381a-e714-4663-9a57-b0e1cdbd6ba7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4dcdce72781669988a0cb15eb9b3a7cd73494bfb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783561"
---
# <a name="hrgetoneprop"></a><span data-ttu-id="36488-103">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="36488-103">HrGetOneProp</span></span>

  
  
<span data-ttu-id="36488-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="36488-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="36488-105">Extrait la valeur d’une propriété unique à partir d’une interface de propriété, autrement dit, une interface dérivée de [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="36488-105">Retrieves the value of a single property from a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36488-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="36488-106">Header file:</span></span>  <br/> |<span data-ttu-id="36488-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="36488-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="36488-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="36488-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="36488-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="36488-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="36488-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="36488-110">Called by:</span></span>  <br/> |<span data-ttu-id="36488-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="36488-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a><span data-ttu-id="36488-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36488-112">Parameters</span></span>

 <span data-ttu-id="36488-113">_nous procure_</span><span class="sxs-lookup"><span data-stu-id="36488-113">_pmp_</span></span>
  
> <span data-ttu-id="36488-114">[in] Pointeur vers l’interface [IMAPIProp](imapipropiunknown.md) à partir de laquelle la valeur de la propriété doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="36488-114">[in] Pointer to the [IMAPIProp](imapipropiunknown.md) interface from which the property value is to be retrieved.</span></span> 
    
 <span data-ttu-id="36488-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="36488-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="36488-116">[in] Balise de propriété de la propriété à récupérer.</span><span class="sxs-lookup"><span data-stu-id="36488-116">[in] Property tag of the property to be retrieved.</span></span> 
    
 <span data-ttu-id="36488-117">_ppprop_</span><span class="sxs-lookup"><span data-stu-id="36488-117">_ppprop_</span></span>
  
> <span data-ttu-id="36488-118">[out] Pointeur vers un pointeur vers la structure [SPropValue](spropvalue.md) retournée définissant la valeur de la propriété extraite.</span><span class="sxs-lookup"><span data-stu-id="36488-118">[out] Pointer to a pointer to the returned [SPropValue](spropvalue.md) structure defining the retrieved property value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="36488-119">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="36488-119">Return value</span></span>

<span data-ttu-id="36488-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="36488-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="36488-121">La propriété demandée n’est pas disponible à partir de l’interface spécifiée.</span><span class="sxs-lookup"><span data-stu-id="36488-121">The requested property is not available from the specified interface.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36488-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="36488-122">Remarks</span></span>

<span data-ttu-id="36488-123">Contrairement à la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) , la fonction **HrGetOneProp** ne retourne jamais aucun avertissement.</span><span class="sxs-lookup"><span data-stu-id="36488-123">Unlike the [IMAPIProp::GetProps](imapiprop-getprops.md) method, the **HrGetOneProp** function never returns any warning.</span></span> <span data-ttu-id="36488-124">Car il récupère une seule propriété, il suffit réussit ou échoue.</span><span class="sxs-lookup"><span data-stu-id="36488-124">Because it retrieves only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="36488-125">Pour extraire plusieurs propriétés, **GetProps** est plus rapide.</span><span class="sxs-lookup"><span data-stu-id="36488-125">For retrieving multiple properties, **GetProps** is faster.</span></span> 
  
<span data-ttu-id="36488-126">Vous pouvez définir ou modifier une propriété unique avec la fonction [HrSetOneProp](hrsetoneprop.md) .</span><span class="sxs-lookup"><span data-stu-id="36488-126">You can set or change a single property with the [HrSetOneProp](hrsetoneprop.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="36488-127">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="36488-127">MFCMAPI reference</span></span>

<span data-ttu-id="36488-128">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="36488-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="36488-129">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="36488-129">**File**</span></span>|<span data-ttu-id="36488-130">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="36488-130">**Function**</span></span>|<span data-ttu-id="36488-131">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="36488-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="36488-132">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="36488-132">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="36488-133">GetMAPIObjectType</span><span class="sxs-lookup"><span data-stu-id="36488-133">GetMAPIObjectType</span></span>  <br/> |<span data-ttu-id="36488-134">MFCMAPI utilise la méthode **HrGetOneProp** pour récupérer le type d’un objet.</span><span class="sxs-lookup"><span data-stu-id="36488-134">MFCMAPI uses the **HrGetOneProp** method to retrieve the type of an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36488-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36488-135">See also</span></span>



[<span data-ttu-id="36488-136">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="36488-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

