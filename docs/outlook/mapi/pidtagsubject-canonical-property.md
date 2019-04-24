---
title: Propriété canonique PidTagSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubject
api_type:
- COM
ms.assetid: aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0cf9e9f8c10f8d27bd174b8b6f2bf19812dc269d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339255"
---
# <a name="pidtagsubject-canonical-property"></a><span data-ttu-id="56aa2-103">Propriété canonique PidTagSubject</span><span class="sxs-lookup"><span data-stu-id="56aa2-103">PidTagSubject Canonical Property</span></span>

  
  
<span data-ttu-id="56aa2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56aa2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56aa2-105">Contient l'objet complet d'un message.</span><span class="sxs-lookup"><span data-stu-id="56aa2-105">Contains the full subject of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="56aa2-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="56aa2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="56aa2-107">PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="56aa2-107">PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="56aa2-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="56aa2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="56aa2-109">0x0037</span><span class="sxs-lookup"><span data-stu-id="56aa2-109">0x0037</span></span>  <br/> |
|<span data-ttu-id="56aa2-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="56aa2-110">Data type:</span></span>  <br/> |<span data-ttu-id="56aa2-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="56aa2-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="56aa2-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="56aa2-112">Area:</span></span>  <br/> |<span data-ttu-id="56aa2-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="56aa2-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56aa2-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="56aa2-114">Remarks</span></span>

<span data-ttu-id="56aa2-115">Ces propriétés sont recommandées sur tous les objets message.</span><span class="sxs-lookup"><span data-stu-id="56aa2-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="56aa2-116">Ces propriétés sont toujours le texte de l'objet complet, c'est-à-dire la concaténation du préfixe et l'objet normalisé.</span><span class="sxs-lookup"><span data-stu-id="56aa2-116">These properties are always the full subject text, that is, the concatenation of the prefix and the normalized subject.</span></span> <span data-ttu-id="56aa2-117">S'il n'y a pas de préfixe, l'objet normalisé doit être identique à l'objet.</span><span class="sxs-lookup"><span data-stu-id="56aa2-117">If there is no prefix, the normalized subject should be the same as the subject.</span></span> <span data-ttu-id="56aa2-118">Une banque de messages ou un fournisseur de transport utilise ces propriétés et les propriétés **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) pour calculer l'objet normalisé à l'aide de la règle décrite sous **PR_NORMALIZED_SUBJECT** ([ PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="56aa2-118">A message store or transport provider uses both these properties and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties to compute the normalized subject using the rule described under **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span></span>
  
<span data-ttu-id="56aa2-119">Les propriétés de l'objet sont généralement de petites chaînes de moins de 256 caractères et un fournisseur de banque de messages n'est pas tenu de prendre en charge l'interface **IStream** sur ces dernières.</span><span class="sxs-lookup"><span data-stu-id="56aa2-119">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the **IStream** interface on them.</span></span> <span data-ttu-id="56aa2-120">Le client doit toujours tenter d'accéder d'abord à travers l'interface **IMAPIProp** et ne recourir à **IStream** que si **MAPI_E_NOT_ENOUGH_MEMORY** est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="56aa2-120">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
<span data-ttu-id="56aa2-121">Pour un État, cette propriété contient l'objet du message d'origine, précédé d'une chaîne indiquant ce qui s'est passé au message.</span><span class="sxs-lookup"><span data-stu-id="56aa2-121">For a report, this property contains the original message's subject preceded by a string indicating what has happened to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="56aa2-122">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="56aa2-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="56aa2-123">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="56aa2-123">Protocol specifications</span></span>

<span data-ttu-id="56aa2-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56aa2-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56aa2-125">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="56aa2-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="56aa2-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56aa2-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56aa2-127">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="56aa2-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="56aa2-128">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="56aa2-128">Header files</span></span>

<span data-ttu-id="56aa2-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="56aa2-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="56aa2-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="56aa2-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="56aa2-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="56aa2-131">Mapitags.h</span></span>
  
> <span data-ttu-id="56aa2-132">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="56aa2-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="56aa2-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56aa2-133">See also</span></span>



[<span data-ttu-id="56aa2-134">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="56aa2-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="56aa2-135">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="56aa2-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="56aa2-136">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="56aa2-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="56aa2-137">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="56aa2-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

