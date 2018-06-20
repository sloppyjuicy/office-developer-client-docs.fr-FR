---
title: Propriété canonique PidTagMessageSubmissionId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSubmissionId
api_type:
- HeaderDef
ms.assetid: 0a799fe5-04e2-4e1d-b0cd-9bdd2577d299
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b3286e9e666d59997693df636263cb04f7b767d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786258"
---
# <a name="pidtagmessagesubmissionid-canonical-property"></a><span data-ttu-id="b4fd5-103">Propriété canonique PidTagMessageSubmissionId</span><span class="sxs-lookup"><span data-stu-id="b4fd5-103">PidTagMessageSubmissionId Canonical Property</span></span>

  
  
<span data-ttu-id="b4fd5-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b4fd5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b4fd5-105">Contient un identificateur de système (MTS) de transfert de message pour l’agent de transfert des messages (MTA).</span><span class="sxs-lookup"><span data-stu-id="b4fd5-105">Contains a message transfer system (MTS) identifier for the message transfer agent (MTA).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b4fd5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b4fd5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b4fd5-107">PR_MESSAGE_SUBMISSION_ID</span><span class="sxs-lookup"><span data-stu-id="b4fd5-107">PR_MESSAGE_SUBMISSION_ID</span></span>  <br/> |
|<span data-ttu-id="b4fd5-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b4fd5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b4fd5-109">0x0047</span><span class="sxs-lookup"><span data-stu-id="b4fd5-109">0x0047</span></span>  <br/> |
|<span data-ttu-id="b4fd5-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b4fd5-110">Data type:</span></span>  <br/> |<span data-ttu-id="b4fd5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b4fd5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b4fd5-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="b4fd5-112">Area:</span></span>  <br/> |<span data-ttu-id="b4fd5-113">Courier électronique</span><span class="sxs-lookup"><span data-stu-id="b4fd5-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4fd5-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b4fd5-114">Remarks</span></span>

<span data-ttu-id="b4fd5-115">Cette propriété est retournée par le MTA en cas de réussite de l’envoi du message.</span><span class="sxs-lookup"><span data-stu-id="b4fd5-115">This property is returned by the MTA upon successful completion of message submission.</span></span> <span data-ttu-id="b4fd5-116">N’importe quel contact futur avec le MTA concernant ce message, tel que demande l’annulation, utilise l’identificateur MTS dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="b4fd5-116">Any future contact with the MTA regarding this message, such as requesting cancellation, uses the MTS identifier in this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b4fd5-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b4fd5-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b4fd5-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="b4fd5-118">Protocol specifications</span></span>

<span data-ttu-id="b4fd5-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4fd5-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4fd5-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="b4fd5-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b4fd5-121">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b4fd5-121">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b4fd5-122">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="b4fd5-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b4fd5-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b4fd5-123">Header files</span></span>

<span data-ttu-id="b4fd5-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4fd5-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="b4fd5-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b4fd5-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="b4fd5-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="b4fd5-126">Mapitags.h</span></span>
  
> <span data-ttu-id="b4fd5-127">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="b4fd5-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4fd5-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4fd5-128">See also</span></span>



[<span data-ttu-id="b4fd5-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b4fd5-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b4fd5-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b4fd5-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b4fd5-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b4fd5-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b4fd5-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="b4fd5-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

