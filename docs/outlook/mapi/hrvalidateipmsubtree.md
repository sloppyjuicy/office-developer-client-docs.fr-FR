---
title: HrValidateIPMSubtree
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrValidateIPMSubtree
api_type:
- COM
ms.assetid: 6454c1fa-5216-4934-a908-48c634ac4a07
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6cf51985e534434c584eff4d63dfbf239121ee85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436572"
---
# <a name="hrvalidateipmsubtree"></a><span data-ttu-id="f37f7-103">HrValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="f37f7-103">HrValidateIPMSubtree</span></span>

  
  
<span data-ttu-id="f37f7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f37f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f37f7-105">Ajoute des dossiers de message interpersonnels standard à une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f37f7-105">Adds standard interpersonal message (IPM) folders to a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f37f7-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f37f7-106">Header file:</span></span>  <br/> |<span data-ttu-id="f37f7-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="f37f7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f37f7-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="f37f7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f37f7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f37f7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f37f7-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="f37f7-110">Called by:</span></span>  <br/> |<span data-ttu-id="f37f7-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="f37f7-111">Client applications</span></span>  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a><span data-ttu-id="f37f7-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f37f7-112">Parameters</span></span>

 <span data-ttu-id="f37f7-113">_lpMDB_</span><span class="sxs-lookup"><span data-stu-id="f37f7-113">_lpMDB_</span></span>
  
> <span data-ttu-id="f37f7-114">dans Pointeur vers l'objet de la Banque de messages à laquelle les dossiers doivent être ajoutés.</span><span class="sxs-lookup"><span data-stu-id="f37f7-114">[in] Pointer to the message store object to which to add the folders.</span></span> 
    
 <span data-ttu-id="f37f7-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f37f7-115">_ulFlags_</span></span>
  
> <span data-ttu-id="f37f7-116">dans Masque de des indicateurs utilisés pour contrôler la façon dont les dossiers sont créés.</span><span class="sxs-lookup"><span data-stu-id="f37f7-116">[in] Bitmask of flags used to control how the folders are created.</span></span> <span data-ttu-id="f37f7-117">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="f37f7-117">The following flags can be set:</span></span>
    
<span data-ttu-id="f37f7-118">MAPI_FORCE_CREATE</span><span class="sxs-lookup"><span data-stu-id="f37f7-118">MAPI_FORCE_CREATE</span></span> 
  
> <span data-ttu-id="f37f7-119">Les dossiers doivent être vérifiés avant la création, même si les propriétés de la Banque de messages indiquent qu'elles sont valides.</span><span class="sxs-lookup"><span data-stu-id="f37f7-119">The folders should be verified before creation, even if message store properties indicate that they are valid.</span></span> <span data-ttu-id="f37f7-120">Une application cliente définit généralement cet indicateur lorsqu'une erreur indique que la structure d'un dossier existant a été endommagée.</span><span class="sxs-lookup"><span data-stu-id="f37f7-120">A client application typically sets this flag when an error indicates that the structure of an existing folder has been damaged.</span></span> 
    
<span data-ttu-id="f37f7-121">MAPI_FULL_IPM_TREE</span><span class="sxs-lookup"><span data-stu-id="f37f7-121">MAPI_FULL_IPM_TREE</span></span> 
  
> <span data-ttu-id="f37f7-122">L'ensemble complet des dossiers IPM doit être créé dans le dossier racine de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f37f7-122">The full set of IPM folders should be created in the message store's root folder.</span></span> <span data-ttu-id="f37f7-123">Les titres de dossier dans la hiérarchie sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="f37f7-123">The folder titles in the hierarchy are:</span></span>
    
    - <span data-ttu-id="f37f7-124">Vues de dossier</span><span class="sxs-lookup"><span data-stu-id="f37f7-124">Folder Views</span></span>
    
    - <span data-ttu-id="f37f7-125">Affichages courants</span><span class="sxs-lookup"><span data-stu-id="f37f7-125">Common Views</span></span>
    
    - <span data-ttu-id="f37f7-126">Racine de recherche\*</span><span class="sxs-lookup"><span data-stu-id="f37f7-126">Search Root\*</span></span>
    
    - <span data-ttu-id="f37f7-127">Sous-arborescence IPM\*</span><span class="sxs-lookup"><span data-stu-id="f37f7-127">IPM Subtree\*</span></span>
    
    - <span data-ttu-id="f37f7-128">Boîte de réception</span><span class="sxs-lookup"><span data-stu-id="f37f7-128">Inbox</span></span>
    
    - <span data-ttu-id="f37f7-129">Boîte d'envoi</span><span class="sxs-lookup"><span data-stu-id="f37f7-129">Outbox</span></span>
    
    - <span data-ttu-id="f37f7-130">Éléments supprimés\*</span><span class="sxs-lookup"><span data-stu-id="f37f7-130">Deleted Items\*</span></span>
    
    - <span data-ttu-id="f37f7-131">Éléments envoyés</span><span class="sxs-lookup"><span data-stu-id="f37f7-131">Sent Items</span></span>
    
    <span data-ttu-id="f37f7-132">où les trois dossiers marqués \* sont le jeu minimum créé, même lorsque l'indicateur MAPI_FULL_IPM_TREE n'a pas été défini.</span><span class="sxs-lookup"><span data-stu-id="f37f7-132">where the three folders marked with \* are the minimum set created even when the MAPI_FULL_IPM_TREE flag has not been set.</span></span> <span data-ttu-id="f37f7-133">Une application cliente définit généralement cet indicateur lorsque la Banque de messages dans laquelle les dossiers doivent être créés est la Banque par défaut.</span><span class="sxs-lookup"><span data-stu-id="f37f7-133">A client application typically sets this flag when the message store in which the folders are to be created is the default store.</span></span>
    
 <span data-ttu-id="f37f7-134">_lpcValues_</span><span class="sxs-lookup"><span data-stu-id="f37f7-134">_lpcValues_</span></span>
  
> <span data-ttu-id="f37f7-135">[in, out] Pointeur vers le nombre de structures [SPropValue](spropvalue.md) dans le tableau renvoyé dans le paramètre _lppProps_ .</span><span class="sxs-lookup"><span data-stu-id="f37f7-135">[in, out] Pointer to the number of [SPropValue](spropvalue.md) structures in the array returned in the  _lppProps_ parameter.</span></span> <span data-ttu-id="f37f7-136">La valeur du paramètre _lpcValues_ peut être zéro si _lppProps_ est null.</span><span class="sxs-lookup"><span data-stu-id="f37f7-136">The value of the  _lpcValues_ parameter can be zero if  _lppProps_ is NULL.</span></span> 
    
 <span data-ttu-id="f37f7-137">_lppProps_</span><span class="sxs-lookup"><span data-stu-id="f37f7-137">_lppProps_</span></span>
  
> <span data-ttu-id="f37f7-138">[in, out] Pointeur vers un pointeur vers un tableau de structures **SPropValue** qui contient des valeurs de propriété pour la propriété **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) et pour les propriétés d'identificateur d'entrée de dossier appropriées.</span><span class="sxs-lookup"><span data-stu-id="f37f7-138">[in, out] Pointer to a pointer to an array of **SPropValue** structures that contains property values for the **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) property and for the appropriate folder entry identifier properties.</span></span> <span data-ttu-id="f37f7-139">Si **HrValidateIPMSubtree** crée une boîte de réception dans la Banque de messages, le tableau **SPropValue** inclut un identificateur d'entrée de boîte de réception avec `PROP_TAG(PT_BINARY, PROP_ID_NULL)`une balise de propriété spéciale codée en tant que.</span><span class="sxs-lookup"><span data-stu-id="f37f7-139">If **HrValidateIPMSubtree** creates an Inbox in the message store, the **SPropValue** array includes an Inbox entry identifier with a special property tag coded as  `PROP_TAG(PT_BINARY, PROP_ID_NULL)`.</span></span> <span data-ttu-id="f37f7-140">Le paramètre _lppProps_ peut être null, ce qui indique que l'implémentation de l'appel ne nécessite pas le renvoi d'un tableau **SPropValue** .</span><span class="sxs-lookup"><span data-stu-id="f37f7-140">The  _lppProps_ parameter can be NULL, indicating that the calling implementation does not require that an **SPropValue** array be returned.</span></span> 
    
 <span data-ttu-id="f37f7-141">_lppMapiError_</span><span class="sxs-lookup"><span data-stu-id="f37f7-141">_lppMapiError_</span></span>
  
> <span data-ttu-id="f37f7-142">remarquer Pointeur vers un pointeur vers une structure [MAPIERROR](mapierror.md) qui contient les informations de version, de composant et de contexte pour une erreur.</span><span class="sxs-lookup"><span data-stu-id="f37f7-142">[out] Pointer to a pointer to a [MAPIERROR](mapierror.md) structure that contains version, component, and context information for an error.</span></span> <span data-ttu-id="f37f7-143">Le paramètre _lppMAPIError_ est défini sur null si aucune structure **MAPIERROR** n'est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="f37f7-143">The  _lppMAPIError_ parameter is set to NULL if no **MAPIERROR** structure is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f37f7-144">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f37f7-144">Return value</span></span>

<span data-ttu-id="f37f7-145">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f37f7-145">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f37f7-146">Remarques</span><span class="sxs-lookup"><span data-stu-id="f37f7-146">Remarks</span></span>

<span data-ttu-id="f37f7-147">MAPI utilise la fonction **HrValidateIPMSubtree** en interne pour construire la sous-arborescence IPM standard dans une banque de messages lors de la première ouverture de la banque ou lorsqu'une banque devient la Banque par défaut.</span><span class="sxs-lookup"><span data-stu-id="f37f7-147">MAPI uses the **HrValidateIPMSubtree** function internally to construct the standard IPM subtree in a message store when the store is first opened, or when a store is made the default store.</span></span> <span data-ttu-id="f37f7-148">Cette fonction peut également être utilisée par les applications clientes pour valider ou réparer des dossiers de messages standard.</span><span class="sxs-lookup"><span data-stu-id="f37f7-148">This function can also be used by client applications to validate or repair standard message folders.</span></span> 
  
 <span data-ttu-id="f37f7-149">**HrValidateIPMSubtree** crée toujours les dossiers racine de recherche et sous-arborescence IPM dans le dossier racine de la Banque et le dossier éléments supprimés dans le dossier sous-arborescence IPM.</span><span class="sxs-lookup"><span data-stu-id="f37f7-149">**HrValidateIPMSubtree** always creates the Search Root and IPM Subtree folders in the store's root folder and the Deleted Items folder in the IPM Subtree folder.</span></span> <span data-ttu-id="f37f7-150">Le dossier de sous-arborescence IPM est la racine de la hiérarchie IPM dans ce magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="f37f7-150">The IPM Subtree folder is the root of the IPM hierarchy in that message store.</span></span> <span data-ttu-id="f37f7-151">Le dossier racine de recherche peut être utilisé comme racine d'une sous-arborescence pour les dossiers de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="f37f7-151">The Search Root folder can be used as the root of a subtree for search-results folders.</span></span> 
  
<span data-ttu-id="f37f7-152">Les clients IPM doivent afficher l'affichage de leur dossier en commençant par le dossier racine de la sous-arborescence IPM et en affichant les dossiers enfants en dessous.</span><span class="sxs-lookup"><span data-stu-id="f37f7-152">IPM clients should display their folder view starting at the IPM subtree root folder and showing child folders beneath it.</span></span> <span data-ttu-id="f37f7-153">Les informations contenues dans le dossier racine d'une banque de messages ne doivent pas apparaître dans l'interface utilisateur d'un client.</span><span class="sxs-lookup"><span data-stu-id="f37f7-153">Information in the root folder of a message store should not appear in a client's user interface.</span></span> <span data-ttu-id="f37f7-154">Cette fonctionnalité signifie que si un client doit masquer les informations, les informations peuvent être placées dans le répertoire racine de la sous-arborescence IPM, où il n'est pas visible par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f37f7-154">This functionality means that if a client must hide information, the information can be put in the IPM subtree root directory, where it is not visible to the user.</span></span> <span data-ttu-id="f37f7-155">En revanche, les applications non-IPM qui nécessitent que des messages et des dossiers soient invisibles pour l'utilisateur, par exemple dans une banque de messages basée sur un serveur, peuvent les placer en dehors de la hiérarchie IPM.</span><span class="sxs-lookup"><span data-stu-id="f37f7-155">In contrast, non-IPM applications that require messages and folders to be invisible to the user, for example in a server-based message store, can put them outside the IPM hierarchy.</span></span> 
  
 <span data-ttu-id="f37f7-156">**HrValidateIPMSubtree** définit la propriété **PR_VALID_FOLDER_MASK** pour indiquer si chaque dossier IPM créé a un identificateur d'entrée valide.</span><span class="sxs-lookup"><span data-stu-id="f37f7-156">**HrValidateIPMSubtree** sets the **PR_VALID_FOLDER_MASK** property to indicate whether each IPM folder it creates has a valid entry identifier.</span></span> <span data-ttu-id="f37f7-157">Les propriétés d'identificateur d'entrée suivantes de la Banque de messages sont définies sur les identificateurs d'entrée des dossiers correspondants et renvoyés dans le paramètre _lppProps_ avec **PR_VALID_FOLDER_MASK**:</span><span class="sxs-lookup"><span data-stu-id="f37f7-157">The following entry identifier properties of the message store are set to the entry identifiers of the corresponding folders and returned in the  _lppProps_ parameter along with **PR_VALID_FOLDER_MASK**:</span></span> 
  
 <span data-ttu-id="f37f7-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f37f7-158">**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f37f7-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f37f7-159">**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f37f7-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f37f7-160">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f37f7-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f37f7-161">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f37f7-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f37f7-162">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f37f7-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f37f7-163">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f37f7-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f37f7-164">**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))</span></span>
  
> <span data-ttu-id="f37f7-165">Un espace réservé [PROP_TAG](prop_tag.md) pour la boîte de réception IPM (PT_BINARY, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="f37f7-165">A placeholder [PROP_TAG](prop_tag.md) for the IPM Inbox (PT_BINARY, PROP_ID_NULL).</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="f37f7-166">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f37f7-166">MFCMAPI reference</span></span>

<span data-ttu-id="f37f7-167">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f37f7-167">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f37f7-168">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="f37f7-168">**File**</span></span>|<span data-ttu-id="f37f7-169">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="f37f7-169">**Function**</span></span>|<span data-ttu-id="f37f7-170">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="f37f7-170">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f37f7-171">MstStoreDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="f37f7-171">MstStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="f37f7-172">CMsgStoreDlg:: OnValidateIPMSubtree</span><span class="sxs-lookup"><span data-stu-id="f37f7-172">CMsgStoreDlg::OnValidateIPMSubtree</span></span>  <br/> |<span data-ttu-id="f37f7-173">MFCMAPI utilise la méthode **HrValidateIPMSubtree** pour ajouter des dossiers standard à une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f37f7-173">MFCMAPI uses the **HrValidateIPMSubtree** method to add standard folders to a message store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f37f7-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f37f7-174">See also</span></span>



[<span data-ttu-id="f37f7-175">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="f37f7-175">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)


[<span data-ttu-id="f37f7-176">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="f37f7-176">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

