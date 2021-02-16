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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e18b08bcbd76cacf7dbb5b5fd36d80d5f266364d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439421"
---
# <a name="pidtagdeliverypoint-canonical-property"></a><span data-ttu-id="92a47-103">Propriété canonique PidTagDeliveryPoint</span><span class="sxs-lookup"><span data-stu-id="92a47-103">PidTagDeliveryPoint Canonical Property</span></span>

  
  
<span data-ttu-id="92a47-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92a47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92a47-105">Spécifie la nature de l’entité fonctionnelle au moyen de laquelle un message a été ou aurait été remis au destinataire.</span><span class="sxs-lookup"><span data-stu-id="92a47-105">Specifies the nature of the functional entity by means of which a message was or would have been delivered to the recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92a47-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="92a47-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="92a47-107">PR_DELIVERY_POINT</span><span class="sxs-lookup"><span data-stu-id="92a47-107">PR_DELIVERY_POINT</span></span>  <br/> |
|<span data-ttu-id="92a47-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="92a47-108">Identifier:</span></span>  <br/> |<span data-ttu-id="92a47-109">0x0C07</span><span class="sxs-lookup"><span data-stu-id="92a47-109">0x0C07</span></span>  <br/> |
|<span data-ttu-id="92a47-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="92a47-110">Data type:</span></span>  <br/> |<span data-ttu-id="92a47-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="92a47-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="92a47-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="92a47-112">Area:</span></span>  <br/> |<span data-ttu-id="92a47-113">Destinataire MAPI</span><span class="sxs-lookup"><span data-stu-id="92a47-113">MAPI recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92a47-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="92a47-114">Remarks</span></span>

<span data-ttu-id="92a47-115">Cette propriété peut avoir exactement l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="92a47-115">This property can have exactly one of the following values:</span></span> 
  
<span data-ttu-id="92a47-116">MAPI_MH_DP_ML</span><span class="sxs-lookup"><span data-stu-id="92a47-116">MAPI_MH_DP_ML</span></span> 
  
> <span data-ttu-id="92a47-117">Remis à une liste de distribution, un point de remise qui à son tour peut distribuer le message à de nombreux destinataires.</span><span class="sxs-lookup"><span data-stu-id="92a47-117">Delivered to a distribution list, a delivery point which in turn may distribute the message to many recipients.</span></span>
    
<span data-ttu-id="92a47-118">MAPI_MH_DP_MS</span><span class="sxs-lookup"><span data-stu-id="92a47-118">MAPI_MH_DP_MS</span></span> 
  
> <span data-ttu-id="92a47-119">Remis à une magasin de messages au lieu d’être directement remis à un destinataire.</span><span class="sxs-lookup"><span data-stu-id="92a47-119">Delivered to a message store instead of directly to a recipient.</span></span>
    
<span data-ttu-id="92a47-120">MAPI_MH_DP_OTHER_AU</span><span class="sxs-lookup"><span data-stu-id="92a47-120">MAPI_MH_DP_OTHER_AU</span></span> 
  
> <span data-ttu-id="92a47-121">Remis à une unité d’accès (AU) autre qu’une unité d’accès de remise physique (PDAU), telle qu’un système de télécopie.</span><span class="sxs-lookup"><span data-stu-id="92a47-121">Delivered to an access unit (AU) other than a physical delivery access unit (PDAU), such as a FAX system.</span></span>
    
<span data-ttu-id="92a47-122">MAPI_MH_DP_PDAU</span><span class="sxs-lookup"><span data-stu-id="92a47-122">MAPI_MH_DP_PDAU</span></span> 
  
> <span data-ttu-id="92a47-123">Remis à une unité d’accès de remise physique, telle qu’un opérateur postal humain.</span><span class="sxs-lookup"><span data-stu-id="92a47-123">Delivered to a physical delivery access unit, such as a human postal carrier.</span></span>
    
<span data-ttu-id="92a47-124">MAPI_MH_DP_PDS_PATRON</span><span class="sxs-lookup"><span data-stu-id="92a47-124">MAPI_MH_DP_PDS_PATRON</span></span> 
  
> <span data-ttu-id="92a47-125">Remis à un protecteur de système de remise physique, tel qu’une boîte aux lettres postale conventionnelle.</span><span class="sxs-lookup"><span data-stu-id="92a47-125">Delivered to a physical delivery system patron, such as a conventional postal mailbox.</span></span>
    
<span data-ttu-id="92a47-126">MAPI_MH_DP_PRIVATE_UA</span><span class="sxs-lookup"><span data-stu-id="92a47-126">MAPI_MH_DP_PRIVATE_UA</span></span> 
  
> <span data-ttu-id="92a47-127">Remis à un agent utilisateur privé (UA), tel qu’un client dans un système de messagerie interne.</span><span class="sxs-lookup"><span data-stu-id="92a47-127">Delivered to a private user agent (UA), such as a client in an in-house messaging system.</span></span>
    
<span data-ttu-id="92a47-128">MAPI_MH_DP_PUBLIC_UA</span><span class="sxs-lookup"><span data-stu-id="92a47-128">MAPI_MH_DP_PUBLIC_UA</span></span> 
  
> <span data-ttu-id="92a47-129">Remis à un agent utilisateur public ou à un fournisseur de services publics.</span><span class="sxs-lookup"><span data-stu-id="92a47-129">Delivered to a public user agent, or public service provider.</span></span>
    
<span data-ttu-id="92a47-130">La valeur par défaut est MAPI_MH_DP_PRIVATE_UA, c’est-à-dire, un client MAPI.</span><span class="sxs-lookup"><span data-stu-id="92a47-130">The default value is MAPI_MH_DP_PRIVATE_UA, that is, a MAPI client.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="92a47-131">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="92a47-131">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="92a47-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="92a47-132">Header files</span></span>

<span data-ttu-id="92a47-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="92a47-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="92a47-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="92a47-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="92a47-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="92a47-135">Mapitags.h</span></span>
  
> <span data-ttu-id="92a47-136">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="92a47-136">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="92a47-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92a47-137">See also</span></span>



[<span data-ttu-id="92a47-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="92a47-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="92a47-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="92a47-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="92a47-140">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="92a47-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="92a47-141">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="92a47-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

