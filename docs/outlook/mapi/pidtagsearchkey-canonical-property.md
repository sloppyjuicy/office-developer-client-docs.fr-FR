---
title: Propriété canonique PidTagSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fcab369a-a1f4-4425-a272-e35046914a4d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 169afc3b8cf982c4767802542b900ae80822cd01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786747"
---
# <a name="pidtagsearchkey-canonical-property"></a><span data-ttu-id="3b0f9-103">Propriété canonique PidTagSearchKey</span><span class="sxs-lookup"><span data-stu-id="3b0f9-103">PidTagSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="3b0f9-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3b0f9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3b0f9-105">Contient une clé comparable binaire qui identifie les objets en corrélation pour une recherche.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-105">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3b0f9-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3b0f9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3b0f9-107">CLÉ PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="3b0f9-107">PR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="3b0f9-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3b0f9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3b0f9-109">0x300B</span><span class="sxs-lookup"><span data-stu-id="3b0f9-109">0x300B</span></span>  <br/> |
|<span data-ttu-id="3b0f9-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3b0f9-110">Data type:</span></span>  <br/> |<span data-ttu-id="3b0f9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3b0f9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3b0f9-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="3b0f9-112">Area:</span></span>  <br/> |<span data-ttu-id="3b0f9-113">Propriétés ID</span><span class="sxs-lookup"><span data-stu-id="3b0f9-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b0f9-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3b0f9-114">Remarks</span></span>

<span data-ttu-id="3b0f9-115">Cette propriété fournit un suivi pour les objets associés, tels que des copies de messages et facilite la recherche des occurrences indésirables, tels que les destinataires en double.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-115">This property provides a trace for related objects, such as message copies, and facilitates finding unwanted occurrences, such as duplicate recipients.</span></span>
  
<span data-ttu-id="3b0f9-116">MAPI utilise des règles spécifiques pour construire les clés de recherche pour les destinataires du message.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-116">MAPI uses specific rules for constructing search keys for message recipients.</span></span> <span data-ttu-id="3b0f9-117">La clé de recherche est formée en concaténant le type d’adresse (en majuscules), le signe deux-points ' :', l’adresse de messagerie dans le formulaire canonique et le caractère de fin null.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-117">The search key is formed by concatenating the address type (in uppercase characters), the colon character ':', the email address in canonical form, and the terminating null character.</span></span> <span data-ttu-id="3b0f9-118">Forme canonique ici signifie que la casse adresses apparaissent dans la casse, et les adresses qui ne respectent pas la casse sont converties en majuscules.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-118">Canonical form here means that case-sensitive addresses appear in the correct case, and addresses that are not case-sensitive are converted to uppercase.</span></span> <span data-ttu-id="3b0f9-119">Il est important de conserver les corrélations entre les messages.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-119">This is important in preserving correlations among messages.</span></span>
  
<span data-ttu-id="3b0f9-120">Pour les objets de message, cette propriété est disponible par le biais de la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) immédiatement après la création du message.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-120">For message objects, this property is available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method immediately following message creation.</span></span> <span data-ttu-id="3b0f9-121">Pour les autres objets, il est disponible après le premier appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="3b0f9-121">For other objects, it is available following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="3b0f9-122">Étant donné que cette propriété est modifiable, il n’est pas fiable pour obtenir par le biais de **GetProps** jusqu'à ce qu’un appel de **SaveChanges** a validé les valeurs défini ou modifié par la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="3b0f9-122">Because this property is changeable, it is unreliable to obtain it through **GetProps** until a **SaveChanges** call has committed any values set or changed by the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
  
<span data-ttu-id="3b0f9-123">Pour les profils, MAPI fournit également une section de profil codé en dur nommée **MUID_PROFILE_INSTANCE**, avec cette propriété en tant que sa propriété unique.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-123">For profiles, MAPI also furnishes a hard-coded profile section named **MUID_PROFILE_INSTANCE**, with this property as its single property.</span></span> <span data-ttu-id="3b0f9-124">Cette clé est garantie unique parmi tous les profils jamais créés et peut être plus fiable que la propriété **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)), qui peut être, par exemple, suppression et recréation portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-124">This key is guaranteed to be unique among all profiles ever created, and can be more reliable than the **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property, which can be, for example, deleted and recreated with the same name.</span></span>
  
<span data-ttu-id="3b0f9-125">Le tableau suivant récapitule les différences importantes entre le **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) et cette propriété.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-125">The following table summarizes important differences among the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and this property.</span></span>
  
|<span data-ttu-id="3b0f9-126">**Caractéristique**</span><span class="sxs-lookup"><span data-stu-id="3b0f9-126">**Characteristic**</span></span>|<span data-ttu-id="3b0f9-127">PR_ENTRYID \*\*\*</span><span class="sxs-lookup"><span data-stu-id="3b0f9-127">****PR_ENTRYID****</span></span>|<span data-ttu-id="3b0f9-128">PR_RECORD_KEY \*\*\*</span><span class="sxs-lookup"><span data-stu-id="3b0f9-128">****PR_RECORD_KEY****</span></span>|<span data-ttu-id="3b0f9-129">CLÉ PR_SEARCH_KEY \*\*\*</span><span class="sxs-lookup"><span data-stu-id="3b0f9-129">****PR_SEARCH_KEY****</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3b0f9-130">Requis sur les objets attachment</span><span class="sxs-lookup"><span data-stu-id="3b0f9-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="3b0f9-131">Non</span><span class="sxs-lookup"><span data-stu-id="3b0f9-131">No</span></span>  <br/> |<span data-ttu-id="3b0f9-132">Oui</span><span class="sxs-lookup"><span data-stu-id="3b0f9-132">Yes</span></span>  <br/> |<span data-ttu-id="3b0f9-133">Non</span><span class="sxs-lookup"><span data-stu-id="3b0f9-133">No</span></span>  <br/> |
|<span data-ttu-id="3b0f9-134">Requis sur les objets de dossier</span><span class="sxs-lookup"><span data-stu-id="3b0f9-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="3b0f9-135">Oui</span><span class="sxs-lookup"><span data-stu-id="3b0f9-135">Yes</span></span>  <br/> |<span data-ttu-id="3b0f9-136">Oui</span><span class="sxs-lookup"><span data-stu-id="3b0f9-136">Yes</span></span>  <br/> |<span data-ttu-id="3b0f9-137">Non</span><span class="sxs-lookup"><span data-stu-id="3b0f9-137">No</span></span>  <br/> |
|<span data-ttu-id="3b0f9-138">Requis sur les objets de banque de messages</span><span class="sxs-lookup"><span data-stu-id="3b0f9-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="3b0f9-139">Oui</span><span class="sxs-lookup"><span data-stu-id="3b0f9-139">Yes</span></span>  <br/> |<span data-ttu-id="3b0f9-140">Oui</span><span class="sxs-lookup"><span data-stu-id="3b0f9-140">Yes</span></span>  <br/> |<span data-ttu-id="3b0f9-141">Non</span><span class="sxs-lookup"><span data-stu-id="3b0f9-141">No</span></span>  <br/> |
|<span data-ttu-id="3b0f9-142">Requis sur les objets d’état</span><span class="sxs-lookup"><span data-stu-id="3b0f9-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="3b0f9-143">Oui</span><span class="sxs-lookup"><span data-stu-id="3b0f9-143">Yes</span></span>  <br/> |<span data-ttu-id="3b0f9-144">Non</span><span class="sxs-lookup"><span data-stu-id="3b0f9-144">No</span></span>  <br/> |<span data-ttu-id="3b0f9-145">Non</span><span class="sxs-lookup"><span data-stu-id="3b0f9-145">No</span></span>  <br/> |
|<span data-ttu-id="3b0f9-146">Qui peut être créé par client</span><span class="sxs-lookup"><span data-stu-id="3b0f9-146">Creatable by client</span></span>  <br/> |<span data-ttu-id="3b0f9-147">Non</span><span class="sxs-lookup"><span data-stu-id="3b0f9-147">No</span></span>  <br/> |<span data-ttu-id="3b0f9-148">Non</span><span class="sxs-lookup"><span data-stu-id="3b0f9-148">No</span></span>  <br/> |<span data-ttu-id="3b0f9-149">Oui</span><span class="sxs-lookup"><span data-stu-id="3b0f9-149">Yes</span></span>  <br/> |
|<span data-ttu-id="3b0f9-150">Avant de **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="3b0f9-150">Available before **SaveChanges**</span></span> <br/> |<span data-ttu-id="3b0f9-151">Dépend de l’implémentation du fournisseur</span><span class="sxs-lookup"><span data-stu-id="3b0f9-151">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="3b0f9-152">Dépend de l’implémentation du fournisseur</span><span class="sxs-lookup"><span data-stu-id="3b0f9-152">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="3b0f9-153">Pour les messages, Oui.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-153">For messages, Yes.</span></span> <span data-ttu-id="3b0f9-154">Pour d’autres personnes, il dépend de l’implémentation du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-154">For others, It depends on the provider implementation.</span></span>  <br/> |
|<span data-ttu-id="3b0f9-155">Modification dans une opération de copie</span><span class="sxs-lookup"><span data-stu-id="3b0f9-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="3b0f9-156">Oui</span><span class="sxs-lookup"><span data-stu-id="3b0f9-156">Yes</span></span>  <br/> |<span data-ttu-id="3b0f9-157">Oui</span><span class="sxs-lookup"><span data-stu-id="3b0f9-157">Yes</span></span>  <br/> |<span data-ttu-id="3b0f9-158">Non</span><span class="sxs-lookup"><span data-stu-id="3b0f9-158">No</span></span>  <br/> |
|<span data-ttu-id="3b0f9-159">Modifiable par client après une copie</span><span class="sxs-lookup"><span data-stu-id="3b0f9-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="3b0f9-160">Non</span><span class="sxs-lookup"><span data-stu-id="3b0f9-160">No</span></span>  <br/> |<span data-ttu-id="3b0f9-161">Non</span><span class="sxs-lookup"><span data-stu-id="3b0f9-161">No</span></span>  <br/> |<span data-ttu-id="3b0f9-162">Oui</span><span class="sxs-lookup"><span data-stu-id="3b0f9-162">Yes</span></span>  <br/> |
|<span data-ttu-id="3b0f9-163">Unique au sein de...</span><span class="sxs-lookup"><span data-stu-id="3b0f9-163">Unique within ...</span></span>  <br/> |<span data-ttu-id="3b0f9-164">Monde entier</span><span class="sxs-lookup"><span data-stu-id="3b0f9-164">Entire world</span></span>  <br/> |<span data-ttu-id="3b0f9-165">Instance de fournisseur</span><span class="sxs-lookup"><span data-stu-id="3b0f9-165">Provider instance</span></span>  <br/> |<span data-ttu-id="3b0f9-166">Monde entier</span><span class="sxs-lookup"><span data-stu-id="3b0f9-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="3b0f9-167">Binaire comparable (comme avec memcmp)</span><span class="sxs-lookup"><span data-stu-id="3b0f9-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="3b0f9-168">No : utilisez [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="3b0f9-168">No -- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="3b0f9-169">Oui</span><span class="sxs-lookup"><span data-stu-id="3b0f9-169">Yes</span></span>  <br/> |<span data-ttu-id="3b0f9-170">Oui</span><span class="sxs-lookup"><span data-stu-id="3b0f9-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="3b0f9-171">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3b0f9-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3b0f9-172">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="3b0f9-172">Protocol specifications</span></span>

<span data-ttu-id="3b0f9-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b0f9-173">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b0f9-174">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3b0f9-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b0f9-175">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b0f9-176">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="3b0f9-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3b0f9-177">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3b0f9-178">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3b0f9-179">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3b0f9-179">Header files</span></span>

<span data-ttu-id="3b0f9-180">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3b0f9-180">Mapidefs.h</span></span>
  
> <span data-ttu-id="3b0f9-181">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-181">Provides data type definitions.</span></span>
    
<span data-ttu-id="3b0f9-182">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="3b0f9-182">Mapitags.h</span></span>
  
> <span data-ttu-id="3b0f9-183">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="3b0f9-183">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3b0f9-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b0f9-184">See also</span></span>



[<span data-ttu-id="3b0f9-185">Propriété canonique PidTagResponsibility</span><span class="sxs-lookup"><span data-stu-id="3b0f9-185">PidTagResponsibility Canonical Property</span></span>](pidtagresponsibility-canonical-property.md)
  
[<span data-ttu-id="3b0f9-186">Propriété canonique PidTagStoreRecordKey</span><span class="sxs-lookup"><span data-stu-id="3b0f9-186">PidTagStoreRecordKey Canonical Property</span></span>](pidtagstorerecordkey-canonical-property.md)


[<span data-ttu-id="3b0f9-187">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3b0f9-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3b0f9-188">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3b0f9-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3b0f9-189">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3b0f9-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3b0f9-190">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="3b0f9-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

