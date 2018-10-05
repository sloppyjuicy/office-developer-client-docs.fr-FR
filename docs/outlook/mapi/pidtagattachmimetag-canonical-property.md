---
title: Propriété canonique PidTagAttachMimeTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMimeTag
api_type:
- HeaderDef
ms.assetid: cbc4585d-f970-4b22-ac08-d7fc91bff3d3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f05fa0816db3b412329372ad392c673c240eb59e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389098"
---
# <a name="pidtagattachmimetag-canonical-property"></a><span data-ttu-id="cd853-103">Propriété canonique PidTagAttachMimeTag</span><span class="sxs-lookup"><span data-stu-id="cd853-103">PidTagAttachMimeTag Canonical Property</span></span>

  
  
<span data-ttu-id="cd853-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd853-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd853-105">Contient des informations de mise en forme sur une pièce jointe Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="cd853-105">Contains formatting information about a Multipurpose Internet Mail Extensions (MIME) attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cd853-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="cd853-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cd853-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span><span class="sxs-lookup"><span data-stu-id="cd853-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span></span>  <br/> |
|<span data-ttu-id="cd853-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="cd853-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cd853-109">0x370E</span><span class="sxs-lookup"><span data-stu-id="cd853-109">0x370E</span></span>  <br/> |
|<span data-ttu-id="cd853-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="cd853-110">Data type:</span></span>  <br/> |<span data-ttu-id="cd853-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="cd853-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="cd853-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="cd853-112">Area:</span></span>  <br/> |<span data-ttu-id="cd853-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="cd853-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd853-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="cd853-114">Remarks</span></span>

<span data-ttu-id="cd853-115">Si la propriété **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) contient la valeur **OID_MIMETAG**, le fournisseur de transport doit se présenter ces propriétés pour déterminer la façon dont la pièce jointe est mis en forme.</span><span class="sxs-lookup"><span data-stu-id="cd853-115">If the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property contains the value **OID_MIMETAG**, the transport provider should look at these properties to determine how the attachment is formatted.</span></span> 
  
<span data-ttu-id="cd853-116">Ces propriétés sont copiées à partir du paramètre type de contenu de l’en-tête MIME entrant.</span><span class="sxs-lookup"><span data-stu-id="cd853-116">These properties are copied from the Content-type parameter of the inbound MIME header.</span></span> <span data-ttu-id="cd853-117">La composition de la chaîne est définie dans le document RFC 1521.</span><span class="sxs-lookup"><span data-stu-id="cd853-117">The composition of the string is defined in the RFC 1521 document.</span></span> <span data-ttu-id="cd853-118">Le format est type/sous-type, telles que l’application/binaire ou texte/ordinaire.</span><span class="sxs-lookup"><span data-stu-id="cd853-118">The format is type/subtype, such as application/binary or text/plain.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cd853-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="cd853-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cd853-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="cd853-120">Protocol specifications</span></span>

<span data-ttu-id="cd853-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd853-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd853-122">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="cd853-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="cd853-123">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cd853-123">[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cd853-124">Spécifie les propriétés des messages codés géré par des droits.</span><span class="sxs-lookup"><span data-stu-id="cd853-124">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cd853-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="cd853-125">Header files</span></span>

<span data-ttu-id="cd853-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cd853-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="cd853-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="cd853-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="cd853-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="cd853-128">Mapitags.h</span></span>
  
> <span data-ttu-id="cd853-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="cd853-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cd853-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd853-130">See also</span></span>



[<span data-ttu-id="cd853-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="cd853-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cd853-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="cd853-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cd853-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="cd853-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cd853-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="cd853-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

