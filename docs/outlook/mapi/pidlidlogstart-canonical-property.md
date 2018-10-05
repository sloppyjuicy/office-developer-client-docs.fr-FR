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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dd5805cb0ee6b172506a532a513d06f57c583eee
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396266"
---
# <a name="pidlidlogstart-canonical-property"></a><span data-ttu-id="007f5-103">Propriété canonique PidLidLogStart</span><span class="sxs-lookup"><span data-stu-id="007f5-103">PidLidLogStart Canonical Property</span></span>

  
  
<span data-ttu-id="007f5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="007f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="007f5-105">Représente la date de début et l’heure pour le message de journal.</span><span class="sxs-lookup"><span data-stu-id="007f5-105">Represents the start date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="007f5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="007f5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="007f5-107">dispidLogStart</span><span class="sxs-lookup"><span data-stu-id="007f5-107">dispidLogStart</span></span>  <br/> |
|<span data-ttu-id="007f5-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="007f5-108">Property set:</span></span>  <br/> |<span data-ttu-id="007f5-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="007f5-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="007f5-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="007f5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="007f5-111">0x00008706</span><span class="sxs-lookup"><span data-stu-id="007f5-111">0x00008706</span></span>  <br/> |
|<span data-ttu-id="007f5-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="007f5-112">Data type:</span></span>  <br/> |<span data-ttu-id="007f5-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="007f5-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="007f5-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="007f5-114">Area:</span></span>  <br/> |<span data-ttu-id="007f5-115">Journal</span><span class="sxs-lookup"><span data-stu-id="007f5-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="007f5-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="007f5-116">Remarks</span></span>

<span data-ttu-id="007f5-117">L’heure en temps universel coordonné (UTC) lorsque le début de l’activité doit être égale à la propriété **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="007f5-117">The time in Coordinated Universal Time (UTC) when the activity began must be equal to the **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="007f5-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="007f5-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="007f5-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="007f5-119">Protocol specifications</span></span>

<span data-ttu-id="007f5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="007f5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="007f5-121">Fournit une définition de propriété et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="007f5-121">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="007f5-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="007f5-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="007f5-123">Spécifie les propriétés et les opérations qui sont autorisées pour les journaux.</span><span class="sxs-lookup"><span data-stu-id="007f5-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="007f5-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="007f5-124">Header files</span></span>

<span data-ttu-id="007f5-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="007f5-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="007f5-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="007f5-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="007f5-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="007f5-127">See also</span></span>



[<span data-ttu-id="007f5-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="007f5-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="007f5-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="007f5-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="007f5-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="007f5-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="007f5-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="007f5-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

