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
ms.openlocfilehash: feb34cdbf8ba917936c3272bcaaf6eff040ddc3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328587"
---
# <a name="pidtagentryid-canonical-property"></a><span data-ttu-id="e9f05-103">Propriété canonique PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="e9f05-103">PidTagEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="e9f05-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9f05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9f05-105">Contient un identificateur d'entrée MAPI utilisé pour ouvrir et modifier les propriétés d'un objet MAPI particulier.</span><span class="sxs-lookup"><span data-stu-id="e9f05-105">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e9f05-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e9f05-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e9f05-107">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e9f05-107">PR_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="e9f05-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="e9f05-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e9f05-109">0x0FFF</span><span class="sxs-lookup"><span data-stu-id="e9f05-109">0x0FFF</span></span>  <br/> |
|<span data-ttu-id="e9f05-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e9f05-110">Data type:</span></span>  <br/> |<span data-ttu-id="e9f05-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e9f05-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e9f05-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e9f05-112">Area:</span></span>  <br/> |<span data-ttu-id="e9f05-113">Propriétés ID</span><span class="sxs-lookup"><span data-stu-id="e9f05-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9f05-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e9f05-114">Remarks</span></span>

<span data-ttu-id="e9f05-115">Cette propriété identifie un objet pour **OpenEntry** à instancier et permet d'accéder à toutes ses propriétés via l'interface dérivée appropriée de **IMAPIProp**.</span><span class="sxs-lookup"><span data-stu-id="e9f05-115">This property identifies an object for **OpenEntry** to instantiate and provides access to all of its properties through the appropriate derived interface of **IMAPIProp**.</span></span> 
  
<span data-ttu-id="e9f05-116">Cette propriété est l'une des propriétés d'adresse de base pour tous les utilisateurs de messagerie.</span><span class="sxs-lookup"><span data-stu-id="e9f05-116">This property is one of the base address properties for all messaging users.</span></span> 
  
<span data-ttu-id="e9f05-117">Cette propriété peut contenir un identificateur à long ou à court terme.</span><span class="sxs-lookup"><span data-stu-id="e9f05-117">This property can contain either a long-term or a short-term identifier.</span></span> <span data-ttu-id="e9f05-118">Les identificateurs à court terme sont plus faciles et plus rapides à créer, mais sont limités en termes de portée et de durée, généralement à la session et à la station de travail en cours.</span><span class="sxs-lookup"><span data-stu-id="e9f05-118">Short-term identifiers are easier and faster to construct, but are limited in their scope and duration, typically to the current session and workstation.</span></span> <span data-ttu-id="e9f05-119">Elles sont généralement utilisées pour les objets de nature temporaire, tels que les lignes de tableau ou les entrées de boîte de dialogue, puis abandonnées.</span><span class="sxs-lookup"><span data-stu-id="e9f05-119">They are commonly used for objects of a temporary nature, such as table rows or dialog box entries, and then abandoned.</span></span> <span data-ttu-id="e9f05-120">Les identificateurs à long terme sont utilisés pour les objets d'un caractère plus large et durable.</span><span class="sxs-lookup"><span data-stu-id="e9f05-120">Long-term identifiers are used for objects of a more wide-ranging and long-lasting nature.</span></span> 
  
<span data-ttu-id="e9f05-121">Cette propriété est toujours disponible par le biais de la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) qui suit le premier appel à la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="e9f05-121">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="e9f05-122">Certains fournisseurs de services peuvent le mettre à disposition immédiatement après l'instanciation.</span><span class="sxs-lookup"><span data-stu-id="e9f05-122">Some service providers can make it available immediately after instantiation.</span></span> <span data-ttu-id="e9f05-123">Le fournisseur doit toujours renvoyer un identificateur d'entrée à long terme à partir de **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="e9f05-123">The provider must always return a long-term entry identifier from **GetProps**.</span></span> <span data-ttu-id="e9f05-124">Par conséquent, pour convertir un identificateur à court terme en un identificateur à long terme, il suffit d'ouvrir l'objet et d'obtenir sa propriété par le biais de **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="e9f05-124">Therefore, to convert a short-term identifier to long-term, simply open the object and get its this property through **GetProps**.</span></span> 
  
<span data-ttu-id="e9f05-125">Le tableau suivant récapitule les différences importantes entre cette propriété, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) et **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e9f05-125">The following table summarizes important differences among this property, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)).</span></span> 
  
|<span data-ttu-id="e9f05-126">**Caractéristique**</span><span class="sxs-lookup"><span data-stu-id="e9f05-126">**Characteristic**</span></span>|<span data-ttu-id="e9f05-127">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="e9f05-127">**PR_ENTRYID**</span></span>|<span data-ttu-id="e9f05-128">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="e9f05-128">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="e9f05-129">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="e9f05-129">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e9f05-130">Obligatoire sur les objets Attachment</span><span class="sxs-lookup"><span data-stu-id="e9f05-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="e9f05-131">Non</span><span class="sxs-lookup"><span data-stu-id="e9f05-131">No</span></span>  <br/> |<span data-ttu-id="e9f05-132">Oui</span><span class="sxs-lookup"><span data-stu-id="e9f05-132">Yes</span></span>  <br/> |<span data-ttu-id="e9f05-133">Non</span><span class="sxs-lookup"><span data-stu-id="e9f05-133">No</span></span>  <br/> |
|<span data-ttu-id="e9f05-134">Obligatoire sur les objets Folder</span><span class="sxs-lookup"><span data-stu-id="e9f05-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="e9f05-135">Oui</span><span class="sxs-lookup"><span data-stu-id="e9f05-135">Yes</span></span>  <br/> |<span data-ttu-id="e9f05-136">Oui</span><span class="sxs-lookup"><span data-stu-id="e9f05-136">Yes</span></span>  <br/> |<span data-ttu-id="e9f05-137">Non</span><span class="sxs-lookup"><span data-stu-id="e9f05-137">No</span></span>  <br/> |
|<span data-ttu-id="e9f05-138">Obligatoire sur les objets de banque de messages</span><span class="sxs-lookup"><span data-stu-id="e9f05-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="e9f05-139">Oui</span><span class="sxs-lookup"><span data-stu-id="e9f05-139">Yes</span></span>  <br/> |<span data-ttu-id="e9f05-140">Oui</span><span class="sxs-lookup"><span data-stu-id="e9f05-140">Yes</span></span>  <br/> |<span data-ttu-id="e9f05-141">Non</span><span class="sxs-lookup"><span data-stu-id="e9f05-141">No</span></span>  <br/> |
|<span data-ttu-id="e9f05-142">Obligatoire sur les objets d'État</span><span class="sxs-lookup"><span data-stu-id="e9f05-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="e9f05-143">Oui</span><span class="sxs-lookup"><span data-stu-id="e9f05-143">Yes</span></span>  <br/> |<span data-ttu-id="e9f05-144">Non</span><span class="sxs-lookup"><span data-stu-id="e9f05-144">No</span></span>  <br/> |<span data-ttu-id="e9f05-145">Non</span><span class="sxs-lookup"><span data-stu-id="e9f05-145">No</span></span>  <br/> |
|<span data-ttu-id="e9f05-146">Créé par le client</span><span class="sxs-lookup"><span data-stu-id="e9f05-146">Created by client</span></span>  <br/> |<span data-ttu-id="e9f05-147">Non</span><span class="sxs-lookup"><span data-stu-id="e9f05-147">No</span></span>  <br/> |<span data-ttu-id="e9f05-148">Non</span><span class="sxs-lookup"><span data-stu-id="e9f05-148">No</span></span>  <br/> |<span data-ttu-id="e9f05-149">Oui</span><span class="sxs-lookup"><span data-stu-id="e9f05-149">Yes</span></span>  <br/> |
|<span data-ttu-id="e9f05-150">Disponible avant l'appel à **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="e9f05-150">Available before call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="e9f05-151">Dépend de l'implémentation du fournisseur</span><span class="sxs-lookup"><span data-stu-id="e9f05-151">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="e9f05-152">Dépend de l'implémentation du fournisseur</span><span class="sxs-lookup"><span data-stu-id="e9f05-152">Depends on provider implementation</span></span>  <br/> |<span data-ttu-id="e9f05-153">Pour les messages, oui.</span><span class="sxs-lookup"><span data-stu-id="e9f05-153">For messages, Yes.</span></span> <span data-ttu-id="e9f05-154">Pour d'autres, dépend de l'implémentation du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e9f05-154">For others, depends on provider implementation.</span></span>  <br/> |
|<span data-ttu-id="e9f05-155">Modifié dans une opération de copie</span><span class="sxs-lookup"><span data-stu-id="e9f05-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="e9f05-156">Oui</span><span class="sxs-lookup"><span data-stu-id="e9f05-156">Yes</span></span>  <br/> |<span data-ttu-id="e9f05-157">Oui</span><span class="sxs-lookup"><span data-stu-id="e9f05-157">Yes</span></span>  <br/> |<span data-ttu-id="e9f05-158">Non</span><span class="sxs-lookup"><span data-stu-id="e9f05-158">No</span></span>  <br/> |
|<span data-ttu-id="e9f05-159">Modifiable par le client après une copie</span><span class="sxs-lookup"><span data-stu-id="e9f05-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="e9f05-160">Non</span><span class="sxs-lookup"><span data-stu-id="e9f05-160">No</span></span>  <br/> |<span data-ttu-id="e9f05-161">Non</span><span class="sxs-lookup"><span data-stu-id="e9f05-161">No</span></span>  <br/> |<span data-ttu-id="e9f05-162">Oui</span><span class="sxs-lookup"><span data-stu-id="e9f05-162">Yes</span></span>  <br/> |
|<span data-ttu-id="e9f05-163">Unique dans</span><span class="sxs-lookup"><span data-stu-id="e9f05-163">Unique within</span></span>  <br/> |<span data-ttu-id="e9f05-164">Tout le monde</span><span class="sxs-lookup"><span data-stu-id="e9f05-164">Entire world</span></span>  <br/> |<span data-ttu-id="e9f05-165">Instance de fournisseur</span><span class="sxs-lookup"><span data-stu-id="e9f05-165">Provider instance</span></span>  <br/> |<span data-ttu-id="e9f05-166">Tout le monde</span><span class="sxs-lookup"><span data-stu-id="e9f05-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="e9f05-167">Binaire comparable (comme avec memcmp)</span><span class="sxs-lookup"><span data-stu-id="e9f05-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="e9f05-168">Ne pas utiliser [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="e9f05-168">No use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="e9f05-169">Oui</span><span class="sxs-lookup"><span data-stu-id="e9f05-169">Yes</span></span>  <br/> |<span data-ttu-id="e9f05-170">Oui</span><span class="sxs-lookup"><span data-stu-id="e9f05-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e9f05-171">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="e9f05-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e9f05-172">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="e9f05-172">Protocol specifications</span></span>

<span data-ttu-id="e9f05-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9f05-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9f05-174">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="e9f05-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e9f05-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9f05-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9f05-176">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="e9f05-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="e9f05-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9f05-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9f05-178">Spécifie les propriétés et les opérations pour les listes d'utilisateurs, de contacts, de groupes et de ressources.</span><span class="sxs-lookup"><span data-stu-id="e9f05-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="e9f05-179">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9f05-179">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9f05-180">ConVertit des conventions de messagerie standard Internet en objets message.</span><span class="sxs-lookup"><span data-stu-id="e9f05-180">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="e9f05-181">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9f05-181">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9f05-182">Gère l'ordre et le flux de transfert de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="e9f05-182">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="e9f05-183">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9f05-183">[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9f05-184">Gère la récupération des listes d'autorisations de dossier stockées sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="e9f05-184">Handles the retrieval of folder permission lists that are stored on the server.</span></span>
    
<span data-ttu-id="e9f05-185">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9f05-185">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9f05-186">Spécifie les méthodes de connexion et de configuration des boîtes aux lettres en tant que délégués, ainsi que les interactions avec les objets message et Calendar lorsqu'ils agissent pour le compte d'un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e9f05-186">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
<span data-ttu-id="e9f05-187">[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9f05-187">[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9f05-188">Spécifie le schéma et les méthodes qui sont utilisés pour demander des informations de disponibilité pour les utilisateurs et les ressources.</span><span class="sxs-lookup"><span data-stu-id="e9f05-188">Specifies the schema and methods that are used to request availability information for users and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e9f05-189">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="e9f05-189">Header files</span></span>

<span data-ttu-id="e9f05-190">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e9f05-190">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9f05-191">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e9f05-191">Provides data type definitions.</span></span>
    
<span data-ttu-id="e9f05-192">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e9f05-192">Mapitags.h</span></span>
  
> <span data-ttu-id="e9f05-193">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="e9f05-193">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9f05-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9f05-194">See also</span></span>



[<span data-ttu-id="e9f05-195">Propriété canonique PidTagStoreEntryId</span><span class="sxs-lookup"><span data-stu-id="e9f05-195">PidTagStoreEntryId Canonical Property</span></span>](pidtagstoreentryid-canonical-property.md)


[<span data-ttu-id="e9f05-196">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e9f05-196">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9f05-197">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e9f05-197">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9f05-198">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e9f05-198">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9f05-199">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e9f05-199">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

