---
title: Propriété canonique PidTagReportName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportName
api_type:
- COM
ms.assetid: 4ec3100f-7cf1-4702-b326-e6da586a7bb2
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3c1a848eec84c7d81792a95baa3f47fa6779e95f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569581"
---
# <a name="pidtagreportname-canonical-property"></a><span data-ttu-id="ce2cc-103">Propriété canonique PidTagReportName</span><span class="sxs-lookup"><span data-stu-id="ce2cc-103">PidTagReportName Canonical Property</span></span>

  
  
<span data-ttu-id="ce2cc-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce2cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce2cc-105">Contient le nom complet pour le destinataire qui doit obtenir des rapports de ce message.</span><span class="sxs-lookup"><span data-stu-id="ce2cc-105">Contains the display name for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ce2cc-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ce2cc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ce2cc-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="ce2cc-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="ce2cc-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ce2cc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ce2cc-109">0x003A</span><span class="sxs-lookup"><span data-stu-id="ce2cc-109">0x003A</span></span>  <br/> |
|<span data-ttu-id="ce2cc-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ce2cc-110">Data type:</span></span>  <br/> |<span data-ttu-id="ce2cc-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ce2cc-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ce2cc-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ce2cc-112">Area:</span></span>  <br/> |<span data-ttu-id="ce2cc-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="ce2cc-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce2cc-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ce2cc-114">Remarks</span></span>

<span data-ttu-id="ce2cc-115">Ces propriétés sont des exemples de propriétés d’adresse du destinataire l’expéditeur a délégué pour recevoir les rapports générés pour ce message.</span><span class="sxs-lookup"><span data-stu-id="ce2cc-115">These properties are examples of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="ce2cc-116">Une application cliente qui doit router les rapports à un autre utilisateur doit définir ces propriétés au moment d’envoi de message.</span><span class="sxs-lookup"><span data-stu-id="ce2cc-116">A client application that must route reports to another user should set these properties at message submission time.</span></span> <span data-ttu-id="ce2cc-117">Si elles ne sont pas définies, les rapports sont envoyés à l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="ce2cc-117">If they are not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ce2cc-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ce2cc-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ce2cc-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ce2cc-119">Header files</span></span>

<span data-ttu-id="ce2cc-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ce2cc-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="ce2cc-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ce2cc-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="ce2cc-122">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ce2cc-122">Mapitags.h</span></span>
  
> <span data-ttu-id="ce2cc-123">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="ce2cc-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ce2cc-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce2cc-124">See also</span></span>



[<span data-ttu-id="ce2cc-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ce2cc-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ce2cc-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ce2cc-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ce2cc-127">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ce2cc-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ce2cc-128">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ce2cc-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

