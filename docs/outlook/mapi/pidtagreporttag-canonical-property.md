---
title: Propriété canonique PidTagReportTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportTag
api_type:
- COM
ms.assetid: 581bf372-8705-4617-aaa4-a1d761eb9b58
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: a328d71aef57f85a5bd33db5cc219dff181dafc0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593304"
---
# <a name="pidtagreporttag-canonical-property"></a><span data-ttu-id="81422-103">Propriété canonique PidTagReportTag</span><span class="sxs-lookup"><span data-stu-id="81422-103">PidTagReportTag Canonical Property</span></span>

  
  
<span data-ttu-id="81422-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81422-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81422-105">Contient une valeur de balise binaires que le système de messagerie doit copier dans un rapport généré pour le message.</span><span class="sxs-lookup"><span data-stu-id="81422-105">Contains a binary tag value that the messaging system should copy to any report generated for the message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81422-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="81422-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="81422-107">PR_REPORT_TAG</span><span class="sxs-lookup"><span data-stu-id="81422-107">PR_REPORT_TAG</span></span>  <br/> |
|<span data-ttu-id="81422-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="81422-108">Identifier:</span></span>  <br/> |<span data-ttu-id="81422-109">0x0031</span><span class="sxs-lookup"><span data-stu-id="81422-109">0x0031</span></span>  <br/> |
|<span data-ttu-id="81422-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="81422-110">Data type:</span></span>  <br/> |<span data-ttu-id="81422-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="81422-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="81422-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="81422-112">Area:</span></span>  <br/> |<span data-ttu-id="81422-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="81422-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81422-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="81422-114">Remarks</span></span>

<span data-ttu-id="81422-115">Cette propriété, comme la propriété **PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)), est utilisée pour faire correspondre un rapport avec le message d’origine.</span><span class="sxs-lookup"><span data-stu-id="81422-115">This property, like the **PR_SUBJECT_IPM** ([PidTagSubjectMessageId](pidtagsubjectmessageid-canonical-property.md)) property, is used to correlate a report with the original message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="81422-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="81422-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="81422-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="81422-117">Protocol specifications</span></span>

<span data-ttu-id="81422-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81422-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81422-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="81422-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="81422-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81422-120">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81422-121">Spécifie les propriétés et les opérations qui sont autorisées sur les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="81422-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="81422-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="81422-122">Header files</span></span>

<span data-ttu-id="81422-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="81422-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="81422-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="81422-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="81422-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="81422-125">Mapitags.h</span></span>
  
> <span data-ttu-id="81422-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="81422-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81422-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81422-127">See also</span></span>



[<span data-ttu-id="81422-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="81422-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="81422-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="81422-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="81422-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="81422-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="81422-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="81422-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

