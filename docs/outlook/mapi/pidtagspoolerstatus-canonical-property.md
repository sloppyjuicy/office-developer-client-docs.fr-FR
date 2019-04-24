---
title: Propriété canonique PidTagSpoolerStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSpoolerStatus
api_type:
- COM
ms.assetid: a10d86fc-3a73-49dc-b974-ed852ec715e9
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 426d26cae147faf3f843ac547de9d205d766ac44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348208"
---
# <a name="pidtagspoolerstatus-canonical-property"></a><span data-ttu-id="78ee3-103">Propriété canonique PidTagSpoolerStatus</span><span class="sxs-lookup"><span data-stu-id="78ee3-103">PidTagSpoolerStatus Canonical Property</span></span>

  
  
<span data-ttu-id="78ee3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78ee3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78ee3-105">Contient l'état du message en fonction des informations qui sont disponibles pour le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="78ee3-105">Contains the status of the message based on information that is available to the MAPI spooler.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="78ee3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="78ee3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="78ee3-107">PR_SPOOLER_STATUS</span><span class="sxs-lookup"><span data-stu-id="78ee3-107">PR_SPOOLER_STATUS</span></span>  <br/> |
|<span data-ttu-id="78ee3-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="78ee3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="78ee3-109">0x0E10</span><span class="sxs-lookup"><span data-stu-id="78ee3-109">0x0E10</span></span>  <br/> |
|<span data-ttu-id="78ee3-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="78ee3-110">Data type:</span></span>  <br/> |<span data-ttu-id="78ee3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="78ee3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="78ee3-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="78ee3-112">Area:</span></span>  <br/> |<span data-ttu-id="78ee3-113">MAPI non transmissible</span><span class="sxs-lookup"><span data-stu-id="78ee3-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78ee3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="78ee3-114">Remarks</span></span>

<span data-ttu-id="78ee3-115">Cette propriété est calculée par MAPI sur les objets message.</span><span class="sxs-lookup"><span data-stu-id="78ee3-115">This property is computed by MAPI on message objects.</span></span>
  
<span data-ttu-id="78ee3-116">Cette propriété s'affiche sur les messages entrants uniquement et est réservée dans tous les autres cas.</span><span class="sxs-lookup"><span data-stu-id="78ee3-116">This property appears on inbound messages only and is reserved in all other cases.</span></span> <span data-ttu-id="78ee3-117">Il indique si un message a été remis ou non à son emplacement final ou si un fournisseur de service de raccordement de messagerie peut avoir supprimé le message lors de son reroutage.</span><span class="sxs-lookup"><span data-stu-id="78ee3-117">It indicates whether or not a message has been delivered to its final location or whether a messaging hook provider potentially deleted the message while rerouting it.</span></span>
  
<span data-ttu-id="78ee3-118">Les applications clientes ne doivent jamais définir cette propriété.</span><span class="sxs-lookup"><span data-stu-id="78ee3-118">Client applications should never set this property.</span></span> <span data-ttu-id="78ee3-119">Pour un message entrant, un client ou un fournisseur de services peut appeler [IMAPIProp:: GetProps](imapiprop-getprops.md) sur cette propriété pour déterminer l'état du message.</span><span class="sxs-lookup"><span data-stu-id="78ee3-119">For an inbound message, a client or service provider can call [IMAPIProp::GetProps](imapiprop-getprops.md) on this property to determine the message status.</span></span> <span data-ttu-id="78ee3-120">La valeur S_OK indique que le message a bien été remis à la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="78ee3-120">The value S_OK indicates that the message was successfully delivered to the message store.</span></span> <span data-ttu-id="78ee3-121">La valeur MAPI_E_OBJECT_DELETED indique que le message a été supprimé et qu'il n'a jamais été validé dans la Banque.</span><span class="sxs-lookup"><span data-stu-id="78ee3-121">The value MAPI_E_OBJECT_DELETED indicates that the message was deleted and was never committed to the store.</span></span> 
  
<span data-ttu-id="78ee3-122">Les fournisseurs de banques de messages doivent prendre en charge cette propriété sur les messages, les tables de destinataires et la table de file d'attente sortante.</span><span class="sxs-lookup"><span data-stu-id="78ee3-122">Message store providers should support this property on messages, recipient tables, and the outgoing queue table.</span></span> <span data-ttu-id="78ee3-123">Les clients et les fournisseurs doivent être en mesure de définir des colonnes sur la table de file d'attente sortante et de restreindre en fonction de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="78ee3-123">Clients and providers should be able to set columns on the outgoing queue table and restrict based on this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="78ee3-124">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="78ee3-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="78ee3-125">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="78ee3-125">Header files</span></span>

<span data-ttu-id="78ee3-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="78ee3-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="78ee3-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="78ee3-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="78ee3-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="78ee3-128">Mapitags.h</span></span>
  
> <span data-ttu-id="78ee3-129">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="78ee3-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="78ee3-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78ee3-130">See also</span></span>



[<span data-ttu-id="78ee3-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="78ee3-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="78ee3-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="78ee3-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="78ee3-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="78ee3-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="78ee3-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="78ee3-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

