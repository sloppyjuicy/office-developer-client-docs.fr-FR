---
title: Propriété canonique PidLidTaskFFixOffline
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFFixOffline
api_type:
- COM
ms.assetid: bbaf7df4-2de0-4da3-9125-eb24dfa94cd8
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b8da927fe0080a83748bbb2941979dcb246222fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785462"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a><span data-ttu-id="03999-103">Propriété canonique PidLidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="03999-103">PidLidTaskFFixOffline Canonical Property</span></span>

  
  
<span data-ttu-id="03999-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="03999-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="03999-105">Indique la précision de la propriété **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="03999-105">Indicates the accuracy of the **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03999-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="03999-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="03999-107">dispidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="03999-107">dispidTaskFFixOffline</span></span>  <br/> |
|<span data-ttu-id="03999-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="03999-108">Property set:</span></span>  <br/> |<span data-ttu-id="03999-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="03999-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="03999-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="03999-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="03999-111">0x0000812C</span><span class="sxs-lookup"><span data-stu-id="03999-111">0x0000812C</span></span>  <br/> |
|<span data-ttu-id="03999-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="03999-112">Data type:</span></span>  <br/> |<span data-ttu-id="03999-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="03999-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="03999-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="03999-114">Area:</span></span>  <br/> |<span data-ttu-id="03999-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="03999-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03999-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="03999-116">Remarks</span></span>

<span data-ttu-id="03999-117">Si la propriété **dispidTaskFFixOffline** est définie sur FALSE ou n’est pas définie, la valeur de la propriété **dispidTaskOwner** est correcte.</span><span class="sxs-lookup"><span data-stu-id="03999-117">If the **dispidTaskFFixOffline** property is set to FALSE or is unset, the value for the **dispidTaskOwner** property is correct.</span></span> <span data-ttu-id="03999-118">Si **dispidTaskFFixOffline** est défini sur TRUE, le client ne peut pas déterminer une valeur précise de **dispidTaskOwner**.</span><span class="sxs-lookup"><span data-stu-id="03999-118">If **dispidTaskFFixOffline** is set to TRUE, the client cannot determine an accurate value for **dispidTaskOwner**.</span></span> <span data-ttu-id="03999-119">Dans ce cas, le client peut définir **dispidTaskOwner** à un nom de propriétaire générique, tel que « Inconnue ».</span><span class="sxs-lookup"><span data-stu-id="03999-119">In that case, the client can set **dispidTaskOwner** to a generic owner name, such as "Unknown".</span></span> <span data-ttu-id="03999-120">Toutefois, si un client rencontre **dispidTaskFFixOffline** la valeur TRUE et peut déterminer un nom de propriétaire précis, le client doit mettre à jour **dispidTaskOwner** et **dispidTaskFFixOffline** la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="03999-120">However, if a client encounters a **dispidTaskFFixOffline** value of TRUE and can determine an accurate owner name, the client should update **dispidTaskOwner** and set **dispidTaskFFixOffline** to FALSE.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="03999-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="03999-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="03999-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="03999-122">Protocol specifications</span></span>

<span data-ttu-id="03999-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03999-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03999-124">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="03999-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="03999-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03999-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03999-126">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="03999-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="03999-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="03999-127">Header files</span></span>

<span data-ttu-id="03999-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03999-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="03999-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="03999-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03999-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03999-130">See also</span></span>



[<span data-ttu-id="03999-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="03999-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="03999-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="03999-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="03999-133">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="03999-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="03999-134">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="03999-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

