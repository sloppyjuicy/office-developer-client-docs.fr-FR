---
title: Propriété canonique PidTagReportTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportTime
api_type:
- COM
ms.assetid: b3646505-a9f0-4a72-8277-b238c909f66f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 298c53e537819f800a3acc5cf07c01a7b9f978ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330148"
---
# <a name="pidtagreporttime-canonical-property"></a><span data-ttu-id="e4656-103">Propriété canonique PidTagReportTime</span><span class="sxs-lookup"><span data-stu-id="e4656-103">PidTagReportTime Canonical Property</span></span>

  
  
<span data-ttu-id="e4656-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4656-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4656-105">Contient la date et l’heure à laquelle le système de messagerie a généré un rapport.</span><span class="sxs-lookup"><span data-stu-id="e4656-105">Contains the date and time when the messaging system generated a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e4656-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e4656-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e4656-107">PR_REPORT_TIME</span><span class="sxs-lookup"><span data-stu-id="e4656-107">PR_REPORT_TIME</span></span>  <br/> |
|<span data-ttu-id="e4656-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="e4656-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e4656-109">0x0032</span><span class="sxs-lookup"><span data-stu-id="e4656-109">0x0032</span></span>  <br/> |
|<span data-ttu-id="e4656-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e4656-110">Data type:</span></span>  <br/> |<span data-ttu-id="e4656-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="e4656-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="e4656-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e4656-112">Area:</span></span>  <br/> |<span data-ttu-id="e4656-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="e4656-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4656-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e4656-114">Remarks</span></span>

<span data-ttu-id="e4656-115">Cette propriété représente une propriété par destinataire sur les rapports de remise et de non remise et une propriété par message sur les rapports de lecture et non lus.</span><span class="sxs-lookup"><span data-stu-id="e4656-115">This property represents a per-recipient property on delivery and nondelivery reports and a per-message property on read and nonread reports.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e4656-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e4656-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e4656-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="e4656-117">Protocol specifications</span></span>

<span data-ttu-id="e4656-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e4656-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e4656-119">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="e4656-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e4656-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e4656-120">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e4656-121">Spécifie les propriétés et opérations autorisées sur les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="e4656-121">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="e4656-122">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e4656-122">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e4656-123">Permet la gestion des listes d’adresses de courriers indésirables et la détermination des messages électroniques indésirables.</span><span class="sxs-lookup"><span data-stu-id="e4656-123">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e4656-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e4656-124">Header files</span></span>

<span data-ttu-id="e4656-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e4656-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e4656-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e4656-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="e4656-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e4656-127">Mapitags.h</span></span>
  
> <span data-ttu-id="e4656-128">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="e4656-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e4656-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4656-129">See also</span></span>



[<span data-ttu-id="e4656-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e4656-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e4656-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e4656-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e4656-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e4656-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e4656-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e4656-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

