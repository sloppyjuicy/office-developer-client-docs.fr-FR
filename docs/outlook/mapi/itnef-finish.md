---
title: ITnefFinish
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.Finish
api_type:
- COM
ms.assetid: 01a868f4-afda-43ba-bc17-c33ae56b7b7d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5b76f9daec89e9229fc7f81e1332c3075c951067
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435676"
---
# <a name="itneffinish"></a><span data-ttu-id="58073-103">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="58073-103">ITnef::Finish</span></span>

  
  
<span data-ttu-id="58073-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58073-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58073-105">Termine le traitement de toutes les Transport-Neutral de format d’encapsulation (TNEF) qui sont en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="58073-105">Finishes processing for all Transport-Neutral Encapsulation Format (TNEF) operations that are queued and waiting.</span></span> 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a><span data-ttu-id="58073-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58073-106">Parameters</span></span>

 <span data-ttu-id="58073-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="58073-107">_ulFlags_</span></span>
  
> <span data-ttu-id="58073-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="58073-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="58073-109">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="58073-109">_lpKey_</span></span>
  
> <span data-ttu-id="58073-110">[out] Pointeur vers la propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) d’une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="58073-110">[out] A pointer to the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) key property of an attachment.</span></span> <span data-ttu-id="58073-111">L’objet d’encapsulation TNEF utilise cette clé pour faire correspondre une pièce jointe à sa balise de placement des pièces jointes dans un message.</span><span class="sxs-lookup"><span data-stu-id="58073-111">The TNEF encapsulation object uses this key to match an attachment to its attachment placement tag in a message.</span></span> <span data-ttu-id="58073-112">Cette clé doit être unique pour chaque pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="58073-112">This key should be unique to each attachment.</span></span>
    
 <span data-ttu-id="58073-113">_lpProblem_</span><span class="sxs-lookup"><span data-stu-id="58073-113">_lpProblem_</span></span>
  
> <span data-ttu-id="58073-114">[out] Pointeur vers un pointeur vers une structure [STnefProblemArray](stnefproblemarray.md) renvoyée.</span><span class="sxs-lookup"><span data-stu-id="58073-114">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="58073-115">La structure **STnefProblemArray** indique les propriétés, le cas contraire, qui n’ont pas été correctement codées.</span><span class="sxs-lookup"><span data-stu-id="58073-115">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="58073-116">Si NULL est transmis dans le  _paramètre lpProblem,_ aucun tableau de problèmes de propriété n’est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="58073-116">If NULL is passed in the  _lpProblem_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="58073-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="58073-117">Return value</span></span>

<span data-ttu-id="58073-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="58073-118">S_OK</span></span> 
  
> <span data-ttu-id="58073-119">L’appel a réussi et a renvoyé la ou les valeurs attendues.</span><span class="sxs-lookup"><span data-stu-id="58073-119">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="58073-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="58073-120">Remarks</span></span>

<span data-ttu-id="58073-121">Les fournisseurs de transport, les fournisseurs de magasins de messages et les passerelles appellent la méthode **ITnef::Finish** pour effectuer le codage de toutes les propriétés pour lesquelles le codage a été demandé dans les appels aux méthodes [ITnef::AddProps](itnef-addprops.md) et [ITnef::SetProps.](itnef-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="58073-121">Transport providers, message store providers, and gateways call the **ITnef::Finish** method to perform the encoding of all properties for which encoding was requested in calls to the [ITnef::AddProps](itnef-addprops.md) and [ITnef::SetProps](itnef-setprops.md) methods.</span></span> <span data-ttu-id="58073-122">Si l’objet TNEF a été ouvert avec l’indicateur TNEF_ENCODE pour la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx,](opentnefstreamex.md) la méthode **Finish** code les propriétés demandées dans le flux d’encapsulation transmis à cet objet.</span><span class="sxs-lookup"><span data-stu-id="58073-122">If the TNEF object was opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function, the **Finish** method encodes the requested properties into the encapsulation stream passed to that object.</span></span> <span data-ttu-id="58073-123">Si l’objet TNEF a été ouvert avec l’indicateur TNEF_DECODE, la méthode **Finish** décode les propriétés du flux TNEF et les écrit dans le message à qui ils appartiennent.</span><span class="sxs-lookup"><span data-stu-id="58073-123">If the TNEF object was opened with the TNEF_DECODE flag, the **Finish** method decodes the properties from the TNEF stream and writes them back to the message they belong to.</span></span> 
  
<span data-ttu-id="58073-124">Après **l’appel Terminer,** le pointeur vers le flux d’encapsulation pointe vers la fin des données TNEF.</span><span class="sxs-lookup"><span data-stu-id="58073-124">After the **Finish** call, the pointer to the encapsulation stream points to the end of the TNEF data.</span></span> <span data-ttu-id="58073-125">Si le fournisseur ou la passerelle doit utiliser  les données de flux TNEF après l’appel de fin, il doit réinitialiser le pointeur de flux au début des données de flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="58073-125">If the provider or gateway needs to use the TNEF stream data after the **Finish** call, it must reset the stream pointer to the beginning of the TNEF stream data.</span></span> 
  
<span data-ttu-id="58073-126">L’implémentation TNEF signale des problèmes de codage de flux TNEF sans arrêter **le processus Finish.**</span><span class="sxs-lookup"><span data-stu-id="58073-126">The TNEF implementation reports TNEF stream encoding problems without stopping the **Finish** process.</span></span> <span data-ttu-id="58073-127">La structure [STnefProblemArray](stnefproblemarray.md) renvoyée dans le paramètre  _lpProblem_ indique quels attributs TNEF ou propriétés MAPI, le cas contraire, n’ont pas pu être traitées.</span><span class="sxs-lookup"><span data-stu-id="58073-127">The [STnefProblemArray](stnefproblemarray.md) structure returned in the  _lpProblem_ parameter indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="58073-128">La valeur renvoyée dans le membre **scode** de l’une des structures **STnefProblem** contenues dans **STnefProblemArray** indique le problème spécifique.</span><span class="sxs-lookup"><span data-stu-id="58073-128">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="58073-129">Le fournisseur ou la passerelle peut fonctionner sur l’hypothèse que toutes les propriétés ou attributs pour lesquels **Finish** ne retourne pas de rapport de problème ont été correctement traitées.</span><span class="sxs-lookup"><span data-stu-id="58073-129">The provider or gateway can work on the assumption that all properties or attributes for which **Finish** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="58073-130">Si un fournisseur ou une passerelle ne fonctionne pas avec des tableaux à problème, il peut transmettre null dans  _lpProblem_; dans ce cas, aucun tableau de problèmes n’est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="58073-130">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lpProblem_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="58073-131">La valeur renvoyée dans  _lpProblem_ n’est valide que si l’appel S_OK.</span><span class="sxs-lookup"><span data-stu-id="58073-131">The value returned in  _lpProblem_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="58073-132">Lorsque S_OK est renvoyé, le fournisseur ou la passerelle doit vérifier les valeurs renvoyées dans la structure **STnefProblemArray.**</span><span class="sxs-lookup"><span data-stu-id="58073-132">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="58073-133">Si une erreur se produit lors de l’appel, la structure **STnefProblemArray** n’est pas remplie et le fournisseur ou la passerelle appelant ne doit pas utiliser ou libérer la structure.</span><span class="sxs-lookup"><span data-stu-id="58073-133">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="58073-134">Si aucune erreur ne se produit lors de l’appel, le fournisseur ou la passerelle appelant doit libérer la mémoire de **l’objet STnefProblemArray** en appelant la fonction [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="58073-134">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="58073-135">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="58073-135">MFCMAPI reference</span></span>

<span data-ttu-id="58073-136">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="58073-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="58073-137">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="58073-137">**File**</span></span>|<span data-ttu-id="58073-138">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="58073-138">**Function**</span></span>|<span data-ttu-id="58073-139">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="58073-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="58073-140">File.cpp</span><span class="sxs-lookup"><span data-stu-id="58073-140">File.cpp</span></span>  <br/> |<span data-ttu-id="58073-141">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="58073-141">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="58073-142">MFCMAPI utilise la **méthode ITnef::Finish** pour terminer le traitement du nouveau flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="58073-142">MFCMAPI uses the **ITnef::Finish** method to finish processing of the new TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="58073-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58073-143">See also</span></span>



[<span data-ttu-id="58073-144">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="58073-144">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="58073-145">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="58073-145">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="58073-146">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="58073-146">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="58073-147">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="58073-147">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="58073-148">Propriété canonique PidTagAttachNumber</span><span class="sxs-lookup"><span data-stu-id="58073-148">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="58073-149">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="58073-149">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="58073-150">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="58073-150">ITnef : IUnknown</span></span>](itnefiunknown.md)


[<span data-ttu-id="58073-151">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="58073-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

