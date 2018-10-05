---
title: Propriété canonique PidTagSubjectPrefix
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubjectPrefix
api_type:
- COM
ms.assetid: 07fcb881-d873-45bf-b048-30f41d0d8d85
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8257c3c3583072d16e96e6ea9bba4632fc78f9ef
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385647"
---
# <a name="pidtagsubjectprefix-canonical-property"></a><span data-ttu-id="200cc-103">Propriété canonique PidTagSubjectPrefix</span><span class="sxs-lookup"><span data-stu-id="200cc-103">PidTagSubjectPrefix Canonical Property</span></span>

  
  
<span data-ttu-id="200cc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="200cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="200cc-105">Contient un préfixe d’objet qui indique généralement une action sur un message, tel que « TR : » pour le transfert.</span><span class="sxs-lookup"><span data-stu-id="200cc-105">Contains a subject prefix that typically indicates some action on a message, such as "FW: " for forwarding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="200cc-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="200cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="200cc-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span><span class="sxs-lookup"><span data-stu-id="200cc-107">PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W</span></span>  <br/> |
|<span data-ttu-id="200cc-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="200cc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="200cc-109">0x003D</span><span class="sxs-lookup"><span data-stu-id="200cc-109">0x003D</span></span>  <br/> |
|<span data-ttu-id="200cc-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="200cc-110">Data type:</span></span>  <br/> |<span data-ttu-id="200cc-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="200cc-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="200cc-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="200cc-112">Area:</span></span>  <br/> |<span data-ttu-id="200cc-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="200cc-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="200cc-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="200cc-114">Remarks</span></span>

<span data-ttu-id="200cc-115">Ces propriétés sont recommandées sur tous les objets de message.</span><span class="sxs-lookup"><span data-stu-id="200cc-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="200cc-116">Le préfixe d’objet se compose d’un ou plusieurs caractères alphanumériques, suivis par un signe deux-points et un espace (qui font partie du préfixe).</span><span class="sxs-lookup"><span data-stu-id="200cc-116">The subject prefix consists of one or more alphanumeric characters, followed by a colon and a space (which are part of the prefix).</span></span> <span data-ttu-id="200cc-117">Ne doit pas contenir des caractères non alphanumériques avant le signe deux-points.</span><span class="sxs-lookup"><span data-stu-id="200cc-117">It must not contain any nonalphanumeric characters before the colon.</span></span> <span data-ttu-id="200cc-118">Absence d’un préfixe peut être représentée par une chaîne vide ou par cette propriété n’est ne pas défini.</span><span class="sxs-lookup"><span data-stu-id="200cc-118">Absence of a prefix can be represented by an empty string or by this property not being set.</span></span> 
  
<span data-ttu-id="200cc-119">Si ces propriétés sont définies de manière explicite, la chaîne peut être n’importe quelle longueur et utiliser des caractères alphanumériques, mais elle doit correspondre à une sous-chaîne au début de la propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="200cc-119">If these properties are set explicitly, the string can be of any length and use any alphanumeric characters, but it must match a substring at the beginning of the **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="200cc-120">Si ces propriétés ne sont pas définies par l’expéditeur et doivent être calculées, leur contenu est plus restreints.</span><span class="sxs-lookup"><span data-stu-id="200cc-120">If these properties are not set by the sender and must be computed, their contents are more restricted.</span></span> <span data-ttu-id="200cc-121">La règle pour calculer le préfixe est que **PR_SUBJECT** doit commencer par un, deux ou trois lettres (alphabétiques uniquement) suivi par un signe deux-points et un espace.</span><span class="sxs-lookup"><span data-stu-id="200cc-121">The rule for computing the prefix is that **PR_SUBJECT** must begin with one, two, or three letters (alphabetic only) followed by a colon and a space.</span></span> <span data-ttu-id="200cc-122">Si ce une sous-chaîne est trouvée au début du **PR_SUBJECT**, il devient alors la chaîne de ces propriétés (et également reste au début du **PR_SUBJECT**).</span><span class="sxs-lookup"><span data-stu-id="200cc-122">If such a substring is found at the beginning of **PR_SUBJECT**, it then becomes the string for these properties (and also stays at the beginning of **PR_SUBJECT**).</span></span> <span data-ttu-id="200cc-123">Dans le cas contraire, ces propriétés restent non définies.</span><span class="sxs-lookup"><span data-stu-id="200cc-123">Otherwise, these properties remain unset.</span></span> 
  
<span data-ttu-id="200cc-124">Ces propriétés et les **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) doivent être calculée dans le cadre de l’implémentation de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="200cc-124">These properties and **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) should be computed as part of the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) implementation.</span></span> <span data-ttu-id="200cc-125">Un client ne doit pas demander [IMAPIProp::GetProps](imapiprop-getprops.md) pour leurs valeurs jusqu'à ce qu’ils ont été validées par un appel **IMAPIProp::SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="200cc-125">A client should not prompt [IMAPIProp::GetProps](imapiprop-getprops.md) for their values until they have been committed by an **IMAPIProp::SaveChanges** call.</span></span> 
  
<span data-ttu-id="200cc-126">Les propriétés de l’objet sont généralement petites chaînes de moins de 256 caractères, et un fournisseur de magasin de message n’est pas tenu prendre en charge l’interface OLE **IStream** sur eux.</span><span class="sxs-lookup"><span data-stu-id="200cc-126">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the OLE **IStream** interface on them.</span></span> <span data-ttu-id="200cc-127">Un client doit toujours tentent d’accéder par le biais de l’interface **IMAPIProp** tout d’abord et recourir aux **IStream** que si **MAPI_E_NOT_ENOUGH_MEMORY** est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="200cc-127">A client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="200cc-128">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="200cc-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="200cc-129">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="200cc-129">Protocol specifications</span></span>

<span data-ttu-id="200cc-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="200cc-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="200cc-131">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="200cc-131">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="200cc-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="200cc-132">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="200cc-133">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="200cc-133">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="200cc-134">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="200cc-134">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="200cc-135">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="200cc-135">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="200cc-136">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="200cc-136">Header files</span></span>

<span data-ttu-id="200cc-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="200cc-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="200cc-138">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="200cc-138">Provides data type definitions.</span></span>
    
<span data-ttu-id="200cc-139">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="200cc-139">Mapitags.h</span></span>
  
> <span data-ttu-id="200cc-140">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="200cc-140">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="200cc-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="200cc-141">See also</span></span>



[<span data-ttu-id="200cc-142">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="200cc-142">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="200cc-143">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="200cc-143">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="200cc-144">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="200cc-144">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="200cc-145">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="200cc-145">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

