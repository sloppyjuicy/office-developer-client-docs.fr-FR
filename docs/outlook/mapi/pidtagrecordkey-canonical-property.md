---
title: Propriété canonique PidTagRecordKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecordKey
api_type:
- COM
ms.assetid: a12fb9a2-799d-4112-b26c-4b2854c47cc2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7a3ae7db1fb97e97f7d0939b67f139af62477bf7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401698"
---
# <a name="pidtagrecordkey-canonical-property"></a><span data-ttu-id="ed944-103">Propriété canonique PidTagRecordKey</span><span class="sxs-lookup"><span data-stu-id="ed944-103">PidTagRecordKey Canonical Property</span></span>

  
  
<span data-ttu-id="ed944-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed944-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed944-105">Contient un identificateur unique comparable binaire pour un objet spécifique.</span><span class="sxs-lookup"><span data-stu-id="ed944-105">Contains a unique binary-comparable identifier for a specific object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed944-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ed944-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ed944-107">PR_RECORD_KEY</span><span class="sxs-lookup"><span data-stu-id="ed944-107">PR_RECORD_KEY</span></span>  <br/> |
|<span data-ttu-id="ed944-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ed944-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ed944-109">0x0FF9</span><span class="sxs-lookup"><span data-stu-id="ed944-109">0x0FF9</span></span>  <br/> |
|<span data-ttu-id="ed944-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ed944-110">Data type:</span></span>  <br/> |<span data-ttu-id="ed944-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ed944-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ed944-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ed944-112">Area:</span></span>  <br/> |<span data-ttu-id="ed944-113">Propriétés ID</span><span class="sxs-lookup"><span data-stu-id="ed944-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed944-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ed944-114">Remarks</span></span>

<span data-ttu-id="ed944-115">Cette propriété facilite la localisation des références à un objet, telles que la recherche de sa ligne dans une table des matières.</span><span class="sxs-lookup"><span data-stu-id="ed944-115">This property facilitates locating references to an object, such as finding its row in a contents table.</span></span> <span data-ttu-id="ed944-116">Cette propriété ne peut pas être utilisée pour ouvrir un objet ; Utilisez l’identificateur d’entrée à cet effet.</span><span class="sxs-lookup"><span data-stu-id="ed944-116">This property cannot be used to open an object; use the entry identifier for that purpose.</span></span>
  
<span data-ttu-id="ed944-117">Un sous-objet de pièce jointe doit être identifiée dans un message par cette propriété.</span><span class="sxs-lookup"><span data-stu-id="ed944-117">An attachment subobject should be uniquely identified within a message by this property.</span></span> <span data-ttu-id="ed944-118">Cet identificateur est la seule caractéristique de pièce jointe garantie reste le même une fois que le message est fermé et rouverte.</span><span class="sxs-lookup"><span data-stu-id="ed944-118">This identifier is the only attachment characteristic guaranteed to stay the same after the message is closed and reopened.</span></span> <span data-ttu-id="ed944-119">Le fournisseur de banque doit conserver cette propriété entre les sessions pour s’assurer de cette garantie.</span><span class="sxs-lookup"><span data-stu-id="ed944-119">The store provider must preserve this property across sessions to ensure this guarantee.</span></span>
  
<span data-ttu-id="ed944-120">Pour les dossiers, cette propriété contient une clé utilisée dans la table de hiérarchie de dossier.</span><span class="sxs-lookup"><span data-stu-id="ed944-120">For folders, this property contains a key used in the folder hierarchy table.</span></span> <span data-ttu-id="ed944-121">Il s’agit généralement de la même valeur que celles fournies par la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ed944-121">Typically this is the same value as that provided by the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="ed944-122">Pour les banques de messages, cette propriété est identique à la propriété **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ed944-122">For message stores, this property is identical to the **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="ed944-123">Dans un objet de banque de messages, cette propriété doit être unique parmi tous les fournisseurs de magasins.</span><span class="sxs-lookup"><span data-stu-id="ed944-123">In a message store object, this property should be unique across all store providers.</span></span> <span data-ttu-id="ed944-124">Pour ce faire consiste à combiner la valeur de la propriété **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) pour le magasin (unique pour ce type de fournisseur) avec une structure [GUID](guid.md) ou une autre valeur unique dans le magasin de message spécifique.</span><span class="sxs-lookup"><span data-stu-id="ed944-124">One way to do this is to combine the value of the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for the store (unique to that provider type) with a [GUID](guid.md) structure or other value unique to the specific message store.</span></span> 
  
<span data-ttu-id="ed944-125">Cette propriété est toujours disponible par le biais de la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) du premier appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) qui suit.</span><span class="sxs-lookup"><span data-stu-id="ed944-125">This property is always available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="ed944-126">Certains fournisseurs peuvent rendre disponibles immédiatement après l’instanciation.</span><span class="sxs-lookup"><span data-stu-id="ed944-126">Some providers can make it available immediately after instantiation.</span></span> 
  
<span data-ttu-id="ed944-127">Un client ou fournisseur de services comparer les valeurs de cette propriété à l’aide de memcmp.</span><span class="sxs-lookup"><span data-stu-id="ed944-127">A client or service provider can compare values from this property by using memcmp.</span></span> <span data-ttu-id="ed944-128">Il n’est pas possible, pour les valeurs d’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ed944-128">This is not possible for entry identifier values.</span></span> <span data-ttu-id="ed944-129">Toutefois, cette propriété est garantie être uniques au sein de la banque de messages même ou ; conteneur de carnets d’adresses deux objets provenant de différents conteneurs peuvent avoir la même valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="ed944-129">However, this property is guaranteed to be unique within the same message store or address book container; two objects from different containers can have the same value of this property.</span></span>
  
<span data-ttu-id="ed944-130">Une distinction entre les clés de recherche et d’enregistrement est la clé d’enregistrement spécifique à l’objet, tandis que la clé de recherche peut être copiée à d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="ed944-130">One distinction between the record and search keys is that the record key is specific to the object, whereas the search key can be copied to other objects.</span></span> <span data-ttu-id="ed944-131">Par exemple, deux copies de l’objet peuvent avoir la même valeur de **clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)), mais doivent avoir des valeurs différentes pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="ed944-131">For example, two copies of the object can have the same **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) value but must have different values for this property.</span></span>
  
<span data-ttu-id="ed944-132">Le tableau suivant récapitule les différences importantes entre **PR_ENTRYID**, **clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) et cette propriété.</span><span class="sxs-lookup"><span data-stu-id="ed944-132">The following table summarizes important differences among **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) and this property.</span></span> 
  
|<span data-ttu-id="ed944-133">**Caractéristique**</span><span class="sxs-lookup"><span data-stu-id="ed944-133">**Characteristic**</span></span>|<span data-ttu-id="ed944-134">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="ed944-134">**PR_ENTRYID**</span></span>|<span data-ttu-id="ed944-135">**PR_RECORD_KEY**</span><span class="sxs-lookup"><span data-stu-id="ed944-135">**PR_RECORD_KEY**</span></span>|<span data-ttu-id="ed944-136">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="ed944-136">**PR_SEARCH_KEY**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ed944-137">Requis sur les objets attachment</span><span class="sxs-lookup"><span data-stu-id="ed944-137">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="ed944-138">Non</span><span class="sxs-lookup"><span data-stu-id="ed944-138">No</span></span>  <br/> |<span data-ttu-id="ed944-139">Oui</span><span class="sxs-lookup"><span data-stu-id="ed944-139">Yes</span></span>  <br/> |<span data-ttu-id="ed944-140">Non</span><span class="sxs-lookup"><span data-stu-id="ed944-140">No</span></span>  <br/> |
|<span data-ttu-id="ed944-141">Requis sur les objets de dossier</span><span class="sxs-lookup"><span data-stu-id="ed944-141">Required on folder objects</span></span>  <br/> |<span data-ttu-id="ed944-142">Oui</span><span class="sxs-lookup"><span data-stu-id="ed944-142">Yes</span></span>  <br/> |<span data-ttu-id="ed944-143">Oui</span><span class="sxs-lookup"><span data-stu-id="ed944-143">Yes</span></span>  <br/> |<span data-ttu-id="ed944-144">Non</span><span class="sxs-lookup"><span data-stu-id="ed944-144">No</span></span>  <br/> |
|<span data-ttu-id="ed944-145">Requis sur les objets de banque de messages</span><span class="sxs-lookup"><span data-stu-id="ed944-145">Required on message store objects</span></span>  <br/> |<span data-ttu-id="ed944-146">Oui</span><span class="sxs-lookup"><span data-stu-id="ed944-146">Yes</span></span>  <br/> |<span data-ttu-id="ed944-147">Oui</span><span class="sxs-lookup"><span data-stu-id="ed944-147">Yes</span></span>  <br/> |<span data-ttu-id="ed944-148">Non</span><span class="sxs-lookup"><span data-stu-id="ed944-148">No</span></span>  <br/> |
|<span data-ttu-id="ed944-149">Requis sur les objets d’état</span><span class="sxs-lookup"><span data-stu-id="ed944-149">Required on status objects</span></span>  <br/> |<span data-ttu-id="ed944-150">Oui</span><span class="sxs-lookup"><span data-stu-id="ed944-150">Yes</span></span>  <br/> |<span data-ttu-id="ed944-151">Non</span><span class="sxs-lookup"><span data-stu-id="ed944-151">No</span></span>  <br/> |<span data-ttu-id="ed944-152">Non</span><span class="sxs-lookup"><span data-stu-id="ed944-152">No</span></span>  <br/> |
|<span data-ttu-id="ed944-153">Qui peut être créé par client</span><span class="sxs-lookup"><span data-stu-id="ed944-153">Creatable by client</span></span>  <br/> |<span data-ttu-id="ed944-154">Non</span><span class="sxs-lookup"><span data-stu-id="ed944-154">No</span></span>  <br/> |<span data-ttu-id="ed944-155">Non</span><span class="sxs-lookup"><span data-stu-id="ed944-155">No</span></span>  <br/> |<span data-ttu-id="ed944-156">Oui</span><span class="sxs-lookup"><span data-stu-id="ed944-156">Yes</span></span>  <br/> |
|<span data-ttu-id="ed944-157">Disponibles avant un appel à **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="ed944-157">Available before a call to **SaveChanges**</span></span> <br/> |<span data-ttu-id="ed944-158">Peut-être</span><span class="sxs-lookup"><span data-stu-id="ed944-158">Maybe</span></span>  <br/> |<span data-ttu-id="ed944-159">Peut-être</span><span class="sxs-lookup"><span data-stu-id="ed944-159">Maybe</span></span>  <br/> |<span data-ttu-id="ed944-160">Messages d’autres personnes Oui peut-être</span><span class="sxs-lookup"><span data-stu-id="ed944-160">Messages Yes Others Maybe</span></span>  <br/> |
|<span data-ttu-id="ed944-161">Modification dans une opération de copie</span><span class="sxs-lookup"><span data-stu-id="ed944-161">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="ed944-162">Oui</span><span class="sxs-lookup"><span data-stu-id="ed944-162">Yes</span></span>  <br/> |<span data-ttu-id="ed944-163">Oui</span><span class="sxs-lookup"><span data-stu-id="ed944-163">Yes</span></span>  <br/> |<span data-ttu-id="ed944-164">Non</span><span class="sxs-lookup"><span data-stu-id="ed944-164">No</span></span>  <br/> |
|<span data-ttu-id="ed944-165">Modifiable par un client après une copie</span><span class="sxs-lookup"><span data-stu-id="ed944-165">Changeable by a client after a copy</span></span>  <br/> |<span data-ttu-id="ed944-166">Non</span><span class="sxs-lookup"><span data-stu-id="ed944-166">No</span></span>  <br/> |<span data-ttu-id="ed944-167">Non</span><span class="sxs-lookup"><span data-stu-id="ed944-167">No</span></span>  <br/> |<span data-ttu-id="ed944-168">Oui</span><span class="sxs-lookup"><span data-stu-id="ed944-168">Yes</span></span>  <br/> |
|<span data-ttu-id="ed944-169">Unique au sein de...</span><span class="sxs-lookup"><span data-stu-id="ed944-169">Unique within ...</span></span>  <br/> |<span data-ttu-id="ed944-170">Monde entier</span><span class="sxs-lookup"><span data-stu-id="ed944-170">Entire world</span></span>  <br/> |<span data-ttu-id="ed944-171">Instance de fournisseur</span><span class="sxs-lookup"><span data-stu-id="ed944-171">Provider instance</span></span>  <br/> |<span data-ttu-id="ed944-172">Monde entier</span><span class="sxs-lookup"><span data-stu-id="ed944-172">Entire world</span></span>  <br/> |
|<span data-ttu-id="ed944-173">Binaire comparable (comme avec memcmp)</span><span class="sxs-lookup"><span data-stu-id="ed944-173">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="ed944-174">No : utilisez **IMAPISupport :: CompareEntryIDs**</span><span class="sxs-lookup"><span data-stu-id="ed944-174">No -- use **IMAPISupport:: CompareEntryIDs**</span></span> <br/> |<span data-ttu-id="ed944-175">Oui</span><span class="sxs-lookup"><span data-stu-id="ed944-175">Yes</span></span>  <br/> |<span data-ttu-id="ed944-176">Oui</span><span class="sxs-lookup"><span data-stu-id="ed944-176">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ed944-177">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ed944-177">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ed944-178">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="ed944-178">Protocol specifications</span></span>

<span data-ttu-id="ed944-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed944-179">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed944-180">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="ed944-180">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ed944-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed944-181">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed944-182">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="ed944-182">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="ed944-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ed944-183">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ed944-184">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="ed944-184">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ed944-185">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ed944-185">Header files</span></span>

<span data-ttu-id="ed944-186">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ed944-186">Mapidefs.h</span></span>
  
> <span data-ttu-id="ed944-187">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ed944-187">Provides data type definitions.</span></span>
    
<span data-ttu-id="ed944-188">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ed944-188">Mapitags.h</span></span>
  
> <span data-ttu-id="ed944-189">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="ed944-189">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed944-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed944-190">See also</span></span>



[<span data-ttu-id="ed944-191">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ed944-191">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ed944-192">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ed944-192">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ed944-193">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ed944-193">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ed944-194">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ed944-194">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

