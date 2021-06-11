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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c8dc10bdb8bcde15dccf7bab4d9e10d2481cef11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416439"
---
# <a name="itneffinishcomponent"></a><span data-ttu-id="49ef9-103">ITnef::FinishComponent</span><span class="sxs-lookup"><span data-stu-id="49ef9-103">ITnef::FinishComponent</span></span>

  
  
<span data-ttu-id="49ef9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49ef9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49ef9-105">Traite les composants individuels d’un message un par un dans Transport-Neutral flux TNEF (Encapsulation Format).</span><span class="sxs-lookup"><span data-stu-id="49ef9-105">Processes individual components from a message one at a time into a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="49ef9-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="49ef9-106">Parameters</span></span>

 <span data-ttu-id="49ef9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="49ef9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="49ef9-108">[in] Masque de bits d’indicateurs qui contrôle le composant à terminer.</span><span class="sxs-lookup"><span data-stu-id="49ef9-108">[in] A bitmask of flags that controls which component will be finished.</span></span> <span data-ttu-id="49ef9-109">L’un ou l’autre des indicateurs suivants doit être définie :</span><span class="sxs-lookup"><span data-stu-id="49ef9-109">One or the other of the following flags must be set:</span></span>
    
<span data-ttu-id="49ef9-110">TNEF_COMPONENT_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="49ef9-110">TNEF_COMPONENT_ATTACHMENT</span></span> 
  
> <span data-ttu-id="49ef9-111">Le traitement sera terminé pour un objet pièce jointe . le  _paramètre ulComponentID_ contient la **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="49ef9-111">Processing will be finished for an attachment object; the  _ulComponentID_ parameter contains the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property of the attachment.</span></span> 
    
<span data-ttu-id="49ef9-112">TNEF_COMPONENT_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="49ef9-112">TNEF_COMPONENT_MESSAGE</span></span> 
  
> <span data-ttu-id="49ef9-113">Le traitement est terminé pour un objet message.</span><span class="sxs-lookup"><span data-stu-id="49ef9-113">Processing will be finished for a message object.</span></span> 
    
 <span data-ttu-id="49ef9-114">_ulComponentID_</span><span class="sxs-lookup"><span data-stu-id="49ef9-114">_ulComponentID_</span></span>
  
> <span data-ttu-id="49ef9-115">[in] 0 pour indiquer le traitement d’un message ou la propriété **PR_ATTACH_NUM** d’une pièce jointe à traiter.</span><span class="sxs-lookup"><span data-stu-id="49ef9-115">[in] 0 to indicate processing for a message, or the **PR_ATTACH_NUM** property of an attachment to be processed.</span></span> <span data-ttu-id="49ef9-116">Si l TNEF_COMPONENT_MESSAGE est définie dans le paramètre  _ulFlags,_  _ulComponentID_ doit être 0.</span><span class="sxs-lookup"><span data-stu-id="49ef9-116">If the TNEF_COMPONENT_MESSAGE flag is set in the  _ulFlags_ parameter,  _ulComponentID_ must be 0.</span></span> 
    
 <span data-ttu-id="49ef9-117">_lpCustomPropList_</span><span class="sxs-lookup"><span data-stu-id="49ef9-117">_lpCustomPropList_</span></span>
  
> <span data-ttu-id="49ef9-118">[in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient des balises de propriété qui identifient les propriétés transmises dans le paramètre _lpCustomProps._</span><span class="sxs-lookup"><span data-stu-id="49ef9-118">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains property tags that identify the properties passed in the  _lpCustomProps_ parameter.</span></span> <span data-ttu-id="49ef9-119">Il doit y avoir une correspondance un-à-un entre chaque valeur de propriété dans _lpCustomProps_ et une balise de propriété dans le paramètre _lpCustomPropList._</span><span class="sxs-lookup"><span data-stu-id="49ef9-119">There must be a one-to-one correspondence between each property value in  _lpCustomProps_ and a property tag in the  _lpCustomPropList_ parameter.</span></span> 
    
 <span data-ttu-id="49ef9-120">_lpCustomProps_</span><span class="sxs-lookup"><span data-stu-id="49ef9-120">_lpCustomProps_</span></span>
  
> <span data-ttu-id="49ef9-121">[in] Pointeur vers une structure [SPropValue](spropvalue.md) qui contient les valeurs des propriétés à coder.</span><span class="sxs-lookup"><span data-stu-id="49ef9-121">[in] A pointer to an [SPropValue](spropvalue.md) structure that contains property values for the properties to encode.</span></span> 
    
 <span data-ttu-id="49ef9-122">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="49ef9-122">_lpPropList_</span></span>
  
> <span data-ttu-id="49ef9-123">[in] Pointeur vers une structure **SPropTagArray** qui contient des balises de propriété pour les propriétés à encoder.</span><span class="sxs-lookup"><span data-stu-id="49ef9-123">[in] A pointer to an **SPropTagArray** structure that contains property tags for the properties to encode.</span></span> 
    
 <span data-ttu-id="49ef9-124">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="49ef9-124">_lppProblems_</span></span>
  
> <span data-ttu-id="49ef9-125">[out] Pointeur vers un pointeur vers une structure [STnefProblemArray](stnefproblemarray.md) renvoyée.</span><span class="sxs-lookup"><span data-stu-id="49ef9-125">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="49ef9-126">La structure **STnefProblemArray** indique les propriétés, le cas contraire, qui n’ont pas été correctement codées.</span><span class="sxs-lookup"><span data-stu-id="49ef9-126">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="49ef9-127">Si NULL est transmis dans le  _paramètre lppProblems,_ aucun tableau de problèmes de propriété n’est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="49ef9-127">If NULL is passed in the  _lppProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="49ef9-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="49ef9-128">Return value</span></span>

<span data-ttu-id="49ef9-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="49ef9-129">S_OK</span></span> 
  
> <span data-ttu-id="49ef9-130">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="49ef9-130">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="49ef9-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="49ef9-131">Remarks</span></span>

<span data-ttu-id="49ef9-132">Les fournisseurs de transport, les fournisseurs de magasins de messages et les passerelles appellent la méthode **ITnef::FinishComponent** pour effectuer un traitement TNEF pour un composant, soit un message, soit une pièce jointe, comme indiqué par l’indicateur définie dans le paramètre _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="49ef9-132">Transport providers, message store providers, and gateways call the **ITnef::FinishComponent** method to perform TNEF processing for one component, either a message or an attachment, as indicated by the flag set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="49ef9-133">Pour que le traitement des composants soit activé, le fournisseur ou la passerelle appelant passe l’indicateur TNEF_COMPONENT_ENCODING dans  _ulFlags_ pour la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) qui a ouvert l’objet pour recevoir le codage.</span><span class="sxs-lookup"><span data-stu-id="49ef9-133">For component processing to be enabled, the calling provider or gateway pass the TNEF_COMPONENT_ENCODING flag in  _ulFlags_ for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function that opened the object to receive encoding.</span></span> 
  
<span data-ttu-id="49ef9-134">La transmission de valeurs dans les paramètres _lpCustomPropList_ et _lpCustomProps_ effectue un codage de composant équivalent à celui effectué par la méthode [ITnef::SetProps.](itnef-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="49ef9-134">Passing values in the  _lpCustomPropList_ and  _lpCustomProps_ parameters performs component encoding equivalent to that done by the [ITnef::SetProps](itnef-setprops.md) method.</span></span> <span data-ttu-id="49ef9-135">La transmission d’une valeur dans le paramètre  _lpPropList_ effectue un codage de composant équivalent à celui effectué par la méthode [ITnef::AddProps](itnef-addprops.md) avec l’indicateur TNEF_PROP_INCLUDE définie dans  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="49ef9-135">Passing a value in the  _lpPropList_ parameter performs component encoding equivalent to that done by the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag set in  _ulFlags_.</span></span> <span data-ttu-id="49ef9-136">La transmission de ces valeurs vous permet d’effectuer des codages avec un seul appel au lieu de plusieurs appels.</span><span class="sxs-lookup"><span data-stu-id="49ef9-136">Passing these values enables you to perform encodings with a single call instead of multiple calls.</span></span>
  
<span data-ttu-id="49ef9-137">L’implémentation TNEF signale des problèmes de codage de flux TNEF sans arrêter **le processus FinishComponent.**</span><span class="sxs-lookup"><span data-stu-id="49ef9-137">The TNEF implementation reports TNEF stream encoding problems without stopping the **FinishComponent** process.</span></span> <span data-ttu-id="49ef9-138">La structure **STnefProblemArray** renvoyée dans  _lppProblems_ indique quels attributs TNEF ou propriétés MAPI, le cas contraire, n’ont pas pu être traitées.</span><span class="sxs-lookup"><span data-stu-id="49ef9-138">The **STnefProblemArray** structure returned in  _lppProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="49ef9-139">La valeur renvoyée dans le membre **scode** de l’une des structures **STnefProblem** contenues dans **STnefProblemArray** indique le problème spécifique.</span><span class="sxs-lookup"><span data-stu-id="49ef9-139">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="49ef9-140">Le fournisseur ou la passerelle peut fonctionner sur l’hypothèse que toutes les propriétés ou attributs pour lesquels **FinishComponent** ne retourne pas de rapport de problème ont été correctement traitées.</span><span class="sxs-lookup"><span data-stu-id="49ef9-140">The provider or gateway can work on the assumption that all properties or attributes for which **FinishComponent** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="49ef9-141">Si un fournisseur ou une passerelle ne fonctionne pas avec des tableaux à problème, il peut transmettre null dans  _lppProblems_; dans ce cas, aucun tableau de problèmes n’est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="49ef9-141">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span>
  
<span data-ttu-id="49ef9-142">La valeur renvoyée dans  _lppProblems n’est_ valide que si l’appel S_OK.</span><span class="sxs-lookup"><span data-stu-id="49ef9-142">The value returned in  _lppProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="49ef9-143">Lorsque S_OK est renvoyé, le fournisseur ou la passerelle doit vérifier les valeurs renvoyées dans la structure [STnefProblemArray.](stnefproblemarray.md)</span><span class="sxs-lookup"><span data-stu-id="49ef9-143">When S_OK is returned, the provider or gateway should check the values returned in the [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="49ef9-144">Si une erreur se produit lors de l’appel, la structure **STnefProblemArray** n’est pas remplie et le fournisseur ou la passerelle appelant ne doit pas utiliser ou libérer la structure.</span><span class="sxs-lookup"><span data-stu-id="49ef9-144">If an error occurs on the call, the **STnefProblemArray** structure is not filled in, and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="49ef9-145">Si aucune erreur ne se produit sur l’appel, le fournisseur ou la passerelle appelant doit libérer la mémoire de **l’objet STnefProblemArray** en appelant la fonction [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="49ef9-145">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="49ef9-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49ef9-146">See also</span></span>



[<span data-ttu-id="49ef9-147">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="49ef9-147">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="49ef9-148">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="49ef9-148">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="49ef9-149">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="49ef9-149">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="49ef9-150">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="49ef9-150">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="49ef9-151">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="49ef9-151">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="49ef9-152">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="49ef9-152">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="49ef9-153">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="49ef9-153">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="49ef9-154">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="49ef9-154">ITnef : IUnknown</span></span>](itnefiunknown.md)

