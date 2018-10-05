---
title: Propriété canonique PidTagOriginalSenderEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderEntryId
api_type:
- COM
ms.assetid: bd182589-afea-4967-92f5-ba1914e4db3f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bd32ef6540e0deec1b793bd49bab651d864754c6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393830"
---
# <a name="pidtagoriginalsenderentryid-canonical-property"></a><span data-ttu-id="8e5b9-103">Propriété canonique PidTagOriginalSenderEntryId</span><span class="sxs-lookup"><span data-stu-id="8e5b9-103">PidTagOriginalSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="8e5b9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e5b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e5b9-105">Contient l’identificateur d’entrée de l’expéditeur de la première version d’un message, autrement dit, le message avant d’être transférés ou une réponse.</span><span class="sxs-lookup"><span data-stu-id="8e5b9-105">Contains the entry identifier of the sender of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8e5b9-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8e5b9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8e5b9-107">PR_ORIGINAL_SENDER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="8e5b9-107">PR_ORIGINAL_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="8e5b9-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="8e5b9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8e5b9-109">0x005B</span><span class="sxs-lookup"><span data-stu-id="8e5b9-109">0x005B</span></span>  <br/> |
|<span data-ttu-id="8e5b9-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8e5b9-110">Data type:</span></span>  <br/> |<span data-ttu-id="8e5b9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8e5b9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8e5b9-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="8e5b9-112">Area:</span></span>  <br/> |<span data-ttu-id="8e5b9-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="8e5b9-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e5b9-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8e5b9-114">Remarks</span></span>

<span data-ttu-id="8e5b9-115">Cette propriété est une des propriétés d’adresse de l’expéditeur d’origine d’un message.</span><span class="sxs-lookup"><span data-stu-id="8e5b9-115">This property is one of the address properties for the original sender of a message.</span></span> <span data-ttu-id="8e5b9-116">Au premier envoi du message, une application cliente doit définir cette propriété à la valeur de la propriété **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8e5b9-116">At first submission of the message, a client application should set this property to the value of the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="8e5b9-117">Il n’est jamais modifié lorsque le message est transféré ou d’une réponse.</span><span class="sxs-lookup"><span data-stu-id="8e5b9-117">It is never changed when the message is forwarded or replied to.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8e5b9-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8e5b9-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8e5b9-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="8e5b9-119">Protocol specifications</span></span>

<span data-ttu-id="8e5b9-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e5b9-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e5b9-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="8e5b9-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8e5b9-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8e5b9-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8e5b9-123">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="8e5b9-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8e5b9-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8e5b9-124">Header files</span></span>

<span data-ttu-id="8e5b9-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e5b9-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8e5b9-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8e5b9-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="8e5b9-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="8e5b9-127">Mapitags.h</span></span>
  
> <span data-ttu-id="8e5b9-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="8e5b9-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e5b9-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e5b9-129">See also</span></span>



[<span data-ttu-id="8e5b9-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8e5b9-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8e5b9-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8e5b9-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8e5b9-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8e5b9-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8e5b9-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="8e5b9-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

