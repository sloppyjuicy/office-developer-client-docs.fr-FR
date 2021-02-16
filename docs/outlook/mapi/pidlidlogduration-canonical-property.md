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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6f25c1a72882f9236d56532b7259f51512734945
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336917"
---
# <a name="pidlidlogduration-canonical-property"></a><span data-ttu-id="d68eb-103">Propriété canonique PidLidLogDuration</span><span class="sxs-lookup"><span data-stu-id="d68eb-103">PidLidLogDuration Canonical Property</span></span>

  
  
<span data-ttu-id="d68eb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d68eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d68eb-105">Représente la durée, en minutes, d’un message de journal.</span><span class="sxs-lookup"><span data-stu-id="d68eb-105">Represents the duration, in minutes, of a journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d68eb-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d68eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d68eb-107">dispidLogDuration</span><span class="sxs-lookup"><span data-stu-id="d68eb-107">dispidLogDuration</span></span>  <br/> |
|<span data-ttu-id="d68eb-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="d68eb-108">Property set:</span></span>  <br/> |<span data-ttu-id="d68eb-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="d68eb-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="d68eb-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="d68eb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d68eb-111">0x00008707</span><span class="sxs-lookup"><span data-stu-id="d68eb-111">0x00008707</span></span>  <br/> |
|<span data-ttu-id="d68eb-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d68eb-112">Data type:</span></span>  <br/> |<span data-ttu-id="d68eb-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d68eb-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d68eb-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d68eb-114">Area:</span></span>  <br/> |<span data-ttu-id="d68eb-115">Journal</span><span class="sxs-lookup"><span data-stu-id="d68eb-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d68eb-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="d68eb-116">Remarks</span></span>

<span data-ttu-id="d68eb-117">Durée, en minutes, de l’activité qui doit être la différence entre les propriétés **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) et **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d68eb-117">The duration, in minutes, of the activity that must be the difference between the **dispidLogEnd** ([PidLidLogEnd](pidlidlogend-canonical-property.md)) and **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d68eb-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d68eb-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d68eb-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="d68eb-119">Protocol specifications</span></span>

<span data-ttu-id="d68eb-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d68eb-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d68eb-121">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="d68eb-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d68eb-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d68eb-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d68eb-123">Spécifie les propriétés et opérations autorisées pour les journaux.</span><span class="sxs-lookup"><span data-stu-id="d68eb-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d68eb-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d68eb-124">Header files</span></span>

<span data-ttu-id="d68eb-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d68eb-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="d68eb-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d68eb-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d68eb-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d68eb-127">See also</span></span>



[<span data-ttu-id="d68eb-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d68eb-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d68eb-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d68eb-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d68eb-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d68eb-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d68eb-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="d68eb-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

