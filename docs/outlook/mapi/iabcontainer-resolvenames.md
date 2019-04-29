---
title: IABContainerResolveNames
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.ResolveNames
api_type:
- COM
ms.assetid: 27474af2-29a2-4cfb-b94f-72eb91562dac
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: fac4978bef94650f85ac3179acd3858602f933ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405813"
---
# <a name="iabcontainerresolvenames"></a><span data-ttu-id="3c52f-103">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="3c52f-103">IABContainer::ResolveNames</span></span>

  
  
<span data-ttu-id="3c52f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c52f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c52f-105">Effectue la résolution de noms pour une ou plusieurs entrées de destinataires.</span><span class="sxs-lookup"><span data-stu-id="3c52f-105">Performs name resolution for one or more recipient entries.</span></span>
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a><span data-ttu-id="3c52f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c52f-106">Parameters</span></span>

 <span data-ttu-id="3c52f-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="3c52f-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="3c52f-108">dans Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété décrivant les propriétés à inclure dans la structure [ADRLIST](adrlist.md) renvoyée par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3c52f-108">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags describing the properties to be included in the [ADRLIST](adrlist.md) structure returned by the provider.</span></span> <span data-ttu-id="3c52f-109">Pour demander le jeu de propriétés par défaut du fournisseur, transmettez la valeur NULL dans le paramètre _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="3c52f-109">To request the provider's default set of properties, pass NULL in the  _lpPropTagArray_ parameter.</span></span> 
    
 <span data-ttu-id="3c52f-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3c52f-110">_ulFlags_</span></span>
  
> <span data-ttu-id="3c52f-111">dans Masque de des indicateurs qui contrôle le type du texte dans les chaînes renvoyées.</span><span class="sxs-lookup"><span data-stu-id="3c52f-111">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="3c52f-112">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="3c52f-112">The following flags can be set:</span></span>
    
<span data-ttu-id="3c52f-113">EMS_AB_ADDRESS_LOOKUP</span><span class="sxs-lookup"><span data-stu-id="3c52f-113">EMS_AB_ADDRESS_LOOKUP</span></span>
  
> <span data-ttu-id="3c52f-114">Seules les correspondances d'adresse proxy exactes seront trouvées; les correspondances partielles sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="3c52f-114">Only exact proxy address matches will be found; partial matches are ignored.</span></span> <span data-ttu-id="3c52f-115">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="3c52f-115">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="3c52f-116">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="3c52f-116">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="3c52f-117">Seul le carnet d'adresses en mode hors connexion sera utilisé pour la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="3c52f-117">Only the offline address book will be used to perform name resolution.</span></span> <span data-ttu-id="3c52f-118">Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d'ouvrir la liste d'adresses globale (LAG) en mode Exchange mis en cache et d'accéder à une entrée de ce carnet d'adresses à partir du cache sans créer de trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="3c52f-118">For example, you can use this flag to enable a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="3c52f-119">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="3c52f-119">This flag is supported only by the Exchange Address Book Provider.</span></span> 
    
<span data-ttu-id="3c52f-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3c52f-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3c52f-121">Les propriétés de chaîne retournées sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="3c52f-121">The returned string properties are in Unicode format.</span></span> <span data-ttu-id="3c52f-122">Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="3c52f-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="3c52f-123">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="3c52f-123">_lpAdrList_</span></span>
  
> <span data-ttu-id="3c52f-124">[in, out] En entrée, pointeur vers une structure **ADRLIST** qui contient la liste des destinataires à résoudre.</span><span class="sxs-lookup"><span data-stu-id="3c52f-124">[in, out] On input, a pointer to an **ADRLIST** structure that contains the list of recipients to be resolved.</span></span> <span data-ttu-id="3c52f-125">En sortie, pointeur vers une structure **ADRLIST** qui contient les noms résolus.</span><span class="sxs-lookup"><span data-stu-id="3c52f-125">On output, a pointer to an **ADRLIST** structure that contains the resolved names.</span></span> 
    
 <span data-ttu-id="3c52f-126">_lpFlagList_</span><span class="sxs-lookup"><span data-stu-id="3c52f-126">_lpFlagList_</span></span>
  
> <span data-ttu-id="3c52f-127">[in, out] Pointeur vers un tableau d'indicateurs, chaque indicateur correspondant à une structure [ADRENTRY](adrentry.md) dans le paramètre _lpAdrList_ , qui fournit l'état de l'opération de résolution de noms pour le destinataire.</span><span class="sxs-lookup"><span data-stu-id="3c52f-127">[in, out] A pointer to an array of flags, each flag corresponding to an [ADRENTRY](adrentry.md) structure in the  _lpAdrList_ parameter, that provides the status of the name resolution operation for the recipient.</span></span> <span data-ttu-id="3c52f-128">Les indicateurs dans le paramètre _lpFlagList_ sont dans le même ordre que les entrées dans _lpAdrList_.</span><span class="sxs-lookup"><span data-stu-id="3c52f-128">The flags in the  _lpFlagList_ parameter are in the same order as the entries in  _lpAdrList_.</span></span> <span data-ttu-id="3c52f-129">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="3c52f-129">The following flags can be set:</span></span>
    
<span data-ttu-id="3c52f-130">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="3c52f-130">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="3c52f-131">Le destinataire correspondant a été résolu, mais pas à un identificateur d'entrée unique.</span><span class="sxs-lookup"><span data-stu-id="3c52f-131">The corresponding recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="3c52f-132">Les autres conteneurs ne doivent pas essayer de résoudre ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="3c52f-132">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="3c52f-133">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="3c52f-133">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="3c52f-134">Le destinataire correspondant a été résolu en un identificateur d'entrée unique.</span><span class="sxs-lookup"><span data-stu-id="3c52f-134">The corresponding recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="3c52f-135">Les autres conteneurs ne doivent pas essayer de résoudre ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="3c52f-135">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="3c52f-136">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="3c52f-136">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="3c52f-137">L'entrée correspondante n'a pas été résolue.</span><span class="sxs-lookup"><span data-stu-id="3c52f-137">The corresponding entry has not been resolved.</span></span> <span data-ttu-id="3c52f-138">D'autres conteneurs doivent essayer de résoudre ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="3c52f-138">Other containers should try to resolve this recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3c52f-139">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3c52f-139">Return value</span></span>

<span data-ttu-id="3c52f-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="3c52f-140">S_OK</span></span> 
  
> <span data-ttu-id="3c52f-141">Le processus de résolution de noms a réussi.</span><span class="sxs-lookup"><span data-stu-id="3c52f-141">The name resolution process was successful.</span></span>
    
<span data-ttu-id="3c52f-142">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="3c52f-142">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="3c52f-143">L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.</span><span class="sxs-lookup"><span data-stu-id="3c52f-143">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="3c52f-144">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="3c52f-144">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="3c52f-145">Le fournisseur de carnet d'adresses ne prend pas en charge la résolution de noms en bloc à l'aide de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3c52f-145">The address book provider does not support bulk name resolution by using this method.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3c52f-146">Remarques</span><span class="sxs-lookup"><span data-stu-id="3c52f-146">Remarks</span></span>

<span data-ttu-id="3c52f-147">La méthode **ResolveNames** tente de faire correspondre les destinataires non résolus du tableau d'entrées du paramètre _lpAdrList_ aux destinataires de ce conteneur de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="3c52f-147">The **ResolveNames** method attempts to match unresolved recipients from the array of entries in the  _lpAdrList_ parameter to recipients in this address book container.</span></span> <span data-ttu-id="3c52f-148">Un destinataire non résolu dispose généralement uniquement de la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) et éventuellement d'autres propriétés.</span><span class="sxs-lookup"><span data-stu-id="3c52f-148">An unresolved recipient typically has only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property and possibly a few other properties.</span></span> <span data-ttu-id="3c52f-149">Un destinataire non résolu ne dispose pas de la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) et son indicateur correspondant dans le paramètre _lpFlagList_ est défini sur MAPI_UNRESOLVED.</span><span class="sxs-lookup"><span data-stu-id="3c52f-149">An unresolved recipient does not have the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, and its corresponding flag in the  _lpFlagList_ parameter is set to MAPI_UNRESOLVED.</span></span> <span data-ttu-id="3c52f-150">À l'inverse, un destinataire résolu dispose toujours au moins de la propriété **PR_ENTRYID** , ainsi que d'autres propriétés telles que **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**et **PR_ADDRTYPE** ([ PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3c52f-150">Conversely, a resolved recipient always has at least the **PR_ENTRYID** property plus several other properties such as **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**, and **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span></span>
  
<span data-ttu-id="3c52f-151">La résolution de noms démarre généralement lorsqu'un client appelle la méthode [IAddrBook:: ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="3c52f-151">Name resolution typically starts when a client calls the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="3c52f-152">Outlook MAPI répond en appelant la méthode **ResolveNames** de chaque conteneur de carnet d'adresses inclus dans le chemin de recherche de carnet d'adresses, spécifié par la propriété **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3c52f-152">Outlook MAPI responds by calling the **ResolveNames** method of each address book container included in the address book search path, specified by the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property.</span></span> <span data-ttu-id="3c52f-153">Les entrées du paramètre _lpAdrList_ incluent les destinataires déjà résolus car il s'agit de conteneurs pour lesquels MAPI a déjà appelé **ResolveNames**, car les entrées apparaissent plus tôt dans le chemin de recherche.</span><span class="sxs-lookup"><span data-stu-id="3c52f-153">The entries in the  _lpAdrList_ parameter include recipients already resolved because they are in containers for which MAPI has already called **ResolveNames**, because the entries appear earlier in the search path.</span></span> 
  
<span data-ttu-id="3c52f-154">Chaque conteneur tente de résoudre les entrées non résolues en faisant correspondre le nom d'affichage du destinataire avec le nom d'affichage de l'une de ses entrées.</span><span class="sxs-lookup"><span data-stu-id="3c52f-154">Each container attempts to resolve the unresolved entries by matching the display name of the recipient with the display name of one of its entries.</span></span> <span data-ttu-id="3c52f-155">Lorsqu'une correspondance unique est trouvée, **ResolveNames** ajoute la propriété **PR_ENTRYID** et d'autres propriétés incluses dans le paramètre _lpPropTagArray_ à l'entrée correspondante dans la structure **ADRLIST** sortante.</span><span class="sxs-lookup"><span data-stu-id="3c52f-155">When a unique match is found, **ResolveNames** adds the **PR_ENTRYID** property and other properties that are included in the  _lpPropTagArray_ parameter to the corresponding entry in the outgoing **ADRLIST** structure.</span></span> <span data-ttu-id="3c52f-156">**ResolveNames** définit ensuite l'entrée dans le paramètre _lpFlagList_ sur MAPI_RESOLVED.</span><span class="sxs-lookup"><span data-stu-id="3c52f-156">**ResolveNames** then sets the entry in the  _lpFlagList_ parameter to MAPI_RESOLVED.</span></span> <span data-ttu-id="3c52f-157">L'identificateur d'entrée stocké dans la propriété **PR_ENTRYID** peut être court ou long terme.</span><span class="sxs-lookup"><span data-stu-id="3c52f-157">The entry identifier stored in the **PR_ENTRYID** property can be short-term or long-term.</span></span> 
  
<span data-ttu-id="3c52f-158">Une fois que tous les conteneurs dans le chemin de recherche ont tenté le processus de résolution de noms, MAPI ouvre une boîte de dialogue, si possible, pour inviter l'utilisateur à trouver de l'aide pour résoudre les conflits restants.</span><span class="sxs-lookup"><span data-stu-id="3c52f-158">After all of the containers in the search path have attempted the name resolution process, MAPI opens a dialog box, if possible, to prompt the user for help in resolving any remaining conflicts.</span></span> 
  
<span data-ttu-id="3c52f-159">Les clients peuvent également utiliser la structure **ADRLIST** renvoyée dans les appels à la méthode [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="3c52f-159">Clients can also use the returned **ADRLIST** structure in calls to the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3c52f-160">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="3c52f-160">Notes to implementers</span></span>

<span data-ttu-id="3c52f-161">Vous n'êtes pas obligé de prendre en charge la résolution de nom avec la méthode **ResolveNames** .</span><span class="sxs-lookup"><span data-stu-id="3c52f-161">You are not required to support name resolution with the **ResolveNames** method.</span></span> <span data-ttu-id="3c52f-162">Au lieu de cela, vous pouvez également le prendre en charge à l'aide de la restriction de propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3c52f-162">Instead, or additionally, you can support it with the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="3c52f-163">Si vous décidez de reposer sur la restriction **PR_ANR** pour la résolution de noms, vous pouvez renvoyer MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="3c52f-163">If you decide to rely on the **PR_ANR** restriction for name resolution, you can return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="3c52f-164">For more information, see [L'impl�mentation de la r�solution de noms](implementing-name-resolution.md).</span><span class="sxs-lookup"><span data-stu-id="3c52f-164">For more information, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="3c52f-165">Définissez l'entrée d'indicateur d'un destinataire dans le paramètre _lpFlagList_ sur MAPI_UNRESOLVED si le destinataire ne correspond à aucun des destinataires du conteneur.</span><span class="sxs-lookup"><span data-stu-id="3c52f-165">Set a recipient's flag entry in the  _lpFlagList_ parameter to MAPI_UNRESOLVED if the recipient does not match any of the container's recipients.</span></span> 
  
<span data-ttu-id="3c52f-166">Lorsqu'un destinataire correspond à plusieurs destinataires, définissez son indicateur sur MAPI_AMBIGUOUS et ne modifiez pas sa structure **ADRENTRY** .</span><span class="sxs-lookup"><span data-stu-id="3c52f-166">When a recipient matches multiple recipients, set its flag to MAPI_AMBIGUOUS and do not change its **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="3c52f-167">MAPI requiert certaines propriétés pour les destinataires inclus dans la liste des destinataires d'un message.</span><span class="sxs-lookup"><span data-stu-id="3c52f-167">MAPI requires certain properties for recipients that are included in a message's recipient list.</span></span> <span data-ttu-id="3c52f-168">Vous pouvez les inclure dans la structure **ADRENTRY** dans le cadre du processus de résolution de noms ou attendre MAPI pour les demander avec des appels à [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) et [IMAPISupport:: ExpandRecips](imapisupport-expandrecips.md) methods.</span><span class="sxs-lookup"><span data-stu-id="3c52f-168">You can include them in the **ADRENTRY** structure as part of the name resolution process or wait for MAPI to request them with calls to the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) and [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) methods.</span></span> <span data-ttu-id="3c52f-169">Vous pouvez éliminer ces appels supplémentaires et améliorer les performances en incluant les propriétés suivantes dans les structures **ADRENTRY** de tous les destinataires résolus:</span><span class="sxs-lookup"><span data-stu-id="3c52f-169">You can eliminate these extra calls and improve performance by including the following properties in the **ADRENTRY** structures of all resolved recipients:</span></span> 
  
- <span data-ttu-id="3c52f-170">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="3c52f-170">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="3c52f-171">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="3c52f-171">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="3c52f-172">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="3c52f-172">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="3c52f-173">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="3c52f-173">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="3c52f-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3c52f-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="3c52f-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3c52f-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
- <span data-ttu-id="3c52f-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3c52f-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="3c52f-177">Si certaines propriétés du paramètre _lpPropTagArray_ ne sont pas disponibles, en général parce que l'entrée de conteneur ne prend pas en charge les propriétés et qu'elles ne sont pas incluses dans le membre **ADRENTRY** du destinataire dans la structure **ADRLIST** , Définissez le type de propriété de chaque propriété unavailable sur PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="3c52f-177">If some of the properties in the  _lpPropTagArray_ parameter are unavailable—typically because the container entry does not support the properties and they are not included in the recipient's **ADRENTRY** member in the **ADRLIST** structure—set the property type of each unavailable property to PT_ERROR.</span></span> 
  
<span data-ttu-id="3c52f-178">Ne supprimez pas les propriétés de la structure **ADRENTRY** d'un destinataire résolu.</span><span class="sxs-lookup"><span data-stu-id="3c52f-178">Do not remove any properties from a resolved recipient's **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="3c52f-179">Si vous devez remplacer au lieu de modifier une structure **ADRENTRY** , libérez d'abord la structure **ADRENTRY** d'origine en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) , puis allouez la structure de **ADRENTRY** de remplacement avec [ MAPIAllocateBuffer](mapiallocatebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="3c52f-179">If you must replace rather than modify an **ADRENTRY** structure, free the original **ADRENTRY** structure first by calling the [MAPIFreeBuffer](mapifreebuffer.md) function, and then allocate the replacement **ADRENTRY** structure with [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3c52f-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c52f-180">See also</span></span>



[<span data-ttu-id="3c52f-181">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="3c52f-181">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="3c52f-182">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="3c52f-182">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="3c52f-183">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="3c52f-183">IAddrBook::PrepareRecips</span></span>](iaddrbook-preparerecips.md)
  
[<span data-ttu-id="3c52f-184">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="3c52f-184">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="3c52f-185">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="3c52f-185">IMAPISupport::ExpandRecips</span></span>](imapisupport-expandrecips.md)
  
[<span data-ttu-id="3c52f-186">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="3c52f-186">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="3c52f-187">Propriété canonique PidTagAnr</span><span class="sxs-lookup"><span data-stu-id="3c52f-187">PidTagAnr Canonical Property</span></span>](pidtaganr-canonical-property.md)
  
[<span data-ttu-id="3c52f-188">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="3c52f-188">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="3c52f-189">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="3c52f-189">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

