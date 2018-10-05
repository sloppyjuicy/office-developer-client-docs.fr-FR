---
title: Propriété canonique PidTagMessageCcMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageCcMe
api_type:
- HeaderDef
ms.assetid: 7310a0f2-a109-40a4-99bf-e963d754a067
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7605739dd6d0f0205a1a4f09eb8c45d235c0c179
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389770"
---
# <a name="pidtagmessageccme-canonical-property"></a><span data-ttu-id="1c040-103">Propriété canonique PidTagMessageCcMe</span><span class="sxs-lookup"><span data-stu-id="1c040-103">PidTagMessageCcMe Canonical Property</span></span>

  
  
<span data-ttu-id="1c040-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c040-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c040-105">Contient la valeur TRUE si cet utilisateur de messagerie est nommé spécifiquement comme destinataire du message en copie carbone (CC) et ne fait pas partie d’une liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="1c040-105">Contains TRUE if this messaging user is specifically named as a carbon copy (CC) recipient of this message and is not part of a distribution list.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1c040-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1c040-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1c040-107">PR_MESSAGE_CC_ME</span><span class="sxs-lookup"><span data-stu-id="1c040-107">PR_MESSAGE_CC_ME</span></span>  <br/> |
|<span data-ttu-id="1c040-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1c040-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1c040-109">0x0058</span><span class="sxs-lookup"><span data-stu-id="1c040-109">0x0058</span></span>  <br/> |
|<span data-ttu-id="1c040-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1c040-110">Data type:</span></span>  <br/> |<span data-ttu-id="1c040-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1c040-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1c040-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="1c040-112">Area:</span></span>  <br/> |<span data-ttu-id="1c040-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="1c040-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c040-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1c040-114">Remarks</span></span>

<span data-ttu-id="1c040-115">Cette propriété fournit un moyen pratique pour déterminer si le nom d’utilisateur apparaît explicitement dans la liste des destinataires en copie carbone, sans examiner toutes les entrées de la liste.</span><span class="sxs-lookup"><span data-stu-id="1c040-115">This property provides a convenient way to determine whether the user name appears explicitly in the carbon copy recipient list, without examining all entries in the list.</span></span> 
  
<span data-ttu-id="1c040-116">Cette propriété permet également de traitement automatisé des messages reçus au moment de la réception.</span><span class="sxs-lookup"><span data-stu-id="1c040-116">This property also assists automated handling of received messages at the time of receipt.</span></span> <span data-ttu-id="1c040-117">Option du fournisseur de transport, cette propriété contient FALSE ou n’est pas définie si l’utilisateur de messagerie ne figure pas directement dans la table de destinataires.</span><span class="sxs-lookup"><span data-stu-id="1c040-117">At the transport provider's option, this property either contains FALSE or is not set if the messaging user is not listed directly in the recipient table.</span></span> 
  
<span data-ttu-id="1c040-118">Remise de messages résultant de l’extension des listes de distribution ou la désignation d’une copie carbone invisible n’entraîne pas cette propriété à définir.</span><span class="sxs-lookup"><span data-stu-id="1c040-118">Message delivery resulting from distribution list expansion or a blind carbon copy designation does not cause this property to be set.</span></span> <span data-ttu-id="1c040-119">Le destinataire doit se nommer explicitement.</span><span class="sxs-lookup"><span data-stu-id="1c040-119">The recipient must be explicitly named.</span></span> 
  
<span data-ttu-id="1c040-120">Généralement, les messages non envoyés ne définissent pas cette propriété, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) ou **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1c040-120">Unsent messages generally do not set this property, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)), or **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)).</span></span> <span data-ttu-id="1c040-121">Si elles sont présentes dans les messages de l’utilisateur peut accéder dans des magasins de messages publique, privé des autres utilisateurs magasins, dans les fichiers sur le disque, ou incorporé à l’intérieur d’autres messages reçus, ils contiennent généralement les valeurs à laquelle ils ont été définies lors de la dernière un fournisseur de transport remis le message.</span><span class="sxs-lookup"><span data-stu-id="1c040-121">If they are present in messages the user can access in public message stores, in other users' private stores, in files on disk, or embedded inside other received messages, they generally contain the values to which they were set the last time a transport provider delivered the message.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1c040-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1c040-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1c040-123">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="1c040-123">Protocol specifications</span></span>

<span data-ttu-id="1c040-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c040-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c040-125">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="1c040-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1c040-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c040-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c040-127">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="1c040-127">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1c040-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1c040-128">Header files</span></span>

<span data-ttu-id="1c040-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1c040-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="1c040-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1c040-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="1c040-131">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="1c040-131">Mapitags.h</span></span>
  
> <span data-ttu-id="1c040-132">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="1c040-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1c040-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c040-133">See also</span></span>



[<span data-ttu-id="1c040-134">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1c040-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1c040-135">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1c040-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1c040-136">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1c040-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1c040-137">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="1c040-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

