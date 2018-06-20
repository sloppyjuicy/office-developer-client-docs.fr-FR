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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 825f6f1eff94635ca2d0f5226cfc3f421d41bcce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785741"
---
# <a name="pidtagattachmentflags-canonical-property"></a><span data-ttu-id="88b2b-103">Propriété canonique PidTagAttachmentFlags</span><span class="sxs-lookup"><span data-stu-id="88b2b-103">PidTagAttachmentFlags Canonical Property</span></span>

  
  
<span data-ttu-id="88b2b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="88b2b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="88b2b-105">Indique le traitement spécial pour cet objet de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="88b2b-105">Indicates special handling for this Attachment object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="88b2b-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="88b2b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="88b2b-107">PR_ATTACHMENT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="88b2b-107">PR_ATTACHMENT_FLAGS</span></span>  <br/> |
|<span data-ttu-id="88b2b-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="88b2b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="88b2b-109">0x7FFD</span><span class="sxs-lookup"><span data-stu-id="88b2b-109">0x7FFD</span></span>  <br/> |
|<span data-ttu-id="88b2b-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="88b2b-110">Data type:</span></span>  <br/> |<span data-ttu-id="88b2b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="88b2b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="88b2b-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="88b2b-112">Area:</span></span>  <br/> |<span data-ttu-id="88b2b-113">Pièce jointe du message</span><span class="sxs-lookup"><span data-stu-id="88b2b-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="88b2b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="88b2b-114">Remarks</span></span>

<span data-ttu-id="88b2b-115">Doit être 0 x 00000000, sauf si d’autres protocoles qui étendent le Message et la pièce jointe objet protocole comme indiqué dans [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88b2b-115">Must be 0x00000000, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="88b2b-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="88b2b-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="88b2b-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="88b2b-117">Protocol specifications</span></span>

<span data-ttu-id="88b2b-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88b2b-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88b2b-119">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="88b2b-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="88b2b-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="88b2b-120">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="88b2b-121">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="88b2b-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="88b2b-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="88b2b-122">Header files</span></span>

<span data-ttu-id="88b2b-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="88b2b-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="88b2b-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="88b2b-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="88b2b-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="88b2b-125">Mapitags.h</span></span>
  
> <span data-ttu-id="88b2b-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="88b2b-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="88b2b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88b2b-127">See also</span></span>



[<span data-ttu-id="88b2b-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="88b2b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="88b2b-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="88b2b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="88b2b-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="88b2b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="88b2b-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="88b2b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

