---
title: Propriété canonique PidTagOriginalSenderSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderSearchKey
api_type:
- COM
ms.assetid: 164eb9dd-e553-459e-99c1-3da0284bb01f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2aa0a8601a72b6d4c40167ac55d3d643bf946708
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786327"
---
# <a name="pidtagoriginalsendersearchkey-canonical-property"></a><span data-ttu-id="85d80-103">Propriété canonique PidTagOriginalSenderSearchKey</span><span class="sxs-lookup"><span data-stu-id="85d80-103">PidTagOriginalSenderSearchKey Canonical Property</span></span>

  
  
<span data-ttu-id="85d80-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="85d80-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="85d80-105">Contient la clé de recherche pour l’expéditeur de la première version d’un message, autrement dit, le message avant d’être transférés ou une réponse.</span><span class="sxs-lookup"><span data-stu-id="85d80-105">Contains the search key for the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="85d80-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="85d80-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="85d80-107">PR_ORIGINAL_SENDER_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="85d80-107">PR_ORIGINAL_SENDER_SEARCH_KEY</span></span>  <br/> |
|<span data-ttu-id="85d80-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="85d80-108">Identifier:</span></span>  <br/> |<span data-ttu-id="85d80-109">0x005C</span><span class="sxs-lookup"><span data-stu-id="85d80-109">0x005C</span></span>  <br/> |
|<span data-ttu-id="85d80-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="85d80-110">Data type:</span></span>  <br/> |<span data-ttu-id="85d80-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="85d80-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="85d80-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="85d80-112">Area:</span></span>  <br/> |<span data-ttu-id="85d80-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="85d80-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85d80-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="85d80-114">Remarks</span></span>

<span data-ttu-id="85d80-115">Cette propriété est une des propriétés d’adresse de l’expéditeur d’origine d’un message.</span><span class="sxs-lookup"><span data-stu-id="85d80-115">This property is one of the address properties for the original sender of a message.</span></span> <span data-ttu-id="85d80-116">Au premier envoi du message, l’application cliente doit définir cette propriété à la valeur de la propriété **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="85d80-116">At first submission of the message, the client application should set this property to the value of the **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)) property.</span></span> <span data-ttu-id="85d80-117">Il n’est jamais modifié lorsque le message est transféré ou d’une réponse.</span><span class="sxs-lookup"><span data-stu-id="85d80-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="85d80-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="85d80-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="85d80-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="85d80-119">Protocol specifications</span></span>

<span data-ttu-id="85d80-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="85d80-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="85d80-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="85d80-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="85d80-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="85d80-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="85d80-123">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="85d80-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="85d80-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="85d80-124">Header files</span></span>

<span data-ttu-id="85d80-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="85d80-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="85d80-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="85d80-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="85d80-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="85d80-127">Mapitags.h</span></span>
  
> <span data-ttu-id="85d80-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="85d80-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="85d80-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85d80-129">See also</span></span>



[<span data-ttu-id="85d80-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="85d80-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="85d80-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="85d80-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="85d80-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="85d80-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="85d80-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="85d80-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

