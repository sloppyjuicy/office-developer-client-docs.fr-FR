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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9e6b9ddf37c1db8ea28ae2f82caed2a487e551e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345464"
---
# <a name="pidtagsearchkey-canonical-property"></a><span data-ttu-id="6f497-103">Propriété canonique PidTagSearchKey</span><span class="sxs-lookup"><span data-stu-id="6f497-103">PidTagSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="6f497-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f497-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f497-105">Contient une clé comparable au binaire qui identifie les objets corrélés pour une recherche.</span><span class="sxs-lookup"><span data-stu-id="6f497-105">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6f497-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6f497-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6f497-107">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="6f497-107">PR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="6f497-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6f497-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6f497-109">0x300B</span><span class="sxs-lookup"><span data-stu-id="6f497-109">0x300B</span></span>  <br/> |
|<span data-ttu-id="6f497-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6f497-110">Data type:</span></span>  <br/> |<span data-ttu-id="6f497-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6f497-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6f497-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6f497-112">Area:</span></span>  <br/> |<span data-ttu-id="6f497-113">Propriétés de l’ID</span><span class="sxs-lookup"><span data-stu-id="6f497-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f497-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6f497-114">Remarks</span></span>

<span data-ttu-id="6f497-115">Cette propriété fournit un suivi pour les objets associés, tels que les copies de messages, et facilite la recherche d’occurrences indésirables, telles que des destinataires en double.</span><span class="sxs-lookup"><span data-stu-id="6f497-115">This property provides a trace for related objects, such as message copies, and facilitates finding unwanted occurrences, such as duplicate recipients.</span></span>
  
<span data-ttu-id="6f497-116">MAPI utilise des règles spécifiques pour la construction de clés de recherche pour les destinataires du message.</span><span class="sxs-lookup"><span data-stu-id="6f497-116">MAPI uses specific rules for constructing search keys for message recipients.</span></span> <span data-ttu-id="6f497-117">La clé de recherche est formée en concassant le type d’adresse (en caractères en minuscules), le caractère deux-points « : », l’adresse e-mail sous la forme canonique et le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="6f497-117">The search key is formed by concatenating the address type (in uppercase characters), the colon character ':', the email address in canonical form, and the terminating null character.</span></span> <span data-ttu-id="6f497-118">La forme canonique ici signifie que les adresses sensibles à la cas apparaissent dans le cas correct et que les adresses qui ne sont pas sensibles à la cas sont converties en minuscules.</span><span class="sxs-lookup"><span data-stu-id="6f497-118">Canonical form here means that case-sensitive addresses appear in the correct case, and addresses that are not case-sensitive are converted to uppercase.</span></span> <span data-ttu-id="6f497-119">Ceci est important pour la conservation des corrélations entre les messages.</span><span class="sxs-lookup"><span data-stu-id="6f497-119">This is important in preserving correlations among messages.</span></span>
  
<span data-ttu-id="6f497-120">Pour les objets de message, cette propriété est disponible via la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) immédiatement après la création du message.</span><span class="sxs-lookup"><span data-stu-id="6f497-120">For message objects, this property is available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method immediately following message creation.</span></span> <span data-ttu-id="6f497-121">Pour d’autres objets, il est disponible après le premier appel à la [méthode IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="6f497-121">For other objects, it is available following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="6f497-122">Étant donné que cette propriété est modifiable, il n’est pas fiable de l’obtenir via **GetProps** jusqu’à ce qu’un appel SaveChanges ait engagé des **valeurs définies** ou modifiées par la méthode [IMAPIProp::SetProps.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="6f497-122">Because this property is changeable, it is unreliable to obtain it through **GetProps** until a **SaveChanges** call has committed any values set or changed by the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
  
<span data-ttu-id="6f497-123">Pour les profils, MAPI fournit également une section de profil codée en dur MUID_PROFILE_INSTANCE **,** avec cette propriété comme propriété unique.</span><span class="sxs-lookup"><span data-stu-id="6f497-123">For profiles, MAPI also furnishes a hard-coded profile section named **MUID_PROFILE_INSTANCE**, with this property as its single property.</span></span> <span data-ttu-id="6f497-124">Cette clé est garantie d’être unique parmi tous les profils créés et peut être plus fiable que la propriété **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)), qui peut, par exemple, être supprimée et recréée avec le même nom.</span><span class="sxs-lookup"><span data-stu-id="6f497-124">This key is guaranteed to be unique among all profiles ever created, and can be more reliable than the **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property, which can be, for example, deleted and recreated with the same name.</span></span>
  
<span data-ttu-id="6f497-125">Le tableau suivant récapitule les différences importantes entre les PR_ENTRYID **(** [PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) et cette propriété.</span><span class="sxs-lookup"><span data-stu-id="6f497-125">The following table summarizes important differences among the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and this property.</span></span>
  
|<span data-ttu-id="6f497-126">**Caractéristique**</span><span class="sxs-lookup"><span data-stu-id="6f497-126">**Characteristic**</span></span>|<span data-ttu-id="6f497-127">PR_ENTRYID\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="6f497-127">\*\*\*\*PR_ENTRYID\*\*\*\*</span></span>|<span data-ttu-id="6f497-128">PR_RECORD_KEY\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="6f497-128">\*\*\*\*PR_RECORD_KEY\*\*\*\*</span></span>|<span data-ttu-id="6f497-129">PR_SEARCH_KEY\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="6f497-129">\*\*\*\*PR_SEARCH_KEY\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6f497-130">Obligatoire pour les objets pièce jointe</span><span class="sxs-lookup"><span data-stu-id="6f497-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="6f497-131">Non</span><span class="sxs-lookup"><span data-stu-id="6f497-131">No</span></span>  <br/> |<span data-ttu-id="6f497-132">Oui</span><span class="sxs-lookup"><span data-stu-id="6f497-132">Yes</span></span>  <br/> |<span data-ttu-id="6f497-133">Non</span><span class="sxs-lookup"><span data-stu-id="6f497-133">No</span></span>  <br/> |
|<span data-ttu-id="6f497-134">Obligatoire pour les objets de dossier</span><span class="sxs-lookup"><span data-stu-id="6f497-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="6f497-135">Oui</span><span class="sxs-lookup"><span data-stu-id="6f497-135">Yes</span></span>  <br/> |<span data-ttu-id="6f497-136">Oui</span><span class="sxs-lookup"><span data-stu-id="6f497-136">Yes</span></span>  <br/> |<span data-ttu-id="6f497-137">Non</span><span class="sxs-lookup"><span data-stu-id="6f497-137">No</span></span>  <br/> |
|<span data-ttu-id="6f497-138">Obligatoire sur les objets de la boutique de messages</span><span class="sxs-lookup"><span data-stu-id="6f497-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="6f497-139">Oui</span><span class="sxs-lookup"><span data-stu-id="6f497-139">Yes</span></span>  <br/> |<span data-ttu-id="6f497-140">Oui</span><span class="sxs-lookup"><span data-stu-id="6f497-140">Yes</span></span>  <br/> |<span data-ttu-id="6f497-141">Non</span><span class="sxs-lookup"><span data-stu-id="6f497-141">No</span></span>  <br/> |
|<span data-ttu-id="6f497-142">Obligatoire sur les objets d’état</span><span class="sxs-lookup"><span data-stu-id="6f497-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="6f497-143">Oui</span><span class="sxs-lookup"><span data-stu-id="6f497-143">Yes</span></span>  <br/> |<span data-ttu-id="6f497-144">Non</span><span class="sxs-lookup"><span data-stu-id="6f497-144">No</span></span>  <br/> |<span data-ttu-id="6f497-145">Non</span><span class="sxs-lookup"><span data-stu-id="6f497-145">No</span></span>  <br/> |
|<span data-ttu-id="6f497-146">Créatable par client</span><span class="sxs-lookup"><span data-stu-id="6f497-146">Creatable by client</span></span>  <br/> |<span data-ttu-id="6f497-147">Non</span><span class="sxs-lookup"><span data-stu-id="6f497-147">No</span></span>  <br/> |<span data-ttu-id="6f497-148">Non</span><span class="sxs-lookup"><span data-stu-id="6f497-148">No</span></span>  <br/> |<span data-ttu-id="6f497-149">Oui</span><span class="sxs-lookup"><span data-stu-id="6f497-149">Yes</span></span>  <br/> |
|<span data-ttu-id="6f497-150">Disponible avant **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="6f497-150">Available before **SaveChanges**</span></span> <br/> |<span data-ttu-id="6f497-151">Dépend de l’implémentation du fournisseur</span><span class="sxs-lookup"><span data-stu-id="6f497-151">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="6f497-152">Dépend de l’implémentation du fournisseur</span><span class="sxs-lookup"><span data-stu-id="6f497-152">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="6f497-153">Pour les messages, Oui.</span><span class="sxs-lookup"><span data-stu-id="6f497-153">For messages, Yes.</span></span> <span data-ttu-id="6f497-154">Pour d’autres, cela dépend de l’implémentation du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="6f497-154">For others, It depends on the provider implementation.</span></span>  <br/> |
|<span data-ttu-id="6f497-155">Modifié dans une opération de copie</span><span class="sxs-lookup"><span data-stu-id="6f497-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="6f497-156">Oui</span><span class="sxs-lookup"><span data-stu-id="6f497-156">Yes</span></span>  <br/> |<span data-ttu-id="6f497-157">Oui</span><span class="sxs-lookup"><span data-stu-id="6f497-157">Yes</span></span>  <br/> |<span data-ttu-id="6f497-158">Non</span><span class="sxs-lookup"><span data-stu-id="6f497-158">No</span></span>  <br/> |
|<span data-ttu-id="6f497-159">Modification possible par client après une copie</span><span class="sxs-lookup"><span data-stu-id="6f497-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="6f497-160">Non</span><span class="sxs-lookup"><span data-stu-id="6f497-160">No</span></span>  <br/> |<span data-ttu-id="6f497-161">Non</span><span class="sxs-lookup"><span data-stu-id="6f497-161">No</span></span>  <br/> |<span data-ttu-id="6f497-162">Oui</span><span class="sxs-lookup"><span data-stu-id="6f497-162">Yes</span></span>  <br/> |
|<span data-ttu-id="6f497-163">Unique dans ...</span><span class="sxs-lookup"><span data-stu-id="6f497-163">Unique within ...</span></span>  <br/> |<span data-ttu-id="6f497-164">Monde entier</span><span class="sxs-lookup"><span data-stu-id="6f497-164">Entire world</span></span>  <br/> |<span data-ttu-id="6f497-165">Instance de fournisseur</span><span class="sxs-lookup"><span data-stu-id="6f497-165">Provider instance</span></span>  <br/> |<span data-ttu-id="6f497-166">Monde entier</span><span class="sxs-lookup"><span data-stu-id="6f497-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="6f497-167">Binary comparable (comme avec memcmp)</span><span class="sxs-lookup"><span data-stu-id="6f497-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="6f497-168">No -- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="6f497-168">No -- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="6f497-169">Oui</span><span class="sxs-lookup"><span data-stu-id="6f497-169">Yes</span></span>  <br/> |<span data-ttu-id="6f497-170">Oui</span><span class="sxs-lookup"><span data-stu-id="6f497-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="6f497-171">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6f497-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6f497-172">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="6f497-172">Protocol specifications</span></span>

<span data-ttu-id="6f497-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f497-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f497-174">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="6f497-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6f497-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f497-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f497-176">Gère les objets message et pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="6f497-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="6f497-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6f497-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6f497-178">Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.</span><span class="sxs-lookup"><span data-stu-id="6f497-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6f497-179">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6f497-179">Header files</span></span>

<span data-ttu-id="6f497-180">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6f497-180">Mapidefs.h</span></span>
  
> <span data-ttu-id="6f497-181">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6f497-181">Provides data type definitions.</span></span>
    
<span data-ttu-id="6f497-182">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6f497-182">Mapitags.h</span></span>
  
> <span data-ttu-id="6f497-183">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="6f497-183">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6f497-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f497-184">See also</span></span>



[<span data-ttu-id="6f497-185">Propriété canonique PidTagResponsibility</span><span class="sxs-lookup"><span data-stu-id="6f497-185">PidTagResponsibility Canonical Property</span></span>](pidtagresponsibility-canonical-property.md)
  
[<span data-ttu-id="6f497-186">Propriété canonique PidTagStoreRecordKey</span><span class="sxs-lookup"><span data-stu-id="6f497-186">PidTagStoreRecordKey Canonical Property</span></span>](pidtagstorerecordkey-canonical-property.md)


[<span data-ttu-id="6f497-187">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6f497-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6f497-188">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6f497-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6f497-189">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6f497-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6f497-190">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6f497-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

