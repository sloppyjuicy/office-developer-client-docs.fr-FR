---
title: Propriété canonique PidTagOriginalMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalMessageClass
api_type:
- COM
ms.assetid: 49deb153-03c6-4be2-a3a5-53cca01accba
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7167b7b51698cda5610356779a8e8342b34a6082
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786342"
---
# <a name="pidtagoriginalmessageclass-canonical-property"></a><span data-ttu-id="72f06-103">Propriété canonique PidTagOriginalMessageClass</span><span class="sxs-lookup"><span data-stu-id="72f06-103">PidTagOriginalMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="72f06-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="72f06-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="72f06-105">Contient la classe du message d’origine pour une utilisation dans un rapport.</span><span class="sxs-lookup"><span data-stu-id="72f06-105">Contains the class of the original message for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="72f06-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="72f06-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="72f06-107">PR_ORIG_MESSAGE_CLASS, PR_ORIG_MESSAGE_CLASS_A, PR_ORIG_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="72f06-107">PR_ORIG_MESSAGE_CLASS, PR_ORIG_MESSAGE_CLASS_A, PR_ORIG_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="72f06-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="72f06-108">Identifier:</span></span>  <br/> |<span data-ttu-id="72f06-109">0x004B</span><span class="sxs-lookup"><span data-stu-id="72f06-109">0x004B</span></span>  <br/> |
|<span data-ttu-id="72f06-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="72f06-110">Data type:</span></span>  <br/> |<span data-ttu-id="72f06-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="72f06-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="72f06-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="72f06-112">Area:</span></span>  <br/> |<span data-ttu-id="72f06-113">Sécuriser les propriétés de messagerie</span><span class="sxs-lookup"><span data-stu-id="72f06-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72f06-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="72f06-114">Remarks</span></span>

<span data-ttu-id="72f06-115">Ces propriétés contiennent une copie de la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) du message pour lequel le rapport est généré.</span><span class="sxs-lookup"><span data-stu-id="72f06-115">These properties contain a copy of the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message for which the report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="72f06-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="72f06-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="72f06-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="72f06-117">Protocol specifications</span></span>

<span data-ttu-id="72f06-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72f06-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72f06-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="72f06-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="72f06-120">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="72f06-120">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="72f06-121">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="72f06-121">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="72f06-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="72f06-122">Header files</span></span>

<span data-ttu-id="72f06-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="72f06-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="72f06-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="72f06-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="72f06-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="72f06-125">Mapitags.h</span></span>
  
> <span data-ttu-id="72f06-126">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="72f06-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="72f06-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72f06-127">See also</span></span>



[<span data-ttu-id="72f06-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="72f06-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="72f06-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="72f06-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="72f06-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="72f06-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="72f06-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="72f06-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

