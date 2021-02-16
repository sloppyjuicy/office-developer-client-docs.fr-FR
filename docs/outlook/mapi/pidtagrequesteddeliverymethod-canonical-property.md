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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ecfed5684ba2166c1c00c1fd07fa074b4ce9fd79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434073"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a><span data-ttu-id="3620c-103">Propriété canonique PidTagRequestedDeliveryMethod</span><span class="sxs-lookup"><span data-stu-id="3620c-103">PidTagRequestedDeliveryMethod Canonical Property</span></span>

  
  
<span data-ttu-id="3620c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3620c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3620c-105">Cette propriété contient un tableau binaire de méthodes de remise (fournisseurs de services), dans l’ordre des préférences de l’expéditeur d’un message.</span><span class="sxs-lookup"><span data-stu-id="3620c-105">This property contains a binary array of delivery methods (service providers), in the order of a message sender's preference.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3620c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3620c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3620c-107">PR_REQUESTED_DELIVERY_METHOD</span><span class="sxs-lookup"><span data-stu-id="3620c-107">PR_REQUESTED_DELIVERY_METHOD</span></span>  <br/> |
|<span data-ttu-id="3620c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3620c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3620c-109">0x0C18</span><span class="sxs-lookup"><span data-stu-id="3620c-109">0x0C18</span></span>  <br/> |
|<span data-ttu-id="3620c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3620c-110">Data type:</span></span>  <br/> |<span data-ttu-id="3620c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3620c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3620c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="3620c-112">Area:</span></span>  <br/> |<span data-ttu-id="3620c-113">Destinataire MAPI</span><span class="sxs-lookup"><span data-stu-id="3620c-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3620c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3620c-114">Remarks</span></span>

<span data-ttu-id="3620c-115">Le tableau contenu dans cette propriété se compose d’identificateurs ASN.1 pour chacun des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="3620c-115">The array contained in the this property consists of ASN.1 identifiers for each of the service providers.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3620c-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3620c-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3620c-117">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3620c-117">Header files</span></span>

<span data-ttu-id="3620c-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3620c-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="3620c-119">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3620c-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="3620c-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3620c-120">Mapitags.h</span></span>
  
> <span data-ttu-id="3620c-121">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="3620c-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3620c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3620c-122">See also</span></span>



[<span data-ttu-id="3620c-123">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3620c-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3620c-124">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3620c-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3620c-125">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3620c-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3620c-126">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="3620c-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

