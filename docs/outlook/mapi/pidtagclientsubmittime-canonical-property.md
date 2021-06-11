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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 851441e419c17d8f5fef27c785ea4b829a4ae443
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345716"
---
# <a name="pidtagclientsubmittime-canonical-property"></a><span data-ttu-id="afdf0-103">Propriété canonique PidTagClientSubmitTime</span><span class="sxs-lookup"><span data-stu-id="afdf0-103">PidTagClientSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="afdf0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="afdf0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="afdf0-105">Contient la date et l’heure à laquelle l’expéditeur du message a envoyé un message.</span><span class="sxs-lookup"><span data-stu-id="afdf0-105">Contains the date and time the message sender submitted a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="afdf0-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="afdf0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="afdf0-107">PR_CLIENT_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="afdf0-107">PR_CLIENT_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="afdf0-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="afdf0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="afdf0-109">0x0039</span><span class="sxs-lookup"><span data-stu-id="afdf0-109">0x0039</span></span>  <br/> |
|<span data-ttu-id="afdf0-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="afdf0-110">Data type:</span></span>  <br/> |<span data-ttu-id="afdf0-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="afdf0-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="afdf0-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="afdf0-112">Area:</span></span>  <br/> |<span data-ttu-id="afdf0-113">Heure du message</span><span class="sxs-lookup"><span data-stu-id="afdf0-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="afdf0-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="afdf0-114">Remarks</span></span>

<span data-ttu-id="afdf0-115">Le fournisseur de la **PR_CLIENT_SUBMIT_TIME** définit l’heure à l’heure à PR_CLIENT_SUBMIT_TIME’application cliente appelée [IMessage::SubmitMessage](imessage-submitmessage.md).</span><span class="sxs-lookup"><span data-stu-id="afdf0-115">The store provider sets **PR_CLIENT_SUBMIT_TIME** to the time that the client application called [IMessage::SubmitMessage](imessage-submitmessage.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="afdf0-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="afdf0-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="afdf0-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="afdf0-117">Protocol specifications</span></span>

<span data-ttu-id="afdf0-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="afdf0-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="afdf0-119">Gère les objets message et pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="afdf0-119">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="afdf0-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="afdf0-120">Header files</span></span>

<span data-ttu-id="afdf0-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="afdf0-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="afdf0-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="afdf0-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="afdf0-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="afdf0-123">Mapitags.h</span></span>
  
> <span data-ttu-id="afdf0-124">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="afdf0-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="afdf0-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="afdf0-125">See also</span></span>



[<span data-ttu-id="afdf0-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="afdf0-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="afdf0-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="afdf0-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="afdf0-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="afdf0-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="afdf0-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="afdf0-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

