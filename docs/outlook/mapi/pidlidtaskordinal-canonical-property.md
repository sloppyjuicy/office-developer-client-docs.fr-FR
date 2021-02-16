---
title: Propriété canonique PidLidTaskOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskOrdinal
api_type:
- COM
ms.assetid: 1021860e-4c40-4c22-aa68-b568d046aaf7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a64008da93584529916a9303176bba0aa08d3fac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357959"
---
# <a name="pidlidtaskordinal-canonical-property"></a><span data-ttu-id="b054e-103">Propriété canonique PidLidTaskOrdinal</span><span class="sxs-lookup"><span data-stu-id="b054e-103">PidLidTaskOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="b054e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b054e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b054e-105">Fournit une aide pour les tâches de tri personnalisées.</span><span class="sxs-lookup"><span data-stu-id="b054e-105">Provides an aid to custom sorting tasks.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b054e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b054e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b054e-107">dispidTaskOrdinal</span><span class="sxs-lookup"><span data-stu-id="b054e-107">dispidTaskOrdinal</span></span>  <br/> |
|<span data-ttu-id="b054e-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="b054e-108">Property set:</span></span>  <br/> |<span data-ttu-id="b054e-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="b054e-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="b054e-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="b054e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b054e-111">0x00008123</span><span class="sxs-lookup"><span data-stu-id="b054e-111">0x00008123</span></span>  <br/> |
|<span data-ttu-id="b054e-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b054e-112">Data type:</span></span>  <br/> |<span data-ttu-id="b054e-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b054e-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b054e-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="b054e-114">Area:</span></span>  <br/> |<span data-ttu-id="b054e-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="b054e-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b054e-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="b054e-116">Remarks</span></span>

<span data-ttu-id="b054e-117">Cette propriété peut être laissée non jeun.</span><span class="sxs-lookup"><span data-stu-id="b054e-117">This property may be left unset.</span></span> <span data-ttu-id="b054e-118">Si elle est définie, sa valeur doit être supérieure à « 0x800186A0 » (-2 147 383 648) et inférieure à « 0x7FFE7960 » (2 147 383 648) et doit être unique parmi les tâches du même dossier.</span><span class="sxs-lookup"><span data-stu-id="b054e-118">If set, its value must be greater than "0x800186A0" (-2,147,383,648) and less than "0x7FFE7960" (2,147,383,648) and must be unique among tasks in the same folder.</span></span>
  
<span data-ttu-id="b054e-119">Chaque fois que le client définit cette propriété sur un nombre inférieur au négatif de la valeur actuelle de la propriété **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) du dossier, le client doit également mettre à jour PR_ORDINAL_MOST sur le dossier. </span><span class="sxs-lookup"><span data-stu-id="b054e-119">Whenever the client sets this property to a number less than the negative of the current value of the **PR_ORDINAL_MOST** ([PidTagOrdinalMost](pidtagordinalmost-canonical-property.md)) property of the folder, the client must also update **PR_ORDINAL_MOST** on the folder.</span></span> 
  
<span data-ttu-id="b054e-120">La **PR_ORDINAL_MOST** du dossier permet de déterminer efficacement une valeur unique parmi les tâches du même dossier.</span><span class="sxs-lookup"><span data-stu-id="b054e-120">The **PR_ORDINAL_MOST** property of the folder provides an efficient way to determine a unique value among tasks in the same folder.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b054e-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b054e-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b054e-122">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="b054e-122">Protocol specifications</span></span>

<span data-ttu-id="b054e-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b054e-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b054e-124">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="b054e-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b054e-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b054e-125">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b054e-126">Définit plusieurs objets qui modélisent l’équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.</span><span class="sxs-lookup"><span data-stu-id="b054e-126">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span> 
    
### <a name="header-files"></a><span data-ttu-id="b054e-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b054e-127">Header files</span></span>

<span data-ttu-id="b054e-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b054e-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="b054e-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b054e-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b054e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b054e-130">See also</span></span>



[<span data-ttu-id="b054e-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b054e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b054e-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b054e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b054e-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b054e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b054e-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="b054e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

