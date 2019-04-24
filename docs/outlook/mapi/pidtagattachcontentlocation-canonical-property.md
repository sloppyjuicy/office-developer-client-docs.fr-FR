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
ms.openlocfilehash: f279d8ea305c0b1e609881b15e39653c41d5828e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345478"
---
# <a name="pidtagattachcontentlocation-canonical-property"></a><span data-ttu-id="36071-103">Propriété canonique PidTagAttachContentLocation</span><span class="sxs-lookup"><span data-stu-id="36071-103">PidTagAttachContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="36071-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36071-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36071-105">Contient l'en-tête d'emplacement de contenu d'une pièce jointe à un message MIME (Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="36071-105">Contains the content location header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="36071-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="36071-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="36071-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="36071-107">PR_ATTACH_CONTENT_LOCATION, PR_ATTACH_CONTENT_LOCATION_A, PR_ATTACH_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="36071-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="36071-108">Identifier:</span></span>  <br/> |<span data-ttu-id="36071-109">0x3713</span><span class="sxs-lookup"><span data-stu-id="36071-109">0x3713</span></span>  <br/> |
|<span data-ttu-id="36071-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="36071-110">Data type:</span></span>  <br/> |<span data-ttu-id="36071-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="36071-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="36071-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="36071-112">Area:</span></span>  <br/> |<span data-ttu-id="36071-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="36071-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36071-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="36071-114">Remarks</span></span>

<span data-ttu-id="36071-115">Ces propriétés sont utilisées pour la prise en charge de MHTML.</span><span class="sxs-lookup"><span data-stu-id="36071-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="36071-116">Elles représentent l'en-tête d'emplacement de contenu pour la partie MIME appropriée.</span><span class="sxs-lookup"><span data-stu-id="36071-116">They represent the content location header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="36071-117">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="36071-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="36071-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="36071-118">Protocol specifications</span></span>

<span data-ttu-id="36071-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36071-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36071-120">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="36071-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="36071-121">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="36071-121">Header files</span></span>

<span data-ttu-id="36071-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="36071-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="36071-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="36071-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="36071-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="36071-124">Mapitags.h</span></span>
  
> <span data-ttu-id="36071-125">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="36071-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="36071-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36071-126">See also</span></span>



[<span data-ttu-id="36071-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="36071-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="36071-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="36071-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="36071-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="36071-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="36071-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="36071-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

