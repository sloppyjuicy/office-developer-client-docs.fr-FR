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
ms.openlocfilehash: 226e59ef6aa88bc290cf5aeb4d620979f926e1eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303037"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a><span data-ttu-id="51c07-103">Propriété canonique PidLidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="51c07-103">PidLidTaskFFixOffline Canonical Property</span></span>

  
  
<span data-ttu-id="51c07-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51c07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51c07-105">Indique l'exactitude de la propriété **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="51c07-105">Indicates the accuracy of the **dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="51c07-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="51c07-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="51c07-107">dispidTaskFFixOffline</span><span class="sxs-lookup"><span data-stu-id="51c07-107">dispidTaskFFixOffline</span></span>  <br/> |
|<span data-ttu-id="51c07-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="51c07-108">Property set:</span></span>  <br/> |<span data-ttu-id="51c07-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="51c07-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="51c07-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="51c07-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="51c07-111">0x0000812C</span><span class="sxs-lookup"><span data-stu-id="51c07-111">0x0000812C</span></span>  <br/> |
|<span data-ttu-id="51c07-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="51c07-112">Data type:</span></span>  <br/> |<span data-ttu-id="51c07-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="51c07-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="51c07-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="51c07-114">Area:</span></span>  <br/> |<span data-ttu-id="51c07-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="51c07-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51c07-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="51c07-116">Remarks</span></span>

<span data-ttu-id="51c07-117">Si la propriété **dispidTaskFFixOffline** a la valeur false ou n'est pas définie, la valeur de la propriété **dispidTaskOwner** est correcte.</span><span class="sxs-lookup"><span data-stu-id="51c07-117">If the **dispidTaskFFixOffline** property is set to FALSE or is unset, the value for the **dispidTaskOwner** property is correct.</span></span> <span data-ttu-id="51c07-118">Si **dispidTaskFFixOffline** est défini sur true, le client ne peut pas déterminer une valeur précise pour **dispidTaskOwner**.</span><span class="sxs-lookup"><span data-stu-id="51c07-118">If **dispidTaskFFixOffline** is set to TRUE, the client cannot determine an accurate value for **dispidTaskOwner**.</span></span> <span data-ttu-id="51c07-119">Dans ce cas, le client peut définir **dispidTaskOwner** sur un nom de propriétaire générique, tel que «inconnu».</span><span class="sxs-lookup"><span data-stu-id="51c07-119">In that case, the client can set **dispidTaskOwner** to a generic owner name, such as "Unknown".</span></span> <span data-ttu-id="51c07-120">Toutefois, si un client rencontre une valeur **DISPIDTASKFFIXOFFLINE** true et peut déterminer un nom de propriétaire précis, le client doit mettre à jour **DispidTaskOwner** et définir **dispidTaskFFixOffline** sur false.</span><span class="sxs-lookup"><span data-stu-id="51c07-120">However, if a client encounters a **dispidTaskFFixOffline** value of TRUE and can determine an accurate owner name, the client should update **dispidTaskOwner** and set **dispidTaskFFixOffline** to FALSE.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="51c07-121">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="51c07-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="51c07-122">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="51c07-122">Protocol specifications</span></span>

<span data-ttu-id="51c07-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51c07-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51c07-124">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="51c07-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="51c07-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="51c07-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="51c07-126">Définit plusieurs objets qui modélisent l'équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.</span><span class="sxs-lookup"><span data-stu-id="51c07-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="51c07-127">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="51c07-127">Header files</span></span>

<span data-ttu-id="51c07-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="51c07-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="51c07-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="51c07-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="51c07-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51c07-130">See also</span></span>



[<span data-ttu-id="51c07-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="51c07-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="51c07-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="51c07-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="51c07-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="51c07-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="51c07-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="51c07-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

