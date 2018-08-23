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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 716d8b5b09ee0e29d1946042cae2631561d74df5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584652"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a><span data-ttu-id="5671c-103">Propriété canonique PidLidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="5671c-103">PidLidTaskFFixOffline Canonical Property</span></span>

  
  
<span data-ttu-id="5671c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5671c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5671c-105">Indique la précision de la propriété **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5671c-105">Indicates the accuracy of the **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5671c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5671c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5671c-107">dispidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="5671c-107">dispidTaskFFixOffline</span></span>  <br/> |
|<span data-ttu-id="5671c-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="5671c-108">Property set:</span></span>  <br/> |<span data-ttu-id="5671c-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="5671c-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="5671c-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="5671c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5671c-111">0x0000812C</span><span class="sxs-lookup"><span data-stu-id="5671c-111">0x0000812C</span></span>  <br/> |
|<span data-ttu-id="5671c-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5671c-112">Data type:</span></span>  <br/> |<span data-ttu-id="5671c-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="5671c-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="5671c-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5671c-114">Area:</span></span>  <br/> |<span data-ttu-id="5671c-115">Task</span><span class="sxs-lookup"><span data-stu-id="5671c-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5671c-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="5671c-116">Remarks</span></span>

<span data-ttu-id="5671c-117">Si la propriété **dispidTaskFFixOffline** est définie sur FALSE ou n’est pas définie, la valeur de la propriété **dispidTaskOwner** est correcte.</span><span class="sxs-lookup"><span data-stu-id="5671c-117">If the **dispidTaskFFixOffline** property is set to FALSE or is unset, the value for the **dispidTaskOwner** property is correct.</span></span> <span data-ttu-id="5671c-118">Si **dispidTaskFFixOffline** est défini sur TRUE, le client ne peut pas déterminer une valeur précise de **dispidTaskOwner**.</span><span class="sxs-lookup"><span data-stu-id="5671c-118">If **dispidTaskFFixOffline** is set to TRUE, the client cannot determine an accurate value for **dispidTaskOwner**.</span></span> <span data-ttu-id="5671c-119">Dans ce cas, le client peut définir **dispidTaskOwner** à un nom de propriétaire générique, tel que « Inconnue ».</span><span class="sxs-lookup"><span data-stu-id="5671c-119">In that case, the client can set **dispidTaskOwner** to a generic owner name, such as "Unknown".</span></span> <span data-ttu-id="5671c-120">Toutefois, si un client rencontre **dispidTaskFFixOffline** la valeur TRUE et peut déterminer un nom de propriétaire précis, le client doit mettre à jour **dispidTaskOwner** et **dispidTaskFFixOffline** la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="5671c-120">However, if a client encounters a **dispidTaskFFixOffline** value of TRUE and can determine an accurate owner name, the client should update **dispidTaskOwner** and set **dispidTaskFFixOffline** to FALSE.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5671c-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5671c-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5671c-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="5671c-122">Protocol specifications</span></span>

<span data-ttu-id="5671c-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5671c-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5671c-124">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="5671c-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5671c-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5671c-125">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5671c-126">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="5671c-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="5671c-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5671c-127">Header files</span></span>

<span data-ttu-id="5671c-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5671c-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="5671c-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5671c-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5671c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5671c-130">See also</span></span>



[<span data-ttu-id="5671c-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5671c-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5671c-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5671c-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5671c-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5671c-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5671c-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5671c-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

