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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b635ad72acc2bd98ca0c207dea71ea2df757e22b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593934"
---
# <a name="pidtagmessagedeliverytime-canonical-property"></a><span data-ttu-id="42bb1-103">Propriété canonique PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="42bb1-103">PidTagMessageDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="42bb1-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42bb1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42bb1-105">Contient la date et l’heure quand un message a été remis.</span><span class="sxs-lookup"><span data-stu-id="42bb1-105">Contains the date and time when a message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="42bb1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="42bb1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="42bb1-107">PR_MESSAGE_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="42bb1-107">PR_MESSAGE_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="42bb1-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="42bb1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="42bb1-109">0x0E06</span><span class="sxs-lookup"><span data-stu-id="42bb1-109">0x0E06</span></span>  <br/> |
|<span data-ttu-id="42bb1-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="42bb1-110">Data type:</span></span>  <br/> |<span data-ttu-id="42bb1-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="42bb1-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="42bb1-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="42bb1-112">Area:</span></span>  <br/> |<span data-ttu-id="42bb1-113">Heure du message</span><span class="sxs-lookup"><span data-stu-id="42bb1-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42bb1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="42bb1-114">Remarks</span></span>

<span data-ttu-id="42bb1-115">Cette propriété indique le moment où que le message a été stocké sur le serveur, plutôt que le temps de téléchargement lorsque le fournisseur de transport copié le message à partir du serveur dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="42bb1-115">This property describes the time the message was stored at the server, rather than the download time when the transport provider copied the message from the server to the local store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="42bb1-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="42bb1-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="42bb1-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="42bb1-117">Protocol specifications</span></span>

<span data-ttu-id="42bb1-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="42bb1-118">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="42bb1-119">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="42bb1-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="42bb1-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="42bb1-120">Header files</span></span>

<span data-ttu-id="42bb1-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="42bb1-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="42bb1-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="42bb1-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="42bb1-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="42bb1-123">Mapitags.h</span></span>
  
> <span data-ttu-id="42bb1-124">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="42bb1-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="42bb1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42bb1-125">See also</span></span>



[<span data-ttu-id="42bb1-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="42bb1-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="42bb1-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="42bb1-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="42bb1-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="42bb1-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="42bb1-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="42bb1-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

