---
title: IMAPIContainerGetContentsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetContentsTable
api_type:
- COM
ms.assetid: 88c7a666-875d-473a-b126-dbbb7009f7d9
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 871dafd7bf8959cf814d65991fe08fdb2b283c08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783705"
---
# <a name="imapicontainergetcontentstable"></a><span data-ttu-id="53f4c-103">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="53f4c-103">IMAPIContainer::GetContentsTable</span></span>

  
  
<span data-ttu-id="53f4c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="53f4c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="53f4c-105">Retourne un pointeur vers la table des matières du conteneur.</span><span class="sxs-lookup"><span data-stu-id="53f4c-105">Returns a pointer to the container's contents table.</span></span>
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="53f4c-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="53f4c-106">Parameters</span></span>

 <span data-ttu-id="53f4c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="53f4c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="53f4c-108">[in] Masque de bits d’indicateurs qui contrôle la façon dont la table des matières est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="53f4c-108">[in] A bitmask of flags that controls how the contents table is returned.</span></span> <span data-ttu-id="53f4c-109">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="53f4c-109">The following flags can be set:</span></span>
    
<span data-ttu-id="53f4c-110">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="53f4c-110">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="53f4c-111">Table des matières associée du conteneur doit être retournée au lieu de la table des matières standard.</span><span class="sxs-lookup"><span data-stu-id="53f4c-111">The container's associated contents table should be returned instead of the standard contents table.</span></span> <span data-ttu-id="53f4c-112">Cet indicateur est utilisé uniquement avec les dossiers.</span><span class="sxs-lookup"><span data-stu-id="53f4c-112">This flag is used only with folders.</span></span> <span data-ttu-id="53f4c-113">Les messages qui sont inclus dans le tableau contenu associé ont été créés avec l’indicateur MAPI_ASSOCIATED défini dans l’appel à la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="53f4c-113">The messages that are included in the associated contents table were created with the MAPI_ASSOCIATED flag set in the call to the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="53f4c-114">Clients utilisent généralement le tableau contenu associé pour récupérer les formulaires, les vues et les autres messages masqués.</span><span class="sxs-lookup"><span data-stu-id="53f4c-114">Clients typically use the associated contents table to retrieve forms, views, and other hidden messages.</span></span> 
    
<span data-ttu-id="53f4c-115">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="53f4c-115">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="53f4c-116">Permet d’accéder aux droits frightsFreeBusySimple et frightsFreeBusyDetailed dans **PR_MEMBER_RIGHTS**.</span><span class="sxs-lookup"><span data-stu-id="53f4c-116">Enables access to the frightsFreeBusySimple and frightsFreeBusyDetailed rights in **PR_MEMBER_RIGHTS**.</span></span>
    
<span data-ttu-id="53f4c-117">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="53f4c-117">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="53f4c-118">**GetContentsTable** peut renvoyer avec succès, probablement que le tableau soit disponible à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="53f4c-118">**GetContentsTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="53f4c-119">Si le tableau n’est pas disponible, l’émission d’un appel de la table suivante peut déclencher une erreur.</span><span class="sxs-lookup"><span data-stu-id="53f4c-119">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="53f4c-120">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="53f4c-120">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="53f4c-121">Demandes de renvoyer les colonnes qui contiennent des données de type chaîne au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="53f4c-121">Requests that the columns that contain string data be returned in the Unicode format.</span></span> <span data-ttu-id="53f4c-122">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes doivent être retournées au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="53f4c-122">If the MAPI_UNICODE flag is not set, the strings should be returned in the ANSI format.</span></span> 
    
<span data-ttu-id="53f4c-123">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="53f4c-123">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="53f4c-124">Affiche les éléments qui sont actuellement marqués comme logicielles supprimés — autrement dit, ils sont dans la rétention des éléments supprimés phase de temps.</span><span class="sxs-lookup"><span data-stu-id="53f4c-124">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="53f4c-125">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="53f4c-125">_lppTable_</span></span>
  
> <span data-ttu-id="53f4c-126">[out] Pointeur vers un pointeur vers la table des matières.</span><span class="sxs-lookup"><span data-stu-id="53f4c-126">[out] A pointer to a pointer to the contents table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="53f4c-127">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="53f4c-127">Return value</span></span>

<span data-ttu-id="53f4c-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="53f4c-128">S_OK</span></span> 
  
> <span data-ttu-id="53f4c-129">Le tableau contenu a été récupéré correctement.</span><span class="sxs-lookup"><span data-stu-id="53f4c-129">The contents table was successfully retrieved.</span></span>
    
<span data-ttu-id="53f4c-130">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="53f4c-130">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="53f4c-131">Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="53f4c-131">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="53f4c-132">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="53f4c-132">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="53f4c-133">Le conteneur n’a pas de contenu et ne peuvent pas fournir une table des matières.</span><span class="sxs-lookup"><span data-stu-id="53f4c-133">The container has no contents and cannot provide a contents table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="53f4c-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="53f4c-134">Remarks</span></span>

<span data-ttu-id="53f4c-135">La méthode **IMAPIContainer::GetContentsTable** renvoie un pointeur vers la table des matières d’un conteneur.</span><span class="sxs-lookup"><span data-stu-id="53f4c-135">The **IMAPIContainer::GetContentsTable** method returns a pointer to the contents table of a container.</span></span> <span data-ttu-id="53f4c-136">Une table des matières contient des informations récapitulatives concernant les objets dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="53f4c-136">A contents table contains summary information about objects in the container.</span></span> 
  
<span data-ttu-id="53f4c-137">Tables des matières disposez d’ensembles de colonne longs.</span><span class="sxs-lookup"><span data-stu-id="53f4c-137">Contents tables have lengthy column sets.</span></span> <span data-ttu-id="53f4c-138">Pour obtenir une liste complète des colonnes obligatoires et facultatifs dans les tableaux de contenu, voir [Les Tables de contenu](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="53f4c-138">For a complete list of the required and optional columns in contents tables, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="53f4c-139">Il est possible pour certains conteneurs de n’avoir aucun contenu.</span><span class="sxs-lookup"><span data-stu-id="53f4c-139">It is possible for some containers to have no contents.</span></span> <span data-ttu-id="53f4c-140">Ces conteneurs renvoient MAPI_E_NO_SUPPORT à partir de leurs implémentations de **GetContentsTable**.</span><span class="sxs-lookup"><span data-stu-id="53f4c-140">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetContentsTable**.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="53f4c-141">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="53f4c-141">Notes to implementers</span></span>

<span data-ttu-id="53f4c-142">Si vous prenez en charge une table des matières pour votre conteneur, vous devez également procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="53f4c-142">If you support a contents table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="53f4c-143">Prend en charge les appels de méthode de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur pour ouvrir la propriété **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="53f4c-143">Support calls to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="53f4c-144">Retourner **PR_CONTAINER_CONTENTS** en réponse à un appel à du conteneur</span><span class="sxs-lookup"><span data-stu-id="53f4c-144">Return **PR_CONTAINER_CONTENTS** in response to a call to the container's</span></span> 
    
    <span data-ttu-id="53f4c-145">Méthodes [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPIProp::GetPropList](imapiprop-getproplist.md) .</span><span class="sxs-lookup"><span data-stu-id="53f4c-145">[IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPIProp::GetPropList](imapiprop-getproplist.md) methods.</span></span> 
    
<span data-ttu-id="53f4c-146">Implémentation d’un fournisseur de transport à distance de cette méthode doit renvoyer un pointeur vers une [IMAPITable : IUnknown](imapitableiunknown.md) interface dans le paramètre _ppTable_ transmis à la méthode **GetContentsTable** .</span><span class="sxs-lookup"><span data-stu-id="53f4c-146">A remote transport provider's implementation of this method must return a pointer to an [IMAPITable : IUnknown](imapitableiunknown.md) interface in the  _ppTable_ parameter passed into the **GetContentsTable** method.</span></span> <span data-ttu-id="53f4c-147">Si votre fournisseur de transport a une table de contenu existante, il suffit de retourner un pointeur.</span><span class="sxs-lookup"><span data-stu-id="53f4c-147">If your transport provider has an existing contents table, it is sufficient to return a pointer to it.</span></span> <span data-ttu-id="53f4c-148">Si pas, cette méthode doit créer une nouvelle [IMAPITable : IUnknown](imapitableiunknown.md) objet, remplir le tableau avec des en-têtes de message (s’ils sont disponibles) et retourner un pointeur vers la nouvelle table.</span><span class="sxs-lookup"><span data-stu-id="53f4c-148">If not, this method must create a new [IMAPITable : IUnknown](imapitableiunknown.md) object, populate the table with message headers (if any are available), and return a pointer to the new table.</span></span> <span data-ttu-id="53f4c-149">La méthode [ITableData::HrGetView](itabledata-hrgetview.md) est utile pour la génération d’une valeur de retour et en stockant le pointeur de la table dans le paramètre _ppTable_ .</span><span class="sxs-lookup"><span data-stu-id="53f4c-149">The [ITableData::HrGetView](itabledata-hrgetview.md) method is useful for generating a return value and storing the table pointer in the  _ppTable_ parameter.</span></span> <span data-ttu-id="53f4c-150">La table des matières doit prendre en charge au moins les colonnes de propriété suivantes :</span><span class="sxs-lookup"><span data-stu-id="53f4c-150">The contents table must support at least the following property columns:</span></span> 
  
- <span data-ttu-id="53f4c-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53f4c-151">**PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="53f4c-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53f4c-152">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>
    
- <span data-ttu-id="53f4c-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53f4c-153">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>
    
- <span data-ttu-id="53f4c-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53f4c-154">**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))</span></span>
    
- <span data-ttu-id="53f4c-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53f4c-155">**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))</span></span>
    
- <span data-ttu-id="53f4c-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53f4c-156">**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))</span></span>
    
- <span data-ttu-id="53f4c-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53f4c-157">**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))</span></span>
    
- <span data-ttu-id="53f4c-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53f4c-158">**PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))</span></span>
    
- <span data-ttu-id="53f4c-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53f4c-159">**PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))</span></span>
    
- <span data-ttu-id="53f4c-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53f4c-160">**PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))</span></span>
    
- <span data-ttu-id="53f4c-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53f4c-161">**PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))</span></span>
    
- <span data-ttu-id="53f4c-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53f4c-162">**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))</span></span>
    
- <span data-ttu-id="53f4c-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53f4c-163">**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="53f4c-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53f4c-164">**PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))</span></span>
    
- <span data-ttu-id="53f4c-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53f4c-165">**PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))</span></span>
    
- <span data-ttu-id="53f4c-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53f4c-166">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="53f4c-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53f4c-167">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>
    
- <span data-ttu-id="53f4c-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53f4c-168">**PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="53f4c-169">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="53f4c-169">Notes to callers</span></span>

<span data-ttu-id="53f4c-170">Colonnes de tableau contenu chaîne et binaires peuvent être tronqués.</span><span class="sxs-lookup"><span data-stu-id="53f4c-170">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="53f4c-171">En règle générale, les fournisseurs retournent 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="53f4c-171">Typically, providers return 255 characters.</span></span> <span data-ttu-id="53f4c-172">Car vous ne pouvez pas savoir au préalable si une table inclut des colonnes tronqués, supposons qu’une colonne est tronquée si la longueur de la colonne est 255 ou 510 octets.</span><span class="sxs-lookup"><span data-stu-id="53f4c-172">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="53f4c-173">Vous pouvez toujours récupérer la valeur complète d’une colonne tronquée, si nécessaire, directement à partir de l’objet à l’aide de son identificateur d’entrée pour l’ouvrir, puis en appelant la méthode **IMAPIProp::GetProps** .</span><span class="sxs-lookup"><span data-stu-id="53f4c-173">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the **IMAPIProp::GetProps** method.</span></span> 
  
<span data-ttu-id="53f4c-174">Selon l’implémentation du fournisseur, les restrictions et les opérations de tri peuvent s’appliquent à l’ensemble d’une chaîne ou vers la version tronquée de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="53f4c-174">Depending on the provider's implementation, restrictions and sorting operations can apply to all of a string or to the truncated version of that string.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="53f4c-175">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="53f4c-175">MFCMAPI reference</span></span>

<span data-ttu-id="53f4c-176">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="53f4c-176">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="53f4c-177">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="53f4c-177">**File**</span></span>|<span data-ttu-id="53f4c-178">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="53f4c-178">**Function**</span></span>|<span data-ttu-id="53f4c-179">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="53f4c-179">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="53f4c-180">ContentsTableDialog.cpp</span><span class="sxs-lookup"><span data-stu-id="53f4c-180">ContentsTableDialog.cpp</span></span>  <br/> |<span data-ttu-id="53f4c-181">CContentsTableDlg::CContentsTableDlg</span><span class="sxs-lookup"><span data-stu-id="53f4c-181">CContentsTableDlg::CContentsTableDlg</span></span>  <br/> |<span data-ttu-id="53f4c-182">La classe **CContentsTableDlg** utilise **GetContentsTable** pour obtenir les entrées dans une table des matières.</span><span class="sxs-lookup"><span data-stu-id="53f4c-182">The **CContentsTableDlg** class uses **GetContentsTable** to obtain the entries in a contents table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53f4c-183">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53f4c-183">See also</span></span>



[<span data-ttu-id="53f4c-184">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="53f4c-184">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="53f4c-185">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="53f4c-185">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="53f4c-186">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="53f4c-186">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="53f4c-187">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="53f4c-187">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="53f4c-188">Propriété canonique PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="53f4c-188">PidTagContainerContents Canonical Property</span></span>](pidtagcontainercontents-canonical-property.md)
  
[<span data-ttu-id="53f4c-189">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="53f4c-189">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="53f4c-190">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="53f4c-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

