---
title: Propriété canonique PidTagAttachAdditionalInformation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachAdditionalInformation
api_type:
- HeaderDef
ms.assetid: 75f092f2-ee3f-45c2-a46f-e1dff2e22b2e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e0a8f49f96bf4c4f8518dddbe52e8692f7b6645a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389630"
---
# <a name="pidtagattachadditionalinformation-canonical-property"></a><span data-ttu-id="3c65b-103">Propriété canonique PidTagAttachAdditionalInformation</span><span class="sxs-lookup"><span data-stu-id="3c65b-103">PidTagAttachAdditionalInformation Canonical Property</span></span>

  
  
<span data-ttu-id="3c65b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c65b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c65b-105">Fournit des informations de type de fichier pour une pièce jointe non Windows.</span><span class="sxs-lookup"><span data-stu-id="3c65b-105">Provides file type information for a non-Windows attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3c65b-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3c65b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3c65b-107">PR_ATTACH_ADDITIONAL_INFO</span><span class="sxs-lookup"><span data-stu-id="3c65b-107">PR_ATTACH_ADDITIONAL_INFO</span></span>  <br/> |
|<span data-ttu-id="3c65b-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3c65b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3c65b-109">0x370F</span><span class="sxs-lookup"><span data-stu-id="3c65b-109">0x370F</span></span>  <br/> |
|<span data-ttu-id="3c65b-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3c65b-110">Data type:</span></span>  <br/> |<span data-ttu-id="3c65b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3c65b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3c65b-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="3c65b-112">Area:</span></span>  <br/> |<span data-ttu-id="3c65b-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="3c65b-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c65b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3c65b-114">Remarks</span></span>

<span data-ttu-id="3c65b-115">Cette propriété fournit des métadonnées relatives à une pièce jointe particulière basée sur le codage de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="3c65b-115">This property provides metadata about a particular attachment based on the attachment's encoding.</span></span> <span data-ttu-id="3c65b-116">Par exemple, lorsque la propriété **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) contient MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contient une chaîne qui représente le créateur de fichier Macintosh et le type de fichier, au format « :CREA:TYPE » pour le fichier Macintosh codé.</span><span class="sxs-lookup"><span data-stu-id="3c65b-116">For example, when the **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)) property contains MacBinary, **PR_ATTACH_ADDITIONAL_INFO** contains a string that represents the Macintosh file creator and file type, formatted as ":CREA:TYPE" for the encoded Macintosh file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3c65b-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3c65b-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3c65b-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="3c65b-118">Protocol specifications</span></span>

<span data-ttu-id="3c65b-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c65b-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3c65b-120">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="3c65b-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3c65b-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3c65b-121">Header files</span></span>

<span data-ttu-id="3c65b-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3c65b-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="3c65b-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3c65b-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="3c65b-124">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="3c65b-124">Mapitags.h</span></span>
  
> <span data-ttu-id="3c65b-125">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="3c65b-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c65b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c65b-126">See also</span></span>



[<span data-ttu-id="3c65b-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3c65b-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3c65b-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3c65b-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3c65b-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3c65b-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3c65b-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="3c65b-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

