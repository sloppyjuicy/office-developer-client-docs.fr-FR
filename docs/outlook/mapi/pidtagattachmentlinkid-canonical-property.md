---
title: Propriété canonique PidTagAttachmentLinkId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachmentLinkId
api_type:
- HeaderDef
ms.assetid: 5d0daae7-248d-459f-9d96-cb949b86f590
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e467fb7c05a647265d007429930ee522fd77b2fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785722"
---
# <a name="pidtagattachmentlinkid-canonical-property"></a><span data-ttu-id="3ea2c-103">Propriété canonique PidTagAttachmentLinkId</span><span class="sxs-lookup"><span data-stu-id="3ea2c-103">PidTagAttachmentLinkId Canonical Property</span></span>

  
  
<span data-ttu-id="3ea2c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3ea2c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3ea2c-105">Indique le type d’objet du Message à laquelle cette pièce jointe est liée.</span><span class="sxs-lookup"><span data-stu-id="3ea2c-105">Indicates the type of Message object to which this attachment is linked.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3ea2c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3ea2c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3ea2c-107">PR_ATTACHMENT_LINKID</span><span class="sxs-lookup"><span data-stu-id="3ea2c-107">PR_ATTACHMENT_LINKID</span></span>  <br/> |
|<span data-ttu-id="3ea2c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3ea2c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3ea2c-109">0x7FFA</span><span class="sxs-lookup"><span data-stu-id="3ea2c-109">0x7FFA</span></span>  <br/> |
|<span data-ttu-id="3ea2c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3ea2c-110">Data type:</span></span>  <br/> |<span data-ttu-id="3ea2c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3ea2c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3ea2c-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="3ea2c-112">Area:</span></span>  <br/> |<span data-ttu-id="3ea2c-113">Pièce jointe du message</span><span class="sxs-lookup"><span data-stu-id="3ea2c-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3ea2c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3ea2c-114">Remarks</span></span>

<span data-ttu-id="3ea2c-115">Doit être 0, sauf si d’autres protocoles qui étendent le Message et la pièce jointe objet protocole comme indiqué dans [[MS-OXCMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="3ea2c-115">Must be 0, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3ea2c-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3ea2c-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3ea2c-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="3ea2c-117">Protocol specifications</span></span>

<span data-ttu-id="3ea2c-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3ea2c-118">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3ea2c-119">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="3ea2c-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="3ea2c-120">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3ea2c-120">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3ea2c-121">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de la feuille.</span><span class="sxs-lookup"><span data-stu-id="3ea2c-121">Specifies the properties and operations that are permissible for journal objects.</span></span>
    
<span data-ttu-id="3ea2c-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3ea2c-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3ea2c-123">Spécifie les propriétés et le modèle d’interaction pour la messagerie et autres rappels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3ea2c-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3ea2c-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3ea2c-124">Header files</span></span>

<span data-ttu-id="3ea2c-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3ea2c-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="3ea2c-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3ea2c-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="3ea2c-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="3ea2c-127">Mapitags.h</span></span>
  
> <span data-ttu-id="3ea2c-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="3ea2c-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3ea2c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ea2c-129">See also</span></span>



[<span data-ttu-id="3ea2c-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3ea2c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3ea2c-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3ea2c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3ea2c-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3ea2c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3ea2c-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="3ea2c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

