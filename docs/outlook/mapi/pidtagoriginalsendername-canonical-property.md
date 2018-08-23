---
title: Propriété canonique PidTagOriginalSenderName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderName
api_type:
- COM
ms.assetid: 5e3b7764-b122-4405-be4f-7fec571c7dfc
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 11f8df87dd9248a9d6061892bb0500274478646d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579164"
---
# <a name="pidtagoriginalsendername-canonical-property"></a><span data-ttu-id="a36e5-103">Propriété canonique PidTagOriginalSenderName</span><span class="sxs-lookup"><span data-stu-id="a36e5-103">PidTagOriginalSenderName Canonical Property</span></span>

  
  
<span data-ttu-id="a36e5-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a36e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a36e5-105">Contient le nom complet de l’expéditeur de la première version d’un message, autrement dit, le message avant d’être transférés ou une réponse.</span><span class="sxs-lookup"><span data-stu-id="a36e5-105">Contains the display name of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a36e5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a36e5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a36e5-107">PR_ORIGINAL_SENDER_NAME, PR_ORIGINAL_SENDER_NAME_A, PR_ORIGINAL_SENDER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="a36e5-107">PR_ORIGINAL_SENDER_NAME, PR_ORIGINAL_SENDER_NAME_A, PR_ORIGINAL_SENDER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="a36e5-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a36e5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a36e5-109">0x005A</span><span class="sxs-lookup"><span data-stu-id="a36e5-109">0x005A</span></span>  <br/> |
|<span data-ttu-id="a36e5-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a36e5-110">Data type:</span></span>  <br/> |<span data-ttu-id="a36e5-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a36e5-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a36e5-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a36e5-112">Area:</span></span>  <br/> |<span data-ttu-id="a36e5-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="a36e5-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a36e5-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a36e5-114">Remarks</span></span>

<span data-ttu-id="a36e5-115">Ces propriétés sont des exemples de propriétés d’adresse de l’expéditeur d’origine d’un message.</span><span class="sxs-lookup"><span data-stu-id="a36e5-115">These properties are examples of the address properties for the original sender of a message.</span></span> <span data-ttu-id="a36e5-116">Au premier envoi du message, une application cliente doit définir ces propriétés à la valeur de la propriété **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a36e5-116">At first submission of the message, a client application should set these properties to the value of the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) property.</span></span> <span data-ttu-id="a36e5-117">Il n’est jamais modifié lorsque le message est transféré ou d’une réponse.</span><span class="sxs-lookup"><span data-stu-id="a36e5-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a36e5-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a36e5-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a36e5-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="a36e5-119">Protocol specifications</span></span>

<span data-ttu-id="a36e5-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a36e5-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a36e5-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="a36e5-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a36e5-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a36e5-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a36e5-123">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="a36e5-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a36e5-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="a36e5-124">Header files</span></span>

<span data-ttu-id="a36e5-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a36e5-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="a36e5-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a36e5-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="a36e5-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="a36e5-127">Mapitags.h</span></span>
  
> <span data-ttu-id="a36e5-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="a36e5-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a36e5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a36e5-129">See also</span></span>



[<span data-ttu-id="a36e5-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a36e5-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a36e5-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a36e5-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a36e5-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a36e5-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a36e5-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a36e5-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

