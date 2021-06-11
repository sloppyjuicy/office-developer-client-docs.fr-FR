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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6a84e51325fcb60c54c2f6b42af0c26a0efd3382
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327236"
---
# <a name="pidtagattachpayloadclass-canonical-property"></a><span data-ttu-id="7b0c9-103">Propriété canonique PidTagAttachPayloadClass</span><span class="sxs-lookup"><span data-stu-id="7b0c9-103">PidTagAttachPayloadClass Canonical Property</span></span>

  
  
<span data-ttu-id="7b0c9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b0c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b0c9-105">Contient la valeur d’un champ d’en-tête MIME X-Payload-Class.</span><span class="sxs-lookup"><span data-stu-id="7b0c9-105">Contains the value of a MIME X-Payload-Class header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7b0c9-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="7b0c9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7b0c9-107">PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="7b0c9-107">PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="7b0c9-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="7b0c9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7b0c9-109">0x371A</span><span class="sxs-lookup"><span data-stu-id="7b0c9-109">0x371A</span></span>  <br/> |
|<span data-ttu-id="7b0c9-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="7b0c9-110">Data type:</span></span>  <br/> |<span data-ttu-id="7b0c9-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7b0c9-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7b0c9-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="7b0c9-112">Area:</span></span>  <br/> |<span data-ttu-id="7b0c9-113">Outlook application</span><span class="sxs-lookup"><span data-stu-id="7b0c9-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b0c9-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="7b0c9-114">Remarks</span></span>

<span data-ttu-id="7b0c9-115">Pour définir la valeur de ces propriétés, les clients MIME doivent écrire un champ d’en-tête de classe de charge utile X dans une entité MIME qui sera analysée en tant que pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="7b0c9-115">To set the value of these properties, MIME clients should write an X-Payload-Class header field to a MIME entity that will be analyzed as an attachment.</span></span>
  
<span data-ttu-id="7b0c9-116">Les lecteurs MIME doivent copier cette valeur de champ d’en-tête sur la valeur de la propriété correspondante.</span><span class="sxs-lookup"><span data-stu-id="7b0c9-116">MIME readers must copy this header field value to the value of the corresponding property.</span></span> <span data-ttu-id="7b0c9-117">Les lecteurs MIME doivent ignorer ce champ d’en-tête lorsqu’il apparaît sur une entité MIME analysée sous forme de message ou de corps de message, plutôt que sous forme de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="7b0c9-117">MIME readers should ignore this header field when it appears on a MIME entity that is analyzed as a message or message body, rather than as an attachment.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7b0c9-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="7b0c9-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7b0c9-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="7b0c9-119">Protocol specifications</span></span>

<span data-ttu-id="7b0c9-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b0c9-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b0c9-121">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="7b0c9-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7b0c9-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7b0c9-122">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7b0c9-123">Convertit des conventions de messagerie standard Internet en objets de message.</span><span class="sxs-lookup"><span data-stu-id="7b0c9-123">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7b0c9-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="7b0c9-124">Header files</span></span>

<span data-ttu-id="7b0c9-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7b0c9-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="7b0c9-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="7b0c9-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="7b0c9-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7b0c9-127">Mapitags.h</span></span>
  
> <span data-ttu-id="7b0c9-128">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="7b0c9-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b0c9-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b0c9-129">See also</span></span>



[<span data-ttu-id="7b0c9-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="7b0c9-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7b0c9-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="7b0c9-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7b0c9-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="7b0c9-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7b0c9-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="7b0c9-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

