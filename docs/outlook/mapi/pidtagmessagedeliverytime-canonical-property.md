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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8ebaea7fb6888e51ee1ef658db53dcf3050644da
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397344"
---
# <a name="pidtagmessagedeliverytime-canonical-property"></a><span data-ttu-id="1f38e-103">Propriété canonique PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="1f38e-103">PidTagMessageDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="1f38e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f38e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f38e-105">Contient la date et l’heure quand un message a été remis.</span><span class="sxs-lookup"><span data-stu-id="1f38e-105">Contains the date and time when a message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1f38e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1f38e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f38e-107">PR_MESSAGE_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="1f38e-107">PR_MESSAGE_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="1f38e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1f38e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1f38e-109">0x0E06</span><span class="sxs-lookup"><span data-stu-id="1f38e-109">0x0E06</span></span>  <br/> |
|<span data-ttu-id="1f38e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1f38e-110">Data type:</span></span>  <br/> |<span data-ttu-id="1f38e-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="1f38e-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="1f38e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="1f38e-112">Area:</span></span>  <br/> |<span data-ttu-id="1f38e-113">Heure du message</span><span class="sxs-lookup"><span data-stu-id="1f38e-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f38e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1f38e-114">Remarks</span></span>

<span data-ttu-id="1f38e-115">Cette propriété indique le moment où que le message a été stocké sur le serveur, plutôt que le temps de téléchargement lorsque le fournisseur de transport copié le message à partir du serveur dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="1f38e-115">This property describes the time the message was stored at the server, rather than the download time when the transport provider copied the message from the server to the local store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1f38e-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1f38e-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1f38e-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="1f38e-117">Protocol specifications</span></span>

<span data-ttu-id="1f38e-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f38e-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f38e-119">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="1f38e-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1f38e-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1f38e-120">Header files</span></span>

<span data-ttu-id="1f38e-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f38e-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f38e-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1f38e-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="1f38e-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="1f38e-123">Mapitags.h</span></span>
  
> <span data-ttu-id="1f38e-124">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="1f38e-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f38e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f38e-125">See also</span></span>



[<span data-ttu-id="1f38e-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1f38e-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f38e-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1f38e-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f38e-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1f38e-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f38e-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="1f38e-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

