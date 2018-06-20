---
title: Propriété canonique PidTagConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationIndex
api_type:
- HeaderDef
ms.assetid: c65cdda7-9515-4da9-be75-43ebf45a02df
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bddb667cba99e240a6ce182c9c1c8ed47f467e15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785876"
---
# <a name="pidtagconversationindex-canonical-property"></a><span data-ttu-id="8840b-103">Propriété canonique PidTagConversationIndex</span><span class="sxs-lookup"><span data-stu-id="8840b-103">PidTagConversationIndex Canonical Property</span></span>

  
  
<span data-ttu-id="8840b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8840b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8840b-105">Contient une valeur binaire qui indique la position relative de ce message dans un thread de conversation.</span><span class="sxs-lookup"><span data-stu-id="8840b-105">Contains a binary value that indicates the relative position of this message within a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8840b-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8840b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8840b-107">PR_CONVERSATION_INDEX</span><span class="sxs-lookup"><span data-stu-id="8840b-107">PR_CONVERSATION_INDEX</span></span>  <br/> |
|<span data-ttu-id="8840b-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="8840b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8840b-109">0x0071</span><span class="sxs-lookup"><span data-stu-id="8840b-109">0x0071</span></span>  <br/> |
|<span data-ttu-id="8840b-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8840b-110">Data type:</span></span>  <br/> |<span data-ttu-id="8840b-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8840b-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8840b-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="8840b-112">Area:</span></span>  <br/> |<span data-ttu-id="8840b-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="8840b-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8840b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8840b-114">Remarks</span></span>

<span data-ttu-id="8840b-115">Un thread de conversations représente une série de messages et de réponses.</span><span class="sxs-lookup"><span data-stu-id="8840b-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="8840b-116">Cette propriété est généralement implémentée à l’aide des valeurs d’horodatage concaténé.</span><span class="sxs-lookup"><span data-stu-id="8840b-116">This property is usually implemented using concatenated time stamp values.</span></span> <span data-ttu-id="8840b-117">Son utilisation est facultative, même si **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) est défini.</span><span class="sxs-lookup"><span data-stu-id="8840b-117">Its use is optional, even if **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) is set.</span></span> 
  
<span data-ttu-id="8840b-118">MAPI fournit la fonction [ScCreateConversationIndex](sccreateconversationindex.md) pour créer ou mettre à jour un index de conversation.</span><span class="sxs-lookup"><span data-stu-id="8840b-118">MAPI provides the [ScCreateConversationIndex](sccreateconversationindex.md) function to create or update a conversation index.</span></span> <span data-ttu-id="8840b-119">La fonction prend la valeur d’index en cours en tant que tableau d’octets comptés et renvoie la valeur d’index avec un horodatage concaténé à la fin.</span><span class="sxs-lookup"><span data-stu-id="8840b-119">The function takes the current index value as a counted byte array and returns the index value with a time stamp concatenated onto the end.</span></span> <span data-ttu-id="8840b-120">Un message qui représente une réponse à un autre message doit utiliser **ScCreateConversationIndex** pour mettre à jour de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="8840b-120">A message representing a reply to another message should use **ScCreateConversationIndex** to update this property.</span></span> 
  
<span data-ttu-id="8840b-121">Un fournisseur de banque de messages a la possibilité de garantir que **PR_CONVERSATION_INDEX** est toujours définie sur les messages entrants ou sortants.</span><span class="sxs-lookup"><span data-stu-id="8840b-121">A message store provider has the option of assuring that **PR_CONVERSATION_INDEX** is always set on incoming or outgoing messages.</span></span> <span data-ttu-id="8840b-122">Il peut le faire en appelant **ScCreateConversationIndex**, avec la valeur existante, si cette propriété est définie ou valeur NULL s’il n’est pas.</span><span class="sxs-lookup"><span data-stu-id="8840b-122">It can do this by calling **ScCreateConversationIndex**, either with the existing value if this property is set or with NULL if it is not.</span></span> <span data-ttu-id="8840b-123">Cette action doit être prise avant l’appel de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="8840b-123">This action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
<span data-ttu-id="8840b-124">Tous les messages qui ont la même valeur pour **PR_CONVERSATION_TOPIC** peuvent être triés sur cette propriété pour faire apparaître la relation hiérarchique entre les messages.</span><span class="sxs-lookup"><span data-stu-id="8840b-124">All messages that have the same value for **PR_CONVERSATION_TOPIC** can be sorted on this property to reveal the hierarchical relationship of the messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8840b-125">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8840b-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8840b-126">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="8840b-126">Protocol specifications</span></span>

<span data-ttu-id="8840b-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8840b-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8840b-128">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="8840b-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8840b-129">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8840b-129">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8840b-130">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="8840b-130">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8840b-131">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8840b-131">Header files</span></span>

<span data-ttu-id="8840b-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8840b-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="8840b-133">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8840b-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="8840b-134">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="8840b-134">Mapitags.h</span></span>
  
> <span data-ttu-id="8840b-135">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="8840b-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8840b-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8840b-136">See also</span></span>



[<span data-ttu-id="8840b-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8840b-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8840b-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8840b-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8840b-139">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8840b-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8840b-140">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="8840b-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

