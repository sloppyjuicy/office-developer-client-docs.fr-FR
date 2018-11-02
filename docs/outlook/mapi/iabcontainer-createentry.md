---
title: IABContainerCreateEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CreateEntry
api_type:
- COM
ms.assetid: ea1daf74-d9e3-4304-bf5d-889afeea6ae9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2f8a6baa9a910b91e633084f1d9cd8ac52b24d5b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575601"
---
# <a name="iabcontainercreateentry"></a><span data-ttu-id="f7167-103">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="f7167-103">IABContainer::CreateEntry</span></span>

  
  
<span data-ttu-id="f7167-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7167-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7167-105">Crée une nouvelle entrée, qui peut être un utilisateur de messagerie, une liste de distribution ou un autre conteneur.</span><span class="sxs-lookup"><span data-stu-id="f7167-105">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a><span data-ttu-id="f7167-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7167-106">Parameters</span></span>

 <span data-ttu-id="f7167-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f7167-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="f7167-108">[in] Le nombre d’octets de l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="f7167-108">[in] The count of the bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f7167-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f7167-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="f7167-110">[in] Pointeur vers l’identificateur d’entrée d’un modèle pour la création de nouvelles entrées d’un type particulier.</span><span class="sxs-lookup"><span data-stu-id="f7167-110">[in] A pointer to the entry identifier of a template for creating new entries of a particular type.</span></span> 
    
 <span data-ttu-id="f7167-111">_ulCreateFlags_</span><span class="sxs-lookup"><span data-stu-id="f7167-111">_ulCreateFlags_</span></span>
  
> <span data-ttu-id="f7167-112">[in] Masque de bits d’indicateurs qui contrôle la création d’entrée est effectuée.</span><span class="sxs-lookup"><span data-stu-id="f7167-112">[in] A bitmask of flags that controls how entry creation is performed.</span></span> <span data-ttu-id="f7167-113">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="f7167-113">The following flags can be set:</span></span>
    
<span data-ttu-id="f7167-114">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="f7167-114">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="f7167-115">Un niveau de vérification de l’entrée en double libre doit être effectué.</span><span class="sxs-lookup"><span data-stu-id="f7167-115">A loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="f7167-116">L’implémentation de vérification de l’entrée en double en vrac est spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f7167-116">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="f7167-117">Par exemple, un fournisseur peut définir une correspondance partielle, comme les deux entrées qui ont le même nom d’affichage.</span><span class="sxs-lookup"><span data-stu-id="f7167-117">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="f7167-118">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="f7167-118">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="f7167-119">Un niveau strict de vérification de l’entrée en double doit être effectué.</span><span class="sxs-lookup"><span data-stu-id="f7167-119">A strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="f7167-120">L’implémentation de vérification stricte entrée en double est spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f7167-120">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="f7167-121">Par exemple, un fournisseur peut définir une correspondance exacte comme les deux entrées qui ont à la fois le même nom et l’adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="f7167-121">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="f7167-122">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="f7167-122">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="f7167-123">Une nouvelle entrée doit remplacer un s’il est déterminé que les deux sont des doublons.</span><span class="sxs-lookup"><span data-stu-id="f7167-123">A new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
 <span data-ttu-id="f7167-124">_lppMAPIPropEntry_</span><span class="sxs-lookup"><span data-stu-id="f7167-124">_lppMAPIPropEntry_</span></span>
  
> <span data-ttu-id="f7167-125">[out] Pointeur vers un pointeur vers l’entrée nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="f7167-125">[out] A pointer to a pointer to the newly created entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f7167-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f7167-126">Return value</span></span>

<span data-ttu-id="f7167-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="f7167-127">S_OK</span></span> 
  
> <span data-ttu-id="f7167-128">La nouvelle entrée a été créée avec succès.</span><span class="sxs-lookup"><span data-stu-id="f7167-128">The new entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f7167-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="f7167-129">Remarks</span></span>

<span data-ttu-id="f7167-130">La méthode **IABContainer::CreateEntry** crée une nouvelle entrée d’un type particulier dans le conteneur spécifié, qui retourne un pointeur vers une implémentation de l’interface pour l’accès à l’entrée.</span><span class="sxs-lookup"><span data-stu-id="f7167-130">The **IABContainer::CreateEntry** method creates a new entry of a particular type in the specified container, returning a pointer to an interface implementation for further access to the entry.</span></span> <span data-ttu-id="f7167-131">La nouvelle entrée est créée à l’aide d’un modèle qui a été sélectionné à partir de la liste du conteneur des modèles disponibles publié dans sa table unique.</span><span class="sxs-lookup"><span data-stu-id="f7167-131">The new entry is created by using a template that has been selected from the container's list of available templates published in its one-off table.</span></span> <span data-ttu-id="f7167-132">Les appelants accéder table uniques d’un conteneur en appelant la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) et demande la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f7167-132">Callers access a container's one-off table by calling its [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f7167-133">Remarques à l’attention des responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="f7167-133">Notes to implementers</span></span>

<span data-ttu-id="f7167-134">Tous les conteneurs qui prennent en charge la méthode **IABContainer::CreateEntry** doivent être modifiables.</span><span class="sxs-lookup"><span data-stu-id="f7167-134">All containers that support the **IABContainer::CreateEntry** method must be modifiable.</span></span> <span data-ttu-id="f7167-135">Définir l’indicateur AB_MODIFIABLE de votre conteneur dans sa propriété **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) pour indiquer qu’il est modifiable.</span><span class="sxs-lookup"><span data-stu-id="f7167-135">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="f7167-136">Vous devez prendre en charge tous les indicateurs _ulCreateFlags_ .</span><span class="sxs-lookup"><span data-stu-id="f7167-136">You should support all of the  _ulCreateFlags_ flags.</span></span> <span data-ttu-id="f7167-137">Toutefois, l’interprétation et l’utilisation de ces indicateurs est spécifique à l’implémentation — autrement dit, vous pouvez déterminer la signification de la sémantique de CREATE_CHECK_DUP_LOOSE et CREATE_CHECK_DUP_STRICT dans le cadre de votre implémentation.</span><span class="sxs-lookup"><span data-stu-id="f7167-137">However, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT mean in the context of your implementation.</span></span> <span data-ttu-id="f7167-138">Si vous ne pouvez pas ou ne déterminez pas si une entrée est un doublon, toujours autoriser l’entrée doit être créé.</span><span class="sxs-lookup"><span data-stu-id="f7167-138">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be created.</span></span> 
  
<span data-ttu-id="f7167-139">Certains fournisseurs implémentent stricte entrée vérification en comparant le nom complet, la messagerie adresse et la clé de recherche dans une entrée ; autres fournisseurs limitent la correspondance pour afficher le nom et l’adresse.</span><span class="sxs-lookup"><span data-stu-id="f7167-139">Some providers implement strict entry checking by matching the display name, messaging address, and search key in an entry; other providers limit the match to display name and address.</span></span> <span data-ttu-id="f7167-140">Vérification de l’entrée en vrac est souvent implémenté en vérifiant seulement le nom d’affichage.</span><span class="sxs-lookup"><span data-stu-id="f7167-140">Loose entry checking is often implemented by checking the display name only.</span></span> 
  
## <a name="notes-to-host-address-book-provider-implementers"></a><span data-ttu-id="f7167-141">Remarques pour héberger l’adresse de l’implémentation de fournisseur livre</span><span class="sxs-lookup"><span data-stu-id="f7167-141">Notes to Host Address Book Provider Implementers</span></span>

<span data-ttu-id="f7167-142">Si votre conteneur peut créer des entrées à partir des modèles d’autres fournisseurs, votre implémentation de **CreateEntry** doit offrir de stockage pour certaines ou toutes les propriétés associées les écritures créées.</span><span class="sxs-lookup"><span data-stu-id="f7167-142">If your container can create entries from the templates of other providers, your implementation of **CreateEntry** should provide storage for some or all of the properties associated with the created entries.</span></span> <span data-ttu-id="f7167-143">Par exemple, si vous fournissez un stockage pour une propriété du **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)), vous pouvez générer la boîte de dialogue Détails sans devoir dépendent du fournisseur étranger.</span><span class="sxs-lookup"><span data-stu-id="f7167-143">For example, if you provide storage for an entry's **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property, you can generate its details dialog box without having to depend on the foreign provider.</span></span> 
  
<span data-ttu-id="f7167-144">Si votre conteneur peut créer des entrées qui prennent en charge la propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), votre implémentation de **CreateEntry** procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="f7167-144">If your container can create entries that support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, your implementation of **CreateEntry** must do the following:</span></span> 
  
1. <span data-ttu-id="f7167-145">Appelez la méthode [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) .</span><span class="sxs-lookup"><span data-stu-id="f7167-145">Call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method.</span></span> <span data-ttu-id="f7167-146">**OpenTemplateID** permet de code du fournisseur étranger pour l’entrée à lier à la nouvelle entrée en cours de création.</span><span class="sxs-lookup"><span data-stu-id="f7167-146">**OpenTemplateID** enables the foreign provider's code for the entry to bind to the new entry being created.</span></span> <span data-ttu-id="f7167-147">Fournisseurs étrangers prennent en charge ce processus de liaison pour contrôler les entrées créées à partir de leurs modèles dans les conteneurs de fournisseurs de carnet d’adresses hôte.</span><span class="sxs-lookup"><span data-stu-id="f7167-147">Foreign providers support this binding process to maintain control over entries created from their templates into the containers of host address book providers.</span></span> 
    
2. <span data-ttu-id="f7167-148">Effectuer toute initialisation nécessaire et remplir le nouvel objet avec toutes les propriétés de l’entrée dans le fournisseur de l’objet retourné dans le paramètre _lppMAPIPropNew_ **d’OpenTemplateID**étrangère.</span><span class="sxs-lookup"><span data-stu-id="f7167-148">Perform any necessary initialization, and populate the new object with all of the properties from the entry in the foreign provider that the object returned in the  _lppMAPIPropNew_ parameter from **OpenTemplateID**.</span></span>
    
<span data-ttu-id="f7167-149">Si **OpenTemplateID** réussit, copiez les propriétés à l’implémentation désignés par le paramètre _lppMAPIPropNew_ plutôt que directement à l’implémentation désignés par le paramètre _lpMAPIPropData_ .</span><span class="sxs-lookup"><span data-stu-id="f7167-149">If **OpenTemplateID** succeeds, copy the properties to the implementation pointed to by the  _lppMAPIPropNew_ parameter rather than directly to the implementation pointed to by the  _lpMAPIPropData_ parameter.</span></span> <span data-ttu-id="f7167-150">Initialiser la nouvelle entrée pour une utilisation en mode hors connexion, comme vous le feriez pour n’importe quel autre entrée d’un fournisseur externe.</span><span class="sxs-lookup"><span data-stu-id="f7167-150">Initialize the new entry for offline use as you would any other entry from a foreign provider.</span></span> 
  
<span data-ttu-id="f7167-151">Si **OpenTemplateID** renvoie une erreur, **CreateEntry** doit échouer.</span><span class="sxs-lookup"><span data-stu-id="f7167-151">If **OpenTemplateID** returns an error, **CreateEntry** should fail.</span></span> <span data-ttu-id="f7167-152">Ne pas autoriser l’entrée doit être créé.</span><span class="sxs-lookup"><span data-stu-id="f7167-152">Do not allow the entry to be created.</span></span> <span data-ttu-id="f7167-153">Étant donné que le fournisseur étranger peut émettre des hypothèses sur les données dans votre fournisseur, ne pas créer une entrée avec un identificateur de modèle qui n’a pas été correctement lié au fournisseur étranger.</span><span class="sxs-lookup"><span data-stu-id="f7167-153">Because the foreign provider can make assumptions about the data in your provider, do not create an entry with a template identifier that has not been successfully bound to the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f7167-154">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="f7167-154">Notes to callers</span></span>

<span data-ttu-id="f7167-155">Lorsque **CreateEntry** renvoie, vous pouvez ou ne sont peut-être pas en mesure d’accéder immédiatement à l’identificateur d’entrée pour la nouvelle entrée.</span><span class="sxs-lookup"><span data-stu-id="f7167-155">When **CreateEntry** returns, you may or may not be able to immediately access the entry identifier for the new entry.</span></span> <span data-ttu-id="f7167-156">Certains fournisseurs de carnet d’adresses n’apportez il disponibles qu’une fois que vous avez appelé la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la nouvelle entrée.</span><span class="sxs-lookup"><span data-stu-id="f7167-156">Some address book providers do not make it available until after you have called the new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="f7167-157">Bien que les indicateurs de vérification en double sont transmis en tant que paramètres à **CreateEntry**, le doublon opération de vérification ne se produit pas jusqu'à ce que **SaveChanges** est appelée.</span><span class="sxs-lookup"><span data-stu-id="f7167-157">Although duplicate checking flags are passed as parameters to **CreateEntry**, the duplicate checking operation does not occur until **SaveChanges** is called.</span></span> <span data-ttu-id="f7167-158">Par conséquent, les erreurs associées, telles que MAPI_E_COLLISION, ce qui indique qu’une tentative a été effectuée pour créer une entrée existante, sont renvoyées par **SaveChanges** plutôt que **CreateEntry**.</span><span class="sxs-lookup"><span data-stu-id="f7167-158">Therefore, related errors such as MAPI_E_COLLISION, which indicates that an attempt was made to create an already existing entry, are returned by **SaveChanges** rather than **CreateEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f7167-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7167-159">See also</span></span>



[<span data-ttu-id="f7167-160">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="f7167-160">IABContainer::CopyEntries</span></span>](iabcontainer-copyentries.md)
  
[<span data-ttu-id="f7167-161">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="f7167-161">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="f7167-162">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="f7167-162">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="f7167-163">Propriété canonique PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="f7167-163">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="f7167-164">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="f7167-164">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

