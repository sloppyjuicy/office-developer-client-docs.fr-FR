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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1d654c2a14728979146ef09618bfc4e9e618f9d8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594767"
---
# <a name="pidtagattachcontentlocation-canonical-property"></a><span data-ttu-id="f22d5-103">Propriété canonique PidTagAttachContentLocation</span><span class="sxs-lookup"><span data-stu-id="f22d5-103">PidTagAttachContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="f22d5-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f22d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f22d5-105">Contient l’en-tête de l’emplacement du contenu d’une pièce jointe du message Multipurpose Internet Mail Extensions (MIME).</span><span class="sxs-lookup"><span data-stu-id="f22d5-105">Contains the content location header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f22d5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f22d5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f22d5-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="f22d5-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="f22d5-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f22d5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f22d5-109">0x3713</span><span class="sxs-lookup"><span data-stu-id="f22d5-109">0x3713</span></span>  <br/> |
|<span data-ttu-id="f22d5-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f22d5-110">Data type:</span></span>  <br/> |<span data-ttu-id="f22d5-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f22d5-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f22d5-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f22d5-112">Area:</span></span>  <br/> |<span data-ttu-id="f22d5-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="f22d5-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f22d5-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f22d5-114">Remarks</span></span>

<span data-ttu-id="f22d5-115">Ces propriétés sont utilisées pour la prise en charge MHTML.</span><span class="sxs-lookup"><span data-stu-id="f22d5-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="f22d5-116">Ils représentent l’en-tête de l’emplacement du contenu pour le composant de corps MIME approprié.</span><span class="sxs-lookup"><span data-stu-id="f22d5-116">They represent the content location header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f22d5-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f22d5-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f22d5-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="f22d5-118">Protocol specifications</span></span>

<span data-ttu-id="f22d5-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f22d5-119">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f22d5-120">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="f22d5-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f22d5-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f22d5-121">Header files</span></span>

<span data-ttu-id="f22d5-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f22d5-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="f22d5-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f22d5-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="f22d5-124">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="f22d5-124">Mapitags.h</span></span>
  
> <span data-ttu-id="f22d5-125">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="f22d5-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f22d5-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f22d5-126">See also</span></span>



[<span data-ttu-id="f22d5-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f22d5-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f22d5-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f22d5-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f22d5-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f22d5-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f22d5-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f22d5-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

