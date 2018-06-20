---
title: Propriété canonique PidTagBodyContentLocation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyContentLocation
api_type:
- HeaderDef
ms.assetid: a66d1c64-5c5a-4980-9acd-72448108fd2c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a05743f2fa10326a358dd92a72cf530740274f2d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785790"
---
# <a name="pidtagbodycontentlocation-canonical-property"></a><span data-ttu-id="afe54-103">Propriété canonique PidTagBodyContentLocation</span><span class="sxs-lookup"><span data-stu-id="afe54-103">PidTagBodyContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="afe54-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="afe54-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="afe54-105">Contient la valeur d’un champ d’en-tête MIME Content-Location.</span><span class="sxs-lookup"><span data-stu-id="afe54-105">Contains the value of a MIME Content-Location header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="afe54-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="afe54-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="afe54-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="afe54-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="afe54-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="afe54-108">Identifier:</span></span>  <br/> |<span data-ttu-id="afe54-109">0x1014</span><span class="sxs-lookup"><span data-stu-id="afe54-109">0x1014</span></span>  <br/> |
|<span data-ttu-id="afe54-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="afe54-110">Data type:</span></span>  <br/> |<span data-ttu-id="afe54-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="afe54-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="afe54-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="afe54-112">Area:</span></span>  <br/> |<span data-ttu-id="afe54-113">MIME</span><span class="sxs-lookup"><span data-stu-id="afe54-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="afe54-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="afe54-114">Remarks</span></span>

<span data-ttu-id="afe54-115">Pour définir la valeur de ces propriétés, les clients MIME doivent écrire la valeur souhaitée pour un champ d’en-tête Content-Location sur une entité MIME qui mappe sur un corps de message.</span><span class="sxs-lookup"><span data-stu-id="afe54-115">To set the value of these properties, MIME clients should write the desired value to a Content-Location header field on a MIME entity that maps to a message body.</span></span>
  
<span data-ttu-id="afe54-116">Lecteurs MIME doivent copier la valeur d’un champ d’en-tête Content-Location sur une entité de MIME de ce type à la valeur de ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="afe54-116">MIME readers should copy the value of a Content-Location header field on such a MIME entity to the value of these properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="afe54-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="afe54-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="afe54-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="afe54-118">Protocol specifications</span></span>

<span data-ttu-id="afe54-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="afe54-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="afe54-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="afe54-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="afe54-121">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="afe54-121">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="afe54-122">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="afe54-122">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="afe54-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="afe54-123">Header files</span></span>

<span data-ttu-id="afe54-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="afe54-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="afe54-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="afe54-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="afe54-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="afe54-126">Mapitags.h</span></span>
  
> <span data-ttu-id="afe54-127">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="afe54-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="afe54-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="afe54-128">See also</span></span>



[<span data-ttu-id="afe54-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="afe54-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="afe54-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="afe54-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="afe54-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="afe54-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="afe54-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="afe54-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

