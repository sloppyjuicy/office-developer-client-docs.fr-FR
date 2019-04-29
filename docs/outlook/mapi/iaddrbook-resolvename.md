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
ms.openlocfilehash: 8a6a73153b857078cb37d94a634a6b0215a0a8c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408130"
---
# <a name="iaddrbookresolvename"></a><span data-ttu-id="c7286-103">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="c7286-103">IAddrBook::ResolveName</span></span>

  
  
<span data-ttu-id="c7286-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7286-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7286-105">Effectue une résolution de noms, en affectant des identificateurs d'entrée à des destinataires dans une liste de destinataires.</span><span class="sxs-lookup"><span data-stu-id="c7286-105">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="c7286-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7286-106">Parameters</span></span>

 <span data-ttu-id="c7286-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c7286-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="c7286-108">dans Handle de la fenêtre parent d'une boîte de dialogue qui s'affiche, s'il est spécifié, pour inviter l'utilisateur à résoudre une ambiguïté.</span><span class="sxs-lookup"><span data-stu-id="c7286-108">[in] A handle to the parent window of a dialog box that is shown, if specified, to prompt the user to resolve ambiguity.</span></span>
    
 <span data-ttu-id="c7286-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c7286-109">_ulFlags_</span></span>
  
> <span data-ttu-id="c7286-110">dans Masque de des indicateurs qui contrôlent différents aspects du processus de résolution.</span><span class="sxs-lookup"><span data-stu-id="c7286-110">[in] A bitmask of flags that control various aspects of the resolution process.</span></span> <span data-ttu-id="c7286-111">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="c7286-111">The following flags can be set:</span></span>
    
<span data-ttu-id="c7286-112">AB_UNICODEUI</span><span class="sxs-lookup"><span data-stu-id="c7286-112">AB_UNICODEUI</span></span>
  
> <span data-ttu-id="c7286-113">Indique que _lpszNewEntryTitle_ est une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="c7286-113">Indicates that  _lpszNewEntryTitle_ is a UNICODE string.</span></span> 
    
<span data-ttu-id="c7286-114">MAPI_CACHE_ONLY</span><span class="sxs-lookup"><span data-stu-id="c7286-114">MAPI_CACHE_ONLY</span></span>
  
> <span data-ttu-id="c7286-115">Utilisez uniquement le carnet d'adresses en mode hors connexion pour effectuer la résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="c7286-115">Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="c7286-116">Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d'ouvrir la liste d'adresses globale (LAG) en mode Exchange mis en cache et d'accéder à une entrée de ce carnet d'adresses à partir du cache sans créer de trafic entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="c7286-116">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="c7286-117">Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.</span><span class="sxs-lookup"><span data-stu-id="c7286-117">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="c7286-118">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="c7286-118">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="c7286-119">Affiche une boîte de dialogue pour inviter l'utilisateur à fournir des informations de résolution de noms supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="c7286-119">Displays a dialog box to prompt the user for additional name resolution information.</span></span> <span data-ttu-id="c7286-120">Si cet indicateur n'est pas défini, aucune boîte de dialogue ne s'affiche.</span><span class="sxs-lookup"><span data-stu-id="c7286-120">If this flag is not set, no dialog box is displayed.</span></span> 
    
<span data-ttu-id="c7286-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c7286-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="c7286-122">Indique que les propriétés retournées dans la liste d'adresses doivent être de type PT_UNICODE au lieu de PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="c7286-122">Indicates that the properties returned in the address list should be of type PT_UNICODE instead of PT_STRING8.</span></span> 
    
 <span data-ttu-id="c7286-123">_lpszNewEntryTitle_</span><span class="sxs-lookup"><span data-stu-id="c7286-123">_lpszNewEntryTitle_</span></span>
  
> <span data-ttu-id="c7286-124">dans Pointeur vers le texte du titre du contrôle dans la boîte de dialogue invitant l'utilisateur à entrer un destinataire.</span><span class="sxs-lookup"><span data-stu-id="c7286-124">[in] A pointer to text for the title of the control in the dialog box that prompts the user to enter a recipient.</span></span> <span data-ttu-id="c7286-125">Le titre varie en fonction du type de destinataire.</span><span class="sxs-lookup"><span data-stu-id="c7286-125">The title varies depending on the type of recipient.</span></span> <span data-ttu-id="c7286-126">Le paramètre _lpszNewEntryTitle_ peut être null.</span><span class="sxs-lookup"><span data-stu-id="c7286-126">The  _lpszNewEntryTitle_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="c7286-127">_lpAdrList_</span><span class="sxs-lookup"><span data-stu-id="c7286-127">_lpAdrList_</span></span>
  
> <span data-ttu-id="c7286-128">[in-out] Pointeur vers une structure [ADRLIST](adrlist.md) qui contient la liste des noms des destinataires à résoudre.</span><span class="sxs-lookup"><span data-stu-id="c7286-128">[in-out] A pointer to an [ADRLIST](adrlist.md) structure that contains the list of recipient names to be resolved.</span></span> <span data-ttu-id="c7286-129">Cette structure **ADRLIST** peut être créée par la méthode [IAddrBook:: Address](iaddrbook-address.md) .</span><span class="sxs-lookup"><span data-stu-id="c7286-129">This **ADRLIST** structure can be created by the [IAddrBook::Address](iaddrbook-address.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c7286-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c7286-130">Return value</span></span>

<span data-ttu-id="c7286-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="c7286-131">S_OK</span></span> 
  
> <span data-ttu-id="c7286-132">Le processus de résolution de noms a réussi.</span><span class="sxs-lookup"><span data-stu-id="c7286-132">The name resolution process succeeded.</span></span>
    
<span data-ttu-id="c7286-133">MAPI_E_AMBIGUOUS_RECIP</span><span class="sxs-lookup"><span data-stu-id="c7286-133">MAPI_E_AMBIGUOUS_RECIP</span></span> 
  
> <span data-ttu-id="c7286-134">Au moins un destinataire dans le paramètre _lpAdrList_ correspond à plusieurs entrées dans le carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="c7286-134">At least one recipient in the  _lpAdrList_ parameter matched more than one entry in the address book.</span></span> <span data-ttu-id="c7286-135">En règle générale, cette valeur est renvoyée lorsque l'indicateur MAPI_DIALOG est défini, ce qui interdit l'affichage d'une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c7286-135">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
<span data-ttu-id="c7286-136">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="c7286-136">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="c7286-137">Au moins un destinataire dans le paramètre _lpAdrList_ ne peut pas être résolu.</span><span class="sxs-lookup"><span data-stu-id="c7286-137">At least one recipient in the  _lpAdrList_ parameter cannot be resolved.</span></span> <span data-ttu-id="c7286-138">En règle générale, cette valeur est renvoyée lorsque l'indicateur MAPI_DIALOG est défini, ce qui interdit l'affichage d'une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c7286-138">Usually, this value is returned when the MAPI_DIALOG flag is set, prohibiting the display of a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c7286-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="c7286-139">Remarks</span></span>

<span data-ttu-id="c7286-140">Les clients et les fournisseurs de services appellent la méthode **ResolveName** pour lancer le processus de résolution de noms.</span><span class="sxs-lookup"><span data-stu-id="c7286-140">Clients and service providers call the **ResolveName** method to initiate the name resolution process.</span></span> <span data-ttu-id="c7286-141">Une entrée non résolue est une entrée qui n'a pas encore d'identificateur d'entrée ou de propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c7286-141">An unresolved entry is an entry that does not yet have an entry identifier or **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
 <span data-ttu-id="c7286-142">**ResolveName** passe en revue le processus suivant pour chaque entrée non résolue dans la liste d'adresses passée dans le paramètre _lpAdrList_ .</span><span class="sxs-lookup"><span data-stu-id="c7286-142">**ResolveName** goes through the following process for each unresolved entry in the address list passed in the  _lpAdrList_ parameter.</span></span> 
  
1. <span data-ttu-id="c7286-143">Si le type d'adresse du destinataire adhère au format d'une adresse SMTP (domaine _DisplayName_@ _. domaine de niveau supérieur_), **ResolveName** lui affecte un identificateur d'entrée unique.</span><span class="sxs-lookup"><span data-stu-id="c7286-143">If the address type of the recipient adheres to the format of an SMTP address ( _displayname_@ _domain.top-level-domain_), **ResolveName** assigns it a one-off entry identifier.</span></span> 
    
2. <span data-ttu-id="c7286-144">Pour chaque conteneur dans la propriété **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)), **ResolveName** appelle la méthode [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) .</span><span class="sxs-lookup"><span data-stu-id="c7286-144">For each container in the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property, **ResolveName** calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="c7286-145">**ResolveNames** tente de faire correspondre le nom d'affichage de chaque destinataire non résolu à un nom complet qui appartient à l'une de ses entrées.</span><span class="sxs-lookup"><span data-stu-id="c7286-145">**ResolveNames** tries to match the display name of each unresolved recipient with a display name that belongs to one of its entries.</span></span> 
    
3. <span data-ttu-id="c7286-146">Si un conteneur ne prend pas en charge **ResolveNames**, **ResolveName** limite la table des matières du conteneur à l'aide d'une restriction de propriété **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c7286-146">If a container does not support **ResolveNames**, **ResolveName** restricts the container's contents table by using a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction.</span></span> <span data-ttu-id="c7286-147">Cette restriction fait en sorte que le conteneur effectue un type de recherche «meilleure estimation» pour localiser un destinataire correspondant.</span><span class="sxs-lookup"><span data-stu-id="c7286-147">This restriction causes the container to perform a "best guess" type of search to locate a matching recipient.</span></span> <span data-ttu-id="c7286-148">Tous les conteneurs doivent prendre en charge la restriction de propriété **PR_ANR** .</span><span class="sxs-lookup"><span data-stu-id="c7286-148">All containers must support the **PR_ANR** property restriction.</span></span> 
    
4. <span data-ttu-id="c7286-149">Lorsqu'un conteneur renvoie un destinataire qui correspond à plusieurs noms, **ResolveName** affiche une boîte de dialogue si l'indicateur MAPI_DIALOG est défini, ce qui permet à l'utilisateur de sélectionner le nom correct.</span><span class="sxs-lookup"><span data-stu-id="c7286-149">When a container returns a recipient that matches multiple names, **ResolveName** displays a dialog box if the MAPI_DIALOG flag is set, which lets the user select the correct name.</span></span> 
    
5. <span data-ttu-id="c7286-150">Si tous les conteneurs de la propriété **PR_AB_SEARCH_PATH** ont été appelés et qu'aucune correspondance n'a été trouvée, le destinataire reste non résolu.</span><span class="sxs-lookup"><span data-stu-id="c7286-150">If all of the containers in the **PR_AB_SEARCH_PATH** property have been called and no match has been found, the recipient remains unresolved.</span></span> 
    
<span data-ttu-id="c7286-151">Si un ou plusieurs destinataires ne sont pas résolus, **ResolveName** renvoie MAPI_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="c7286-151">If one or more recipients are unresolved, **ResolveName** returns MAPI_E_NOT_FOUND.</span></span> <span data-ttu-id="c7286-152">Si un ou plusieurs destinataires ont une résolution ambiguë qui n'a pas pu être résolue à l'aide d'une boîte de dialogue ou parce que l'indicateur MAPI_DIALOG n'a pas été défini, **ResolveName** renvoie MAPI_E_AMBIGUOUS_RECIP.</span><span class="sxs-lookup"><span data-stu-id="c7286-152">If one or more recipients had ambiguous resolution that could not be resolved with a dialog box, or because the MAPI_DIALOG flag was not set, **ResolveName** returns MAPI_E_AMBIGUOUS_RECIP.</span></span> <span data-ttu-id="c7286-153">Lorsqu'une partie des destinataires est ambiguë et qu'une partie ne peut pas être résolue, **ResolveName** peut renvoyer l'une des valeurs d'erreur.</span><span class="sxs-lookup"><span data-stu-id="c7286-153">When some of the recipients are ambiguous and some cannot be resolved, **ResolveName** can return either error value.</span></span> 
  
<span data-ttu-id="c7286-154">Si un nom ne peut pas être résolu, le client peut créer une adresse unique ayant une adresse et un identificateur d'entrée spécialement mis en forme.</span><span class="sxs-lookup"><span data-stu-id="c7286-154">If a name cannot be resolved, the client can create a one-off address that has a specially formatted address and entry identifier.</span></span> <span data-ttu-id="c7286-155">Pour plus d'informations sur le format des identificateurs d'entrée uniques, consultez la rubrique identificateurs d' [entrée uniques](one-off-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="c7286-155">For more information about the format of one-off entry identifiers, see [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span> <span data-ttu-id="c7286-156">Pour plus d'informations sur le format des adresses ponctuelles, consultez la rubrique [adresses ponctuelles](one-off-addresses.md).</span><span class="sxs-lookup"><span data-stu-id="c7286-156">For more information about the format of one-off addresses, see [One-Off Addresses](one-off-addresses.md).</span></span>
  
<span data-ttu-id="c7286-157">MAPI prend en charge les chaînes de caractères Unicode pour le **ADRLIST** et les nouveaux paramètres de titre d'entrée pour **ResolveName**; Si vous définissez l'indicateur MAPI_UNICODE, les propriétés suivantes sont renvoyées en tant que type PT_UNICODE dans les structures [ADRENTRY](adrentry.md) :</span><span class="sxs-lookup"><span data-stu-id="c7286-157">MAPI supports Unicode character strings for the **ADRLIST** and the new entry title parameters to **ResolveName**; if you set the MAPI_UNICODE flag, the following properties are returned as type PT_UNICODE in the [ADRENTRY](adrentry.md) structures:</span></span> 
  
- <span data-ttu-id="c7286-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c7286-158">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="c7286-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c7286-159">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="c7286-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c7286-160">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
- <span data-ttu-id="c7286-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c7286-161">**PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))</span></span>
    
<span data-ttu-id="c7286-162">Toutefois, la propriété **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) est toujours renvoyée en tant que type PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="c7286-162">However, the **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) property is always returned as type PT_STRING8.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c7286-163">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c7286-163">MFCMAPI reference</span></span>

<span data-ttu-id="c7286-164">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c7286-164">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c7286-165">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="c7286-165">**File**</span></span>|<span data-ttu-id="c7286-166">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="c7286-166">**Function**</span></span>|<span data-ttu-id="c7286-167">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="c7286-167">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c7286-168">MAPIABFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="c7286-168">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="c7286-169">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="c7286-169">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="c7286-170">MFCMAPI utilise la méthode **ResolveName** pour résoudre une adresse ponctuelle avant de l'ajouter à un message.</span><span class="sxs-lookup"><span data-stu-id="c7286-170">MFCMAPI uses the **ResolveName** method to resolve a one-off address before adding it to a message.</span></span>  <br/> |
|<span data-ttu-id="c7286-171">MAPIABFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="c7286-171">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="c7286-172">AddRecipient</span><span class="sxs-lookup"><span data-stu-id="c7286-172">AddRecipient</span></span>  <br/> |<span data-ttu-id="c7286-173">MFCMAPI utilise la méthode **ResolveName** pour rechercher une entrée de carnet d'adresses par son nom complet.</span><span class="sxs-lookup"><span data-stu-id="c7286-173">MFCMAPI uses the **ResolveName** method to look up an address book entry by display name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c7286-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7286-174">See also</span></span>



[<span data-ttu-id="c7286-175">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="c7286-175">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="c7286-176">IABContainer::ResolveNames</span><span class="sxs-lookup"><span data-stu-id="c7286-176">IABContainer::ResolveNames</span></span>](iabcontainer-resolvenames.md)
  
[<span data-ttu-id="c7286-177">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="c7286-177">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="c7286-178">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="c7286-178">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="c7286-179">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="c7286-179">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

