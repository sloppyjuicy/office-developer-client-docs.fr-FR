---
title: Propriété canonique PidLidLogDuration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogDocumentSaved
api_type:
- COM
ms.assetid: 012a3f6e-fd16-4dc9-845d-2bf4cebeaa42
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cc2d52ec183cc336bf126b1fda9a85d41f704f7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785283"
---
# <a name="pidlidlogduration-canonical-property"></a><span data-ttu-id="18710-103">Propriété canonique PidLidLogDuration</span><span class="sxs-lookup"><span data-stu-id="18710-103">PidLidLogDuration Canonical Property</span></span>

  
  
<span data-ttu-id="18710-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="18710-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="18710-105">Représente la durée, en minutes, d’un message de journal.</span><span class="sxs-lookup"><span data-stu-id="18710-105">Represents the duration, in minutes, of a journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18710-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="18710-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18710-107">dispidLogDuration</span><span class="sxs-lookup"><span data-stu-id="18710-107">dispidLogDuration</span></span>  <br/> |
|<span data-ttu-id="18710-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="18710-108">Property set:</span></span>  <br/> |<span data-ttu-id="18710-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="18710-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="18710-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="18710-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="18710-111">0x00008707</span><span class="sxs-lookup"><span data-stu-id="18710-111">0x00008707</span></span>  <br/> |
|<span data-ttu-id="18710-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="18710-112">Data type:</span></span>  <br/> |<span data-ttu-id="18710-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="18710-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="18710-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="18710-114">Area:</span></span>  <br/> |<span data-ttu-id="18710-115">Journal</span><span class="sxs-lookup"><span data-stu-id="18710-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18710-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="18710-116">Remarks</span></span>

<span data-ttu-id="18710-117">La durée, en minutes, de l’activité doit correspondre à la différence entre les **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) et les propriétés de **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="18710-117">The duration, in minutes, of the activity that must be the difference between the **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) and **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="18710-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="18710-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="18710-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="18710-119">Protocol specifications</span></span>

<span data-ttu-id="18710-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18710-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18710-121">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="18710-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="18710-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18710-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18710-123">Spécifie les propriétés et les opérations qui sont autorisées pour les journaux.</span><span class="sxs-lookup"><span data-stu-id="18710-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="18710-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="18710-124">Header files</span></span>

<span data-ttu-id="18710-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18710-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="18710-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="18710-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18710-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18710-127">See also</span></span>



[<span data-ttu-id="18710-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="18710-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18710-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="18710-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18710-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="18710-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18710-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="18710-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

