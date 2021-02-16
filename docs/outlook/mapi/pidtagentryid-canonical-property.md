---
title: Propriété canonique PidTagEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEntryId
api_type:
- HeaderDef
ms.assetid: ca02e873-c2d2-4d58-8df8-c05fbcdc8fba
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: feb34cdbf8ba917936c3272bcaaf6eff040ddc3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328587"
---
# <a name="pidtagentryid-canonical-property"></a><span data-ttu-id="7f7ac-103">Propriété canonique PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="7f7ac-103">PidTagEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="7f7ac-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f7ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f7ac-105">Contient un identificateur d’entrée MAPI utilisé pour ouvrir et modifier les propriétés d’un objet MAPI particulier.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-105">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f7ac-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="7f7ac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7f7ac-107">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="7f7ac-107">PR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="7f7ac-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="7f7ac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7f7ac-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="7f7ac-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="7f7ac-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="7f7ac-110">Data type:</span></span>  <br/> |<span data-ttu-id="7f7ac-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="7f7ac-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="7f7ac-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="7f7ac-112">Area:</span></span>  <br/> |<span data-ttu-id="7f7ac-113">Propriétés de l’ID</span><span class="sxs-lookup"><span data-stu-id="7f7ac-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f7ac-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="7f7ac-114">Remarks</span></span>

<span data-ttu-id="7f7ac-115">Cette propriété identifie un objet pour **qu’OpenEntry** s’insère et donne accès à toutes ses propriétés via l’interface dérivée appropriée **d’IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-115">This property identifies an object for **OpenEntry** to instantiate and provides access to all of its properties through the appropriate derived interface of **IMAPIProp**.</span></span> 
  
<span data-ttu-id="7f7ac-116">Cette propriété est l’une des propriétés d’adresse de base de tous les utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-116">This property is one of the base address properties for all messaging users.</span></span> 
  
<span data-ttu-id="7f7ac-117">Cette propriété peut contenir un identificateur à long terme ou à court terme.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-117">This property can contain either a long-term or a short-term identifier.</span></span> <span data-ttu-id="7f7ac-118">Les identificateurs à court terme sont plus faciles et plus rapides à construire, mais sont limités en termes d’étendue et de durée, généralement à la session et à la station de travail actuelles.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-118">Short-term identifiers are easier and faster to construct, but are limited in their scope and duration, typically to the current session and workstation.</span></span> <span data-ttu-id="7f7ac-119">Ils sont couramment utilisés pour les objets de nature temporaire, tels que les lignes de tableau ou les entrées de boîte de dialogue, puis abandonnés.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-119">They are commonly used for objects of a temporary nature, such as table rows or dialog box entries, and then abandoned.</span></span> <span data-ttu-id="7f7ac-120">Les identificateurs à long terme sont utilisés pour les objets de nature plus large et de longue durée.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-120">Long-term identifiers are used for objects of a more wide-ranging and long-lasting nature.</span></span> 
  
<span data-ttu-id="7f7ac-121">Cette propriété est toujours disponible via la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) après le premier appel à la méthode [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="7f7ac-121">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="7f7ac-122">Certains fournisseurs de services peuvent le rendre disponible immédiatement après l’ins instantiation.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-122">Some service providers can make it available immediately after instantiation.</span></span> <span data-ttu-id="7f7ac-123">Le fournisseur doit toujours renvoyer un identificateur d’entrée à long terme à partir **de GetProps**.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-123">The provider must always return a long-term entry identifier from **GetProps**.</span></span> <span data-ttu-id="7f7ac-124">Par conséquent, pour convertir un identificateur à court terme en identificateur à long terme, ouvrez simplement l’objet et obtenez sa propriété via **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-124">Therefore, to convert a short-term identifier to long-term, simply open the object and get its this property through **GetProps**.</span></span> 
  
<span data-ttu-id="7f7ac-125">Le tableau suivant récapitule les différences importantes entre cette propriété, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) et **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7f7ac-125">The following table summarizes important differences among this property, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span></span> 
  
|<span data-ttu-id="7f7ac-126">**Caractéristique**</span><span class="sxs-lookup"><span data-stu-id="7f7ac-126">**Characteristic**</span></span>|<span data-ttu-id="7f7ac-127">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="7f7ac-127">**PR_ENTRYID**</span></span>|<span data-ttu-id="7f7ac-128">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="7f7ac-128">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="7f7ac-129">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="7f7ac-129">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7f7ac-130">Obligatoire pour les objets pièce jointe</span><span class="sxs-lookup"><span data-stu-id="7f7ac-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="7f7ac-131">Non</span><span class="sxs-lookup"><span data-stu-id="7f7ac-131">No</span></span>  <br/> |<span data-ttu-id="7f7ac-132">Oui</span><span class="sxs-lookup"><span data-stu-id="7f7ac-132">Yes</span></span>  <br/> |<span data-ttu-id="7f7ac-133">Non</span><span class="sxs-lookup"><span data-stu-id="7f7ac-133">No</span></span>  <br/> |
|<span data-ttu-id="7f7ac-134">Obligatoire pour les objets de dossier</span><span class="sxs-lookup"><span data-stu-id="7f7ac-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="7f7ac-135">Oui</span><span class="sxs-lookup"><span data-stu-id="7f7ac-135">Yes</span></span>  <br/> |<span data-ttu-id="7f7ac-136">Oui</span><span class="sxs-lookup"><span data-stu-id="7f7ac-136">Yes</span></span>  <br/> |<span data-ttu-id="7f7ac-137">Non</span><span class="sxs-lookup"><span data-stu-id="7f7ac-137">No</span></span>  <br/> |
|<span data-ttu-id="7f7ac-138">Obligatoire sur les objets de la boutique de messages</span><span class="sxs-lookup"><span data-stu-id="7f7ac-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="7f7ac-139">Oui</span><span class="sxs-lookup"><span data-stu-id="7f7ac-139">Yes</span></span>  <br/> |<span data-ttu-id="7f7ac-140">Oui</span><span class="sxs-lookup"><span data-stu-id="7f7ac-140">Yes</span></span>  <br/> |<span data-ttu-id="7f7ac-141">Non</span><span class="sxs-lookup"><span data-stu-id="7f7ac-141">No</span></span>  <br/> |
|<span data-ttu-id="7f7ac-142">Obligatoire sur les objets d’état</span><span class="sxs-lookup"><span data-stu-id="7f7ac-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="7f7ac-143">Oui</span><span class="sxs-lookup"><span data-stu-id="7f7ac-143">Yes</span></span>  <br/> |<span data-ttu-id="7f7ac-144">Non</span><span class="sxs-lookup"><span data-stu-id="7f7ac-144">No</span></span>  <br/> |<span data-ttu-id="7f7ac-145">Non</span><span class="sxs-lookup"><span data-stu-id="7f7ac-145">No</span></span>  <br/> |
|<span data-ttu-id="7f7ac-146">Créé par le client</span><span class="sxs-lookup"><span data-stu-id="7f7ac-146">Created by client</span></span>  <br/> |<span data-ttu-id="7f7ac-147">Non</span><span class="sxs-lookup"><span data-stu-id="7f7ac-147">No</span></span>  <br/> |<span data-ttu-id="7f7ac-148">Non</span><span class="sxs-lookup"><span data-stu-id="7f7ac-148">No</span></span>  <br/> |<span data-ttu-id="7f7ac-149">Oui</span><span class="sxs-lookup"><span data-stu-id="7f7ac-149">Yes</span></span>  <br/> |
|<span data-ttu-id="7f7ac-150">Disponible avant l’appel **de SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="7f7ac-150">Available before call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="7f7ac-151">Dépend de l’implémentation du fournisseur</span><span class="sxs-lookup"><span data-stu-id="7f7ac-151">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="7f7ac-152">Dépend de l’implémentation du fournisseur</span><span class="sxs-lookup"><span data-stu-id="7f7ac-152">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="7f7ac-153">Pour les messages, Oui.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-153">For messages, Yes.</span></span> <span data-ttu-id="7f7ac-154">Pour d’autres, dépend de l’implémentation du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-154">For others, depends on provider implementation.</span></span>  <br/> |
|<span data-ttu-id="7f7ac-155">Modifié dans une opération de copie</span><span class="sxs-lookup"><span data-stu-id="7f7ac-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="7f7ac-156">Oui</span><span class="sxs-lookup"><span data-stu-id="7f7ac-156">Yes</span></span>  <br/> |<span data-ttu-id="7f7ac-157">Oui</span><span class="sxs-lookup"><span data-stu-id="7f7ac-157">Yes</span></span>  <br/> |<span data-ttu-id="7f7ac-158">Non</span><span class="sxs-lookup"><span data-stu-id="7f7ac-158">No</span></span>  <br/> |
|<span data-ttu-id="7f7ac-159">Modification possible par client après une copie</span><span class="sxs-lookup"><span data-stu-id="7f7ac-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="7f7ac-160">Non</span><span class="sxs-lookup"><span data-stu-id="7f7ac-160">No</span></span>  <br/> |<span data-ttu-id="7f7ac-161">Non</span><span class="sxs-lookup"><span data-stu-id="7f7ac-161">No</span></span>  <br/> |<span data-ttu-id="7f7ac-162">Oui</span><span class="sxs-lookup"><span data-stu-id="7f7ac-162">Yes</span></span>  <br/> |
|<span data-ttu-id="7f7ac-163">Unique dans</span><span class="sxs-lookup"><span data-stu-id="7f7ac-163">Unique within</span></span>  <br/> |<span data-ttu-id="7f7ac-164">Monde entier</span><span class="sxs-lookup"><span data-stu-id="7f7ac-164">Entire world</span></span>  <br/> |<span data-ttu-id="7f7ac-165">Instance du fournisseur</span><span class="sxs-lookup"><span data-stu-id="7f7ac-165">Provider instance</span></span>  <br/> |<span data-ttu-id="7f7ac-166">Monde entier</span><span class="sxs-lookup"><span data-stu-id="7f7ac-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="7f7ac-167">Comparaison binaire (comme avec memcmp)</span><span class="sxs-lookup"><span data-stu-id="7f7ac-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="7f7ac-168">No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="7f7ac-168">No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="7f7ac-169">Oui</span><span class="sxs-lookup"><span data-stu-id="7f7ac-169">Yes</span></span>  <br/> |<span data-ttu-id="7f7ac-170">Oui</span><span class="sxs-lookup"><span data-stu-id="7f7ac-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7f7ac-171">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="7f7ac-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7f7ac-172">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="7f7ac-172">Protocol specifications</span></span>

<span data-ttu-id="7f7ac-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f7ac-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f7ac-174">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7f7ac-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f7ac-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f7ac-176">Gère les objets message et pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="7f7ac-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f7ac-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f7ac-178">Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="7f7ac-179">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f7ac-179">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f7ac-180">Convertit des conventions de messagerie standard Internet en objets de message.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-180">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="7f7ac-181">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f7ac-181">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f7ac-182">Gère l’ordre et le flux des transferts de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-182">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="7f7ac-183">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f7ac-183">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f7ac-184">Gère la récupération des listes d’autorisations de dossier stockées sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-184">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="7f7ac-185">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f7ac-185">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f7ac-186">Spécifie les méthodes de connexion et de configuration des boîtes aux lettres en tant que délégués, ainsi que les interactions avec les objets de message et de calendrier lorsqu’ils agissent pour le compte d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-186">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="7f7ac-187">[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f7ac-187">[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f7ac-188">Spécifie le schéma et les méthodes utilisés pour demander des informations de disponibilité pour les utilisateurs et les ressources.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-188">Specifies the schema and methods that are used to request availability information for users and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7f7ac-189">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="7f7ac-189">Header files</span></span>

<span data-ttu-id="7f7ac-190">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7f7ac-190">Mapidefs.h</span></span>
  
> <span data-ttu-id="7f7ac-191">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-191">Provides data type definitions.</span></span>
    
<span data-ttu-id="7f7ac-192">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7f7ac-192">Mapitags.h</span></span>
  
> <span data-ttu-id="7f7ac-193">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="7f7ac-193">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f7ac-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f7ac-194">See also</span></span>



[<span data-ttu-id="7f7ac-195">Propriété canonique PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="7f7ac-195">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="7f7ac-196">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="7f7ac-196">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7f7ac-197">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="7f7ac-197">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7f7ac-198">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="7f7ac-198">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7f7ac-199">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="7f7ac-199">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

