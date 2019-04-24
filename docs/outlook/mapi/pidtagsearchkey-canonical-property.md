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
ms.openlocfilehash: 9e6b9ddf37c1db8ea28ae2f82caed2a487e551e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345464"
---
# <a name="pidtagsearchkey-canonical-property"></a><span data-ttu-id="496ad-103">Propriété canonique PidTagSearchKey</span><span class="sxs-lookup"><span data-stu-id="496ad-103">PidTagSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="496ad-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="496ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="496ad-105">Contient une clé comparable binaire qui identifie les objets corrélés pour une recherche.</span><span class="sxs-lookup"><span data-stu-id="496ad-105">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="496ad-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="496ad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="496ad-107">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="496ad-107">PR_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="496ad-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="496ad-108">Identifier:</span></span>  <br/> |<span data-ttu-id="496ad-109">0x300B</span><span class="sxs-lookup"><span data-stu-id="496ad-109">0x300B</span></span>  <br/> |
|<span data-ttu-id="496ad-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="496ad-110">Data type:</span></span>  <br/> |<span data-ttu-id="496ad-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="496ad-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="496ad-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="496ad-112">Area:</span></span>  <br/> |<span data-ttu-id="496ad-113">Propriétés ID</span><span class="sxs-lookup"><span data-stu-id="496ad-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="496ad-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="496ad-114">Remarks</span></span>

<span data-ttu-id="496ad-115">Cette propriété fournit un suivi pour les objets associés, tels que les copies de messages, et facilite la recherche des occurrences indésirables, telles que des destinataires en double.</span><span class="sxs-lookup"><span data-stu-id="496ad-115">This property provides a trace for related objects, such as message copies, and facilitates finding unwanted occurrences, such as duplicate recipients.</span></span>
  
<span data-ttu-id="496ad-116">MAPI utilise des règles spécifiques pour la création de clés de recherche pour les destinataires des messages.</span><span class="sxs-lookup"><span data-stu-id="496ad-116">MAPI uses specific rules for constructing search keys for message recipients.</span></span> <span data-ttu-id="496ad-117">La clé de recherche est formée en concaténant le type d'adresse (en majuscules), le signe deux-points «:», l'adresse de messagerie au format canonique et le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="496ad-117">The search key is formed by concatenating the address type (in uppercase characters), the colon character ':', the email address in canonical form, and the terminating null character.</span></span> <span data-ttu-id="496ad-118">Formulaire canonique cela signifie que les adresses respectant la casse apparaissent dans la casse correcte et que les adresses qui ne respectent pas la casse sont converties en majuscules.</span><span class="sxs-lookup"><span data-stu-id="496ad-118">Canonical form here means that case-sensitive addresses appear in the correct case, and addresses that are not case-sensitive are converted to uppercase.</span></span> <span data-ttu-id="496ad-119">Ceci est important en matière de conservation des corrélations entre les messages.</span><span class="sxs-lookup"><span data-stu-id="496ad-119">This is important in preserving correlations among messages.</span></span>
  
<span data-ttu-id="496ad-120">Pour les objets message, cette propriété est disponible par le biais de la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) immédiatement après la création de messages.</span><span class="sxs-lookup"><span data-stu-id="496ad-120">For message objects, this property is available through the [IMAPIProp::GetProps](imapiprop-getprops.md) method immediately following message creation.</span></span> <span data-ttu-id="496ad-121">Pour les autres objets, elle est disponible après le premier appel à la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="496ad-121">For other objects, it is available following the first call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="496ad-122">Étant donné que cette propriété est modifiable, il est peu fiable de l'obtenir via **GetProps** jusqu'à ce qu'un appel de **SaveChanges** ait validé des valeurs définies ou modifiées par la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="496ad-122">Because this property is changeable, it is unreliable to obtain it through **GetProps** until a **SaveChanges** call has committed any values set or changed by the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
  
<span data-ttu-id="496ad-123">Pour les profils, MAPI fournit également une section de profil codé en dur nommée **MUID_PROFILE_INSTANCE**, avec cette propriété comme propriété unique.</span><span class="sxs-lookup"><span data-stu-id="496ad-123">For profiles, MAPI also furnishes a hard-coded profile section named **MUID_PROFILE_INSTANCE**, with this property as its single property.</span></span> <span data-ttu-id="496ad-124">Cette clé est unique dans tous les profils créés, et peut être plus fiable que la propriété **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)), qui peut être, par exemple, supprimée et recréée avec le même nom.</span><span class="sxs-lookup"><span data-stu-id="496ad-124">This key is guaranteed to be unique among all profiles ever created, and can be more reliable than the **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property, which can be, for example, deleted and recreated with the same name.</span></span>
  
<span data-ttu-id="496ad-125">Le tableau suivant récapitule les différences importantes entre le **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) et cette propriété.</span><span class="sxs-lookup"><span data-stu-id="496ad-125">The following table summarizes important differences among the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), and this property.</span></span>
  
|<span data-ttu-id="496ad-126">**Caractéristique**</span><span class="sxs-lookup"><span data-stu-id="496ad-126">**Characteristic**</span></span>|<span data-ttu-id="496ad-127">PR_ENTRYID \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="496ad-127">\*\*\*\*PR_ENTRYID\*\*\*\*</span></span>|<span data-ttu-id="496ad-128">PR_RECORD_KEY \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="496ad-128">\*\*\*\*PR_RECORD_KEY\*\*\*\*</span></span>|<span data-ttu-id="496ad-129">PR_SEARCH_KEY \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="496ad-129">\*\*\*\*PR_SEARCH_KEY\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="496ad-130">Obligatoire sur les objets Attachment</span><span class="sxs-lookup"><span data-stu-id="496ad-130">Required on attachment objects</span></span>  <br/> |<span data-ttu-id="496ad-131">Non</span><span class="sxs-lookup"><span data-stu-id="496ad-131">No</span></span>  <br/> |<span data-ttu-id="496ad-132">Oui</span><span class="sxs-lookup"><span data-stu-id="496ad-132">Yes</span></span>  <br/> |<span data-ttu-id="496ad-133">Non</span><span class="sxs-lookup"><span data-stu-id="496ad-133">No</span></span>  <br/> |
|<span data-ttu-id="496ad-134">Obligatoire sur les objets Folder</span><span class="sxs-lookup"><span data-stu-id="496ad-134">Required on folder objects</span></span>  <br/> |<span data-ttu-id="496ad-135">Oui</span><span class="sxs-lookup"><span data-stu-id="496ad-135">Yes</span></span>  <br/> |<span data-ttu-id="496ad-136">Oui</span><span class="sxs-lookup"><span data-stu-id="496ad-136">Yes</span></span>  <br/> |<span data-ttu-id="496ad-137">Non</span><span class="sxs-lookup"><span data-stu-id="496ad-137">No</span></span>  <br/> |
|<span data-ttu-id="496ad-138">Obligatoire sur les objets de banque de messages</span><span class="sxs-lookup"><span data-stu-id="496ad-138">Required on message store objects</span></span>  <br/> |<span data-ttu-id="496ad-139">Oui</span><span class="sxs-lookup"><span data-stu-id="496ad-139">Yes</span></span>  <br/> |<span data-ttu-id="496ad-140">Oui</span><span class="sxs-lookup"><span data-stu-id="496ad-140">Yes</span></span>  <br/> |<span data-ttu-id="496ad-141">Non</span><span class="sxs-lookup"><span data-stu-id="496ad-141">No</span></span>  <br/> |
|<span data-ttu-id="496ad-142">Obligatoire sur les objets d'État</span><span class="sxs-lookup"><span data-stu-id="496ad-142">Required on status objects</span></span>  <br/> |<span data-ttu-id="496ad-143">Oui</span><span class="sxs-lookup"><span data-stu-id="496ad-143">Yes</span></span>  <br/> |<span data-ttu-id="496ad-144">Non</span><span class="sxs-lookup"><span data-stu-id="496ad-144">No</span></span>  <br/> |<span data-ttu-id="496ad-145">Non</span><span class="sxs-lookup"><span data-stu-id="496ad-145">No</span></span>  <br/> |
|<span data-ttu-id="496ad-146">Pouvant être créé par le client</span><span class="sxs-lookup"><span data-stu-id="496ad-146">Creatable by client</span></span>  <br/> |<span data-ttu-id="496ad-147">Non</span><span class="sxs-lookup"><span data-stu-id="496ad-147">No</span></span>  <br/> |<span data-ttu-id="496ad-148">Non</span><span class="sxs-lookup"><span data-stu-id="496ad-148">No</span></span>  <br/> |<span data-ttu-id="496ad-149">Oui</span><span class="sxs-lookup"><span data-stu-id="496ad-149">Yes</span></span>  <br/> |
|<span data-ttu-id="496ad-150">Disponible avant **SaveChanges**</span><span class="sxs-lookup"><span data-stu-id="496ad-150">Available before **SaveChanges**</span></span> <br/> |<span data-ttu-id="496ad-151">Dépend de l'implémentation du fournisseur</span><span class="sxs-lookup"><span data-stu-id="496ad-151">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="496ad-152">Dépend de l'implémentation du fournisseur</span><span class="sxs-lookup"><span data-stu-id="496ad-152">Depends on the provider implementation</span></span>  <br/> |<span data-ttu-id="496ad-153">Pour les messages, oui.</span><span class="sxs-lookup"><span data-stu-id="496ad-153">For messages, Yes.</span></span> <span data-ttu-id="496ad-154">Pour d'autres, cela dépend de l'implémentation du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="496ad-154">For others, It depends on the provider implementation.</span></span>  <br/> |
|<span data-ttu-id="496ad-155">Modifié dans une opération de copie</span><span class="sxs-lookup"><span data-stu-id="496ad-155">Changed in a copy operation</span></span>  <br/> |<span data-ttu-id="496ad-156">Oui</span><span class="sxs-lookup"><span data-stu-id="496ad-156">Yes</span></span>  <br/> |<span data-ttu-id="496ad-157">Oui</span><span class="sxs-lookup"><span data-stu-id="496ad-157">Yes</span></span>  <br/> |<span data-ttu-id="496ad-158">Non</span><span class="sxs-lookup"><span data-stu-id="496ad-158">No</span></span>  <br/> |
|<span data-ttu-id="496ad-159">Modifiable par le client après une copie</span><span class="sxs-lookup"><span data-stu-id="496ad-159">Changeable by client after a copy</span></span>  <br/> |<span data-ttu-id="496ad-160">Non</span><span class="sxs-lookup"><span data-stu-id="496ad-160">No</span></span>  <br/> |<span data-ttu-id="496ad-161">Non</span><span class="sxs-lookup"><span data-stu-id="496ad-161">No</span></span>  <br/> |<span data-ttu-id="496ad-162">Oui</span><span class="sxs-lookup"><span data-stu-id="496ad-162">Yes</span></span>  <br/> |
|<span data-ttu-id="496ad-163">Unique au sein de...</span><span class="sxs-lookup"><span data-stu-id="496ad-163">Unique within ...</span></span>  <br/> |<span data-ttu-id="496ad-164">Tout le monde</span><span class="sxs-lookup"><span data-stu-id="496ad-164">Entire world</span></span>  <br/> |<span data-ttu-id="496ad-165">Instance de fournisseur</span><span class="sxs-lookup"><span data-stu-id="496ad-165">Provider instance</span></span>  <br/> |<span data-ttu-id="496ad-166">Tout le monde</span><span class="sxs-lookup"><span data-stu-id="496ad-166">Entire world</span></span>  <br/> |
|<span data-ttu-id="496ad-167">Binaire comparable (comme avec memcmp)</span><span class="sxs-lookup"><span data-stu-id="496ad-167">Binary comparable (as with memcmp)</span></span>  <br/> |<span data-ttu-id="496ad-168">Non--utiliser [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md)</span><span class="sxs-lookup"><span data-stu-id="496ad-168">No -- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)</span></span> <br/> |<span data-ttu-id="496ad-169">Oui</span><span class="sxs-lookup"><span data-stu-id="496ad-169">Yes</span></span>  <br/> |<span data-ttu-id="496ad-170">Oui</span><span class="sxs-lookup"><span data-stu-id="496ad-170">Yes</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="496ad-171">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="496ad-171">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="496ad-172">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="496ad-172">Protocol specifications</span></span>

<span data-ttu-id="496ad-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="496ad-173">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="496ad-174">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="496ad-174">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="496ad-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="496ad-175">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="496ad-176">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="496ad-176">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="496ad-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="496ad-177">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="496ad-178">Spécifie les propriétés et les opérations pour les listes d'utilisateurs, de contacts, de groupes et de ressources.</span><span class="sxs-lookup"><span data-stu-id="496ad-178">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="496ad-179">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="496ad-179">Header files</span></span>

<span data-ttu-id="496ad-180">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="496ad-180">Mapidefs.h</span></span>
  
> <span data-ttu-id="496ad-181">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="496ad-181">Provides data type definitions.</span></span>
    
<span data-ttu-id="496ad-182">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="496ad-182">Mapitags.h</span></span>
  
> <span data-ttu-id="496ad-183">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="496ad-183">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="496ad-184">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="496ad-184">See also</span></span>



[<span data-ttu-id="496ad-185">Propriété canonique PidTagResponsibility</span><span class="sxs-lookup"><span data-stu-id="496ad-185">PidTagResponsibility Canonical Property</span></span>](pidtagresponsibility-canonical-property.md)
  
[<span data-ttu-id="496ad-186">Propriété canonique PidTagStoreRecordKey</span><span class="sxs-lookup"><span data-stu-id="496ad-186">PidTagStoreRecordKey Canonical Property</span></span>](pidtagstorerecordkey-canonical-property.md)


[<span data-ttu-id="496ad-187">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="496ad-187">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="496ad-188">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="496ad-188">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="496ad-189">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="496ad-189">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="496ad-190">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="496ad-190">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

