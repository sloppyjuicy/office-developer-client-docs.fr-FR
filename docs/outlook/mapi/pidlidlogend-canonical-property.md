---
title: Propriété canonique PidLidLogEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogEnd
api_type:
- COM
ms.assetid: 621459ea-adf5-4420-9f0f-6f31b9b95508
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ef1c9814aa6d1f81a44883d09ac635a5eed76517
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785281"
---
# <a name="pidlidlogend-canonical-property"></a><span data-ttu-id="d9577-103">Propriété canonique PidLidLogEnd</span><span class="sxs-lookup"><span data-stu-id="d9577-103">PidLidLogEnd Canonical Property</span></span>

  
  
<span data-ttu-id="d9577-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9577-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d9577-105">Représente la date de fin et l’heure pour le message de journal.</span><span class="sxs-lookup"><span data-stu-id="d9577-105">Represents the end date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d9577-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d9577-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d9577-107">dispidLogEnd</span><span class="sxs-lookup"><span data-stu-id="d9577-107">dispidLogEnd</span></span>  <br/> |
|<span data-ttu-id="d9577-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="d9577-108">Property set:</span></span>  <br/> |<span data-ttu-id="d9577-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="d9577-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="d9577-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="d9577-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d9577-111">0x00008708</span><span class="sxs-lookup"><span data-stu-id="d9577-111">0x00008708</span></span>  <br/> |
|<span data-ttu-id="d9577-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d9577-112">Data type:</span></span>  <br/> |<span data-ttu-id="d9577-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="d9577-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="d9577-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="d9577-114">Area:</span></span>  <br/> |<span data-ttu-id="d9577-115">Journal</span><span class="sxs-lookup"><span data-stu-id="d9577-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9577-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="d9577-116">Remarks</span></span>

<span data-ttu-id="d9577-117">L’heure de l’activité de fin en temps universel coordonné le (UTC), qui doit être égale à la propriété **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) et supérieure ou égale à la propriété **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d9577-117">The time when the activity ended in Coordinated Universal Time The (UTC), which must be equal to the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property and greater than or equal to **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d9577-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d9577-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d9577-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="d9577-119">Protocol specifications</span></span>

<span data-ttu-id="d9577-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9577-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9577-121">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="d9577-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d9577-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d9577-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d9577-123">Spécifie les propriétés et les opérations qui sont autorisées pour les journaux.</span><span class="sxs-lookup"><span data-stu-id="d9577-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d9577-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d9577-124">Header files</span></span>

<span data-ttu-id="d9577-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d9577-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d9577-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d9577-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d9577-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9577-127">See also</span></span>



[<span data-ttu-id="d9577-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d9577-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d9577-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d9577-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d9577-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d9577-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d9577-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="d9577-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

