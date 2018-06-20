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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6f65d67903fa9ebb255345f8666cd53de5512cab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785737"
---
# <a name="pidtagattachmimetag-canonical-property"></a><span data-ttu-id="4a666-103">Propriété canonique PidTagAttachMimeTag</span><span class="sxs-lookup"><span data-stu-id="4a666-103">PidTagAttachMimeTag Canonical Property</span></span>

  
  
<span data-ttu-id="4a666-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4a666-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4a666-105">Contient des informations de mise en forme sur une pièce jointe Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="4a666-105">Contains formatting information about a Multipurpose Internet Mail Extensions (MIME) attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4a666-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4a666-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4a666-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span><span class="sxs-lookup"><span data-stu-id="4a666-107">PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W</span></span>  <br/> |
|<span data-ttu-id="4a666-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="4a666-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4a666-109">0x370E</span><span class="sxs-lookup"><span data-stu-id="4a666-109">0x370E</span></span>  <br/> |
|<span data-ttu-id="4a666-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4a666-110">Data type:</span></span>  <br/> |<span data-ttu-id="4a666-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4a666-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4a666-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="4a666-112">Area:</span></span>  <br/> |<span data-ttu-id="4a666-113">Pièce jointe du message</span><span class="sxs-lookup"><span data-stu-id="4a666-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a666-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4a666-114">Remarks</span></span>

<span data-ttu-id="4a666-115">Si la propriété **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) contient la valeur **OID_MIMETAG**, le fournisseur de transport doit se présenter ces propriétés pour déterminer la façon dont la pièce jointe est mis en forme.</span><span class="sxs-lookup"><span data-stu-id="4a666-115">If the **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) property contains the value **OID_MIMETAG**, the transport provider should look at these properties to determine how the attachment is formatted.</span></span> 
  
<span data-ttu-id="4a666-116">Ces propriétés sont copiées à partir du paramètre type de contenu de l’en-tête MIME entrant.</span><span class="sxs-lookup"><span data-stu-id="4a666-116">These properties are copied from the Content-type parameter of the inbound MIME header.</span></span> <span data-ttu-id="4a666-117">La composition de la chaîne est définie dans le document RFC 1521.</span><span class="sxs-lookup"><span data-stu-id="4a666-117">The composition of the string is defined in the RFC 1521 document.</span></span> <span data-ttu-id="4a666-118">Le format est type/sous-type, telles que l’application/binaire ou texte/ordinaire.</span><span class="sxs-lookup"><span data-stu-id="4a666-118">The format is type/subtype, such as application/binary or text/plain.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4a666-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="4a666-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4a666-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="4a666-120">Protocol specifications</span></span>

<span data-ttu-id="4a666-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a666-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a666-122">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="4a666-122">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="4a666-123">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4a666-123">[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4a666-124">Spécifie les propriétés des messages codés géré par des droits.</span><span class="sxs-lookup"><span data-stu-id="4a666-124">Specifies the properties of rights-managed encoded messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4a666-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="4a666-125">Header files</span></span>

<span data-ttu-id="4a666-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4a666-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="4a666-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4a666-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="4a666-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="4a666-128">Mapitags.h</span></span>
  
> <span data-ttu-id="4a666-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="4a666-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4a666-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a666-130">See also</span></span>



[<span data-ttu-id="4a666-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4a666-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4a666-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4a666-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4a666-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4a666-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4a666-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="4a666-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

