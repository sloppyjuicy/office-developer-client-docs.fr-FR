---
title: Propriété canonique PidTagConversationTopic
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationTopic
api_type:
- HeaderDef
ms.assetid: db852b99-ce04-49bf-a714-7549571502e2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dfd437fac3a784212807c495f6e8f1adbe759cb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334684"
---
# <a name="pidtagconversationtopic-canonical-property"></a><span data-ttu-id="f4f66-103">Propriété canonique PidTagConversationTopic</span><span class="sxs-lookup"><span data-stu-id="f4f66-103">PidTagConversationTopic Canonical Property</span></span>

  
  
<span data-ttu-id="f4f66-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4f66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4f66-105">Contient la rubrique du premier message dans un thread de conversation.</span><span class="sxs-lookup"><span data-stu-id="f4f66-105">Contains the topic of the first message in a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4f66-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f4f66-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4f66-107">PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W</span><span class="sxs-lookup"><span data-stu-id="f4f66-107">PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W</span></span>  <br/> |
|<span data-ttu-id="f4f66-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f4f66-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f4f66-109">0x0070</span><span class="sxs-lookup"><span data-stu-id="f4f66-109">0x0070</span></span>  <br/> |
|<span data-ttu-id="f4f66-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f4f66-110">Data type:</span></span>  <br/> |<span data-ttu-id="f4f66-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f4f66-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f4f66-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f4f66-112">Area:</span></span>  <br/> |<span data-ttu-id="f4f66-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="f4f66-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4f66-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f4f66-114">Remarks</span></span>

<span data-ttu-id="f4f66-115">Un thread de conversation représente une série de messages et de réponses.</span><span class="sxs-lookup"><span data-stu-id="f4f66-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="f4f66-116">Ces propriétés sont définies pour le premier message d’un thread, généralement à la propriété **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f4f66-116">These properties are set for the first message in a thread, usually to the **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) property.</span></span> <span data-ttu-id="f4f66-117">Les messages suivants dans le thread doivent utiliser la même rubrique sans modification.</span><span class="sxs-lookup"><span data-stu-id="f4f66-117">Subsequent messages in the thread should use the same topic without modification.</span></span> 
  
<span data-ttu-id="f4f66-118">La **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) indique la relation d’ordre entre les messages et réponses suivants.</span><span class="sxs-lookup"><span data-stu-id="f4f66-118">The **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) property indicates the order relationship between subsequent messages and replies.</span></span> <span data-ttu-id="f4f66-119">Son utilisation est facultative, même si ces propriétés sont définies.</span><span class="sxs-lookup"><span data-stu-id="f4f66-119">Its use is optional, even if these properties are set.</span></span> 
  
<span data-ttu-id="f4f66-120">Un fournisseur de magasins de messages a la possibilité de s’assurer que ces propriétés sont toujours définies sur les messages entrants ou sortants.</span><span class="sxs-lookup"><span data-stu-id="f4f66-120">A message store provider has the option of assuring that these properties are always set on incoming or outgoing messages.</span></span> <span data-ttu-id="f4f66-121">Si ces propriétés sont déjà définies, elles ne doivent pas être modifiées.</span><span class="sxs-lookup"><span data-stu-id="f4f66-121">If these properties are already set they should not be altered.</span></span> <span data-ttu-id="f4f66-122">Si ce n’est pas le cas, ils peuvent être **PR_NORMALIZED_SUBJECT**.</span><span class="sxs-lookup"><span data-stu-id="f4f66-122">If not, they can be set to **PR_NORMALIZED_SUBJECT**.</span></span> <span data-ttu-id="f4f66-123">Toute action doit être prise avant [l’appel d’IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="f4f66-123">Any action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f4f66-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f4f66-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f4f66-125">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="f4f66-125">Protocol specifications</span></span>

<span data-ttu-id="f4f66-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4f66-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4f66-127">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="f4f66-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f4f66-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f4f66-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f4f66-129">Spécifie les propriétés et opérations autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="f4f66-129">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f4f66-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f4f66-130">Header files</span></span>

<span data-ttu-id="f4f66-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4f66-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4f66-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f4f66-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="f4f66-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f4f66-133">Mapitags.h</span></span>
  
> <span data-ttu-id="f4f66-134">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="f4f66-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4f66-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4f66-135">See also</span></span>



[<span data-ttu-id="f4f66-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f4f66-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4f66-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f4f66-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4f66-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f4f66-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4f66-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f4f66-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

