---
title: ITnefFinishComponent
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.FinishComponent
api_type:
- COM
ms.assetid: bcdd0688-0897-47d7-9601-f592ba453b39
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 7008549111f1b914cf2025c8d61ebc07196706fb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784481"
---
# <a name="itneffinishcomponent"></a><span data-ttu-id="38e14-103">ITnef::FinishComponent</span><span class="sxs-lookup"><span data-stu-id="38e14-103">ITnef::FinishComponent</span></span>

  
  
<span data-ttu-id="38e14-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="38e14-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="38e14-105">Traite des composants individuels à partir d’un message à la fois dans un flux de Transport-Neutral Encapsulation Format (TNEF).</span><span class="sxs-lookup"><span data-stu-id="38e14-105">Processes individual components from a message one at a time into a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
```cpp
HRESULT FinishComponent(
  ULONG ulFlags,
  ULONG ulComponentID,
  LPSPropTagArray lpCustomPropList,
  LPSPropValue lpCustomProps,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="38e14-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="38e14-106">Parameters</span></span>

 <span data-ttu-id="38e14-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="38e14-107">_ulFlags_</span></span>
  
> <span data-ttu-id="38e14-108">[in] Masque de bits d’indicateurs qui contrôle le composant sera terminé.</span><span class="sxs-lookup"><span data-stu-id="38e14-108">[in] A bitmask of flags that controls which component will be finished.</span></span> <span data-ttu-id="38e14-109">Doit avoir une ou l’autre des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="38e14-109">One or the other of the following flags must be set:</span></span>
    
<span data-ttu-id="38e14-110">TNEF_COMPONENT_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="38e14-110">TNEF_COMPONENT_ATTACHMENT</span></span> 
  
> <span data-ttu-id="38e14-111">Traitement sera terminé pour un objet attachment ; le paramètre _ulComponentID_ contient la propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="38e14-111">Processing will be finished for an attachment object; the  _ulComponentID_ parameter contains the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property of the attachment.</span></span> 
    
<span data-ttu-id="38e14-112">TNEF_COMPONENT_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="38e14-112">TNEF_COMPONENT_MESSAGE</span></span> 
  
> <span data-ttu-id="38e14-113">Traitement sera terminé pour un objet de message.</span><span class="sxs-lookup"><span data-stu-id="38e14-113">Processing will be finished for a message object.</span></span> 
    
 <span data-ttu-id="38e14-114">_ulComponentID_</span><span class="sxs-lookup"><span data-stu-id="38e14-114">_ulComponentID_</span></span>
  
> <span data-ttu-id="38e14-115">[in] 0 pour indiquer le traitement d’un message, ou de la propriété **PR_ATTACH_NUM** d’une pièce jointe à traiter.</span><span class="sxs-lookup"><span data-stu-id="38e14-115">[in] 0 to indicate processing for a message, or the **PR_ATTACH_NUM** property of an attachment to be processed.</span></span> <span data-ttu-id="38e14-116">Si l’indicateur TNEF_COMPONENT_MESSAGE est défini dans le paramètre _ulFlags_ , _ulComponentID_ doit être 0.</span><span class="sxs-lookup"><span data-stu-id="38e14-116">If the TNEF_COMPONENT_MESSAGE flag is set in the  _ulFlags_ parameter,  _ulComponentID_ must be 0.</span></span> 
    
 <span data-ttu-id="38e14-117">_lpCustomPropList_</span><span class="sxs-lookup"><span data-stu-id="38e14-117">_lpCustomPropList_</span></span>
  
> <span data-ttu-id="38e14-118">[in] Un pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient des balises de propriété qui identifient les propriétés passé dans le paramètre _lpCustomProps_ .</span><span class="sxs-lookup"><span data-stu-id="38e14-118">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains property tags that identify the properties passed in the  _lpCustomProps_ parameter.</span></span> <span data-ttu-id="38e14-119">Il doit être une correspondance entre chaque valeur de la propriété dans _lpCustomProps_ et une balise de propriété dans le paramètre _lpCustomPropList_ .</span><span class="sxs-lookup"><span data-stu-id="38e14-119">There must be a one-to-one correspondence between each property value in  _lpCustomProps_ and a property tag in the  _lpCustomPropList_ parameter.</span></span> 
    
 <span data-ttu-id="38e14-120">_lpCustomProps_</span><span class="sxs-lookup"><span data-stu-id="38e14-120">_lpCustomProps_</span></span>
  
> <span data-ttu-id="38e14-121">[in] Pointeur vers une structure [SPropValue](spropvalue.md) qui contienne les valeurs de propriété pour les propriétés à coder.</span><span class="sxs-lookup"><span data-stu-id="38e14-121">[in] A pointer to an [SPropValue](spropvalue.md) structure that contains property values for the properties to encode.</span></span> 
    
 <span data-ttu-id="38e14-122">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="38e14-122">_lpPropList_</span></span>
  
> <span data-ttu-id="38e14-123">[in] Pointeur vers une structure **SPropTagArray** qui contient des balises de propriété pour les propriétés à coder.</span><span class="sxs-lookup"><span data-stu-id="38e14-123">[in] A pointer to an **SPropTagArray** structure that contains property tags for the properties to encode.</span></span> 
    
 <span data-ttu-id="38e14-124">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="38e14-124">_lppProblems_</span></span>
  
> <span data-ttu-id="38e14-125">[out] Pointeur vers un pointeur vers une structure [STnefProblemArray](stnefproblemarray.md) renvoyée.</span><span class="sxs-lookup"><span data-stu-id="38e14-125">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="38e14-126">La structure **STnefProblemArray** indique les propriétés, le cas échéant, ont été pas codées correctement.</span><span class="sxs-lookup"><span data-stu-id="38e14-126">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="38e14-127">Si NULL est indiqué dans le paramètre _lppProblems_ , aucun tableau de problème de propriété n’est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="38e14-127">If NULL is passed in the  _lppProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="38e14-128">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="38e14-128">Return value</span></span>

<span data-ttu-id="38e14-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="38e14-129">S_OK</span></span> 
  
> <span data-ttu-id="38e14-130">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="38e14-130">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="38e14-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="38e14-131">Remarks</span></span>

<span data-ttu-id="38e14-132">Fournisseurs, les fournisseurs de banque de message et passerelles appel la méthode **ITnef::FinishComponent** pour effectuer le traitement d’un composant, un message ou une pièce jointe TNEF telle qu’indiquée par l’indicateur défini dans le paramètre _ulFlags_ de transport.</span><span class="sxs-lookup"><span data-stu-id="38e14-132">Transport providers, message store providers, and gateways call the **ITnef::FinishComponent** method to perform TNEF processing for one component, either a message or an attachment, as indicated by the flag set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="38e14-133">Pour le traitement du composant soit activé, le fournisseur ou la passerelle appelant passez l’indicateur TNEF_COMPONENT_ENCODING _ulFlags_ pour la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) qui ouvre l’objet pour la réception de codage.</span><span class="sxs-lookup"><span data-stu-id="38e14-133">For component processing to be enabled, the calling provider or gateway pass the TNEF_COMPONENT_ENCODING flag in  _ulFlags_ for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function that opened the object to receive encoding.</span></span> 
  
<span data-ttu-id="38e14-134">Passage de valeurs dans les paramètres _lpCustomPropList_ et _lpCustomProps_ exécute le composant codage équivalentes à celles effectuées par la méthode [ITnef::SetProps](itnef-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="38e14-134">Passing values in the  _lpCustomPropList_ and  _lpCustomProps_ parameters performs component encoding equivalent to that done by the [ITnef::SetProps](itnef-setprops.md) method.</span></span> <span data-ttu-id="38e14-135">Passage d’une valeur dans le paramètre _lpPropList_ effectue composant codage équivalent effectuée par la méthode [ITnef::AddProps](itnef-addprops.md) avec l’indicateur TNEF_PROP_INCLUDE défini dans _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="38e14-135">Passing a value in the  _lpPropList_ parameter performs component encoding equivalent to that done by the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag set in  _ulFlags_.</span></span> <span data-ttu-id="38e14-136">Transmission de ces valeurs permet d’exécuter les codages avec un seul appel au lieu de plusieurs appels.</span><span class="sxs-lookup"><span data-stu-id="38e14-136">Passing these values enables you to perform encodings with a single call instead of multiple calls.</span></span>
  
<span data-ttu-id="38e14-137">L’implémentation TNEF signale des problèmes de codage TNEF flux sans interrompre le processus **FinishComponent** .</span><span class="sxs-lookup"><span data-stu-id="38e14-137">The TNEF implementation reports TNEF stream encoding problems without stopping the **FinishComponent** process.</span></span> <span data-ttu-id="38e14-138">La structure **STnefProblemArray** retournée dans _lppProblems_ indique les attributs TNEF ou des propriétés MAPI, le cas échéant, pas peuvent être traitées.</span><span class="sxs-lookup"><span data-stu-id="38e14-138">The **STnefProblemArray** structure returned in  _lppProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="38e14-139">La valeur renvoyée dans le membre **scode** de l’une des structures **STnefProblem** contenues dans **STnefProblemArray** indiquant le problème spécifique.</span><span class="sxs-lookup"><span data-stu-id="38e14-139">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="38e14-140">Le fournisseur ou la passerelle peut travailler sur l’hypothèse que toutes les propriétés ou les attributs pour lesquels **FinishComponent** ne renvoie pas un rapport de problème ont été correctement traités.</span><span class="sxs-lookup"><span data-stu-id="38e14-140">The provider or gateway can work on the assumption that all properties or attributes for which **FinishComponent** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="38e14-141">Si un fournisseur ou une passerelle ne fonctionne pas avec des tableaux de problème, il peut passer NULL dans _lppProblems_; Dans ce cas, aucun tableau de problème n’est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="38e14-141">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span>
  
<span data-ttu-id="38e14-142">La valeur renvoyée dans _lppProblems_ est valide uniquement si l’appel renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="38e14-142">The value returned in  _lppProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="38e14-143">Lorsque S_OK est retourné, le fournisseur ou la passerelle doit vérifier les valeurs renvoyées dans la structure [STnefProblemArray](stnefproblemarray.md) .</span><span class="sxs-lookup"><span data-stu-id="38e14-143">When S_OK is returned, the provider or gateway should check the values returned in the [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="38e14-144">Si une erreur se produit lors de l’appel, la structure **STnefProblemArray** n’est pas remplie, et la passerelle ou le fournisseur appelant ne doit pas utiliser ou libérer la structure.</span><span class="sxs-lookup"><span data-stu-id="38e14-144">If an error occurs on the call, the **STnefProblemArray** structure is not filled in, and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="38e14-145">Si aucune erreur ne se produit lors de l’appel, la passerelle ou le fournisseur appelant doit libérer la mémoire pour le **STnefProblemArray** en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="38e14-145">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="38e14-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38e14-146">See also</span></span>



[<span data-ttu-id="38e14-147">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="38e14-147">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="38e14-148">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="38e14-148">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="38e14-149">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="38e14-149">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="38e14-150">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="38e14-150">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="38e14-151">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="38e14-151">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="38e14-152">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="38e14-152">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="38e14-153">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="38e14-153">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="38e14-154">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="38e14-154">ITnef : IUnknown</span></span>](itnefiunknown.md)

