---
title: Propriété canonique PidTagClientSubmitTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagClientSubmitTime
api_type:
- HeaderDef
ms.assetid: d46e1063-6421-410d-a445-7477fea42089
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 8c7ca5b2b6f5f3131c2fcb70ff0043825a68a91f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580123"
---
# <a name="pidtagclientsubmittime-canonical-property"></a><span data-ttu-id="ab051-103">Propriété canonique PidTagClientSubmitTime</span><span class="sxs-lookup"><span data-stu-id="ab051-103">PidTagClientSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="ab051-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab051-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab051-105">Contient la date et l’heure à laquelle que l’expéditeur du message envoyé un message.</span><span class="sxs-lookup"><span data-stu-id="ab051-105">Contains the date and time the message sender submitted a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab051-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ab051-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ab051-107">PR_CLIENT_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="ab051-107">PR_CLIENT_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="ab051-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ab051-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ab051-109">0x0039</span><span class="sxs-lookup"><span data-stu-id="ab051-109">0x0039</span></span>  <br/> |
|<span data-ttu-id="ab051-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ab051-110">Data type:</span></span>  <br/> |<span data-ttu-id="ab051-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ab051-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="ab051-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ab051-112">Area:</span></span>  <br/> |<span data-ttu-id="ab051-113">Heure du message</span><span class="sxs-lookup"><span data-stu-id="ab051-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab051-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ab051-114">Remarks</span></span>

<span data-ttu-id="ab051-115">Le fournisseur de banque définit l’heure à laquelle l’application cliente appelée [IMessage::SubmitMessage](imessage-submitmessage.md) **PR_CLIENT_SUBMIT_TIME** .</span><span class="sxs-lookup"><span data-stu-id="ab051-115">The store provider sets **PR_CLIENT_SUBMIT_TIME** to the time that the client application called [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ab051-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ab051-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ab051-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="ab051-117">Protocol specifications</span></span>

<span data-ttu-id="ab051-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ab051-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ab051-119">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="ab051-119">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ab051-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ab051-120">Header files</span></span>

<span data-ttu-id="ab051-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ab051-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="ab051-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ab051-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="ab051-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ab051-123">Mapitags.h</span></span>
  
> <span data-ttu-id="ab051-124">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="ab051-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ab051-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab051-125">See also</span></span>



[<span data-ttu-id="ab051-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ab051-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ab051-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ab051-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ab051-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ab051-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ab051-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ab051-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

