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
ms.openlocfilehash: e5adc7d0c317d8b803645d78227777998d7d241f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347837"
---
# <a name="hrgetoneprop"></a><span data-ttu-id="f443e-103">HrGetOneProp</span><span class="sxs-lookup"><span data-stu-id="f443e-103">HrGetOneProp</span></span>

  
  
<span data-ttu-id="f443e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f443e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f443e-105">Récupère la valeur d'une propriété unique à partir d'une interface de propriété, c'est-à-dire une interface dérivée de [IMAPIProp](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="f443e-105">Retrieves the value of a single property from a property interface, that is, an interface derived from [IMAPIProp](imapipropiunknown.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f443e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f443e-106">Header file:</span></span>  <br/> |<span data-ttu-id="f443e-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="f443e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f443e-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="f443e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f443e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f443e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f443e-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="f443e-110">Called by:</span></span>  <br/> |<span data-ttu-id="f443e-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="f443e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a><span data-ttu-id="f443e-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f443e-112">Parameters</span></span>

 <span data-ttu-id="f443e-113">_PMP_</span><span class="sxs-lookup"><span data-stu-id="f443e-113">_pmp_</span></span>
  
> <span data-ttu-id="f443e-114">dans Pointeur vers l'interface [IMAPIProp](imapipropiunknown.md) à partir de laquelle la valeur de propriété doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="f443e-114">[in] Pointer to the [IMAPIProp](imapipropiunknown.md) interface from which the property value is to be retrieved.</span></span> 
    
 <span data-ttu-id="f443e-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="f443e-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="f443e-116">dans Balise de propriété de la propriété à récupérer.</span><span class="sxs-lookup"><span data-stu-id="f443e-116">[in] Property tag of the property to be retrieved.</span></span> 
    
 <span data-ttu-id="f443e-117">_ppprop_</span><span class="sxs-lookup"><span data-stu-id="f443e-117">_ppprop_</span></span>
  
> <span data-ttu-id="f443e-118">remarquer Pointeur vers un pointeur vers la structure [SPropValue](spropvalue.md) renvoyée qui définit la valeur de la propriété récupérée.</span><span class="sxs-lookup"><span data-stu-id="f443e-118">[out] Pointer to a pointer to the returned [SPropValue](spropvalue.md) structure defining the retrieved property value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f443e-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f443e-119">Return value</span></span>

<span data-ttu-id="f443e-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f443e-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="f443e-121">La propriété demandée n'est pas disponible à partir de l'interface spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f443e-121">The requested property is not available from the specified interface.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f443e-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="f443e-122">Remarks</span></span>

<span data-ttu-id="f443e-123">Contrairement à la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) , la fonction **HrGetOneProp** ne renvoie aucun avertissement.</span><span class="sxs-lookup"><span data-stu-id="f443e-123">Unlike the [IMAPIProp::GetProps](imapiprop-getprops.md) method, the **HrGetOneProp** function never returns any warning.</span></span> <span data-ttu-id="f443e-124">Étant donné qu'elle récupère une seule propriété, elle réussit ou échoue.</span><span class="sxs-lookup"><span data-stu-id="f443e-124">Because it retrieves only one property, it simply either succeeds or fails.</span></span> <span data-ttu-id="f443e-125">Pour récupérer plusieurs propriétés, **GetProps** est plus rapide.</span><span class="sxs-lookup"><span data-stu-id="f443e-125">For retrieving multiple properties, **GetProps** is faster.</span></span> 
  
<span data-ttu-id="f443e-126">Vous pouvez définir ou modifier une seule propriété à l'aide de la fonction [HrSetOneProp](hrsetoneprop.md) .</span><span class="sxs-lookup"><span data-stu-id="f443e-126">You can set or change a single property with the [HrSetOneProp](hrsetoneprop.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f443e-127">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f443e-127">MFCMAPI reference</span></span>

<span data-ttu-id="f443e-128">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f443e-128">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f443e-129">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="f443e-129">**File**</span></span>|<span data-ttu-id="f443e-130">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="f443e-130">**Function**</span></span>|<span data-ttu-id="f443e-131">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="f443e-131">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f443e-132">MAPIFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="f443e-132">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="f443e-133">GetMAPIObjectType</span><span class="sxs-lookup"><span data-stu-id="f443e-133">GetMAPIObjectType</span></span>  <br/> |<span data-ttu-id="f443e-134">MFCMAPI utilise la méthode **HrGetOneProp** pour récupérer le type d'un objet.</span><span class="sxs-lookup"><span data-stu-id="f443e-134">MFCMAPI uses the **HrGetOneProp** method to retrieve the type of an object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f443e-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f443e-135">See also</span></span>



[<span data-ttu-id="f443e-136">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="f443e-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

