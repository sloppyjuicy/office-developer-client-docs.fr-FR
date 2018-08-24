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
ms.openlocfilehash: 81f35f659342d6258d60f40b12bd0a3ac2dc20b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588474"
---
# <a name="iabcontainerresolvenames"></a><span data-ttu-id="327e5-103">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="327e5-103">IABContainer::ResolveNames</span></span>

  
  
<span data-ttu-id="327e5-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="327e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="327e5-105">Effectue la résolution de noms pour une ou plusieurs entrées de destinataire.</span><span class="sxs-lookup"><span data-stu-id="327e5-105">Performs name resolution for one or more recipient entries.</span></span>
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a><span data-ttu-id="327e5-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="327e5-106">Parameters</span></span>

 <span data-ttu-id="327e5-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="327e5-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="327e5-108">[in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriétés décrivant les propriétés à inclure dans la structure [ADRLIST](adrlist.md) retournée par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="327e5-108">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags describing the properties to be included in the [ADRLIST](adrlist.md) structure returned by the provider.</span></span> <span data-ttu-id="327e5-109">Pour demander le jeu de propriétés par défaut du fournisseur, passez la valeur NULL dans le paramètre _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="327e5-109">To request the provider's default set of properties, pass NULL in the  _lpPropTagArray_ parameter.</span></span> 
    
 <span data-ttu-id="327e5-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="327e5-110">_ulFlags_</span></span>
  
> <span data-ttu-id="327e5-111">[in] Masque de bits d’indicateurs qui contrôle le type du texte dans les chaînes retournées.</span><span class="sxs-lookup"><span data-stu-id="327e5-111">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="327e5-112">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="327e5-112">The following flags can be set:</span></span>
    
<span data-ttu-id="327e5-113">EMS_AB_ADDRESS_LOOKUP</span><span class="sxs-lookup"><span data-stu-id="327e5-113">EMS_AB_ADDRESS_LOOKUP</span></span>
  
> <span data-ttu-id="327e5-114">Vous trouverez les correspondances d’adresse proxy exacte uniquement ; correspondances partielles sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="327e5-114">Only exact proxy address matches will be found; partial matches are ignored.</span></span> <span data-ttu-id="327e5-115">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="327e5-115">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="327e5-116">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="327e5-116">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="327e5-117">Uniquement le carnet d’adresses en mode hors connexion permet de résoudre les noms.</span><span class="sxs-lookup"><span data-stu-id="327e5-117">Only the offline address book will be used to perform name resolution.</span></span> <span data-ttu-id="327e5-118">Par exemple, vous pouvez utiliser cet indicateur pour activer une application cliente ouvrir la liste d’adresses globale (LAG) en mode exchange mis en cache et accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer le trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="327e5-118">For example, you can use this flag to enable a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="327e5-119">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="327e5-119">This flag is supported only by the Exchange Address Book Provider.</span></span> 
    
<span data-ttu-id="327e5-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="327e5-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="327e5-121">Les propriétés de la chaîne retournée sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="327e5-121">The returned string properties are in Unicode format.</span></span> <span data-ttu-id="327e5-122">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="327e5-122">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="327e5-123">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="327e5-123">_lpAdrList_</span></span>
  
> <span data-ttu-id="327e5-124">[entrée, sortie] À l’entrée, un pointeur vers une structure **ADRLIST** qui contient la liste des destinataires à résoudre.</span><span class="sxs-lookup"><span data-stu-id="327e5-124">[in, out] On input, a pointer to an **ADRLIST** structure that contains the list of recipients to be resolved.</span></span> <span data-ttu-id="327e5-125">Dans la sortie, un pointeur vers une structure **ADRLIST** qui contient les noms résolus.</span><span class="sxs-lookup"><span data-stu-id="327e5-125">On output, a pointer to an **ADRLIST** structure that contains the resolved names.</span></span> 
    
 <span data-ttu-id="327e5-126">_lpFlagList_</span><span class="sxs-lookup"><span data-stu-id="327e5-126">_lpFlagList_</span></span>
  
> <span data-ttu-id="327e5-127">[entrée, sortie] Un pointeur vers un tableau d’indicateurs, chaque indicateur correspondant à une structure [ADRENTRY](adrentry.md) dans le paramètre _lpAdrList_ , qui fournit l’état de l’opération de résolution de nom pour le destinataire.</span><span class="sxs-lookup"><span data-stu-id="327e5-127">[in, out] A pointer to an array of flags, each flag corresponding to an [ADRENTRY](adrentry.md) structure in the  _lpAdrList_ parameter, that provides the status of the name resolution operation for the recipient.</span></span> <span data-ttu-id="327e5-128">Les indicateurs dans le paramètre _lpFlagList_ sont dans le même ordre que les entrées dans _lpAdrList_.</span><span class="sxs-lookup"><span data-stu-id="327e5-128">The flags in the  _lpFlagList_ parameter are in the same order as the entries in  _lpAdrList_.</span></span> <span data-ttu-id="327e5-129">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="327e5-129">The following flags can be set:</span></span>
    
<span data-ttu-id="327e5-130">MAPI_AMBIGUOUS</span><span class="sxs-lookup"><span data-stu-id="327e5-130">MAPI_AMBIGUOUS</span></span> 
  
> <span data-ttu-id="327e5-131">Le destinataire a été résolu, mais pas à un identificateur d’entrée unique.</span><span class="sxs-lookup"><span data-stu-id="327e5-131">The corresponding recipient has been resolved, but not to a unique entry identifier.</span></span> <span data-ttu-id="327e5-132">Autres conteneurs ne doivent pas essayer de résoudre ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="327e5-132">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="327e5-133">MAPI_RESOLVED</span><span class="sxs-lookup"><span data-stu-id="327e5-133">MAPI_RESOLVED</span></span> 
  
> <span data-ttu-id="327e5-134">Le destinataire a été résolu à un identificateur d’entrée unique.</span><span class="sxs-lookup"><span data-stu-id="327e5-134">The corresponding recipient has been resolved to a unique entry identifier.</span></span> <span data-ttu-id="327e5-135">Autres conteneurs ne doivent pas essayer de résoudre ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="327e5-135">Other containers should not try to resolve this recipient.</span></span> 
    
<span data-ttu-id="327e5-136">MAPI_UNRESOLVED</span><span class="sxs-lookup"><span data-stu-id="327e5-136">MAPI_UNRESOLVED</span></span> 
  
> <span data-ttu-id="327e5-137">L’entrée correspondante n’a pas été résolue.</span><span class="sxs-lookup"><span data-stu-id="327e5-137">The corresponding entry has not been resolved.</span></span> <span data-ttu-id="327e5-138">Autres conteneurs doivent essayer de résoudre ce destinataire.</span><span class="sxs-lookup"><span data-stu-id="327e5-138">Other containers should try to resolve this recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="327e5-139">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="327e5-139">Return value</span></span>

<span data-ttu-id="327e5-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="327e5-140">S_OK</span></span> 
  
> <span data-ttu-id="327e5-141">Le processus de résolution de nom a réussi.</span><span class="sxs-lookup"><span data-stu-id="327e5-141">The name resolution process was successful.</span></span>
    
<span data-ttu-id="327e5-142">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="327e5-142">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="327e5-143">Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="327e5-143">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="327e5-144">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="327e5-144">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="327e5-145">Le fournisseur de carnet d’adresses ne gère pas la résolution de noms en bloc à l’aide de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="327e5-145">The address book provider does not support bulk name resolution by using this method.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="327e5-146">Remarques</span><span class="sxs-lookup"><span data-stu-id="327e5-146">Remarks</span></span>

<span data-ttu-id="327e5-147">La méthode **ResolveNames** tente de faire correspondre les destinataires du tableau des entrées dans le paramètre _lpAdrList_ aux destinataires de ce conteneur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="327e5-147">The **ResolveNames** method attempts to match unresolved recipients from the array of entries in the  _lpAdrList_ parameter to recipients in this address book container.</span></span> <span data-ttu-id="327e5-148">Généralement, un destinataire non résolu a uniquement la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) et éventuellement quelques autres propriétés.</span><span class="sxs-lookup"><span data-stu-id="327e5-148">An unresolved recipient typically has only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property and possibly a few other properties.</span></span> <span data-ttu-id="327e5-149">Un destinataire non résolu n’a pas la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) et son correspondante dans le paramètre _lpFlagList_ est défini à MAPI_UNRESOLVED.</span><span class="sxs-lookup"><span data-stu-id="327e5-149">An unresolved recipient does not have the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, and its corresponding flag in the  _lpFlagList_ parameter is set to MAPI_UNRESOLVED.</span></span> <span data-ttu-id="327e5-150">Inversement, un destinataire résolu a toujours au moins la propriété **PR_ENTRYID** ainsi que plusieurs autres propriétés telles que **TYPEADR_PR** ([ , **PR_DISPLAY_NAME**et **ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="327e5-150">Conversely, a resolved recipient always has at least the **PR_ENTRYID** property plus several other properties such as **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**, and **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).</span></span>
  
<span data-ttu-id="327e5-151">Résolution de noms commence généralement lorsqu’un client appelle la méthode [IAddrBook::ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="327e5-151">Name resolution typically starts when a client calls the [IAddrBook::ResolveName](iaddrbook-resolvename.md) method.</span></span> <span data-ttu-id="327e5-152">Outlook MAPI répond en appelant la méthode **ResolveNames** de chaque conteneur de carnet d’adresses incluse dans le chemin de recherche de livre adresse, spécifié par la propriété **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="327e5-152">Outlook MAPI responds by calling the **ResolveNames** method of each address book container included in the address book search path, specified by the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property.</span></span> <span data-ttu-id="327e5-153">Les entrées dans le paramètre _lpAdrList_ les destinataires déjà résolus car ils sont dans des conteneurs dont MAPI a déjà appelé **ResolveNames**, étant donné que les entrées apparaissent plus haut dans le chemin de recherche.</span><span class="sxs-lookup"><span data-stu-id="327e5-153">The entries in the  _lpAdrList_ parameter include recipients already resolved because they are in containers for which MAPI has already called **ResolveNames**, because the entries appear earlier in the search path.</span></span> 
  
<span data-ttu-id="327e5-154">Chaque conteneur essaie de résoudre les entrées non résolues par correspondant au nom d’affichage du destinataire dont le nom complet de l’un de ses entrées.</span><span class="sxs-lookup"><span data-stu-id="327e5-154">Each container attempts to resolve the unresolved entries by matching the display name of the recipient with the display name of one of its entries.</span></span> <span data-ttu-id="327e5-155">Lorsqu’une correspondance unique est trouvée, **ResolveNames** ajoute la propriété **PR_ENTRYID** et autres propriétés qui sont incluses dans le paramètre _lpPropTagArray_ à l’entrée correspondante dans la structure **ADRLIST** sortante.</span><span class="sxs-lookup"><span data-stu-id="327e5-155">When a unique match is found, **ResolveNames** adds the **PR_ENTRYID** property and other properties that are included in the  _lpPropTagArray_ parameter to the corresponding entry in the outgoing **ADRLIST** structure.</span></span> <span data-ttu-id="327e5-156">**ResolveNames** définit ensuite l’entrée dans le paramètre _lpFlagList_ pour MAPI_RESOLVED.</span><span class="sxs-lookup"><span data-stu-id="327e5-156">**ResolveNames** then sets the entry in the  _lpFlagList_ parameter to MAPI_RESOLVED.</span></span> <span data-ttu-id="327e5-157">L’identificateur d’entrée stockée dans la propriété **PR_ENTRYID** peut être à court terme ou à long terme.</span><span class="sxs-lookup"><span data-stu-id="327e5-157">The entry identifier stored in the **PR_ENTRYID** property can be short-term or long-term.</span></span> 
  
<span data-ttu-id="327e5-158">Après tout des conteneurs de la recherche de chemin d’accès tenté le processus de résolution de noms, MAPI ouvre une boîte de dialogue, dans la mesure du possible, pour inviter l’utilisateur à l’aide pour résoudre les conflits restants.</span><span class="sxs-lookup"><span data-stu-id="327e5-158">After all of the containers in the search path have attempted the name resolution process, MAPI opens a dialog box, if possible, to prompt the user for help in resolving any remaining conflicts.</span></span> 
  
<span data-ttu-id="327e5-159">Les clients peuvent également utiliser la structure **ADRLIST** retournée dans les appels à la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="327e5-159">Clients can also use the returned **ADRLIST** structure in calls to the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="327e5-160">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="327e5-160">Notes to implementers</span></span>

<span data-ttu-id="327e5-161">Vous ne sont pas requis pour prendre en charge la résolution de noms avec la méthode **ResolveNames** .</span><span class="sxs-lookup"><span data-stu-id="327e5-161">You are not required to support name resolution with the **ResolveNames** method.</span></span> <span data-ttu-id="327e5-162">Au lieu de cela, ou en outre, vous pouvez en charge avec la restriction de propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="327e5-162">Instead, or additionally, you can support it with the **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="327e5-163">Si vous décidez s’appuient sur la restriction de **PR_ANR** pour la résolution de noms, vous pouvez retourner MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="327e5-163">If you decide to rely on the **PR_ANR** restriction for name resolution, you can return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="327e5-164">For more information, see [L'impl�mentation de la r�solution de noms](implementing-name-resolution.md).</span><span class="sxs-lookup"><span data-stu-id="327e5-164">For more information, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="327e5-165">Définissez l’entrée indicateur d’un destinataire dans le paramètre _lpFlagList_ pour MAPI_UNRESOLVED si le destinataire ne correspond pas à un des destinataires du conteneur.</span><span class="sxs-lookup"><span data-stu-id="327e5-165">Set a recipient's flag entry in the  _lpFlagList_ parameter to MAPI_UNRESOLVED if the recipient does not match any of the container's recipients.</span></span> 
  
<span data-ttu-id="327e5-166">Lorsqu’un destinataire correspond à plusieurs destinataires, affectez à son indicateur MAPI_AMBIGUOUS et ne modifiez pas la structure **ADRENTRY** .</span><span class="sxs-lookup"><span data-stu-id="327e5-166">When a recipient matches multiple recipients, set its flag to MAPI_AMBIGUOUS and do not change its **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="327e5-167">MAPI nécessite certaines propriétés pour les destinataires qui sont inclus dans la liste des destinataires d’un message.</span><span class="sxs-lookup"><span data-stu-id="327e5-167">MAPI requires certain properties for recipients that are included in a message's recipient list.</span></span> <span data-ttu-id="327e5-168">Vous pouvez les inclure dans la structure **ADRENTRY** dans le cadre du processus de résolution de nom ou attendre MAPI demander les avec les appels aux méthodes [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) et [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) .</span><span class="sxs-lookup"><span data-stu-id="327e5-168">You can include them in the **ADRENTRY** structure as part of the name resolution process or wait for MAPI to request them with calls to the [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) and [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) methods.</span></span> <span data-ttu-id="327e5-169">Vous pouvez éliminer ces appels supplémentaires et améliorer les performances en y compris les propriétés suivantes dans les structures **ADRENTRY** de tous les destinataires résolus :</span><span class="sxs-lookup"><span data-stu-id="327e5-169">You can eliminate these extra calls and improve performance by including the following properties in the **ADRENTRY** structures of all resolved recipients:</span></span> 
  
- <span data-ttu-id="327e5-170">**TYPEADR_PR**</span><span class="sxs-lookup"><span data-stu-id="327e5-170">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="327e5-171">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="327e5-171">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="327e5-172">**ADRESSE_EMAIL_PR**</span><span class="sxs-lookup"><span data-stu-id="327e5-172">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="327e5-173">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="327e5-173">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="327e5-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="327e5-174">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="327e5-175">**Clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="327e5-175">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
- <span data-ttu-id="327e5-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="327e5-176">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="327e5-177">Si certaines des propriétés dans le paramètre _lpPropTagArray_ ne sont pas disponibles, en général car l’entrée de conteneur ne gère pas les propriétés et qu’ils ne figurent pas dans le membre **ADRENTRY** du destinataire dans la structure **ADRLIST** : définir le type de propriété de chaque propriété non disponible PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="327e5-177">If some of the properties in the  _lpPropTagArray_ parameter are unavailable—typically because the container entry does not support the properties and they are not included in the recipient's **ADRENTRY** member in the **ADRLIST** structure—set the property type of each unavailable property to PT_ERROR.</span></span> 
  
<span data-ttu-id="327e5-178">Ne supprimez pas toutes les propriétés de structure de **ADRENTRY** d’un destinataire résolu.</span><span class="sxs-lookup"><span data-stu-id="327e5-178">Do not remove any properties from a resolved recipient's **ADRENTRY** structure.</span></span> 
  
<span data-ttu-id="327e5-179">Si vous devez remplacer plutôt que de modifier une structure **ADRENTRY** , libérer la structure **ADRENTRY** d’origine en appelant d’abord la fonction [MAPIFreeBuffer](mapifreebuffer.md) , puis allouer le remplacement structure **ADRENTRY** avec [ MAPIAllocateBuffer](mapiallocatebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="327e5-179">If you must replace rather than modify an **ADRENTRY** structure, free the original **ADRENTRY** structure first by calling the [MAPIFreeBuffer](mapifreebuffer.md) function, and then allocate the replacement **ADRENTRY** structure with [MAPIAllocateBuffer](mapiallocatebuffer.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="327e5-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="327e5-180">See also</span></span>



[<span data-ttu-id="327e5-181">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="327e5-181">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="327e5-182">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="327e5-182">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="327e5-183">IAddrBook::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="327e5-183">IAddrBook::PrepareRecips</span></span>](iaddrbook-preparerecips.md)
  
[<span data-ttu-id="327e5-184">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="327e5-184">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
[<span data-ttu-id="327e5-185">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="327e5-185">IMAPISupport::ExpandRecips</span></span>](imapisupport-expandrecips.md)
  
[<span data-ttu-id="327e5-186">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="327e5-186">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="327e5-187">Propriété canonique PidTagAnr</span><span class="sxs-lookup"><span data-stu-id="327e5-187">PidTagAnr Canonical Property</span></span>](pidtaganr-canonical-property.md)
  
[<span data-ttu-id="327e5-188">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="327e5-188">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="327e5-189">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="327e5-189">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

