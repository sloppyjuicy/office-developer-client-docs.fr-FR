---
title: Propriété canonique PidTagAttachContentLocation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentLocation
api_type:
- HeaderDef
ms.assetid: af2f776c-1b77-4942-827a-4363eda3924f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d886bf1e30eae6b4b26512eed95988516a609c94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785702"
---
# <a name="pidtagattachcontentlocation-canonical-property"></a><span data-ttu-id="08101-103">Propriété canonique PidTagAttachContentLocation</span><span class="sxs-lookup"><span data-stu-id="08101-103">PidTagAttachContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="08101-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="08101-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="08101-105">Contient l’en-tête de l’emplacement du contenu d’une pièce jointe du message Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="08101-105">Contains the content location header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08101-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="08101-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08101-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="08101-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="08101-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="08101-108">Identifier:</span></span>  <br/> |<span data-ttu-id="08101-109">0x3713</span><span class="sxs-lookup"><span data-stu-id="08101-109">0x3713</span></span>  <br/> |
|<span data-ttu-id="08101-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="08101-110">Data type:</span></span>  <br/> |<span data-ttu-id="08101-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="08101-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="08101-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="08101-112">Area:</span></span>  <br/> |<span data-ttu-id="08101-113">Pièce jointe du message</span><span class="sxs-lookup"><span data-stu-id="08101-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08101-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="08101-114">Remarks</span></span>

<span data-ttu-id="08101-115">Ces propriétés sont utilisées pour la prise en charge MHTML.</span><span class="sxs-lookup"><span data-stu-id="08101-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="08101-116">Ils représentent l’en-tête de l’emplacement du contenu pour le composant de corps MIME approprié.</span><span class="sxs-lookup"><span data-stu-id="08101-116">They represent the content location header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="08101-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="08101-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="08101-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="08101-118">Protocol specifications</span></span>

<span data-ttu-id="08101-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08101-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08101-120">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="08101-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="08101-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="08101-121">Header files</span></span>

<span data-ttu-id="08101-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08101-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="08101-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="08101-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="08101-124">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="08101-124">Mapitags.h</span></span>
  
> <span data-ttu-id="08101-125">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="08101-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08101-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08101-126">See also</span></span>



[<span data-ttu-id="08101-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="08101-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08101-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="08101-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08101-129">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="08101-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08101-130">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="08101-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

