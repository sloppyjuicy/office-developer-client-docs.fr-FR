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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 623b4195b7128667b9aaa6bc97d03c21d62c690a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345695"
---
# <a name="pidtagattachmentlinkid-canonical-property"></a><span data-ttu-id="0b941-103">Propriété canonique PidTagAttachmentLinkId</span><span class="sxs-lookup"><span data-stu-id="0b941-103">PidTagAttachmentLinkId Canonical Property</span></span>

  
  
<span data-ttu-id="0b941-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b941-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b941-105">Indique le type d’objet Message auquel cette pièce jointe est liée.</span><span class="sxs-lookup"><span data-stu-id="0b941-105">Indicates the type of Message object to which this attachment is linked.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0b941-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0b941-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0b941-107">PR_ATTACHMENT_LINKID</span><span class="sxs-lookup"><span data-stu-id="0b941-107">PR_ATTACHMENT_LINKID</span></span>  <br/> |
|<span data-ttu-id="0b941-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="0b941-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0b941-109">0x7FFA</span><span class="sxs-lookup"><span data-stu-id="0b941-109">0x7FFA</span></span>  <br/> |
|<span data-ttu-id="0b941-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0b941-110">Data type:</span></span>  <br/> |<span data-ttu-id="0b941-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0b941-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0b941-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="0b941-112">Area:</span></span>  <br/> |<span data-ttu-id="0b941-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="0b941-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b941-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0b941-114">Remarks</span></span>

<span data-ttu-id="0b941-115">Doit être 0, sauf en cas de non-lieu par d’autres protocoles qui étendent le protocole d’objet de message et de pièce jointe, comme indiqué dans [[MS-OXCMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="0b941-115">Must be 0, unless overridden by other protocols that extend the Message and Attachment Object Protocol as noted in [[MS-OXCMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0b941-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0b941-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0b941-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="0b941-117">Protocol specifications</span></span>

<span data-ttu-id="0b941-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b941-118">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b941-119">Gère les objets de message et de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="0b941-119">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="0b941-120">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b941-120">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b941-121">Spécifie les propriétés et opérations autorisées pour les objets de journal.</span><span class="sxs-lookup"><span data-stu-id="0b941-121">Specifies the properties and operations that are permissible for journal objects.</span></span>
    
<span data-ttu-id="0b941-122">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b941-122">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b941-123">Spécifie les propriétés et le modèle d’interaction pour les messages électroniques et autres rappels d’objets.</span><span class="sxs-lookup"><span data-stu-id="0b941-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0b941-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0b941-124">Header files</span></span>

<span data-ttu-id="0b941-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0b941-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0b941-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0b941-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="0b941-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0b941-127">Mapitags.h</span></span>
  
> <span data-ttu-id="0b941-128">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="0b941-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0b941-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b941-129">See also</span></span>



[<span data-ttu-id="0b941-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0b941-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0b941-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0b941-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0b941-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0b941-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0b941-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="0b941-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

