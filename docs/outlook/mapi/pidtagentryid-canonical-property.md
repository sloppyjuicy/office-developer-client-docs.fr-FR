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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 971462b9e85878677b57ec7b53fe46aa64db6dba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785990"
---
# <a name="pidtagentryid-canonical-property"></a><span data-ttu-id="430de-103">Propriété canonique PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="430de-103">PidTagEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="430de-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="430de-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="430de-105">Contient un identificateur d’entrée MAPI utilisé pour ouvrir et modifier les propriétés d’un objet MAPI particulier.</span><span class="sxs-lookup"><span data-stu-id="430de-105">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="430de-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="430de-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="430de-107">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="430de-107">PR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="430de-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="430de-108">Identifier:</span></span>  <br/> |<span data-ttu-id="430de-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="430de-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="430de-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="430de-110">Data type:</span></span>  <br/> |<span data-ttu-id="430de-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="430de-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="430de-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="430de-112">Area:</span></span>  <br/> |<span data-ttu-id="430de-113">Propriétés ID</span><span class="sxs-lookup"><span data-stu-id="430de-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="430de-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="430de-114">Remarks</span></span>

<span data-ttu-id="430de-115">Cette propriété identifie un objet pour **OpenEntry** instancier et donne accès à toutes ses propriétés via l’interface dérivée appropriée de **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="430de-115">This property identifies an object for **OpenEntry** to instantiate and provides access to all of its properties through the appropriate derived interface of **IMAPIProp**.</span></span> 
  
<span data-ttu-id="430de-116">Cette propriété est une des propriétés d’adresse de base pour tous les utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="430de-116">This property is one of the base address properties for all messaging users.</span></span> 
  
<span data-ttu-id="430de-117">Cette propriété peut contenir une à long terme ou un identificateur à court terme.</span><span class="sxs-lookup"><span data-stu-id="430de-117">This property can contain either a long-term or a short-term identifier.</span></span> <span data-ttu-id="430de-118">Identificateurs à court terme sont plus facile et plus rapide de construction, mais sont limités dans leur étendue et la durée, généralement pour la session en cours et la station de travail.</span><span class="sxs-lookup"><span data-stu-id="430de-118">Short-term identifiers are easier and faster to construct, but are limited in their scope and duration, typically to the current session and workstation.</span></span> <span data-ttu-id="430de-119">Ils sont couramment utilisés pour les objets de nature temporaire, telles que les lignes ou les entrées de boîte de dialogue et puis abandonnés.</span><span class="sxs-lookup"><span data-stu-id="430de-119">They are commonly used for objects of a temporary nature, such as table rows or dialog box entries, and then abandoned.</span></span> <span data-ttu-id="430de-120">Identificateurs à long terme sont utilisés pour les objets de nature plus vaste et durables.</span><span class="sxs-lookup"><span data-stu-id="430de-120">Long-term identifiers are used for objects of a more wide-ranging and long-lasting nature.</span></span> 
  
<span data-ttu-id="430de-121">Cette propriété est toujours disponible par le biais de la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) du premier appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) qui suit.</span><span class="sxs-lookup"><span data-stu-id="430de-121">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="430de-122">Certains fournisseurs de services peuvent rendre disponibles immédiatement après l’instanciation.</span><span class="sxs-lookup"><span data-stu-id="430de-122">Some service providers can make it available immediately after instantiation.</span></span> <span data-ttu-id="430de-123">Le fournisseur doit toujours retourner un identificateur d’entrée à long terme de **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="430de-123">The provider must always return a long-term entry identifier from **GetProps**.</span></span> <span data-ttu-id="430de-124">Par conséquent, pour convertir un identificateur à court terme à long terme, simplement ouvrir l’objet et ses cette propriété via **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="430de-124">Therefore, to convert a short-term identifier to long-term, simply open the object and get its this property through **GetProps**.</span></span> 
  
<span data-ttu-id="430de-125">Le tableau suivant récapitule les différences importantes entre cette propriété, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) et **clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="430de-125">The following table summarizes important differences among this property, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span></span> 
  
|<span data-ttu-id="430de-126">**Caractéristique**</span><span class="sxs-lookup"><span data-stu-id="430de-126">**Characteristic**</span></span>|<span data-ttu-id="430de-127">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="430de-127">**PR_ENTRYID**</span></span>|<span data-ttu-id="430de-128">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="430de-128">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="430de-129">**CLÉ PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="430de-129">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="430de-130">Requis sur les objets attachment</span><span class="sxs-lookup"><span data-stu-id="430de-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="430de-131">Non</span><span class="sxs-lookup"><span data-stu-id="430de-131">No</span></span>  <br/> |<span data-ttu-id="430de-132">Oui</span><span class="sxs-lookup"><span data-stu-id="430de-132">Yes</span></span>  <br/> |<span data-ttu-id="430de-133">Non</span><span class="sxs-lookup"><span data-stu-id="430de-133">No</span></span>  <br/> |
|<span data-ttu-id="430de-134">Requis sur les objets de dossier</span><span class="sxs-lookup"><span data-stu-id="430de-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="430de-135">Oui</span><span class="sxs-lookup"><span data-stu-id="430de-135">Yes</span></span>  <br/> |<span data-ttu-id="430de-136">Oui</span><span class="sxs-lookup"><span data-stu-id="430de-136">Yes</span></span>  <br/> |<span data-ttu-id="430de-137">Non</span><span class="sxs-lookup"><span data-stu-id="430de-137">No</span></span>  <br/> |
|<span data-ttu-id="430de-138">Requis sur les objets de banque de messages</span><span class="sxs-lookup"><span data-stu-id="430de-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="430de-139">Oui</span><span class="sxs-lookup"><span data-stu-id="430de-139">Yes</span></span>  <br/> |<span data-ttu-id="430de-140">Oui</span><span class="sxs-lookup"><span data-stu-id="430de-140">Yes</span></span>  <br/> |<span data-ttu-id="430de-141">Non</span><span class="sxs-lookup"><span data-stu-id="430de-141">No</span></span>  <br/> |
|<span data-ttu-id="430de-142">Requis sur les objets d’état</span><span class="sxs-lookup"><span data-stu-id="430de-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="430de-143">Oui</span><span class="sxs-lookup"><span data-stu-id="430de-143">Yes</span></span>  <br/> |<span data-ttu-id="430de-144">Non</span><span class="sxs-lookup"><span data-stu-id="430de-144">No</span></span>  <br/> |<span data-ttu-id="430de-145">Non</span><span class="sxs-lookup"><span data-stu-id="430de-145">No</span></span>  <br/> |
|<span data-ttu-id="430de-146">Créé par client</span><span class="sxs-lookup"><span data-stu-id="430de-146">Created by client</span></span>  <br/> |<span data-ttu-id="430de-147">Non</span><span class="sxs-lookup"><span data-stu-id="430de-147">No</span></span>  <br/> |<span data-ttu-id="430de-148">Non</span><span class="sxs-lookup"><span data-stu-id="430de-148">No</span></span>  <br/> |<span data-ttu-id="430de-149">Oui</span><span class="sxs-lookup"><span data-stu-id="430de-149">Yes</span></span>  <br/> |
|<span data-ttu-id="430de-150">Avant l’appel à **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="430de-150">Available before call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="430de-151">Dépend de l’implémentation du fournisseur</span><span class="sxs-lookup"><span data-stu-id="430de-151">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="430de-152">Dépend de l’implémentation du fournisseur</span><span class="sxs-lookup"><span data-stu-id="430de-152">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="430de-153">Pour les messages, Oui.</span><span class="sxs-lookup"><span data-stu-id="430de-153">For messages, Yes.</span></span> <span data-ttu-id="430de-154">Pour d’autres personnes, dépend de l’implémentation du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="430de-154">For others, depends on provider implementation.</span></span>  <br/> |
|<span data-ttu-id="430de-155">Modification dans une opération de copie</span><span class="sxs-lookup"><span data-stu-id="430de-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="430de-156">Oui</span><span class="sxs-lookup"><span data-stu-id="430de-156">Yes</span></span>  <br/> |<span data-ttu-id="430de-157">Oui</span><span class="sxs-lookup"><span data-stu-id="430de-157">Yes</span></span>  <br/> |<span data-ttu-id="430de-158">Non</span><span class="sxs-lookup"><span data-stu-id="430de-158">No</span></span>  <br/> |
|<span data-ttu-id="430de-159">Modifiable par client après une copie</span><span class="sxs-lookup"><span data-stu-id="430de-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="430de-160">Non</span><span class="sxs-lookup"><span data-stu-id="430de-160">No</span></span>  <br/> |<span data-ttu-id="430de-161">Non</span><span class="sxs-lookup"><span data-stu-id="430de-161">No</span></span>  <br/> |<span data-ttu-id="430de-162">Oui</span><span class="sxs-lookup"><span data-stu-id="430de-162">Yes</span></span>  <br/> |
|<span data-ttu-id="430de-163">Unique dans</span><span class="sxs-lookup"><span data-stu-id="430de-163">Unique within</span></span>  <br/> |<span data-ttu-id="430de-164">Monde entier</span><span class="sxs-lookup"><span data-stu-id="430de-164">Entire world</span></span>  <br/> |<span data-ttu-id="430de-165">Instance de fournisseur</span><span class="sxs-lookup"><span data-stu-id="430de-165">Provider instance</span></span>  <br/> |<span data-ttu-id="430de-166">Monde entier</span><span class="sxs-lookup"><span data-stu-id="430de-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="430de-167">Binaire comparable (comme avec memcmp)</span><span class="sxs-lookup"><span data-stu-id="430de-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="430de-168">Aucune utilisation [IMAPISupport :: CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="430de-168">No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="430de-169">Oui</span><span class="sxs-lookup"><span data-stu-id="430de-169">Yes</span></span>  <br/> |<span data-ttu-id="430de-170">Oui</span><span class="sxs-lookup"><span data-stu-id="430de-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="430de-171">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="430de-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="430de-172">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="430de-172">Protocol specifications</span></span>

<span data-ttu-id="430de-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="430de-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="430de-174">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="430de-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="430de-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="430de-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="430de-176">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="430de-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="430de-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="430de-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="430de-178">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="430de-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="430de-179">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="430de-179">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="430de-180">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="430de-180">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="430de-181">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="430de-181">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="430de-182">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="430de-182">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="430de-183">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="430de-183">[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="430de-184">Gère la récupération des listes d’autorisations de dossier sont stockés sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="430de-184">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="430de-185">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="430de-185">[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="430de-186">Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les objets de messagerie et de calendrier lorsqu’ils agissent au nom d’un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="430de-186">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="430de-187">[[MS-OXWAVLS]](http://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="430de-187">[[MS-OXWAVLS]](http://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="430de-188">Spécifie le schéma et les méthodes qui sont utilisées pour demander les informations de disponibilité des utilisateurs et des ressources.</span><span class="sxs-lookup"><span data-stu-id="430de-188">Specifies the schema and methods that are used to request availability information for users and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="430de-189">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="430de-189">Header files</span></span>

<span data-ttu-id="430de-190">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="430de-190">Mapidefs.h</span></span>
  
> <span data-ttu-id="430de-191">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="430de-191">Provides data type definitions.</span></span>
    
<span data-ttu-id="430de-192">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="430de-192">Mapitags.h</span></span>
  
> <span data-ttu-id="430de-193">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="430de-193">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="430de-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="430de-194">See also</span></span>



[<span data-ttu-id="430de-195">Propriété canonique PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="430de-195">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="430de-196">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="430de-196">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="430de-197">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="430de-197">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="430de-198">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="430de-198">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="430de-199">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="430de-199">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

