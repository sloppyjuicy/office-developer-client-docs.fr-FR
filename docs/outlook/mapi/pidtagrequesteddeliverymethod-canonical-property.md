---
title: Propriété canonique PidTagRequestedDeliveryMethod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRequestedDeliveryMethod
api_type:
- COM
ms.assetid: cc55089b-e389-405e-8174-f5b5ec352f78
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ecfed5684ba2166c1c00c1fd07fa074b4ce9fd79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331415"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a><span data-ttu-id="22fe3-103">Propriété canonique PidTagRequestedDeliveryMethod</span><span class="sxs-lookup"><span data-stu-id="22fe3-103">PidTagRequestedDeliveryMethod Canonical Property</span></span>

  
  
<span data-ttu-id="22fe3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22fe3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22fe3-105">Cette propriété contient un tableau binaire des méthodes de remise (fournisseurs de services), dans l'ordre de préférence de l'expéditeur d'un message.</span><span class="sxs-lookup"><span data-stu-id="22fe3-105">This property contains a binary array of delivery methods (service providers), in the order of a message sender's preference.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="22fe3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="22fe3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="22fe3-107">PR_REQUESTED_DELIVERY_METHOD</span><span class="sxs-lookup"><span data-stu-id="22fe3-107">PR_REQUESTED_DELIVERY_METHOD</span></span>  <br/> |
|<span data-ttu-id="22fe3-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="22fe3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="22fe3-109">0x0C18</span><span class="sxs-lookup"><span data-stu-id="22fe3-109">0x0C18</span></span>  <br/> |
|<span data-ttu-id="22fe3-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="22fe3-110">Data type:</span></span>  <br/> |<span data-ttu-id="22fe3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="22fe3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="22fe3-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="22fe3-112">Area:</span></span>  <br/> |<span data-ttu-id="22fe3-113">Destinataire MAPI</span><span class="sxs-lookup"><span data-stu-id="22fe3-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22fe3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="22fe3-114">Remarks</span></span>

<span data-ttu-id="22fe3-115">Le tableau contenu dans cette propriété est composé des identificateurs ASN. 1 pour chacun des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="22fe3-115">The array contained in the this property consists of ASN.1 identifiers for each of the service providers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="22fe3-116">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="22fe3-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="22fe3-117">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="22fe3-117">Header files</span></span>

<span data-ttu-id="22fe3-118">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="22fe3-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="22fe3-119">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="22fe3-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="22fe3-120">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="22fe3-120">Mapitags.h</span></span>
  
> <span data-ttu-id="22fe3-121">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="22fe3-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="22fe3-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22fe3-122">See also</span></span>



[<span data-ttu-id="22fe3-123">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="22fe3-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="22fe3-124">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="22fe3-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="22fe3-125">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="22fe3-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="22fe3-126">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="22fe3-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

