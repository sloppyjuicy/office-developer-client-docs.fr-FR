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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 26949f10e22c4d2ea49594ee3365ae7d3bb3662d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784493"
---
# <a name="itnefextractprops"></a><span data-ttu-id="69657-103">ITnef::ExtractProps</span><span class="sxs-lookup"><span data-stu-id="69657-103">ITnef::ExtractProps</span></span>

  
  
<span data-ttu-id="69657-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="69657-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="69657-105">Extrait les propriétés d’une encapsulation TNEF.</span><span class="sxs-lookup"><span data-stu-id="69657-105">Extracts the properties from a TNEF encapsulation.</span></span> 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a><span data-ttu-id="69657-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="69657-106">Parameters</span></span>

 <span data-ttu-id="69657-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="69657-107">_ulFlags_</span></span>
  
> <span data-ttu-id="69657-108">[in] Masque de bits d’indicateurs qui contrôle la façon dont les propriétés sont décodées.</span><span class="sxs-lookup"><span data-stu-id="69657-108">[in] A bitmask of flags that controls how properties are decoded.</span></span> <span data-ttu-id="69657-109">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="69657-109">The following flags can be set:</span></span>
    
<span data-ttu-id="69657-110">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="69657-110">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="69657-111">Décode toutes les propriétés non spécifiées dans le paramètre _lpPropList_ .</span><span class="sxs-lookup"><span data-stu-id="69657-111">Decodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="69657-112">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="69657-112">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="69657-113">Décode toutes les propriétés spécifiées dans _lpPropList_.</span><span class="sxs-lookup"><span data-stu-id="69657-113">Decodes all properties specified in  _lpPropList_.</span></span>
    
 <span data-ttu-id="69657-114">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="69657-114">_lpPropList_</span></span>
  
> <span data-ttu-id="69657-115">[in] Pointeur vers la liste des propriétés à inclure ou exclure de l’opération de décodage.</span><span class="sxs-lookup"><span data-stu-id="69657-115">[in] A pointer to the list of properties to include in or exclude from the decoding operation.</span></span>
    
 <span data-ttu-id="69657-116">_lpProblems_</span><span class="sxs-lookup"><span data-stu-id="69657-116">_lpProblems_</span></span>
  
> <span data-ttu-id="69657-117">[out] Pointeur vers un pointeur vers une structure [STnefProblemArray](stnefproblemarray.md) renvoyée.</span><span class="sxs-lookup"><span data-stu-id="69657-117">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="69657-118">La structure **STnefProblemArray** indique les propriétés, le cas échéant, ont été pas codées correctement.</span><span class="sxs-lookup"><span data-stu-id="69657-118">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="69657-119">Si NULL est indiqué dans le paramètre _lpProblems_ , aucun tableau de problème de propriété n’est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="69657-119">If NULL is passed in the  _lpProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="69657-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="69657-120">Return value</span></span>

<span data-ttu-id="69657-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="69657-121">S_OK</span></span> 
  
> <span data-ttu-id="69657-122">L’appel a réussi et renvoyé la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="69657-122">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="69657-123">MAPI_E_CORRUPT_DATA</span><span class="sxs-lookup"><span data-stu-id="69657-123">MAPI_E_CORRUPT_DATA</span></span> 
  
> <span data-ttu-id="69657-124">En cours de décodage dans un flux de données sont endommagées.</span><span class="sxs-lookup"><span data-stu-id="69657-124">Data being decoded into a stream is corrupted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="69657-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="69657-125">Remarks</span></span>

<span data-ttu-id="69657-126">Fournisseurs de transport, les fournisseurs de banque de message et passerelles appellent la méthode de **ITnef::ExtractProps** pour extraire (qui est, décoder) propriétés à partir de l’encapsulation d’un message ou d’une pièce jointe qui a été passée à la fonction [OpenTnefStream](opentnefstream.md) .</span><span class="sxs-lookup"><span data-stu-id="69657-126">Transport providers, message store providers, and gateways call the **ITnef::ExtractProps** method to extract (that is, decode) properties from the encapsulation of a message or an attachment that was passed to the [OpenTnefStream](opentnefstream.md) function.</span></span> <span data-ttu-id="69657-127">La passerelle ou le fournisseur appelant peut spécifier une liste de propriétés à décoder.</span><span class="sxs-lookup"><span data-stu-id="69657-127">The calling provider or gateway can specify a list of properties to decode.</span></span> <span data-ttu-id="69657-128">Fournisseurs et des passerelles peuvent également utiliser **ExtractProps** pour fournir des informations sur aucun traitement spécial pour les pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="69657-128">Providers and gateways can also use **ExtractProps** to provide information about any special handling for attachments.</span></span> 
  
 <span data-ttu-id="69657-129">**ExtractProps** remplit le message d’origine est passé en **OpenTnefStream** avec les propriétés décodées.</span><span class="sxs-lookup"><span data-stu-id="69657-129">**ExtractProps** populates the original message passed into **OpenTnefStream** with the decoded properties.</span></span> <span data-ttu-id="69657-130">Les appels suivants **ExtractProps** revenir au message et extrayez la nouvelle liste de propriétés.</span><span class="sxs-lookup"><span data-stu-id="69657-130">Subsequent **ExtractProps** calls go back to the message and extract the new list of properties.</span></span> 
  
<span data-ttu-id="69657-131">Contrairement à la méthode [ITnef::AddProps](itnef-addprops.md) , files d’attente demandé actions jusqu'à ce que la méthode **ITnef::Finish** est appelée, la méthode **ExtractProps** décode les propriétés encapsulées immédiatement lorsqu’elle est appelée.</span><span class="sxs-lookup"><span data-stu-id="69657-131">Unlike the [ITnef::AddProps](itnef-addprops.md) method, which queues requested actions until the **ITnef::Finish** method is called, the **ExtractProps** method decodes the encapsulated properties immediately when it is called.</span></span> <span data-ttu-id="69657-132">Pour cette raison, le message cible de décodage encapsulation doit être relativement vide.</span><span class="sxs-lookup"><span data-stu-id="69657-132">For that reason, the target message for encapsulation decoding should be relatively empty.</span></span> <span data-ttu-id="69657-133">Propriétés existantes dans le message cible sont remplacées par les propriétés encapsulées.</span><span class="sxs-lookup"><span data-stu-id="69657-133">Existing properties in the target message are overwritten by encapsulated properties.</span></span> 
  
 <span data-ttu-id="69657-134">**ExtractProps** est pris en charge uniquement pour les objets qui sont ouverts avec l’indicateur TNEF_DECODE pour la fonction **OpenTnefStream** ou [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="69657-134">**ExtractProps** is supported only for objects that are opened with the TNEF_DECODE flag for the **OpenTnefStream** or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="69657-135">L’implémentation TNEF signale des problèmes de codage TNEF flux sans interrompre le processus **ExtractProps** .</span><span class="sxs-lookup"><span data-stu-id="69657-135">The TNEF implementation reports TNEF stream encoding problems without stopping the **ExtractProps** process.</span></span> <span data-ttu-id="69657-136">La structure [STnefProblemArray](stnefproblemarray.md) retournée dans _lpProblems_ indique les attributs TNEF ou des propriétés MAPI, le cas échéant, pas peuvent être traitées.</span><span class="sxs-lookup"><span data-stu-id="69657-136">The [STnefProblemArray](stnefproblemarray.md) structure returned in  _lpProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="69657-137">La valeur renvoyée dans le membre **scode** de l’une des structures **STnefProblem** contenues dans **STnefProblemArray** indiquant le problème spécifique.</span><span class="sxs-lookup"><span data-stu-id="69657-137">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="69657-138">Le fournisseur ou la passerelle peut travailler sur l’hypothèse que toutes les propriétés ou les attributs pour lesquels **ExtractProps** ne renvoie pas un rapport de problème ont été correctement traités.</span><span class="sxs-lookup"><span data-stu-id="69657-138">The provider or gateway can work on the assumption that all properties or attributes for which **ExtractProps** does not return a problem report were processed successfully.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="69657-139">Si une propriété dans le bloc d’encapsulation MAPI ne peut pas être traitée et laisse le flux non fiables pendant le décodage d’un flux TNEF, décodage du bloc encapsulation est arrêté et un problème est signalé.</span><span class="sxs-lookup"><span data-stu-id="69657-139">If a property in the MAPI encapsulation block cannot be processed and leaves the stream unreliable during the decoding of a TNEF stream, decoding of the encapsulation block is stopped and a problem is reported.</span></span> <span data-ttu-id="69657-140">Le tableau de problème pour ce type de problème contient 0L du membre **ulPropTag** , `attMAPIProps` ou `attAttachment` pour le membre **ulAttribute** et MAPI_E_UNABLE_TO_COMPLETE du membre **scode** .</span><span class="sxs-lookup"><span data-stu-id="69657-140">The problem array for this type of problem contains 0L for the **ulPropTag** member,  `attMAPIProps` or  `attAttachment` for the **ulAttribute** member, and MAPI_E_UNABLE_TO_COMPLETE for the **scode** member.</span></span> <span data-ttu-id="69657-141">Notez que le décodage du flux n’est pas interrompu, simplement le décodage du bloc encapsulation MAPI.</span><span class="sxs-lookup"><span data-stu-id="69657-141">Note that the decoding of the stream is not halted, just the decoding of the MAPI encapsulation block.</span></span> <span data-ttu-id="69657-142">Le décodage des flux se poursuit avec le bloc d’attributs suivant.</span><span class="sxs-lookup"><span data-stu-id="69657-142">The stream decoding continues with the next attribute block.</span></span> 
  
<span data-ttu-id="69657-143">Si un fournisseur ou une passerelle ne fonctionne pas avec des tableaux de problème, il peut passer NULL dans _lppProblems_; Dans ce cas, aucun tableau de problème n’est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="69657-143">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="69657-144">La valeur renvoyée dans _lpProblems_ est valide uniquement si l’appel renvoie S_OK.</span><span class="sxs-lookup"><span data-stu-id="69657-144">The value returned in  _lpProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="69657-145">Lorsque S_OK est retourné, le fournisseur ou la passerelle doit vérifier les valeurs renvoyées dans la structure **STnefProblemArray** .</span><span class="sxs-lookup"><span data-stu-id="69657-145">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="69657-146">Si une erreur se produit lors de l’appel, la structure **STnefProblemArray** n’est pas renseignée et la passerelle ou le fournisseur appelant ne doit pas utiliser ou libérer la structure.</span><span class="sxs-lookup"><span data-stu-id="69657-146">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="69657-147">Si aucune erreur ne se produit lors de l’appel, la passerelle ou le fournisseur appelant doit libérer de la mémoire de la structure **STnefProblemArray** en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="69657-147">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="69657-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69657-148">See also</span></span>



[<span data-ttu-id="69657-149">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="69657-149">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="69657-150">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="69657-150">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="69657-151">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="69657-151">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="69657-152">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="69657-152">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="69657-153">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="69657-153">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="69657-154">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="69657-154">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="69657-155">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="69657-155">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="69657-156">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="69657-156">ITnef : IUnknown</span></span>](itnefiunknown.md)

