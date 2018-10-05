---
title: Propriété canonique PidTagAttachmentFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachmentFlags
api_type:
- HeaderDef
ms.assetid: 42981aac-f9e7-45dd-91a2-15d9784f30aa
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d494f1f14daff75be55e910da56204ecb3dbcf83
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400711"
---
# <a name="pidtagattachmentflags-canonical-property"></a><span data-ttu-id="f85ab-103">Propriété canonique PidTagAttachmentFlags</span><span class="sxs-lookup"><span data-stu-id="f85ab-103">PidTagAttachmentFlags Canonical Property</span></span>

  
  
<span data-ttu-id="f85ab-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f85ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f85ab-105">Indique le traitement spécial pour cet objet de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="f85ab-105">Indicates special handling for this Attachment object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f85ab-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f85ab-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f85ab-107">PR_ATTACHMENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="f85ab-107">PR_ATTACHMENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="f85ab-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f85ab-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f85ab-109">0x7FFD</span><span class="sxs-lookup"><span data-stu-id="f85ab-109">0x7FFD</span></span>  <br/> |
|<span data-ttu-id="f85ab-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f85ab-110">Data type:</span></span>  <br/> |<span data-ttu-id="f85ab-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f85ab-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f85ab-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f85ab-112">Area:</span></span>  <br/> |<span data-ttu-id="f85ab-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="f85ab-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f85ab-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f85ab-114">Remarks</span></span>

<span data-ttu-id="f85ab-115">Doit être 0 x 00000000, sauf si d’autres protocoles qui étendent le Message et la pièce jointe objet protocole comme indiqué dans [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f85ab-115">Must be 0x00000000, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f85ab-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f85ab-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f85ab-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="f85ab-117">Protocol specifications</span></span>

<span data-ttu-id="f85ab-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f85ab-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f85ab-119">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="f85ab-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="f85ab-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f85ab-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f85ab-121">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="f85ab-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f85ab-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f85ab-122">Header files</span></span>

<span data-ttu-id="f85ab-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f85ab-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f85ab-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f85ab-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f85ab-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="f85ab-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f85ab-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="f85ab-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f85ab-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f85ab-127">See also</span></span>



[<span data-ttu-id="f85ab-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f85ab-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f85ab-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f85ab-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f85ab-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f85ab-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f85ab-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f85ab-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

