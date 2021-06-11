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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 677ba61e3d812909ac4f28f3542f6a79f971ed06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342622"
---
# <a name="pidtagoriginalmessageclass-canonical-property"></a><span data-ttu-id="e2466-103">Propriété canonique PidTagOriginalMessageClass</span><span class="sxs-lookup"><span data-stu-id="e2466-103">PidTagOriginalMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="e2466-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2466-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2466-105">Contient la classe du message d’origine à utiliser dans un état.</span><span class="sxs-lookup"><span data-stu-id="e2466-105">Contains the class of the original message for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e2466-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e2466-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e2466-107">PR_ORIG_MESSAGE_CLASS, PR_ORIG_MESSAGE_CLASS_A, PR_ORIG_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="e2466-107">PR_ORIG_MESSAGE_CLASS, PR_ORIG_MESSAGE_CLASS_A, PR_ORIG_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="e2466-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="e2466-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e2466-109">0x004B</span><span class="sxs-lookup"><span data-stu-id="e2466-109">0x004B</span></span>  <br/> |
|<span data-ttu-id="e2466-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e2466-110">Data type:</span></span>  <br/> |<span data-ttu-id="e2466-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e2466-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e2466-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e2466-112">Area:</span></span>  <br/> |<span data-ttu-id="e2466-113">Propriétés de messagerie sécurisée</span><span class="sxs-lookup"><span data-stu-id="e2466-113">Secure Messaging Properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2466-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e2466-114">Remarks</span></span>

<span data-ttu-id="e2466-115">Ces propriétés contiennent une copie **de la propriété PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) du message pour lequel l’état est généré.</span><span class="sxs-lookup"><span data-stu-id="e2466-115">These properties contain a copy of the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the message for which the report is being generated.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e2466-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e2466-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e2466-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="e2466-117">Protocol specifications</span></span>

<span data-ttu-id="e2466-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2466-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2466-119">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="e2466-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e2466-120">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e2466-120">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e2466-121">Encode et décode les objets de message et de pièce jointe dans une représentation de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="e2466-121">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e2466-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e2466-122">Header files</span></span>

<span data-ttu-id="e2466-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e2466-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e2466-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e2466-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e2466-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e2466-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e2466-126">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="e2466-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2466-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2466-127">See also</span></span>



[<span data-ttu-id="e2466-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e2466-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e2466-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e2466-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e2466-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e2466-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e2466-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e2466-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

