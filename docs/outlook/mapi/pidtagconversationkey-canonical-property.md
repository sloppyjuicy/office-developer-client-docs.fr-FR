---
title: Propriété canonique PidTagConversationKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b4c8c6cf3bee0575a42bc42a1ebf5e185ef78ab4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591631"
---
# <a name="pidtagconversationkey-canonical-property"></a><span data-ttu-id="e3635-103">Propriété canonique PidTagConversationKey</span><span class="sxs-lookup"><span data-stu-id="e3635-103">PidTagConversationKey Canonical Property</span></span>

  
  
<span data-ttu-id="e3635-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3635-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3635-105">Contient la clé de conversation utilisée dans Microsoft Outlook uniquement lors de la recherche **IPM. MessageManager** messages, tels que le message qui contient l’historique de téléchargement d’un compte Post Office Protocol (POP3).</span><span class="sxs-lookup"><span data-stu-id="e3635-105">Contains the conversation key used in Microsoft Outlook only when locating **IPM.MessageManager** messages, such as the message that contains download history for a Post Office Protocol (POP3) account.</span></span> <span data-ttu-id="e3635-106">Cette propriété a été déconseillée dans Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e3635-106">This property has been deprecated in Microsoft Exchange Server.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3635-107">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e3635-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="e3635-108">PR_CONVERSATION_KEY</span><span class="sxs-lookup"><span data-stu-id="e3635-108">PR_CONVERSATION_KEY</span></span>  <br/> |
|<span data-ttu-id="e3635-109">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="e3635-109">Identifier:</span></span>  <br/> |<span data-ttu-id="e3635-110">0x000B</span><span class="sxs-lookup"><span data-stu-id="e3635-110">0x000B</span></span>  <br/> |
|<span data-ttu-id="e3635-111">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e3635-111">Data type:</span></span>  <br/> |<span data-ttu-id="e3635-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e3635-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e3635-113">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e3635-113">Area:</span></span>  <br/> |<span data-ttu-id="e3635-114">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="e3635-114">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3635-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="e3635-115">Remarks</span></span>

<span data-ttu-id="e3635-116">Lorsque vous accédez à des messages électroniques en tant que conversations et la conversion des propriétés de message pour le [Transport-Neutral Encapsulation Format (TNEF)](transport-neutral-encapsulation-format-tnef.md), n’utilisez pas cette propriété ; au lieu de cela, utilisez les propriétés canoniques [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) et [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="e3635-116">When accessing email messages as conversations and converting message properties to [Transport-Neutral Encapsulation Format (TNEF)](transport-neutral-encapsulation-format-tnef.md), do not use this property; instead, use the [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) and [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) canonical properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e3635-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e3635-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e3635-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="e3635-118">Protocol specifications</span></span>

<span data-ttu-id="e3635-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3635-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3635-120">Fournit des références aux spécifications du protocole connexes Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e3635-120">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e3635-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3635-121">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3635-122">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="e3635-122">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="e3635-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e3635-123">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e3635-124">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="e3635-124">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e3635-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e3635-125">Header files</span></span>

<span data-ttu-id="e3635-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e3635-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e3635-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e3635-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="e3635-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="e3635-128">Mapitags.h</span></span>
  
> <span data-ttu-id="e3635-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="e3635-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e3635-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3635-130">See also</span></span>



[<span data-ttu-id="e3635-131">Sous-arborescence IPM</span><span class="sxs-lookup"><span data-stu-id="e3635-131">IPM Subtree</span></span>](ipm-subtree.md)
  
[<span data-ttu-id="e3635-132">Dossiers sp�ciaux MAPI</span><span class="sxs-lookup"><span data-stu-id="e3635-132">MAPI Special Folders</span></span>](mapi-special-folders.md)
  
[<span data-ttu-id="e3635-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e3635-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e3635-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e3635-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e3635-135">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e3635-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e3635-136">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e3635-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

