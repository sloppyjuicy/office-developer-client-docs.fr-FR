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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f18d726c1b06a6fb7f79964165bbdb9074a6d4d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571366"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a><span data-ttu-id="a4d10-103">Propriété canonique PidTagRequestedDeliveryMethod</span><span class="sxs-lookup"><span data-stu-id="a4d10-103">PidTagRequestedDeliveryMethod Canonical Property</span></span>

  
  
<span data-ttu-id="a4d10-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4d10-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4d10-105">Cette propriété contient un tableau binaire de livraison (fournisseurs de services), par ordre de préférence de l’expéditeur d’un message.</span><span class="sxs-lookup"><span data-stu-id="a4d10-105">This property contains a binary array of delivery methods (service providers), in the order of a message sender's preference.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a4d10-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a4d10-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a4d10-107">PR_REQUESTED_DELIVERY_METHOD</span><span class="sxs-lookup"><span data-stu-id="a4d10-107">PR_REQUESTED_DELIVERY_METHOD</span></span>  <br/> |
|<span data-ttu-id="a4d10-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a4d10-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a4d10-109">0x0C18</span><span class="sxs-lookup"><span data-stu-id="a4d10-109">0x0C18</span></span>  <br/> |
|<span data-ttu-id="a4d10-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a4d10-110">Data type:</span></span>  <br/> |<span data-ttu-id="a4d10-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a4d10-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a4d10-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a4d10-112">Area:</span></span>  <br/> |<span data-ttu-id="a4d10-113">Destinataire MAPI</span><span class="sxs-lookup"><span data-stu-id="a4d10-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a4d10-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a4d10-114">Remarks</span></span>

<span data-ttu-id="a4d10-115">Le tableau contenu dans cette propriété se compose d’identificateurs ASN.1 pour chacun des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="a4d10-115">The array contained in the this property consists of ASN.1 identifiers for each of the service providers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a4d10-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a4d10-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="a4d10-117">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="a4d10-117">Header files</span></span>

<span data-ttu-id="a4d10-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a4d10-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="a4d10-119">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a4d10-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="a4d10-120">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="a4d10-120">Mapitags.h</span></span>
  
> <span data-ttu-id="a4d10-121">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="a4d10-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a4d10-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4d10-122">See also</span></span>



[<span data-ttu-id="a4d10-123">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a4d10-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a4d10-124">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a4d10-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a4d10-125">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a4d10-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a4d10-126">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a4d10-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

