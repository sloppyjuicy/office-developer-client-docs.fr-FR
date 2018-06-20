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
ms.openlocfilehash: df52f668e91b707c0436b394186b27fdbb3a5dbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786820"
---
# <a name="pidtagspoolerstatus-canonical-property"></a><span data-ttu-id="72a6b-103">Propriété canonique PidTagSpoolerStatus</span><span class="sxs-lookup"><span data-stu-id="72a6b-103">PidTagSpoolerStatus Canonical Property</span></span>

  
  
<span data-ttu-id="72a6b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="72a6b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="72a6b-105">Indique le statut du message en fonction des informations qui est disponibles pour le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="72a6b-105">Contains the status of the message based on information that is available to the MAPI spooler.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="72a6b-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="72a6b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="72a6b-107">PR_SPOOLER_STATUS</span><span class="sxs-lookup"><span data-stu-id="72a6b-107">PR_SPOOLER_STATUS</span></span>  <br/> |
|<span data-ttu-id="72a6b-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="72a6b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="72a6b-109">0x0E10</span><span class="sxs-lookup"><span data-stu-id="72a6b-109">0x0E10</span></span>  <br/> |
|<span data-ttu-id="72a6b-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="72a6b-110">Data type:</span></span>  <br/> |<span data-ttu-id="72a6b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="72a6b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="72a6b-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="72a6b-112">Area:</span></span>  <br/> |<span data-ttu-id="72a6b-113">MAPI non transmissible</span><span class="sxs-lookup"><span data-stu-id="72a6b-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72a6b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="72a6b-114">Remarks</span></span>

<span data-ttu-id="72a6b-115">Cette propriété est calculée par MAPI sur les objets de message.</span><span class="sxs-lookup"><span data-stu-id="72a6b-115">This property is computed by MAPI on message objects.</span></span>
  
<span data-ttu-id="72a6b-116">Cette propriété s’affiche uniquement les messages entrants et est réservée dans tous les autres cas.</span><span class="sxs-lookup"><span data-stu-id="72a6b-116">This property appears on inbound messages only and is reserved in all other cases.</span></span> <span data-ttu-id="72a6b-117">Il indique si un message a été remis à son emplacement final ou si un fournisseur de messagerie crochet potentiellement a supprimé le message lors de son réacheminement.</span><span class="sxs-lookup"><span data-stu-id="72a6b-117">It indicates whether or not a message has been delivered to its final location or whether a messaging hook provider potentially deleted the message while rerouting it.</span></span>
  
<span data-ttu-id="72a6b-118">Applications clientes ne doivent jamais définir cette propriété.</span><span class="sxs-lookup"><span data-stu-id="72a6b-118">Client applications should never set this property.</span></span> <span data-ttu-id="72a6b-119">Pour un message entrant, un client ou fournisseur de services peut appeler [IMAPIProp::GetProps](imapiprop-getprops.md) sur cette propriété pour déterminer le statut du message.</span><span class="sxs-lookup"><span data-stu-id="72a6b-119">For an inbound message, a client or service provider can call [IMAPIProp::GetProps](imapiprop-getprops.md) on this property to determine the message status.</span></span> <span data-ttu-id="72a6b-120">La valeur S_OK indique que le message a bien été remis à la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="72a6b-120">The value S_OK indicates that the message was successfully delivered to the message store.</span></span> <span data-ttu-id="72a6b-121">La valeur MAPI_E_OBJECT_DELETED indique que le message a été supprimé et n’a jamais validé dans le magasin.</span><span class="sxs-lookup"><span data-stu-id="72a6b-121">The value MAPI_E_OBJECT_DELETED indicates that the message was deleted and was never committed to the store.</span></span> 
  
<span data-ttu-id="72a6b-122">Fournisseurs de magasins de message doivent prendre en charge cette propriété dans les messages, les tables de destinataires et la table sortant de la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="72a6b-122">Message store providers should support this property on messages, recipient tables, and the outgoing queue table.</span></span> <span data-ttu-id="72a6b-123">Fournisseurs et clients doivent être en mesure de définir les colonnes de la table sortant de la file d’attente et de restreindre en fonction de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="72a6b-123">Clients and providers should be able to set columns on the outgoing queue table and restrict based on this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="72a6b-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="72a6b-124">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="72a6b-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="72a6b-125">Header files</span></span>

<span data-ttu-id="72a6b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="72a6b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="72a6b-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="72a6b-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="72a6b-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="72a6b-128">Mapitags.h</span></span>
  
> <span data-ttu-id="72a6b-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="72a6b-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="72a6b-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72a6b-130">See also</span></span>



[<span data-ttu-id="72a6b-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="72a6b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="72a6b-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="72a6b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="72a6b-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="72a6b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="72a6b-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="72a6b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

