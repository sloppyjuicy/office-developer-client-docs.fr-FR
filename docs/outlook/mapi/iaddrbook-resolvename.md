---
title: IAddrBookResolveName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.ResolveName
api_type:
- COM
ms.assetid: a7823c16-efda-45c2-b931-3e1fbc823b0b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1f09c88d9bd6720720e2d30ac24fa4a19aed5538
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567229"
---
# <a name="iaddrbookresolvename"></a><span data-ttu-id="298b3-103">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="298b3-103">IAddrBook::ResolveName</span></span>

  
  
<span data-ttu-id="298b3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="298b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="298b3-105">Effectue la résolution de noms, affectation d’identificateurs d’entrée aux destinataires dans une liste de destinataires.</span><span class="sxs-lookup"><span data-stu-id="298b3-105">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="298b3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="298b3-106">Parameters</span></span>

 <span data-ttu-id="298b3-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="298b3-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="298b3-108">[in] Un handle vers la fenêtre parent d’une boîte de dialogue qui s’affiche, si spécifié, pour inviter l’utilisateur à résoudre l’ambiguïté.</span><span class="sxs-lookup"><span data-stu-id="298b3-108">[in] A handle to the parent window of a dialog box that is shown, if specified, to prompt the user to resolve ambiguity.</span></span>
    
 <span data-ttu-id="298b3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="298b3-109">_ulFlags_</span></span>
  
> <span data-ttu-id="298b3-110">[in] Masque de bits d’indicateurs qui contrôlent les différents aspects du processus de résolution.</span><span class="sxs-lookup"><span data-stu-id="298b3-110">[in] A bitmask of flags that control various aspects of the resolution process.</span></span> <span data-ttu-id="298b3-111">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="298b3-111">The following flags can be set:</span></span>
    
<span data-ttu-id="298b3-112">AB_UNICODEUI</span><span class="sxs-lookup"><span data-stu-id="298b3-112">AB_UNICODEUI</span></span>
  
> <span data-ttu-id="298b3-113">Indique que _lpszNewEntryTitle_ est une chaîne UNICODE.</span><span class="sxs-lookup"><span data-stu-id="298b3-113">Indicates that  _lpszNewEntryTitle_ is a UNICODE string.</span></span> 
    
<span data-ttu-id="298b3-114">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="298b3-114">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="298b3-115">Utilisez uniquement le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="298b3-115">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="298b3-116">Par exemple, vous pouvez utiliser cet indicateur pour autoriser une application cliente ouvrir la liste d’adresses globale (LAG) en mode exchange mis en cache et accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer le trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="298b3-116">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="298b3-117">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="298b3-117">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="298b3-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="298b3-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="298b3-119">Affiche une boîte de dialogue pour inviter l’utilisateur pour les informations de résolution de nom supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="298b3-119">Displays a dialog box to prompt the user for additional name resolution information.</span></span> <span data-ttu-id="298b3-120">Si cet indicateur n’est pas défini, aucune boîte de dialogue ne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="298b3-120">If this flag is not set, no dialog box is displayed.</span></span> 
    
<span data-ttu-id="298b3-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="298b3-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="298b3-122">Indique que les propriétés renvoyées dans la liste d’adresses doivent être de type PT_UNICODE au lieu de PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="298b3-122">Indicates that the properties returned in the address list should be of type PT_UNICODE instead of PT_STRING8.</span></span> 
    
 <span data-ttu-id="298b3-123">_lpszNewEntryTitle_</span><span class="sxs-lookup"><span data-stu-id="298b3-123">_lpszNewEntryTitle_</span></span>
  
> <span data-ttu-id="298b3-124">[in] Pointeur vers le texte du titre du contrôle dans la boîte de dialogue qui invite l’utilisateur à entrer un destinataire.</span><span class="sxs-lookup"><span data-stu-id="298b3-124">[in] A pointer to text for the title of the control in the dialog box that prompts the user to enter a recipient.</span></span> <span data-ttu-id="298b3-125">Le titre varie selon le type de destinataire.</span><span class="sxs-lookup"><span data-stu-id="298b3-125">The title varies depending on the type of recipient.</span></span> <span data-ttu-id="298b3-126">Le paramètre _lpszNewEntryTitle_ peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="298b3-126">The  _lpszNewEntryTitle_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="298b3-127">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="298b3-127">_lpAdrList_</span></span>
  
> <span data-ttu-id="298b3-128">[-out] Pointeur vers une structure [ADRLIST](adrlist.md) qui contient la liste des noms des destinataires à résoudre.</span><span class="sxs-lookup"><span data-stu-id="298b3-128">[in-out] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipient names to be resolved.</span></span> <span data-ttu-id="298b3-129">Cette structure **ADRLIST** peut être créée par la méthode [IAddrBook::Address](iaddrbook-address.md) .</span><span class="sxs-lookup"><span data-stu-id="298b3-129">This **ADRLIST** structure can be created by the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="298b3-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="298b3-130">Return value</span></span>

<span data-ttu-id="298b3-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="298b3-131">S_OK</span></span> 
  
> <span data-ttu-id="298b3-132">Le processus de résolution de nom a réussi.</span><span class="sxs-lookup"><span data-stu-id="298b3-132">The name resolution process succeeded.</span></span>
    
<span data-ttu-id="298b3-133">MAPI_E_AMBIGUOUS_RECIP</span><span class="sxs-lookup"><span data-stu-id="298b3-133">MAPI_E_AMBIGUOUS_RECIP</span></span> 
  
> <span data-ttu-id="298b3-134">Au moins un destinataire dans le paramètre _lpAdrList_ correspondant plus d’une entrée dans le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="298b3-134">At least one recipient in the  _lpAdrList_ parameter matched more than one entry in the address book.</span></span> <span data-ttu-id="298b3-135">En règle générale, cette valeur est renvoyée lorsque la valeur de l’indicateur MAPI_DIALOG, interdisant l’affichage d’une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="298b3-135">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
<span data-ttu-id="298b3-136">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="298b3-136">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="298b3-137">Au moins un destinataire dans le paramètre _lpAdrList_ ne peut pas être résolu.</span><span class="sxs-lookup"><span data-stu-id="298b3-137">At least one recipient in the  _lpAdrList_ parameter cannot be resolved.</span></span> <span data-ttu-id="298b3-138">En règle générale, cette valeur est renvoyée lorsque la valeur de l’indicateur MAPI_DIALOG, interdisant l’affichage d’une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="298b3-138">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="298b3-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="298b3-139">Remarks</span></span>

<span data-ttu-id="298b3-140">Clients et fournisseurs de services appellent la méthode **ResolveName** pour lancer le processus de résolution de nom.</span><span class="sxs-lookup"><span data-stu-id="298b3-140">Clients and service providers call the **ResolveName** method to initiate the name resolution process.</span></span> <span data-ttu-id="298b3-141">Une entrée non résolue est une entrée qui n’a pas encore un identificateur d’entrée ou de la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="298b3-141">An unresolved entry is an entry that does not yet have an entry identifier or **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
 <span data-ttu-id="298b3-142">**ResolveName** passe par le processus suivant pour chaque entrée dans la liste d’adresses passée dans le paramètre _lpAdrList_ non résolue.</span><span class="sxs-lookup"><span data-stu-id="298b3-142">**ResolveName** goes through the following process for each unresolved entry in the address list passed in the  _lpAdrList_ parameter.</span></span> 
  
1. <span data-ttu-id="298b3-143">Si le type d’adresse du destinataire respecte le format d’adresse SMTP ( _displayname_@ _domaine de niveau domain.top_), **ResolveName** lui attribue un identificateur d’entrée unique.</span><span class="sxs-lookup"><span data-stu-id="298b3-143">If the address type of the recipient adheres to the format of an SMTP address ( _displayname_@ _domain.top-level-domain_), **ResolveName** assigns it a one-off entry identifier.</span></span> 
    
2. <span data-ttu-id="298b3-144">Pour chaque conteneur dans la propriété **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)), **ResolveName** appelle la méthode [IABContainer::ResolveNames](iabcontainer-resolvenames.md) .</span><span class="sxs-lookup"><span data-stu-id="298b3-144">For each container in the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property, **ResolveName** calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="298b3-145">**ResolveNames** tente de faire correspondre le nom complet de chaque destinataire non résolu avec un nom d’affichage qui appartienne à l’un de ses entrées.</span><span class="sxs-lookup"><span data-stu-id="298b3-145">**ResolveNames** tries to match the display name of each unresolved recipient with a display name that belongs to one of its entries.</span></span> 
    
3. <span data-ttu-id="298b3-146">Si un conteneur ne prend pas en charge **ResolveNames**, **ResolveName** limite la table des matières du conteneur à l’aide d’une restriction de propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="298b3-146">If a container does not support **ResolveNames**, **ResolveName** restricts the container's contents table by using a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="298b3-147">Cette restriction provoque le conteneur exécuter un type de recherche pour localiser un destinataire correspondant « mieux deviner ».</span><span class="sxs-lookup"><span data-stu-id="298b3-147">This restriction causes the container to perform a "best guess" type of search to locate a matching recipient.</span></span> <span data-ttu-id="298b3-148">Tous les conteneurs doivent prendre en charge la restriction de propriété **PR_ANR** .</span><span class="sxs-lookup"><span data-stu-id="298b3-148">All containers must support the **PR_ANR** property restriction.</span></span> 
    
4. <span data-ttu-id="298b3-149">Lorsqu’un conteneur renvoie un destinataire qui correspond à plusieurs noms, **ResolveName** affiche une boîte de dialogue si l’indicateur MAPI_DIALOG est défini, ce qui permet à l’utilisateur de sélectionner le nom correct.</span><span class="sxs-lookup"><span data-stu-id="298b3-149">When a container returns a recipient that matches multiple names, **ResolveName** displays a dialog box if the MAPI_DIALOG flag is set, which lets the user select the correct name.</span></span> 
    
5. <span data-ttu-id="298b3-150">Si tous les conteneurs dans la propriété **PR_AB_SEARCH_PATH** ont été appelées et si aucune correspondance n’a été trouvée, le destinataire reste non résolu.</span><span class="sxs-lookup"><span data-stu-id="298b3-150">If all of the containers in the **PR_AB_SEARCH_PATH** property have been called and no match has been found, the recipient remains unresolved.</span></span> 
    
<span data-ttu-id="298b3-151">Si un ou plusieurs destinataires résolues, **ResolveName** renvoie MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="298b3-151">If one or more recipients are unresolved, **ResolveName** returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="298b3-152">Si un ou plusieurs destinataires AMBIGUE résolution qui n’a pas pu être résolue avec une boîte de dialogue, ou parce que l’indicateur MAPI_DIALOG n’a pas été défini, **ResolveName** renvoie MAPI_E_AMBIGUOUS_RECIP.</span><span class="sxs-lookup"><span data-stu-id="298b3-152">If one or more recipients had ambiguous resolution that could not be resolved with a dialog box, or because the MAPI_DIALOG flag was not set, **ResolveName** returns MAPI_E_AMBIGUOUS_RECIP.</span></span> <span data-ttu-id="298b3-153">Lorsque des destinataires sont ambigus et certaines ne peut pas être résolu, **ResolveName** peut renvoyer une valeur d’erreur.</span><span class="sxs-lookup"><span data-stu-id="298b3-153">When some of the recipients are ambiguous and some cannot be resolved, **ResolveName** can return either error value.</span></span> 
  
<span data-ttu-id="298b3-154">Si un nom ne peut pas être résolu, le client peut créer une adresse unique ayant une adresse spécialement mise en forme et l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="298b3-154">If a name cannot be resolved, the client can create a one-off address that has a specially formatted address and entry identifier.</span></span> <span data-ttu-id="298b3-155">Pour plus d’informations sur le format des identificateurs d’entrée unique, voir [Identificateurs uniques d’entrée](one-off-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="298b3-155">For more information about the format of one-off entry identifiers, see [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span> <span data-ttu-id="298b3-156">Pour plus d’informations sur le format des adresses uniques, voir [Adresses uniques](one-off-addresses.md).</span><span class="sxs-lookup"><span data-stu-id="298b3-156">For more information about the format of one-off addresses, see [One-Off Addresses](one-off-addresses.md).</span></span>
  
<span data-ttu-id="298b3-157">MAPI prend en charge les chaînes de caractères Unicode pour les **ADRLIST** et les nouveaux paramètres de titre de l’entrée à **ResolveName**; Si vous définissez l’indicateur MAPI_UNICODE, les propriétés suivantes sont renvoyées sous forme de type PT_UNICODE dans les structures [ADRENTRY](adrentry.md) :</span><span class="sxs-lookup"><span data-stu-id="298b3-157">MAPI supports Unicode character strings for the **ADRLIST** and the new entry title parameters to **ResolveName**; if you set the MAPI_UNICODE flag, the following properties are returned as type PT_UNICODE in the [ADRENTRY](adrentry.md) structures:</span></span> 
  
- <span data-ttu-id="298b3-158">**TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="298b3-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="298b3-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="298b3-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="298b3-160">**ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="298b3-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
- <span data-ttu-id="298b3-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="298b3-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="298b3-162">Toutefois, la propriété **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) est toujours renvoyée comme type PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="298b3-162">However, the **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) property is always returned as type PT_STRING8.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="298b3-163">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="298b3-163">MFCMAPI reference</span></span>

<span data-ttu-id="298b3-164">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="298b3-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="298b3-165">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="298b3-165">**File**</span></span>|<span data-ttu-id="298b3-166">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="298b3-166">**Function**</span></span>|<span data-ttu-id="298b3-167">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="298b3-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="298b3-168">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="298b3-168">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="298b3-169">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="298b3-169">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="298b3-170">MFCMAPI utilise la méthode **ResolveName** pour résoudre une adresse unique avant son ajout à un message.</span><span class="sxs-lookup"><span data-stu-id="298b3-170">MFCMAPI uses the **ResolveName** method to resolve a one-off address before adding it to a message.</span></span>  <br/> |
|<span data-ttu-id="298b3-171">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="298b3-171">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="298b3-172">Ajouter destinataire</span><span class="sxs-lookup"><span data-stu-id="298b3-172">AddRecipient</span></span>  <br/> |<span data-ttu-id="298b3-173">MFCMAPI utilise la méthode **ResolveName** pour rechercher une entrée de carnet d’adresses par nom complet.</span><span class="sxs-lookup"><span data-stu-id="298b3-173">MFCMAPI uses the **ResolveName** method to look up an address book entry by display name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="298b3-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="298b3-174">See also</span></span>



[<span data-ttu-id="298b3-175">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="298b3-175">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="298b3-176">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="298b3-176">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)
  
[<span data-ttu-id="298b3-177">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="298b3-177">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="298b3-178">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="298b3-178">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="298b3-179">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="298b3-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

