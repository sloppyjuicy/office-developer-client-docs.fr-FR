---
title: Propriété canonique PidTagReportSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportSearchKey
api_type:
- COM
ms.assetid: d4f4c40b-b6a8-45f3-b750-07b92c535322
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b82e27358c9f30a649dc10e1a53ee7c321cb3d82
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584960"
---
# <a name="pidtagreportsearchkey-canonical-property"></a><span data-ttu-id="b6bf8-103">Propriété canonique PidTagReportSearchKey</span><span class="sxs-lookup"><span data-stu-id="b6bf8-103">PidTagReportSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="b6bf8-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6bf8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6bf8-105">Contient la clé de recherche pour le destinataire qui doit obtenir des rapports de ce message.</span><span class="sxs-lookup"><span data-stu-id="b6bf8-105">Contains the search key for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b6bf8-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b6bf8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b6bf8-107">PR_REPORT_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="b6bf8-107">PR_REPORT_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="b6bf8-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b6bf8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b6bf8-109">0x0054</span><span class="sxs-lookup"><span data-stu-id="b6bf8-109">0x0054</span></span>  <br/> |
|<span data-ttu-id="b6bf8-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b6bf8-110">Data type:</span></span>  <br/> |<span data-ttu-id="b6bf8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b6bf8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b6bf8-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="b6bf8-112">Area:</span></span>  <br/> |<span data-ttu-id="b6bf8-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="b6bf8-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6bf8-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b6bf8-114">Remarks</span></span>

<span data-ttu-id="b6bf8-115">Cette propriété est une des propriétés d’adresse du destinataire l’expéditeur a délégué pour recevoir les rapports générés pour ce message.</span><span class="sxs-lookup"><span data-stu-id="b6bf8-115">This property is one of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="b6bf8-116">Une application cliente qui doit router les rapports à un autre utilisateur doit définir cette propriété à l’heure d’envoi de message.</span><span class="sxs-lookup"><span data-stu-id="b6bf8-116">A client application that must route reports to another user should set this property at message submission time.</span></span> <span data-ttu-id="b6bf8-117">Si elle n’est pas définie, les rapports sont envoyés à l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="b6bf8-117">If it is not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b6bf8-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b6bf8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b6bf8-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="b6bf8-119">Protocol specifications</span></span>

<span data-ttu-id="b6bf8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6bf8-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6bf8-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="b6bf8-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b6bf8-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b6bf8-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b6bf8-123">Spécifie les propriétés et les opérations qui sont autorisées sur les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="b6bf8-123">Specifies the properties and operations that are permissible on email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b6bf8-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b6bf8-124">Header files</span></span>

<span data-ttu-id="b6bf8-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b6bf8-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="b6bf8-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b6bf8-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="b6bf8-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="b6bf8-127">Mapitags.h</span></span>
  
> <span data-ttu-id="b6bf8-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="b6bf8-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b6bf8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6bf8-129">See also</span></span>



[<span data-ttu-id="b6bf8-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b6bf8-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b6bf8-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b6bf8-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b6bf8-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b6bf8-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b6bf8-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="b6bf8-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

