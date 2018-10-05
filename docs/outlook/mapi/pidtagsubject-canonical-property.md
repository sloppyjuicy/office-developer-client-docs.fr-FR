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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0cf9e9f8c10f8d27bd174b8b6f2bf19812dc269d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386305"
---
# <a name="pidtagsubject-canonical-property"></a><span data-ttu-id="7f0d6-103">Propriété canonique PidTagSubject</span><span class="sxs-lookup"><span data-stu-id="7f0d6-103">PidTagSubject Canonical Property</span></span>

  
  
<span data-ttu-id="7f0d6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f0d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f0d6-105">Contient la totalité de l’objet d’un message.</span><span class="sxs-lookup"><span data-stu-id="7f0d6-105">Contains the full subject of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f0d6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="7f0d6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7f0d6-107">PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W</span><span class="sxs-lookup"><span data-stu-id="7f0d6-107">PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W</span></span>  <br/> |
|<span data-ttu-id="7f0d6-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="7f0d6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7f0d6-109">0 x 0037</span><span class="sxs-lookup"><span data-stu-id="7f0d6-109">0x0037</span></span>  <br/> |
|<span data-ttu-id="7f0d6-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="7f0d6-110">Data type:</span></span>  <br/> |<span data-ttu-id="7f0d6-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7f0d6-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7f0d6-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="7f0d6-112">Area:</span></span>  <br/> |<span data-ttu-id="7f0d6-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="7f0d6-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f0d6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="7f0d6-114">Remarks</span></span>

<span data-ttu-id="7f0d6-115">Ces propriétés sont recommandées sur tous les objets de message.</span><span class="sxs-lookup"><span data-stu-id="7f0d6-115">These properties are recommended on all message objects.</span></span> 
  
<span data-ttu-id="7f0d6-116">Ces propriétés sont toujours le texte de l’objet complet, autrement dit, la concaténation du préfixe et l’objet normalisé.</span><span class="sxs-lookup"><span data-stu-id="7f0d6-116">These properties are always the full subject text, that is, the concatenation of the prefix and the normalized subject.</span></span> <span data-ttu-id="7f0d6-117">S’il n’existe pas de préfixe, l’objet normalisée doit être identique à l’objet.</span><span class="sxs-lookup"><span data-stu-id="7f0d6-117">If there is no prefix, the normalized subject should be the same as the subject.</span></span> <span data-ttu-id="7f0d6-118">Un message doit être stockée ou fournisseur utilise ces propriétés et les propriétés **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) pour calculer l’objet normalisée à l’aide de la règle décrite sous **PR_NORMALIZED_SUBJECT** ([ de transport PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7f0d6-118">A message store or transport provider uses both these properties and **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) properties to compute the normalized subject using the rule described under **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span></span>
  
<span data-ttu-id="7f0d6-119">Les propriétés de l’objet sont généralement petites chaînes de moins de 256 caractères, et un fournisseur de magasin de message n’est pas tenu prendre en charge l’interface **IStream** sur eux.</span><span class="sxs-lookup"><span data-stu-id="7f0d6-119">The subject properties are typically small strings of fewer than 256 characters, and a message store provider is not obligated to support the **IStream** interface on them.</span></span> <span data-ttu-id="7f0d6-120">Le client doit toujours tentent d’accéder par le biais de l’interface **IMAPIProp** tout d’abord et recourir aux **IStream** que si **MAPI_E_NOT_ENOUGH_MEMORY** est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="7f0d6-120">The client should always attempt access through the **IMAPIProp** interface first, and resort to **IStream** only if **MAPI_E_NOT_ENOUGH_MEMORY** is returned.</span></span> 
  
<span data-ttu-id="7f0d6-121">Pour un état, cette propriété contient le sujet du message d’origine précédé d’une chaîne qui indique ce qui est arrivé au message.</span><span class="sxs-lookup"><span data-stu-id="7f0d6-121">For a report, this property contains the original message's subject preceded by a string indicating what has happened to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7f0d6-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="7f0d6-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7f0d6-123">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="7f0d6-123">Protocol specifications</span></span>

<span data-ttu-id="7f0d6-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f0d6-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f0d6-125">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="7f0d6-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7f0d6-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7f0d6-126">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7f0d6-127">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="7f0d6-127">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7f0d6-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="7f0d6-128">Header files</span></span>

<span data-ttu-id="7f0d6-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7f0d6-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="7f0d6-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="7f0d6-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="7f0d6-131">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="7f0d6-131">Mapitags.h</span></span>
  
> <span data-ttu-id="7f0d6-132">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="7f0d6-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7f0d6-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f0d6-133">See also</span></span>



[<span data-ttu-id="7f0d6-134">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="7f0d6-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7f0d6-135">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="7f0d6-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7f0d6-136">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="7f0d6-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7f0d6-137">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="7f0d6-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

