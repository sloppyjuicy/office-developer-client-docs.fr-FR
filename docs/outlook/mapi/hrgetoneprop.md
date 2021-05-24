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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 95273bf6025d6ef995d7c21c0e44bdbbf59072f6
ms.sourcegitcommit: fb521c23df785c9c3aefa5062272b2630a32e587
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/20/2021
ms.locfileid: "52589172"
---
# <a name="hrgetoneprop"></a><span data-ttu-id="45509-103">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="45509-103">HrGetOneProp</span></span>

  
  
<span data-ttu-id="45509-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45509-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45509-105">Extrait la valeur d’une propriété unique à partir d’une interface de propriété, c’est-à-dire une interface dérivée [d’IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="45509-105">Retrieves the value of a single property from a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="45509-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="45509-106">Header file:</span></span>  <br/> |<span data-ttu-id="45509-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="45509-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="45509-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="45509-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="45509-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="45509-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="45509-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="45509-110">Called by:</span></span>  <br/> |<span data-ttu-id="45509-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="45509-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a><span data-ttu-id="45509-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="45509-112">Parameters</span></span>

 <span data-ttu-id="45509-113">_pmp_</span><span class="sxs-lookup"><span data-stu-id="45509-113">_pmp_</span></span>
  
> <span data-ttu-id="45509-114">[in] Pointeur vers [l’interface IMAPIProp](imapipropiunknown.md) à partir de laquelle la valeur de propriété doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="45509-114">[in] Pointer to the [IMAPIProp](imapipropiunknown.md) interface from which the property value is to be retrieved.</span></span> 
    
 <span data-ttu-id="45509-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="45509-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="45509-116">[in] Balise de propriété de la propriété à récupérer.</span><span class="sxs-lookup"><span data-stu-id="45509-116">[in] Property tag of the property to be retrieved.</span></span> 
    
 <span data-ttu-id="45509-117">_ppprop_</span><span class="sxs-lookup"><span data-stu-id="45509-117">_ppprop_</span></span>
  
> <span data-ttu-id="45509-118">[out] Pointeur vers un pointeur vers la structure [SPropValue renvoyée](spropvalue.md) définissant la valeur de propriété récupérée.</span><span class="sxs-lookup"><span data-stu-id="45509-118">[out] Pointer to a pointer to the returned [SPropValue](spropvalue.md) structure defining the retrieved property value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="45509-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="45509-119">Return value</span></span>

<span data-ttu-id="45509-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="45509-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="45509-121">La propriété demandée n’est pas disponible à partir de l’interface spécifiée.</span><span class="sxs-lookup"><span data-stu-id="45509-121">The requested property is not available from the specified interface.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="45509-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="45509-122">Remarks</span></span>

<span data-ttu-id="45509-123">Contrairement à [la méthode IMAPIProp::GetProps,](imapiprop-getprops.md) la fonction **HrGetOneProp** ne renvoie jamais d’avertissement.</span><span class="sxs-lookup"><span data-stu-id="45509-123">Unlike the [IMAPIProp::GetProps](imapiprop-getprops.md) method, the **HrGetOneProp** function never returns any warning.</span></span> <span data-ttu-id="45509-124">Comme elle récupère une seule propriété, elle réussit ou échoue simplement.</span><span class="sxs-lookup"><span data-stu-id="45509-124">Because it retrieves only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="45509-125">Pour récupérer plusieurs propriétés, **GetProps** est plus rapide.</span><span class="sxs-lookup"><span data-stu-id="45509-125">For retrieving multiple properties, **GetProps** is faster.</span></span> 
  
<span data-ttu-id="45509-126">Vous pouvez définir ou modifier une propriété unique avec [la fonction HrSetOneProp.](hrsetoneprop.md)</span><span class="sxs-lookup"><span data-stu-id="45509-126">You can set or change a single property with the [HrSetOneProp](hrsetoneprop.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="45509-127">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="45509-127">MFCMAPI reference</span></span>

<span data-ttu-id="45509-128">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="45509-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="45509-129">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="45509-129">**File**</span></span>|<span data-ttu-id="45509-130">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="45509-130">**Function**</span></span>|<span data-ttu-id="45509-131">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="45509-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="45509-132">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="45509-132">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="45509-133">GetMAPIObjectType</span><span class="sxs-lookup"><span data-stu-id="45509-133">GetMAPIObjectType</span></span>  <br/> |<span data-ttu-id="45509-134">MFCMAPI utilise la **méthode HrGetOneProp** pour récupérer le type d’un objet.</span><span class="sxs-lookup"><span data-stu-id="45509-134">MFCMAPI uses the **HrGetOneProp** method to retrieve the type of an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="45509-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45509-135">See also</span></span>



[<span data-ttu-id="45509-136">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="45509-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

