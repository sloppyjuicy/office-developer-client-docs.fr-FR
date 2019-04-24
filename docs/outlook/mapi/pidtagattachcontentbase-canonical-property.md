---
title: Propriété canonique PidTagAttachContentBase
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachContentBase
api_type:
- HeaderDef
ms.assetid: 35c10264-6998-4c46-8cef-82708c96d9c7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ec1db68d9168e7260a32aaf7708897df6124725a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360507"
---
# <a name="pidtagattachcontentbase-canonical-property"></a><span data-ttu-id="4b48e-103">Propriété canonique PidTagAttachContentBase</span><span class="sxs-lookup"><span data-stu-id="4b48e-103">PidTagAttachContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="4b48e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b48e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b48e-105">Contient l'en-tête de base de contenu d'une pièce jointe à un message MIME (Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="4b48e-105">Contains the content base header of a Multipurpose Internet Mail Extensions (MIME) message attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4b48e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4b48e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4b48e-107">PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A, PR_ATTACH_CONTENT_BASE_W</span><span class="sxs-lookup"><span data-stu-id="4b48e-107">PR_ATTACH_CONTENT_BASE, PR_ATTACH_CONTENT_BASE_A, PR_ATTACH_CONTENT_BASE_W</span></span>  <br/> |
|<span data-ttu-id="4b48e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="4b48e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4b48e-109">0x3711</span><span class="sxs-lookup"><span data-stu-id="4b48e-109">0x3711</span></span>  <br/> |
|<span data-ttu-id="4b48e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4b48e-110">Data type:</span></span>  <br/> |<span data-ttu-id="4b48e-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4b48e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4b48e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="4b48e-112">Area:</span></span>  <br/> |<span data-ttu-id="4b48e-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="4b48e-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b48e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4b48e-114">Remarks</span></span>

<span data-ttu-id="4b48e-115">Ces propriétés sont utilisées pour la prise en charge de MHTML.</span><span class="sxs-lookup"><span data-stu-id="4b48e-115">These properties are used for MHTML support.</span></span> <span data-ttu-id="4b48e-116">Ils représentent l'en-tête de base de contenu pour la partie MIME appropriée.</span><span class="sxs-lookup"><span data-stu-id="4b48e-116">They represent the content base header for the appropriate MIME body part.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4b48e-117">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="4b48e-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4b48e-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="4b48e-118">Protocol specifications</span></span>

<span data-ttu-id="4b48e-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4b48e-119">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4b48e-120">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="4b48e-120">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4b48e-121">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="4b48e-121">Header files</span></span>

<span data-ttu-id="4b48e-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4b48e-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="4b48e-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4b48e-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="4b48e-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="4b48e-124">Mapitags.h</span></span>
  
> <span data-ttu-id="4b48e-125">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="4b48e-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4b48e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b48e-126">See also</span></span>



[<span data-ttu-id="4b48e-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4b48e-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4b48e-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4b48e-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4b48e-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4b48e-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4b48e-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="4b48e-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

