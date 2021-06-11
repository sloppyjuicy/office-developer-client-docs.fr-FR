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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325612"
---
# <a name="pidtagmessagedeliverytime-canonical-property"></a><span data-ttu-id="22cf1-103">Propriété canonique PidTagMessageDeliveryTime</span><span class="sxs-lookup"><span data-stu-id="22cf1-103">PidTagMessageDeliveryTime Canonical Property</span></span>

  
  
<span data-ttu-id="22cf1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22cf1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22cf1-105">Contient la date et l’heure de livraison d’un message.</span><span class="sxs-lookup"><span data-stu-id="22cf1-105">Contains the date and time when a message was delivered.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="22cf1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="22cf1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="22cf1-107">PR_MESSAGE_DELIVERY_TIME</span><span class="sxs-lookup"><span data-stu-id="22cf1-107">PR_MESSAGE_DELIVERY_TIME</span></span>  <br/> |
|<span data-ttu-id="22cf1-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="22cf1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="22cf1-109">0x0E06</span><span class="sxs-lookup"><span data-stu-id="22cf1-109">0x0E06</span></span>  <br/> |
|<span data-ttu-id="22cf1-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="22cf1-110">Data type:</span></span>  <br/> |<span data-ttu-id="22cf1-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="22cf1-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="22cf1-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="22cf1-112">Area:</span></span>  <br/> |<span data-ttu-id="22cf1-113">Heure du message</span><span class="sxs-lookup"><span data-stu-id="22cf1-113">Message time</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22cf1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="22cf1-114">Remarks</span></span>

<span data-ttu-id="22cf1-115">Cette propriété décrit l’heure à partir de quel moment le message a été stocké sur le serveur, plutôt que l’heure de téléchargement où le fournisseur de transport a copié le message du serveur vers le magasin local.</span><span class="sxs-lookup"><span data-stu-id="22cf1-115">This property describes the time the message was stored at the server, rather than the download time when the transport provider copied the message from the server to the local store.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="22cf1-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="22cf1-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="22cf1-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="22cf1-117">Protocol specifications</span></span>

<span data-ttu-id="22cf1-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="22cf1-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="22cf1-119">Spécifie les propriétés et opérations autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="22cf1-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="22cf1-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="22cf1-120">Header files</span></span>

<span data-ttu-id="22cf1-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="22cf1-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="22cf1-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="22cf1-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="22cf1-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="22cf1-123">Mapitags.h</span></span>
  
> <span data-ttu-id="22cf1-124">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="22cf1-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="22cf1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22cf1-125">See also</span></span>



[<span data-ttu-id="22cf1-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="22cf1-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="22cf1-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="22cf1-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="22cf1-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="22cf1-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="22cf1-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="22cf1-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

