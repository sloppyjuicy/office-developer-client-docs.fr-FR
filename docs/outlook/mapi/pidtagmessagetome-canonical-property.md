---
title: Propriété canonique PidTagMessageToMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToMe
api_type:
- HeaderDef
ms.assetid: aeb0fa71-f471-46c5-ad9c-f8afb3fed533
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 51a8f1768f9b4ed859989058c66044c807068386
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583931"
---
# <a name="pidtagmessagetome-canonical-property"></a><span data-ttu-id="46be1-103">Propriété canonique PidTagMessageToMe</span><span class="sxs-lookup"><span data-stu-id="46be1-103">PidTagMessageToMe Canonical Property</span></span>

  
  
<span data-ttu-id="46be1-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46be1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46be1-105">Contient la valeur TRUE si cet utilisateur de messagerie est nommé spécifiquement comme (destinataire du message à) principale et ne fait pas partie d’une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="46be1-105">Contains TRUE if this messaging user is specifically named as a primary (To) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="46be1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="46be1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="46be1-107">PR_MESSAGE_TO_ME</span><span class="sxs-lookup"><span data-stu-id="46be1-107">PR_MESSAGE_TO_ME</span></span>  <br/> |
|<span data-ttu-id="46be1-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="46be1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="46be1-109">0x0057</span><span class="sxs-lookup"><span data-stu-id="46be1-109">0x0057</span></span>  <br/> |
|<span data-ttu-id="46be1-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="46be1-110">Data type:</span></span>  <br/> |<span data-ttu-id="46be1-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="46be1-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="46be1-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="46be1-112">Area:</span></span>  <br/> |<span data-ttu-id="46be1-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="46be1-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46be1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="46be1-114">Remarks</span></span>

<span data-ttu-id="46be1-115">Cette propriété fournit un moyen pratique pour déterminer si le nom d’utilisateur apparaît explicitement dans la liste des destinataires principale sans examiner toutes les entrées de la liste.</span><span class="sxs-lookup"><span data-stu-id="46be1-115">This property provides a convenient way to determine whether the user name appears explicitly in the primary recipient list, without examining all entries in the list.</span></span> 
  
<span data-ttu-id="46be1-116">Cette propriété permet également de traitement automatisé des messages reçus au moment de la réception.</span><span class="sxs-lookup"><span data-stu-id="46be1-116">This property also assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="46be1-117">Option du fournisseur de transport, cette propriété contient FALSE ou n’est pas incluse si l’utilisateur de messagerie ne figure pas directement dans la table de destinataires.</span><span class="sxs-lookup"><span data-stu-id="46be1-117">At the transport provider's option, this property either contains FALSE or is not included if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="46be1-118">Remise de messages résultant de l’extension des listes de distribution ou la désignation d’une copie carbone invisible n’entraîne pas cette propriété à définir.</span><span class="sxs-lookup"><span data-stu-id="46be1-118">Message delivery resulting from distribution list expansion or a blind carbon copy designation does not cause this property to be set.</span></span> <span data-ttu-id="46be1-119">Le destinataire doit se nommer explicitement.</span><span class="sxs-lookup"><span data-stu-id="46be1-119">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="46be1-120">Les messages ne définissent généralement pas cette propriété, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) ou le **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="46be1-120">Unsent messages generally do not set the **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)), **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)), or this property.</span></span> <span data-ttu-id="46be1-121">Si elles sont présentes dans les messages de l’utilisateur peut accéder dans des magasins de messages publique, privé des autres utilisateurs magasins, dans les fichiers sur le disque, ou incorporé à l’intérieur d’autres messages reçus, ils contiennent généralement les valeurs à laquelle ils ont été définies lors de la dernière un fournisseur de transport remis le message.</span><span class="sxs-lookup"><span data-stu-id="46be1-121">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="46be1-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="46be1-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="46be1-123">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="46be1-123">Protocol specifications</span></span>

<span data-ttu-id="46be1-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46be1-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46be1-125">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="46be1-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="46be1-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="46be1-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="46be1-127">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="46be1-127">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="46be1-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="46be1-128">Header files</span></span>

<span data-ttu-id="46be1-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="46be1-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="46be1-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="46be1-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="46be1-131">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="46be1-131">Mapitags.h</span></span>
  
> <span data-ttu-id="46be1-132">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="46be1-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="46be1-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46be1-133">See also</span></span>



[<span data-ttu-id="46be1-134">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="46be1-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="46be1-135">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="46be1-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="46be1-136">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="46be1-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="46be1-137">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="46be1-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

