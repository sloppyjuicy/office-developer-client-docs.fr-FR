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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 723affa054cb35a9cc7a2ee28e051e3b9a6d04e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329399"
---
# <a name="pidtagmessagesubmissionid-canonical-property"></a><span data-ttu-id="9ffa6-103">Propriété canonique PidTagMessageSubmissionId</span><span class="sxs-lookup"><span data-stu-id="9ffa6-103">PidTagMessageSubmissionId Canonical Property</span></span>

  
  
<span data-ttu-id="9ffa6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ffa6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ffa6-105">Contient un identificateur de système de transfert de messages (MTS) pour l’agent de transfert de messages (MTA).</span><span class="sxs-lookup"><span data-stu-id="9ffa6-105">Contains a message transfer system (MTS) identifier for the message transfer agent (MTA).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9ffa6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9ffa6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ffa6-107">PR_MESSAGE_SUBMISSION_ID</span><span class="sxs-lookup"><span data-stu-id="9ffa6-107">PR_MESSAGE_SUBMISSION_ID</span></span>  <br/> |
|<span data-ttu-id="9ffa6-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9ffa6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9ffa6-109">0x0047</span><span class="sxs-lookup"><span data-stu-id="9ffa6-109">0x0047</span></span>  <br/> |
|<span data-ttu-id="9ffa6-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9ffa6-110">Data type:</span></span>  <br/> |<span data-ttu-id="9ffa6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9ffa6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9ffa6-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9ffa6-112">Area:</span></span>  <br/> |<span data-ttu-id="9ffa6-113">E-mail</span><span class="sxs-lookup"><span data-stu-id="9ffa6-113">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ffa6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9ffa6-114">Remarks</span></span>

<span data-ttu-id="9ffa6-115">Cette propriété est renvoyée par le MTA à la fin de l’envoi du message.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-115">This property is returned by the MTA upon successful completion of message submission.</span></span> <span data-ttu-id="9ffa6-116">Tout contact futur avec le MTA concernant ce message, tel que la demande d’annulation, utilise l’identificateur MTS dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-116">Any future contact with the MTA regarding this message, such as requesting cancellation, uses the MTS identifier in this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9ffa6-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9ffa6-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9ffa6-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="9ffa6-118">Protocol specifications</span></span>

<span data-ttu-id="9ffa6-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ffa6-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ffa6-120">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9ffa6-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ffa6-121">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ffa6-122">Encode et décode les objets de message et de pièce jointe dans une représentation de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-122">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9ffa6-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9ffa6-123">Header files</span></span>

<span data-ttu-id="9ffa6-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9ffa6-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ffa6-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="9ffa6-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9ffa6-126">Mapitags.h</span></span>
  
> <span data-ttu-id="9ffa6-127">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="9ffa6-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ffa6-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ffa6-128">See also</span></span>



[<span data-ttu-id="9ffa6-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9ffa6-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ffa6-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9ffa6-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ffa6-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9ffa6-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ffa6-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9ffa6-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

