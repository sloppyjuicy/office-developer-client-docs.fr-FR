---
title: Propriété canonique PidTagMessageDeliveryTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageDeliveryTime
api_type:
- HeaderDef
ms.assetid: 4f9d44f2-4faa-4f16-9e33-22f80c17db85
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4fd74e99a8073db03ad47292677ff98efca58af3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786221"
---
# <a name="pidtagmessagedeliverytime-canonical-property"></a><span data-ttu-id="8d141-103">Propriété canonique PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="8d141-103">PidTagMessageDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="8d141-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8d141-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8d141-105">Contient la date et l’heure quand un message a été remis.</span><span class="sxs-lookup"><span data-stu-id="8d141-105">Contains the date and time when a message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8d141-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8d141-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8d141-107">PR_MESSAGE_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="8d141-107">PR_MESSAGE_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="8d141-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="8d141-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8d141-109">0x0E06</span><span class="sxs-lookup"><span data-stu-id="8d141-109">0x0E06</span></span>  <br/> |
|<span data-ttu-id="8d141-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8d141-110">Data type:</span></span>  <br/> |<span data-ttu-id="8d141-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="8d141-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="8d141-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="8d141-112">Area:</span></span>  <br/> |<span data-ttu-id="8d141-113">Heure du message</span><span class="sxs-lookup"><span data-stu-id="8d141-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d141-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8d141-114">Remarks</span></span>

<span data-ttu-id="8d141-115">Cette propriété indique le moment où que le message a été stocké sur le serveur, plutôt que le temps de téléchargement lorsque le fournisseur de transport copié le message à partir du serveur dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="8d141-115">This property describes the time the message was stored at the server, rather than the download time when the transport provider copied the message from the server to the local store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8d141-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8d141-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8d141-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="8d141-117">Protocol specifications</span></span>

<span data-ttu-id="8d141-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8d141-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8d141-119">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="8d141-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8d141-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8d141-120">Header files</span></span>

<span data-ttu-id="8d141-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d141-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="8d141-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8d141-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="8d141-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="8d141-123">Mapitags.h</span></span>
  
> <span data-ttu-id="8d141-124">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="8d141-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d141-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d141-125">See also</span></span>



[<span data-ttu-id="8d141-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8d141-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8d141-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8d141-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8d141-128">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8d141-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8d141-129">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="8d141-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

