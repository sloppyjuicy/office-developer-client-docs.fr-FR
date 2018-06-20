---
title: Propriété canonique PidLidLogStart
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogStart
api_type:
- COM
ms.assetid: b8c0c871-51d8-4752-ad4b-607463a9f837
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 55ba18a1dcbce5e3f7996184dae45a638f9531e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785280"
---
# <a name="pidlidlogstart-canonical-property"></a><span data-ttu-id="f54eb-103">Propriété canonique PidLidLogStart</span><span class="sxs-lookup"><span data-stu-id="f54eb-103">PidLidLogStart Canonical Property</span></span>

  
  
<span data-ttu-id="f54eb-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f54eb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f54eb-105">Représente la date de début et l’heure pour le message de journal.</span><span class="sxs-lookup"><span data-stu-id="f54eb-105">Represents the start date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f54eb-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f54eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f54eb-107">dispidLogStart</span><span class="sxs-lookup"><span data-stu-id="f54eb-107">dispidLogStart</span></span>  <br/> |
|<span data-ttu-id="f54eb-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="f54eb-108">Property set:</span></span>  <br/> |<span data-ttu-id="f54eb-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="f54eb-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="f54eb-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="f54eb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f54eb-111">0x00008706</span><span class="sxs-lookup"><span data-stu-id="f54eb-111">0x00008706</span></span>  <br/> |
|<span data-ttu-id="f54eb-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f54eb-112">Data type:</span></span>  <br/> |<span data-ttu-id="f54eb-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="f54eb-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="f54eb-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="f54eb-114">Area:</span></span>  <br/> |<span data-ttu-id="f54eb-115">Journal</span><span class="sxs-lookup"><span data-stu-id="f54eb-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f54eb-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="f54eb-116">Remarks</span></span>

<span data-ttu-id="f54eb-117">L’heure en temps universel coordonné (UTC) lorsque le début de l’activité doit être égale à la propriété **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f54eb-117">The time in Coordinated Universal Time (UTC) when the activity began must be equal to the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f54eb-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f54eb-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f54eb-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="f54eb-119">Protocol specifications</span></span>

<span data-ttu-id="f54eb-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f54eb-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f54eb-121">Fournit une définition de propriété et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="f54eb-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f54eb-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f54eb-122">[[MS-OXOJRNL]](http://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f54eb-123">Spécifie les propriétés et les opérations qui sont autorisées pour les journaux.</span><span class="sxs-lookup"><span data-stu-id="f54eb-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f54eb-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f54eb-124">Header files</span></span>

<span data-ttu-id="f54eb-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f54eb-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="f54eb-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f54eb-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f54eb-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f54eb-127">See also</span></span>



[<span data-ttu-id="f54eb-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f54eb-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f54eb-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f54eb-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f54eb-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f54eb-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f54eb-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="f54eb-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

