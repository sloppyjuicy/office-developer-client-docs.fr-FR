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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 90a873174b5b990f165d0b2173efa38fc7df2d9d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394916"
---
# <a name="pidtagbodycontentlocation-canonical-property"></a><span data-ttu-id="66ace-103">Propriété canonique PidTagBodyContentLocation</span><span class="sxs-lookup"><span data-stu-id="66ace-103">PidTagBodyContentLocation Canonical Property</span></span>

  
  
<span data-ttu-id="66ace-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66ace-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66ace-105">Contient la valeur d’un champ d’en-tête MIME Content-Location.</span><span class="sxs-lookup"><span data-stu-id="66ace-105">Contains the value of a MIME Content-Location header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="66ace-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="66ace-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="66ace-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span><span class="sxs-lookup"><span data-stu-id="66ace-107">PR_BODY_CONTENT_LOCATION, PR_BODY_CONTENT_LOCATION_A, PR_BODY_CONTENT_LOCATION_W</span></span>  <br/> |
|<span data-ttu-id="66ace-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="66ace-108">Identifier:</span></span>  <br/> |<span data-ttu-id="66ace-109">0x1014</span><span class="sxs-lookup"><span data-stu-id="66ace-109">0x1014</span></span>  <br/> |
|<span data-ttu-id="66ace-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="66ace-110">Data type:</span></span>  <br/> |<span data-ttu-id="66ace-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="66ace-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="66ace-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="66ace-112">Area:</span></span>  <br/> |<span data-ttu-id="66ace-113">MIME</span><span class="sxs-lookup"><span data-stu-id="66ace-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66ace-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="66ace-114">Remarks</span></span>

<span data-ttu-id="66ace-115">Pour définir la valeur de ces propriétés, les clients MIME doivent écrire la valeur souhaitée pour un champ d’en-tête Content-Location sur une entité MIME qui mappe sur un corps de message.</span><span class="sxs-lookup"><span data-stu-id="66ace-115">To set the value of these properties, MIME clients should write the desired value to a Content-Location header field on a MIME entity that maps to a message body.</span></span>
  
<span data-ttu-id="66ace-116">Lecteurs MIME doivent copier la valeur d’un champ d’en-tête Content-Location sur une entité de MIME de ce type à la valeur de ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="66ace-116">MIME readers should copy the value of a Content-Location header field on such a MIME entity to the value of these properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="66ace-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="66ace-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="66ace-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="66ace-118">Protocol specifications</span></span>

<span data-ttu-id="66ace-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66ace-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66ace-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="66ace-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="66ace-121">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="66ace-121">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="66ace-122">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="66ace-122">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="66ace-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="66ace-123">Header files</span></span>

<span data-ttu-id="66ace-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="66ace-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="66ace-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="66ace-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="66ace-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="66ace-126">Mapitags.h</span></span>
  
> <span data-ttu-id="66ace-127">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="66ace-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="66ace-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66ace-128">See also</span></span>



[<span data-ttu-id="66ace-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="66ace-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="66ace-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="66ace-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="66ace-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="66ace-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="66ace-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="66ace-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

