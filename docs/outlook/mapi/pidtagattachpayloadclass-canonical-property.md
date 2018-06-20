---
title: Propriété canonique PidTagAttachPayloadClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadClass
api_type:
- HeaderDef
ms.assetid: bc4de217-8241-45e7-9e97-8f0c1b16691a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cef412d212bf29cfd1a1d5c4b2911440fae6a15e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785743"
---
# <a name="pidtagattachpayloadclass-canonical-property"></a><span data-ttu-id="ea2ee-103">Propriété canonique PidTagAttachPayloadClass</span><span class="sxs-lookup"><span data-stu-id="ea2ee-103">PidTagAttachPayloadClass Canonical Property</span></span>

  
  
<span data-ttu-id="ea2ee-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ea2ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ea2ee-105">Contient la valeur d’un champ d’en-tête X-charge utile-classe MIME.</span><span class="sxs-lookup"><span data-stu-id="ea2ee-105">Contains the value of a MIME X-Payload-Class header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ea2ee-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ea2ee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ea2ee-107">PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="ea2ee-107">PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="ea2ee-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ea2ee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ea2ee-109">0x371A</span><span class="sxs-lookup"><span data-stu-id="ea2ee-109">0x371A</span></span>  <br/> |
|<span data-ttu-id="ea2ee-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ea2ee-110">Data type:</span></span>  <br/> |<span data-ttu-id="ea2ee-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ea2ee-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ea2ee-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="ea2ee-112">Area:</span></span>  <br/> |<span data-ttu-id="ea2ee-113">Application Outlook</span><span class="sxs-lookup"><span data-stu-id="ea2ee-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea2ee-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ea2ee-114">Remarks</span></span>

<span data-ttu-id="ea2ee-115">Pour définir la valeur de ces propriétés, les clients MIME doivent écrire un champ d’en-tête X-charge utile-classe à une entité MIME qui est analysée en tant que pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="ea2ee-115">To set the value of these properties, MIME clients should write an X-Payload-Class header field to a MIME entity that will be analyzed as an attachment.</span></span>
  
<span data-ttu-id="ea2ee-116">Lecteurs MIME doivent copier cette valeur de champ d’en-tête sur la valeur de la propriété correspondante.</span><span class="sxs-lookup"><span data-stu-id="ea2ee-116">MIME readers must copy this header field value to the value of the corresponding property.</span></span> <span data-ttu-id="ea2ee-117">Lecteurs MIME doivent ignorer ce champ d’en-tête lorsqu’il apparaît sur une entité MIME qui est analysée en tant que message ou le corps du message, au lieu d’une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="ea2ee-117">MIME readers should ignore this header field when it appears on a MIME entity that is analyzed as a message or message body, rather than as an attachment.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ea2ee-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ea2ee-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ea2ee-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="ea2ee-119">Protocol specifications</span></span>

<span data-ttu-id="ea2ee-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea2ee-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea2ee-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="ea2ee-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ea2ee-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ea2ee-122">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ea2ee-123">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="ea2ee-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ea2ee-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ea2ee-124">Header files</span></span>

<span data-ttu-id="ea2ee-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ea2ee-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="ea2ee-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ea2ee-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="ea2ee-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ea2ee-127">Mapitags.h</span></span>
  
> <span data-ttu-id="ea2ee-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="ea2ee-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ea2ee-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea2ee-129">See also</span></span>



[<span data-ttu-id="ea2ee-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ea2ee-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ea2ee-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ea2ee-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ea2ee-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ea2ee-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ea2ee-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="ea2ee-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

