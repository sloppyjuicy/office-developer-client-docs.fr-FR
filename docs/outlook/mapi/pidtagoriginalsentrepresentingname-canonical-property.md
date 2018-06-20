---
title: Propriété canonique PidTagOriginalSentRepresentingName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSentRepresentingName
api_type:
- COM
ms.assetid: 1be45cad-05a2-44cb-8c3d-7f6ac092fa0d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c71182fc5190e64bdeb95dd5d19dfa7c588a41d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786358"
---
# <a name="pidtagoriginalsentrepresentingname-canonical-property"></a><span data-ttu-id="238ee-103">Propriété canonique PidTagOriginalSentRepresentingName</span><span class="sxs-lookup"><span data-stu-id="238ee-103">PidTagOriginalSentRepresentingName Canonical Property</span></span>

  
  
<span data-ttu-id="238ee-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="238ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="238ee-105">Contient le nom complet de l’utilisateur de messagerie pour le compte duquel le message d’origine a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="238ee-105">Contains the display name of the messaging user on whose behalf the original message was sent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="238ee-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="238ee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="238ee-107">PR_ORIGINAL_SENT_REPRESENTING_NAME, PR_ORIGINAL_SENT_REPRESENTING_NAME_A, PR_ORIGINAL_SENT_REPRESENTING_NAME_W</span><span class="sxs-lookup"><span data-stu-id="238ee-107">PR_ORIGINAL_SENT_REPRESENTING_NAME, PR_ORIGINAL_SENT_REPRESENTING_NAME_A, PR_ORIGINAL_SENT_REPRESENTING_NAME_W</span></span>  <br/> |
|<span data-ttu-id="238ee-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="238ee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="238ee-109">0x005D</span><span class="sxs-lookup"><span data-stu-id="238ee-109">0x005D</span></span>  <br/> |
|<span data-ttu-id="238ee-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="238ee-110">Data type:</span></span>  <br/> |<span data-ttu-id="238ee-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="238ee-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="238ee-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="238ee-112">Area:</span></span>  <br/> |<span data-ttu-id="238ee-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="238ee-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="238ee-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="238ee-114">Remarks</span></span>

<span data-ttu-id="238ee-115">Ces exemples de propriétés propriétés d’adresse de l’expéditeur d’origine représenté d’un message.</span><span class="sxs-lookup"><span data-stu-id="238ee-115">These properties examples of the address properties for the original represented sender of a message.</span></span> <span data-ttu-id="238ee-116">Il est utilisé dans un thread de conversation.</span><span class="sxs-lookup"><span data-stu-id="238ee-116">It is used in a conversation thread.</span></span>
  
<span data-ttu-id="238ee-117">Une application cliente envoie un message de la part d’un autre client doit définir ces propriétés à la valeur de la propriété **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) à la première soumission du message.</span><span class="sxs-lookup"><span data-stu-id="238ee-117">A client application sending a message on behalf of another client should set these properties to the value of the **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) property at the first submission of the message.</span></span> <span data-ttu-id="238ee-118">Une fois définies, il doit jamais être modifié.</span><span class="sxs-lookup"><span data-stu-id="238ee-118">Once set, it should never be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="238ee-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="238ee-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="238ee-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="238ee-120">Protocol specifications</span></span>

<span data-ttu-id="238ee-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="238ee-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="238ee-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="238ee-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="238ee-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="238ee-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="238ee-124">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="238ee-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="238ee-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="238ee-125">Header files</span></span>

<span data-ttu-id="238ee-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="238ee-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="238ee-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="238ee-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="238ee-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="238ee-128">Mapitags.h</span></span>
  
> <span data-ttu-id="238ee-129">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="238ee-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="238ee-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="238ee-130">See also</span></span>



[<span data-ttu-id="238ee-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="238ee-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="238ee-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="238ee-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="238ee-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="238ee-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="238ee-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="238ee-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

