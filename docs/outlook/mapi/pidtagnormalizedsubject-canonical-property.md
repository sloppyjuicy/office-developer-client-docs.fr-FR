---
title: Propriété canonique PidTagNormalizedSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNormalizedSubject
api_type:
- HeaderDef
ms.assetid: 2000e6e8-d908-4814-8093-28f8011250c8
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b5bc464bc5a251579d262f5926193b7f7a731728
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563660"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a><span data-ttu-id="00a84-103">Propriété canonique PidTagNormalizedSubject</span><span class="sxs-lookup"><span data-stu-id="00a84-103">PidTagNormalizedSubject Canonical Property</span></span>

  
  
<span data-ttu-id="00a84-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00a84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00a84-105">Contient l’objet du message avec le préfixe supprimé.</span><span class="sxs-lookup"><span data-stu-id="00a84-105">Contains the message subject with any prefix removed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="00a84-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="00a84-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00a84-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="00a84-107">PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="00a84-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="00a84-108">Identifier:</span></span>  <br/> |<span data-ttu-id="00a84-109">0x0E1D</span><span class="sxs-lookup"><span data-stu-id="00a84-109">0x0E1D</span></span>  <br/> |
|<span data-ttu-id="00a84-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="00a84-110">Data type:</span></span>  <br/> |<span data-ttu-id="00a84-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="00a84-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="00a84-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="00a84-112">Area:</span></span>  <br/> |<span data-ttu-id="00a84-113">E-mail</span><span class="sxs-lookup"><span data-stu-id="00a84-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00a84-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="00a84-114">Remarks</span></span>

<span data-ttu-id="00a84-115">Ces propriétés sont calculées par la banque de messages ou de propriétés **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) et des fournisseurs de transport de la manière suivante.</span><span class="sxs-lookup"><span data-stu-id="00a84-115">These properties are computed by message store or transport providers from the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties in the following manner.</span></span>
  
- <span data-ttu-id="00a84-116">Si la **PR_SUBJECT_PREFIX** est présente et est une sous-chaîne initiale de **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** et les propriétés associées sont définies pour le contenu de **PR_SUBJECT** sans le préfixe.</span><span class="sxs-lookup"><span data-stu-id="00a84-116">If the **PR_SUBJECT_PREFIX** is present and is an initial substring of **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** and associated properties are set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
- <span data-ttu-id="00a84-117">Si **PR_SUBJECT_PREFIX** est présent, mais il n’est pas une sous-chaîne initiale de **PR_SUBJECT**, **PR_SUBJECT_PREFIX** est supprimé et recalculé à partir de **PR_SUBJECT** à l’aide de la règle suivante : si la chaîne contenue dans **PR_SUBJECT** commence par un à trois chiffres suivis par un signe deux-points et un espace, puis la chaîne avec le signe deux-points et blanc devient le préfixe.</span><span class="sxs-lookup"><span data-stu-id="00a84-117">If **PR_SUBJECT_PREFIX** is present, but it is not an initial substring of **PR_SUBJECT**, **PR_SUBJECT_PREFIX** is deleted and recalculated from **PR_SUBJECT** using the following rule: If the string contained in **PR_SUBJECT** begins with one to three non-numeric characters followed by a colon and a space, then the string together with the colon and the blank becomes the prefix.</span></span> <span data-ttu-id="00a84-118">Numéros, les espaces et les signes de ponctuation n’est pas des caractères de préfixe valide.</span><span class="sxs-lookup"><span data-stu-id="00a84-118">Numbers, blanks, and punctuation characters are not valid prefix characters.</span></span> 
    
- <span data-ttu-id="00a84-119">Si **PR_SUBJECT_PREFIX** n’est pas présent, il est calculé à partir de **PR_SUBJECT** à l’aide de la règle décrite à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="00a84-119">If **PR_SUBJECT_PREFIX** is not present, it is calculated from **PR_SUBJECT** using the rule outlined in the previous step.</span></span> <span data-ttu-id="00a84-120">Puis cette propriété est définie pour le contenu de **PR_SUBJECT** sans le préfixe.</span><span class="sxs-lookup"><span data-stu-id="00a84-120">This property then is set to the contents of **PR_SUBJECT** with the prefix removed.</span></span> 
    
 <span data-ttu-id="00a84-121">**Remarque** Lorsque **PR_SUBJECT_PREFIX** est une chaîne vide, **PR_SUBJECT** et cette propriété sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="00a84-121">**Note** When **PR_SUBJECT_PREFIX** is an empty string, **PR_SUBJECT** and this property are the same.</span></span> 
  
<span data-ttu-id="00a84-122">Enfin, cette propriété doit être la partie de **PR_SUBJECT** suit le préfixe.</span><span class="sxs-lookup"><span data-stu-id="00a84-122">Ultimately, this property should be the part of **PR_SUBJECT** following the prefix.</span></span> <span data-ttu-id="00a84-123">S’il n’existe pas de préfixe, cette propriété est identique à **PR_SUBJECT**.</span><span class="sxs-lookup"><span data-stu-id="00a84-123">If there is no prefix, this property becomes the same as **PR_SUBJECT**.</span></span>
  
 <span data-ttu-id="00a84-124">**PR_SUBJECT_PREFIX** et cette propriété doivent être calculées dans le cadre de l’implémentation de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="00a84-124">**PR_SUBJECT_PREFIX** and this property should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="00a84-125">Une application cliente doit demander pas à la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour leurs valeurs jusqu'à ce qu’ils ont été validées par un appel **IMAPIProp::SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="00a84-125">A client application should not prompt the [IMAPIProp::GetProps](imapiprop-getprops.md) method for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="00a84-126">Les propriétés de l’objet sont généralement petites chaînes de moins de 256 caractères, et un fournisseur de magasin de message n’est pas tenu prendre en charge l’interface Object Linking and Embedding (OLE) **IStream** sur eux.</span><span class="sxs-lookup"><span data-stu-id="00a84-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the Object Linking and Embedding (OLE) **IStream** interface on them.</span></span> <span data-ttu-id="00a84-127">Le client doit toujours tentent d’accéder par le biais de l’interface **IMAPIProp** tout d’abord et recourir aux **IStream** que si MAPI_E_NOT_ENOUGH_MEMORY est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="00a84-127">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if MAPI_E_NOT_ENOUGH_MEMORY is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="00a84-128">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="00a84-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="00a84-129">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="00a84-129">Protocol specifications</span></span>

<span data-ttu-id="00a84-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00a84-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00a84-131">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="00a84-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="00a84-132">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00a84-132">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00a84-133">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="00a84-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="00a84-134">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00a84-134">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00a84-135">Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="00a84-135">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="00a84-136">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="00a84-136">Header files</span></span>

<span data-ttu-id="00a84-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00a84-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="00a84-138">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="00a84-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="00a84-139">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="00a84-139">Mapitags.h</span></span>
  
> <span data-ttu-id="00a84-140">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="00a84-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00a84-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00a84-141">See also</span></span>



[<span data-ttu-id="00a84-142">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="00a84-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00a84-143">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="00a84-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00a84-144">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="00a84-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00a84-145">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="00a84-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

