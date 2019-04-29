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
ms.openlocfilehash: 9f80130279e3437dd9be947de97d3f0d4181165e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411273"
---
# <a name="iabcontainercreateentry"></a><span data-ttu-id="5e465-103">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="5e465-103">IABContainer::CreateEntry</span></span>

  
  
<span data-ttu-id="5e465-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e465-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e465-105">Crée une nouvelle entrée, qui peut être un utilisateur de messagerie, une liste de distribution ou un autre conteneur.</span><span class="sxs-lookup"><span data-stu-id="5e465-105">Creates a new entry, which can be a messaging user, a distribution list, or another container.</span></span>
  
```cpp
HRESULT CreateEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulCreateFlags,
  LPMAPIPROP FAR * lppMAPIPropEntry
);
```

## <a name="parameters"></a><span data-ttu-id="5e465-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e465-106">Parameters</span></span>

 <span data-ttu-id="5e465-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="5e465-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="5e465-108">dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="5e465-108">[in] The count of the bytes in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="5e465-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="5e465-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="5e465-110">dans Pointeur vers l'identificateur d'entrée d'un modèle pour la création de nouvelles entrées d'un type particulier.</span><span class="sxs-lookup"><span data-stu-id="5e465-110">[in] A pointer to the entry identifier of a template for creating new entries of a particular type.</span></span> 
    
 <span data-ttu-id="5e465-111">_ulCreateFlags_</span><span class="sxs-lookup"><span data-stu-id="5e465-111">_ulCreateFlags_</span></span>
  
> <span data-ttu-id="5e465-112">dans Masque de des indicateurs qui contrôle le mode de création de l'entrée.</span><span class="sxs-lookup"><span data-stu-id="5e465-112">[in] A bitmask of flags that controls how entry creation is performed.</span></span> <span data-ttu-id="5e465-113">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="5e465-113">The following flags can be set:</span></span>
    
<span data-ttu-id="5e465-114">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="5e465-114">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="5e465-115">Un niveau faible de vérification des entrées en double doit être effectué.</span><span class="sxs-lookup"><span data-stu-id="5e465-115">A loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="5e465-116">L'implémentation de la vérification des entrées en double libre est spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5e465-116">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="5e465-117">Par exemple, un fournisseur peut définir une correspondance libre comme deux entrées portant le même nom complet.</span><span class="sxs-lookup"><span data-stu-id="5e465-117">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="5e465-118">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="5e465-118">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="5e465-119">Un niveau strict de vérification des entrées en double doit être effectué.</span><span class="sxs-lookup"><span data-stu-id="5e465-119">A strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="5e465-120">L'implémentation d'une vérification d'entrée stricte en double est propre au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5e465-120">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="5e465-121">Par exemple, un fournisseur peut définir une correspondance stricte comme deux entrées ayant à la fois le même nom d'affichage et l'même adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="5e465-121">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="5e465-122">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="5e465-122">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="5e465-123">Une nouvelle entrée doit remplacer une entrée existante s'il est déterminé que les deux sont des doublons.</span><span class="sxs-lookup"><span data-stu-id="5e465-123">A new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
 <span data-ttu-id="5e465-124">_lppMAPIPropEntry_</span><span class="sxs-lookup"><span data-stu-id="5e465-124">_lppMAPIPropEntry_</span></span>
  
> <span data-ttu-id="5e465-125">remarquer Pointeur vers un pointeur vers l'entrée nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="5e465-125">[out] A pointer to a pointer to the newly created entry.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5e465-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5e465-126">Return value</span></span>

<span data-ttu-id="5e465-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="5e465-127">S_OK</span></span> 
  
> <span data-ttu-id="5e465-128">La création de l'entrée a réussi.</span><span class="sxs-lookup"><span data-stu-id="5e465-128">The new entry was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5e465-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="5e465-129">Remarks</span></span>

<span data-ttu-id="5e465-130">La méthode **IABContainer:: CreateEntry** crée une nouvelle entrée d'un type particulier dans le conteneur spécifié, en renvoyant un pointeur vers une implémentation d'interface pour un accès supplémentaire à l'entrée.</span><span class="sxs-lookup"><span data-stu-id="5e465-130">The **IABContainer::CreateEntry** method creates a new entry of a particular type in the specified container, returning a pointer to an interface implementation for further access to the entry.</span></span> <span data-ttu-id="5e465-131">La nouvelle entrée est créée à l'aide d'un modèle qui a été sélectionné dans la liste des modèles disponibles du conteneur publié dans sa table One-Off.</span><span class="sxs-lookup"><span data-stu-id="5e465-131">The new entry is created by using a template that has been selected from the container's list of available templates published in its one-off table.</span></span> <span data-ttu-id="5e465-132">Les appelants accèdent à la table ponctuelle d'un conteneur en appelant sa méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) et en demandant la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5e465-132">Callers access a container's one-off table by calling its [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5e465-133">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="5e465-133">Notes to implementers</span></span>

<span data-ttu-id="5e465-134">Tous les conteneurs qui prennent en charge la méthode **IABContainer:: CreateEntry** doivent être modifiables.</span><span class="sxs-lookup"><span data-stu-id="5e465-134">All containers that support the **IABContainer::CreateEntry** method must be modifiable.</span></span> <span data-ttu-id="5e465-135">Définissez l'indicateur AB_MODIFIABLE de votre conteneur dans sa propriété **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) pour indiquer qu'il est modifiable.</span><span class="sxs-lookup"><span data-stu-id="5e465-135">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="5e465-136">Vous devez prendre en charge tous les indicateurs _ulCreateFlags_ .</span><span class="sxs-lookup"><span data-stu-id="5e465-136">You should support all of the  _ulCreateFlags_ flags.</span></span> <span data-ttu-id="5e465-137">Toutefois, l'interprétation et l'utilisation de ces indicateurs sont propres à l'implémentation, autrement dit, vous pouvez déterminer les sémantiques de CREATE_CHECK_DUP_LOOSE et CREATE_CHECK_DUP_STRICT dans le contexte de votre implémentation.</span><span class="sxs-lookup"><span data-stu-id="5e465-137">However, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT mean in the context of your implementation.</span></span> <span data-ttu-id="5e465-138">Si vous ne pouvez pas ou ne Déterminez pas si une entrée est un doublon, autorisez toujours la création de l'entrée.</span><span class="sxs-lookup"><span data-stu-id="5e465-138">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be created.</span></span> 
  
<span data-ttu-id="5e465-139">Certains fournisseurs implémentent une vérification stricte de l'entrée en faisant correspondre le nom complet, l'adresse de messagerie et la clé de recherche dans une entrée; les autres fournisseurs limitent la correspondance au nom complet et à l'adresse.</span><span class="sxs-lookup"><span data-stu-id="5e465-139">Some providers implement strict entry checking by matching the display name, messaging address, and search key in an entry; other providers limit the match to display name and address.</span></span> <span data-ttu-id="5e465-140">La vérification d'entrée libre est souvent implémentée en vérifiant uniquement le nom d'affichage.</span><span class="sxs-lookup"><span data-stu-id="5e465-140">Loose entry checking is often implemented by checking the display name only.</span></span> 
  
## <a name="notes-to-host-address-book-provider-implementers"></a><span data-ttu-id="5e465-141">Notes pour héberger les implémenteurs de fournisseurs de carnets d'adresses</span><span class="sxs-lookup"><span data-stu-id="5e465-141">Notes to Host Address Book Provider Implementers</span></span>

<span data-ttu-id="5e465-142">Si votre conteneur peut créer des entrées à partir des modèles d'autres fournisseurs, votre implémentation de **CreateEntry** doit fournir une partie ou la totalité des propriétés associées aux entrées créées.</span><span class="sxs-lookup"><span data-stu-id="5e465-142">If your container can create entries from the templates of other providers, your implementation of **CreateEntry** should provide storage for some or all of the properties associated with the created entries.</span></span> <span data-ttu-id="5e465-143">Par exemple, si vous fournissez un espace de stockage pour la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) d'une entrée, vous pouvez générer sa boîte de dialogue détails sans devoir compter sur le fournisseur étranger.</span><span class="sxs-lookup"><span data-stu-id="5e465-143">For example, if you provide storage for an entry's **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property, you can generate its details dialog box without having to depend on the foreign provider.</span></span> 
  
<span data-ttu-id="5e465-144">Si votre conteneur peut créer des entrées qui prennent en charge la propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), votre implémentation de **CreateEntry** doit effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="5e465-144">If your container can create entries that support the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property, your implementation of **CreateEntry** must do the following:</span></span> 
  
1. <span data-ttu-id="5e465-145">Appelez la méthode [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) .</span><span class="sxs-lookup"><span data-stu-id="5e465-145">Call the [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) method.</span></span> <span data-ttu-id="5e465-146">**OpenTemplateID** permet au fournisseur étranger de lier l'entrée à la nouvelle entrée en cours de création.</span><span class="sxs-lookup"><span data-stu-id="5e465-146">**OpenTemplateID** enables the foreign provider's code for the entry to bind to the new entry being created.</span></span> <span data-ttu-id="5e465-147">Les fournisseurs étrangers prennent en charge ce processus de liaison pour maintenir le contrôle des entrées créées à partir de leurs modèles dans les conteneurs de fournisseurs de carnets d'adresses hôtes.</span><span class="sxs-lookup"><span data-stu-id="5e465-147">Foreign providers support this binding process to maintain control over entries created from their templates into the containers of host address book providers.</span></span> 
    
2. <span data-ttu-id="5e465-148">Effectuez toute initialisation nécessaire et remplissez le nouvel objet avec toutes les propriétés de l'entrée dans le fournisseur étranger que l'objet a renvoyé dans le paramètre _lppMAPIPropNew_ à partir de **OpenTemplateID**.</span><span class="sxs-lookup"><span data-stu-id="5e465-148">Perform any necessary initialization, and populate the new object with all of the properties from the entry in the foreign provider that the object returned in the  _lppMAPIPropNew_ parameter from **OpenTemplateID**.</span></span>
    
<span data-ttu-id="5e465-149">Si **OpenTemplateID** réussit, copiez les propriétés vers l'implémentation vers laquelle pointe le paramètre _lppMAPIPropNew_ et non directement vers l'implémentation vers laquelle pointe le paramètre _lpMAPIPropData_ .</span><span class="sxs-lookup"><span data-stu-id="5e465-149">If **OpenTemplateID** succeeds, copy the properties to the implementation pointed to by the  _lppMAPIPropNew_ parameter rather than directly to the implementation pointed to by the  _lpMAPIPropData_ parameter.</span></span> <span data-ttu-id="5e465-150">Initialisez la nouvelle entrée pour une utilisation en mode hors connexion comme vous le feriez pour toute autre entrée à partir d'un fournisseur étranger.</span><span class="sxs-lookup"><span data-stu-id="5e465-150">Initialize the new entry for offline use as you would any other entry from a foreign provider.</span></span> 
  
<span data-ttu-id="5e465-151">Si **OpenTemplateID** renvoie une erreur, **CreateEntry** doit échouer.</span><span class="sxs-lookup"><span data-stu-id="5e465-151">If **OpenTemplateID** returns an error, **CreateEntry** should fail.</span></span> <span data-ttu-id="5e465-152">Ne pas autoriser la création de l'entrée.</span><span class="sxs-lookup"><span data-stu-id="5e465-152">Do not allow the entry to be created.</span></span> <span data-ttu-id="5e465-153">Étant donné que le fournisseur étranger peut faire des hypothèses sur les données de votre fournisseur, ne créez pas d'entrée avec un identificateur de modèle qui n'a pas été correctement lié au fournisseur étranger.</span><span class="sxs-lookup"><span data-stu-id="5e465-153">Because the foreign provider can make assumptions about the data in your provider, do not create an entry with a template identifier that has not been successfully bound to the foreign provider.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5e465-154">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="5e465-154">Notes to callers</span></span>

<span data-ttu-id="5e465-155">Lorsque **CreateEntry** renvoie, vous pouvez ou non accéder immédiatement à l'identificateur d'entrée de la nouvelle entrée.</span><span class="sxs-lookup"><span data-stu-id="5e465-155">When **CreateEntry** returns, you may or may not be able to immediately access the entry identifier for the new entry.</span></span> <span data-ttu-id="5e465-156">Certains fournisseurs de carnets d'adresses ne les rendent pas disponibles tant que vous n'avez pas appelé la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) de la nouvelle entrée.</span><span class="sxs-lookup"><span data-stu-id="5e465-156">Some address book providers do not make it available until after you have called the new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
  
<span data-ttu-id="5e465-157">Bien que les indicateurs de vérification des doublons soient passés en tant que paramètres à **CreateEntry**, l'opération de vérification des doublons ne se produit qu'après l'appel de **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="5e465-157">Although duplicate checking flags are passed as parameters to **CreateEntry**, the duplicate checking operation does not occur until **SaveChanges** is called.</span></span> <span data-ttu-id="5e465-158">Par conséquent, les erreurs connexes telles que MAPI_E_COLLISION, qui indique qu'une tentative de création d'une entrée déjà existante, sont renvoyées par **SaveChanges** plutôt que **CreateEntry**.</span><span class="sxs-lookup"><span data-stu-id="5e465-158">Therefore, related errors such as MAPI_E_COLLISION, which indicates that an attempt was made to create an already existing entry, are returned by **SaveChanges** rather than **CreateEntry**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5e465-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e465-159">See also</span></span>



[<span data-ttu-id="5e465-160">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="5e465-160">IABContainer::CopyEntries</span></span>](iabcontainer-copyentries.md)
  
[<span data-ttu-id="5e465-161">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="5e465-161">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="5e465-162">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="5e465-162">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="5e465-163">Propriété canonique PidTagCreateTemplates</span><span class="sxs-lookup"><span data-stu-id="5e465-163">PidTagCreateTemplates Canonical Property</span></span>](pidtagcreatetemplates-canonical-property.md)
  
[<span data-ttu-id="5e465-164">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="5e465-164">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

