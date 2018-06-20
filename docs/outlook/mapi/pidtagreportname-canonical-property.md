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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4d3a38f55fa2869df3f8afa1301cf1ad0c7b0737
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786592"
---
# <a name="pidtagreportname-canonical-property"></a><span data-ttu-id="b5cbb-103">Propriété canonique PidTagReportName</span><span class="sxs-lookup"><span data-stu-id="b5cbb-103">PidTagReportName Canonical Property</span></span>

  
  
<span data-ttu-id="b5cbb-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b5cbb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b5cbb-105">Contient le nom complet pour le destinataire qui doit obtenir des rapports de ce message.</span><span class="sxs-lookup"><span data-stu-id="b5cbb-105">Contains the display name for the recipient that should get reports for this message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b5cbb-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b5cbb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b5cbb-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="b5cbb-107">PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="b5cbb-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b5cbb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b5cbb-109">0x003A</span><span class="sxs-lookup"><span data-stu-id="b5cbb-109">0x003A</span></span>  <br/> |
|<span data-ttu-id="b5cbb-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b5cbb-110">Data type:</span></span>  <br/> |<span data-ttu-id="b5cbb-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b5cbb-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b5cbb-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="b5cbb-112">Area:</span></span>  <br/> |<span data-ttu-id="b5cbb-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="b5cbb-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5cbb-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b5cbb-114">Remarks</span></span>

<span data-ttu-id="b5cbb-115">Ces propriétés sont des exemples de propriétés d’adresse du destinataire l’expéditeur a délégué pour recevoir les rapports générés pour ce message.</span><span class="sxs-lookup"><span data-stu-id="b5cbb-115">These properties are examples of the address properties for the recipient that the sender has delegated to receive any reports generated for this message.</span></span>
  
<span data-ttu-id="b5cbb-116">Une application cliente qui doit router les rapports à un autre utilisateur doit définir ces propriétés au moment d’envoi de message.</span><span class="sxs-lookup"><span data-stu-id="b5cbb-116">A client application that must route reports to another user should set these properties at message submission time.</span></span> <span data-ttu-id="b5cbb-117">Si elles ne sont pas définies, les rapports sont envoyés à l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="b5cbb-117">If they are not set, the reports are sent to the message sender.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b5cbb-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b5cbb-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b5cbb-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b5cbb-119">Header files</span></span>

<span data-ttu-id="b5cbb-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b5cbb-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="b5cbb-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b5cbb-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="b5cbb-122">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="b5cbb-122">Mapitags.h</span></span>
  
> <span data-ttu-id="b5cbb-123">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="b5cbb-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b5cbb-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5cbb-124">See also</span></span>



[<span data-ttu-id="b5cbb-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b5cbb-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b5cbb-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b5cbb-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b5cbb-127">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b5cbb-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b5cbb-128">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="b5cbb-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

