---
title: Propriété canonique PidTagDeliveryPoint
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliveryPoint
api_type:
- HeaderDef
ms.assetid: 715a9dbd-78f8-41e1-a76e-29448d06ec19
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 2d8157c761cd21d5c8fcdf04948646d8102e774a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580137"
---
# <a name="pidtagdeliverypoint-canonical-property"></a><span data-ttu-id="8ce43-103">Propriété canonique PidTagDeliveryPoint</span><span class="sxs-lookup"><span data-stu-id="8ce43-103">PidTagDeliveryPoint Canonical Property</span></span>

  
  
<span data-ttu-id="8ce43-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ce43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ce43-105">Spécifie la nature de l’entité fonctionnelle par lequel le message a été ou serait ont été remis au destinataire.</span><span class="sxs-lookup"><span data-stu-id="8ce43-105">Specifies the nature of the functional entity by means of which a message was or would have been delivered to the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8ce43-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8ce43-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8ce43-107">PR_DELIVERY_POINT</span><span class="sxs-lookup"><span data-stu-id="8ce43-107">PR_DELIVERY_POINT</span></span>  <br/> |
|<span data-ttu-id="8ce43-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="8ce43-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8ce43-109">0x0C07</span><span class="sxs-lookup"><span data-stu-id="8ce43-109">0x0C07</span></span>  <br/> |
|<span data-ttu-id="8ce43-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8ce43-110">Data type:</span></span>  <br/> |<span data-ttu-id="8ce43-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8ce43-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8ce43-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="8ce43-112">Area:</span></span>  <br/> |<span data-ttu-id="8ce43-113">Destinataire MAPI</span><span class="sxs-lookup"><span data-stu-id="8ce43-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ce43-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8ce43-114">Remarks</span></span>

<span data-ttu-id="8ce43-115">Cette propriété peut avoir exactement une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8ce43-115">This property can have exactly one of the following values:</span></span> 
  
<span data-ttu-id="8ce43-116">MAPI_MH_DP_ML</span><span class="sxs-lookup"><span data-stu-id="8ce43-116">MAPI_MH_DP_ML</span></span> 
  
> <span data-ttu-id="8ce43-117">Remis à une liste de distribution, une remise point qui peut à son tour distribuer le message à plusieurs destinataires.</span><span class="sxs-lookup"><span data-stu-id="8ce43-117">Delivered to a distribution list, a delivery point which in turn may distribute the message to many recipients.</span></span>
    
<span data-ttu-id="8ce43-118">MAPI_MH_DP_MS</span><span class="sxs-lookup"><span data-stu-id="8ce43-118">MAPI_MH_DP_MS</span></span> 
  
> <span data-ttu-id="8ce43-119">Remis à une banque de messages à la place de directement à un destinataire.</span><span class="sxs-lookup"><span data-stu-id="8ce43-119">Delivered to a message store instead of directly to a recipient.</span></span>
    
<span data-ttu-id="8ce43-120">MAPI_MH_DP_OTHER_AU</span><span class="sxs-lookup"><span data-stu-id="8ce43-120">MAPI_MH_DP_OTHER_AU</span></span> 
  
> <span data-ttu-id="8ce43-121">Remis à une unité d’accès (UA) autre qu’une unité d’accès remise physique (PDAU), telles qu’un système de télécopie.</span><span class="sxs-lookup"><span data-stu-id="8ce43-121">Delivered to an access unit (AU) other than a physical delivery access unit (PDAU), such as a FAX system.</span></span>
    
<span data-ttu-id="8ce43-122">MAPI_MH_DP_PDAU</span><span class="sxs-lookup"><span data-stu-id="8ce43-122">MAPI_MH_DP_PDAU</span></span> 
  
> <span data-ttu-id="8ce43-123">Remis à une unité d’accès remise physique, par exemple un opérateur postal humaine.</span><span class="sxs-lookup"><span data-stu-id="8ce43-123">Delivered to a physical delivery access unit, such as a human postal carrier.</span></span>
    
<span data-ttu-id="8ce43-124">MAPI_MH_DP_PDS_PATRON</span><span class="sxs-lookup"><span data-stu-id="8ce43-124">MAPI_MH_DP_PDS_PATRON</span></span> 
  
> <span data-ttu-id="8ce43-125">Remis à un patron remise physique du système, par exemple une boîte aux lettres postal classique.</span><span class="sxs-lookup"><span data-stu-id="8ce43-125">Delivered to a physical delivery system patron, such as a conventional postal mailbox.</span></span>
    
<span data-ttu-id="8ce43-126">MAPI_MH_DP_PRIVATE_UA</span><span class="sxs-lookup"><span data-stu-id="8ce43-126">MAPI_MH_DP_PRIVATE_UA</span></span> 
  
> <span data-ttu-id="8ce43-127">Remis à un agent utilisateur privés (UA), comme un client dans un système de messagerie en interne.</span><span class="sxs-lookup"><span data-stu-id="8ce43-127">Delivered to a private user agent (UA), such as a client in an in-house messaging system.</span></span>
    
<span data-ttu-id="8ce43-128">MAPI_MH_DP_PUBLIC_UA</span><span class="sxs-lookup"><span data-stu-id="8ce43-128">MAPI_MH_DP_PUBLIC_UA</span></span> 
  
> <span data-ttu-id="8ce43-129">Remis à un agent utilisateur public ou le fournisseur de services public.</span><span class="sxs-lookup"><span data-stu-id="8ce43-129">Delivered to a public user agent, or public service provider.</span></span>
    
<span data-ttu-id="8ce43-130">La valeur par défaut est MAPI_MH_DP_PRIVATE_UA, autrement dit, un client MAPI.</span><span class="sxs-lookup"><span data-stu-id="8ce43-130">The default value is MAPI_MH_DP_PRIVATE_UA, that is, a MAPI client.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8ce43-131">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8ce43-131">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8ce43-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8ce43-132">Header files</span></span>

<span data-ttu-id="8ce43-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8ce43-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="8ce43-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8ce43-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="8ce43-135">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="8ce43-135">Mapitags.h</span></span>
  
> <span data-ttu-id="8ce43-136">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="8ce43-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8ce43-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ce43-137">See also</span></span>



[<span data-ttu-id="8ce43-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8ce43-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8ce43-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8ce43-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8ce43-140">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8ce43-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8ce43-141">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="8ce43-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

