---
title: ITnefExtractProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.ExtractProps
api_type:
- COM
ms.assetid: 9169a5be-21dd-4938-8db3-522bea165c92
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5a01c65bbec061248537558257c66d1a90128b5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407500"
---
# <a name="itnefextractprops"></a><span data-ttu-id="ec753-103">ITnef::ExtractProps</span><span class="sxs-lookup"><span data-stu-id="ec753-103">ITnef::ExtractProps</span></span>

  
  
<span data-ttu-id="ec753-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec753-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec753-105">Extrait les propriétés d'une encapsulation TNEF.</span><span class="sxs-lookup"><span data-stu-id="ec753-105">Extracts the properties from a TNEF encapsulation.</span></span> 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a><span data-ttu-id="ec753-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec753-106">Parameters</span></span>

 <span data-ttu-id="ec753-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ec753-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ec753-108">dans Masque de des indicateurs qui contrôle la manière dont les propriétés sont décodées.</span><span class="sxs-lookup"><span data-stu-id="ec753-108">[in] A bitmask of flags that controls how properties are decoded.</span></span> <span data-ttu-id="ec753-109">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="ec753-109">The following flags can be set:</span></span>
    
<span data-ttu-id="ec753-110">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="ec753-110">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="ec753-111">Décode toutes les propriétés non spécifiées dans le paramètre _lpPropList_ .</span><span class="sxs-lookup"><span data-stu-id="ec753-111">Decodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="ec753-112">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="ec753-112">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="ec753-113">Décode toutes les propriétés spécifiées dans _lpPropList_.</span><span class="sxs-lookup"><span data-stu-id="ec753-113">Decodes all properties specified in  _lpPropList_.</span></span>
    
 <span data-ttu-id="ec753-114">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="ec753-114">_lpPropList_</span></span>
  
> <span data-ttu-id="ec753-115">dans Pointeur vers la liste des propriétés à inclure dans l'opération de décodage ou à exclure de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="ec753-115">[in] A pointer to the list of properties to include in or exclude from the decoding operation.</span></span>
    
 <span data-ttu-id="ec753-116">_lpProblems_</span><span class="sxs-lookup"><span data-stu-id="ec753-116">_lpProblems_</span></span>
  
> <span data-ttu-id="ec753-117">remarquer Pointeur vers un pointeur vers une structure [STnefProblemArray](stnefproblemarray.md) renvoyée.</span><span class="sxs-lookup"><span data-stu-id="ec753-117">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="ec753-118">La structure **STnefProblemArray** indique les propriétés, le cas échéant, qui n'ont pas été codées correctement.</span><span class="sxs-lookup"><span data-stu-id="ec753-118">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="ec753-119">Si NULL est passé dans le paramètre _lpProblems_ , aucun tableau de problèmes de propriété n'est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="ec753-119">If NULL is passed in the  _lpProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ec753-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ec753-120">Return value</span></span>

<span data-ttu-id="ec753-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="ec753-121">S_OK</span></span> 
  
> <span data-ttu-id="ec753-122">L'appel a réussi et a renvoyé la ou les valeurs attendues.</span><span class="sxs-lookup"><span data-stu-id="ec753-122">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="ec753-123">MAPI_E_CORRUPT_DATA</span><span class="sxs-lookup"><span data-stu-id="ec753-123">MAPI_E_CORRUPT_DATA</span></span> 
  
> <span data-ttu-id="ec753-124">Les données en cours de décodage dans un flux sont endommagées.</span><span class="sxs-lookup"><span data-stu-id="ec753-124">Data being decoded into a stream is corrupted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ec753-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="ec753-125">Remarks</span></span>

<span data-ttu-id="ec753-126">Les fournisseurs de transport, les fournisseurs de banques de messages et les passerelles appellent la méthode **ITnef:: ExtractProps** pour extraire (c'est-à-dire décoder) les propriétés de l'encapsulation d'un message ou d'une pièce jointe qui a été transmise à la fonction [OpenTnefStream](opentnefstream.md) .</span><span class="sxs-lookup"><span data-stu-id="ec753-126">Transport providers, message store providers, and gateways call the **ITnef::ExtractProps** method to extract (that is, decode) properties from the encapsulation of a message or an attachment that was passed to the [OpenTnefStream](opentnefstream.md) function.</span></span> <span data-ttu-id="ec753-127">Le fournisseur ou la passerelle appelant peut spécifier une liste de propriétés à décoder.</span><span class="sxs-lookup"><span data-stu-id="ec753-127">The calling provider or gateway can specify a list of properties to decode.</span></span> <span data-ttu-id="ec753-128">Les fournisseurs et les passerelles peuvent également utiliser **ExtractProps** pour fournir des informations sur toute gestion spéciale des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="ec753-128">Providers and gateways can also use **ExtractProps** to provide information about any special handling for attachments.</span></span> 
  
 <span data-ttu-id="ec753-129">**ExtractProps** remplit le message d'origine transmis à **OpenTnefStream** avec les propriétés décodées.</span><span class="sxs-lookup"><span data-stu-id="ec753-129">**ExtractProps** populates the original message passed into **OpenTnefStream** with the decoded properties.</span></span> <span data-ttu-id="ec753-130">Les appels **ExtractProps** suivants renvoient au message et extraient la nouvelle liste de propriétés.</span><span class="sxs-lookup"><span data-stu-id="ec753-130">Subsequent **ExtractProps** calls go back to the message and extract the new list of properties.</span></span> 
  
<span data-ttu-id="ec753-131">Contrairement à la méthode [ITnef:: AddProps](itnef-addprops.md) , qui met en file d'attente les actions demandées jusqu'à ce que la méthode **ITnef:: Finish** soit appelée, la méthode **ExtractProps** décode les propriétés encapsulées immédiatement lorsqu'elle est appelée.</span><span class="sxs-lookup"><span data-stu-id="ec753-131">Unlike the [ITnef::AddProps](itnef-addprops.md) method, which queues requested actions until the **ITnef::Finish** method is called, the **ExtractProps** method decodes the encapsulated properties immediately when it is called.</span></span> <span data-ttu-id="ec753-132">Pour cette raison, le message cible pour le décodage d'encapsulation doit être relativement vide.</span><span class="sxs-lookup"><span data-stu-id="ec753-132">For that reason, the target message for encapsulation decoding should be relatively empty.</span></span> <span data-ttu-id="ec753-133">Les propriétés existantes dans le message cible sont remplacées par les propriétés encapsulées.</span><span class="sxs-lookup"><span data-stu-id="ec753-133">Existing properties in the target message are overwritten by encapsulated properties.</span></span> 
  
 <span data-ttu-id="ec753-134">**ExtractProps** est pris en charge uniquement pour les objets ouverts avec l'indicateur TNEF_DECODE pour la fonction **OpenTnefStream** ou [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="ec753-134">**ExtractProps** is supported only for objects that are opened with the TNEF_DECODE flag for the **OpenTnefStream** or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="ec753-135">L'implémentation TNEF signale les problèmes de codage de flux TNEF sans arrêter le processus **ExtractProps** .</span><span class="sxs-lookup"><span data-stu-id="ec753-135">The TNEF implementation reports TNEF stream encoding problems without stopping the **ExtractProps** process.</span></span> <span data-ttu-id="ec753-136">La structure [STnefProblemArray](stnefproblemarray.md) renvoyée dans _lpProblems_ indique les attributs TNEF ou les propriétés MAPI, le cas échéant, qui n'ont pas pu être traités.</span><span class="sxs-lookup"><span data-stu-id="ec753-136">The [STnefProblemArray](stnefproblemarray.md) structure returned in  _lpProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="ec753-137">La valeur renvoyée dans le membre **SCODE** de l'une des structures **STnefProblem** contenues dans **STnefProblemArray** indique le problème spécifique.</span><span class="sxs-lookup"><span data-stu-id="ec753-137">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="ec753-138">Le fournisseur ou la passerelle peut fonctionner en supposant que toutes les propriétés ou tous les attributs pour lesquels **ExtractProps** ne renvoie pas un rapport de problème ont été traités avec succès.</span><span class="sxs-lookup"><span data-stu-id="ec753-138">The provider or gateway can work on the assumption that all properties or attributes for which **ExtractProps** does not return a problem report were processed successfully.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ec753-139">Si une propriété dans le bloc d'encapsulation MAPI ne peut pas être traitée et que le flux n'est pas fiable pendant le décodage d'un flux TNEF, le décodage du bloc d'encapsulation est arrêté et un problème est signalé.</span><span class="sxs-lookup"><span data-stu-id="ec753-139">If a property in the MAPI encapsulation block cannot be processed and leaves the stream unreliable during the decoding of a TNEF stream, decoding of the encapsulation block is stopped and a problem is reported.</span></span> <span data-ttu-id="ec753-140">Le tableau des problèmes pour ce type de problème contient 0L pour \*\*\*\* le membre ulPropTag `attMAPIProps` , `attAttachment` ou pour le membre **ulAttribute** , et MAPI_E_UNABLE_TO_COMPLETE pour le membre **SCODE** .</span><span class="sxs-lookup"><span data-stu-id="ec753-140">The problem array for this type of problem contains 0L for the **ulPropTag** member,  `attMAPIProps` or  `attAttachment` for the **ulAttribute** member, and MAPI_E_UNABLE_TO_COMPLETE for the **scode** member.</span></span> <span data-ttu-id="ec753-141">Notez que le décodage du flux n'est pas interrompu, uniquement le décodage du bloc d'encapsulation MAPI.</span><span class="sxs-lookup"><span data-stu-id="ec753-141">Note that the decoding of the stream is not halted, just the decoding of the MAPI encapsulation block.</span></span> <span data-ttu-id="ec753-142">Le décodage de flux continue avec le prochain bloc d'attributs.</span><span class="sxs-lookup"><span data-stu-id="ec753-142">The stream decoding continues with the next attribute block.</span></span> 
  
<span data-ttu-id="ec753-143">Si un fournisseur ou une passerelle ne fonctionne pas avec les tableaux de problèmes, elle peut transmettre la valeur NULL dans _lppProblems_; dans ce cas, aucun tableau de problèmes n'est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="ec753-143">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="ec753-144">La valeur renvoyée dans _lpProblems_ est valide uniquement si l'appel retourne S_OK.</span><span class="sxs-lookup"><span data-stu-id="ec753-144">The value returned in  _lpProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="ec753-145">Lorsque S_OK est renvoyé, le fournisseur ou la passerelle doit vérifier les valeurs renvoyées dans la structure **STnefProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="ec753-145">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="ec753-146">Si une erreur se produit lors de l'appel, la structure **STnefProblemArray** n'est pas renseignée et le fournisseur ou la passerelle appelant ne doit pas utiliser ou libérer la structure.</span><span class="sxs-lookup"><span data-stu-id="ec753-146">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="ec753-147">Si aucune erreur ne se produit lors de l'appel, le fournisseur ou la passerelle d'appel doit libérer la mémoire pour la structure **STnefProblemArray** en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ec753-147">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ec753-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec753-148">See also</span></span>



[<span data-ttu-id="ec753-149">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="ec753-149">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="ec753-150">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="ec753-150">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="ec753-151">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="ec753-151">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="ec753-152">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ec753-152">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ec753-153">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="ec753-153">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="ec753-154">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="ec753-154">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="ec753-155">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="ec753-155">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="ec753-156">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ec753-156">ITnef : IUnknown</span></span>](itnefiunknown.md)

