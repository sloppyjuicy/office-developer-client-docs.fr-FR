---
title: Propriété canonique PidTagSensitivity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSensitivity
api_type:
- COM
ms.assetid: 5b678475-f2a8-4831-ad68-11654e09c821
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: eab8ce71d28a672d7069a1c16da5cd2cc2e149f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342503"
---
# <a name="pidtagsensitivity-canonical-property"></a><span data-ttu-id="67a0c-103">Propriété canonique PidTagSensitivity</span><span class="sxs-lookup"><span data-stu-id="67a0c-103">PidTagSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="67a0c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67a0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67a0c-105">Contient une valeur qui indique l'avis de l'expéditeur du message du critère de diffusion d'un message.</span><span class="sxs-lookup"><span data-stu-id="67a0c-105">Contains a value that indicates the message sender's opinion of the sensitivity of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="67a0c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="67a0c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="67a0c-107">PR_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="67a0c-107">PR_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="67a0c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="67a0c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="67a0c-109">0x0036</span><span class="sxs-lookup"><span data-stu-id="67a0c-109">0x0036</span></span>  <br/> |
|<span data-ttu-id="67a0c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="67a0c-110">Data type:</span></span>  <br/> |<span data-ttu-id="67a0c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="67a0c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="67a0c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="67a0c-112">Area:</span></span>  <br/> |<span data-ttu-id="67a0c-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="67a0c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67a0c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="67a0c-114">Remarks</span></span>

<span data-ttu-id="67a0c-115">Il est recommandé que les objets message exposent cette propriété.</span><span class="sxs-lookup"><span data-stu-id="67a0c-115">It is recommended that message objects expose this property.</span></span>
  
<span data-ttu-id="67a0c-116">Cette propriété peut avoir exactement l'une des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="67a0c-116">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="67a0c-117">SENSITIVITY_NONE</span><span class="sxs-lookup"><span data-stu-id="67a0c-117">SENSITIVITY_NONE</span></span> 
  
> <span data-ttu-id="67a0c-118">Le message n'a pas de confidentialité particulière.</span><span class="sxs-lookup"><span data-stu-id="67a0c-118">The message has no special sensitivity.</span></span>
    
<span data-ttu-id="67a0c-119">SENSITIVITY_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="67a0c-119">SENSITIVITY_PERSONAL</span></span> 
  
> <span data-ttu-id="67a0c-120">Le message est personnel.</span><span class="sxs-lookup"><span data-stu-id="67a0c-120">The message is personal.</span></span>
    
<span data-ttu-id="67a0c-121">SENSITIVITY_PRIVATE</span><span class="sxs-lookup"><span data-stu-id="67a0c-121">SENSITIVITY_PRIVATE</span></span> 
  
> <span data-ttu-id="67a0c-122">Le message est privé.</span><span class="sxs-lookup"><span data-stu-id="67a0c-122">The message is private.</span></span>
    
<span data-ttu-id="67a0c-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span><span class="sxs-lookup"><span data-stu-id="67a0c-123">SENSITIVITY_COMPANY_CONFIDENTIAL</span></span> 
  
> <span data-ttu-id="67a0c-124">Le message est désigné confidentiel.</span><span class="sxs-lookup"><span data-stu-id="67a0c-124">The message is designated company confidential.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="67a0c-125">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="67a0c-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="67a0c-126">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="67a0c-126">Protocol specifications</span></span>

<span data-ttu-id="67a0c-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67a0c-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67a0c-128">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="67a0c-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="67a0c-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="67a0c-129">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="67a0c-130">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="67a0c-130">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="67a0c-131">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="67a0c-131">Header files</span></span>

<span data-ttu-id="67a0c-132">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="67a0c-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="67a0c-133">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="67a0c-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="67a0c-134">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="67a0c-134">Mapitags.h</span></span>
  
> <span data-ttu-id="67a0c-135">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="67a0c-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="67a0c-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67a0c-136">See also</span></span>



[<span data-ttu-id="67a0c-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="67a0c-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="67a0c-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="67a0c-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="67a0c-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="67a0c-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="67a0c-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="67a0c-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

