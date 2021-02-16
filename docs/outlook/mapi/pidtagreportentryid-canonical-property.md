---
title: Propriété canonique PidTagReportEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportEntryId
api_type:
- COM
ms.assetid: ea2bcc06-0089-4999-b115-06a14de4a0f1
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3b4432650d5c9fc77c4db0bc9aed4234d85e7fdf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346318"
---
# <a name="pidtagreportentryid-canonical-property"></a><span data-ttu-id="f2ce5-103">Propriété canonique PidTagReportEntryId</span><span class="sxs-lookup"><span data-stu-id="f2ce5-103">PidTagReportEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="f2ce5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2ce5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2ce5-105">Contient l’identificateur d’entrée du destinataire qui doit recevoir des rapports pour ce message.</span><span class="sxs-lookup"><span data-stu-id="f2ce5-105">Contains the entry identifier for the recipient who should receive reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f2ce5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f2ce5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f2ce5-107">PR_REPORT_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f2ce5-107">PR_REPORT_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="f2ce5-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f2ce5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f2ce5-109">0x0045</span><span class="sxs-lookup"><span data-stu-id="f2ce5-109">0x0045</span></span>  <br/> |
|<span data-ttu-id="f2ce5-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f2ce5-110">Data type:</span></span>  <br/> |<span data-ttu-id="f2ce5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f2ce5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f2ce5-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f2ce5-112">Area:</span></span>  <br/> |<span data-ttu-id="f2ce5-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="f2ce5-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2ce5-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f2ce5-114">Remarks</span></span>

<span data-ttu-id="f2ce5-115">Cette propriété est l’une des propriétés d’adresse du destinataire que l’expéditeur a délégué pour recevoir les rapports générés pour ce message.</span><span class="sxs-lookup"><span data-stu-id="f2ce5-115">This property is one of the address properties for the recipient who the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="f2ce5-116">Une application cliente qui doit router des rapports vers un autre utilisateur doit définir cette propriété au moment de l’envoi du message.</span><span class="sxs-lookup"><span data-stu-id="f2ce5-116">A client application that must route reports to another user should set this property at message submission time.</span></span> <span data-ttu-id="f2ce5-117">S’il n’est pas définie, les rapports sont envoyés à l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="f2ce5-117">If it is not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f2ce5-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f2ce5-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f2ce5-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="f2ce5-119">Protocol specifications</span></span>

<span data-ttu-id="f2ce5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2ce5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2ce5-121">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="f2ce5-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f2ce5-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f2ce5-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f2ce5-123">Spécifie les propriétés et opérations autorisées sur les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="f2ce5-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f2ce5-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f2ce5-124">Header files</span></span>

<span data-ttu-id="f2ce5-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f2ce5-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f2ce5-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f2ce5-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="f2ce5-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f2ce5-127">Mapitags.h</span></span>
  
> <span data-ttu-id="f2ce5-128">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="f2ce5-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f2ce5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2ce5-129">See also</span></span>



[<span data-ttu-id="f2ce5-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f2ce5-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f2ce5-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f2ce5-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f2ce5-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f2ce5-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f2ce5-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f2ce5-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

