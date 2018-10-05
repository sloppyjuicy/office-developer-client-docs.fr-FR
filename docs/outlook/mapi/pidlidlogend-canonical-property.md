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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bed1692a4860d59ba7a6c297ab8e88645b023a86
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398940"
---
# <a name="pidlidlogend-canonical-property"></a><span data-ttu-id="10809-103">Propriété canonique PidLidLogEnd</span><span class="sxs-lookup"><span data-stu-id="10809-103">PidLidLogEnd Canonical Property</span></span>

  
  
<span data-ttu-id="10809-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10809-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10809-105">Représente la date de fin et l’heure pour le message de journal.</span><span class="sxs-lookup"><span data-stu-id="10809-105">Represents the end date and time for the journal message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10809-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="10809-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="10809-107">dispidLogEnd</span><span class="sxs-lookup"><span data-stu-id="10809-107">dispidLogEnd</span></span>  <br/> |
|<span data-ttu-id="10809-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="10809-108">Property set:</span></span>  <br/> |<span data-ttu-id="10809-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="10809-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="10809-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="10809-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="10809-111">0x00008708</span><span class="sxs-lookup"><span data-stu-id="10809-111">0x00008708</span></span>  <br/> |
|<span data-ttu-id="10809-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="10809-112">Data type:</span></span>  <br/> |<span data-ttu-id="10809-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="10809-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="10809-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="10809-114">Area:</span></span>  <br/> |<span data-ttu-id="10809-115">Journal</span><span class="sxs-lookup"><span data-stu-id="10809-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10809-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="10809-116">Remarks</span></span>

<span data-ttu-id="10809-117">L’heure de l’activité de fin en temps universel coordonné le (UTC), qui doit être égale à la propriété **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) et supérieure ou égale à la propriété **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="10809-117">The time when the activity ended in Coordinated Universal Time The (UTC), which must be equal to the **dispidCommonEnd** ([PidLidCommonEnd](pidlidcommonend-canonical-property.md)) property and greater than or equal to **dispidLogStart** ([PidLidLogStart](pidlidlogstart-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="10809-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="10809-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="10809-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="10809-119">Protocol specifications</span></span>

<span data-ttu-id="10809-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10809-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10809-121">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="10809-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="10809-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="10809-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="10809-123">Spécifie les propriétés et les opérations qui sont autorisées pour les journaux.</span><span class="sxs-lookup"><span data-stu-id="10809-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="10809-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="10809-124">Header files</span></span>

<span data-ttu-id="10809-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="10809-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="10809-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="10809-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="10809-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10809-127">See also</span></span>



[<span data-ttu-id="10809-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="10809-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="10809-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="10809-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="10809-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="10809-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="10809-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="10809-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

