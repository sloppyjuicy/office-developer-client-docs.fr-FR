---
title: Propriété canonique PidLidTaskState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskState
api_type:
- COM
ms.assetid: 06d1f8a3-53e1-4c9a-9703-75de7a11a772
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 149f238ea53e0669f4d95c8e6c2b17a2b5a1c209
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316533"
---
# <a name="pidlidtaskstate-canonical-property"></a><span data-ttu-id="3210d-103">Propriété canonique PidLidTaskState</span><span class="sxs-lookup"><span data-stu-id="3210d-103">PidLidTaskState Canonical Property</span></span>

  
  
<span data-ttu-id="3210d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3210d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3210d-105">Indique l’état d’affectation actuel de la tâche.</span><span class="sxs-lookup"><span data-stu-id="3210d-105">Indicates the current assignment state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3210d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3210d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3210d-107">dispidTaskState</span><span class="sxs-lookup"><span data-stu-id="3210d-107">dispidTaskState</span></span>  <br/> |
|<span data-ttu-id="3210d-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="3210d-108">Property set:</span></span>  <br/> |<span data-ttu-id="3210d-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="3210d-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="3210d-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="3210d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="3210d-111">0x00008113</span><span class="sxs-lookup"><span data-stu-id="3210d-111">0x00008113</span></span>  <br/> |
|<span data-ttu-id="3210d-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3210d-112">Data type:</span></span>  <br/> |<span data-ttu-id="3210d-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3210d-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3210d-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="3210d-114">Area:</span></span>  <br/> |<span data-ttu-id="3210d-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="3210d-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3210d-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="3210d-116">Remarks</span></span>

<span data-ttu-id="3210d-117">La valeur de cette propriété doit être l’une des suivantes.</span><span class="sxs-lookup"><span data-stu-id="3210d-117">The value of this property must be one of the following.</span></span>
  
|<span data-ttu-id="3210d-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="3210d-118">**Value**</span></span>|<span data-ttu-id="3210d-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="3210d-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3210d-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="3210d-120">0x00000000</span></span>  <br/> |<span data-ttu-id="3210d-121">Cette tâche a été créée pour correspondre à une tâche qui a été incorporée dans un rejet de tâche mais qui n’a pas pu être trouvée localement.</span><span class="sxs-lookup"><span data-stu-id="3210d-121">This task was created to correspond to a task that was embedded in a task rejection but could not be found locally.</span></span>  <br/> |
|<span data-ttu-id="3210d-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="3210d-122">0x00000001</span></span>  <br/> |<span data-ttu-id="3210d-123">La tâche n’est pas affectée.</span><span class="sxs-lookup"><span data-stu-id="3210d-123">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="3210d-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="3210d-124">0x00000002</span></span>  <br/> |<span data-ttu-id="3210d-125">La tâche est la copie de la tâche affectée à la personne affectée.</span><span class="sxs-lookup"><span data-stu-id="3210d-125">The task is the task assignee's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="3210d-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="3210d-126">0x00000003</span></span>  <br/> |<span data-ttu-id="3210d-127">La tâche est la copie d’une tâche affectée par l’assigneur de la tâche.</span><span class="sxs-lookup"><span data-stu-id="3210d-127">The task is the task assigner's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="3210d-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="3210d-128">0x00000004</span></span>  <br/> |<span data-ttu-id="3210d-129">La tâche est la copie d’une tâche rejetée par l’assigneur de la tâche.</span><span class="sxs-lookup"><span data-stu-id="3210d-129">The task is the task assigner's copy of a rejected task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="3210d-130">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3210d-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3210d-131">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="3210d-131">Protocol specifications</span></span>

<span data-ttu-id="3210d-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3210d-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3210d-133">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="3210d-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="3210d-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3210d-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3210d-135">Définit plusieurs objets qui modélisent l’équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.</span><span class="sxs-lookup"><span data-stu-id="3210d-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="3210d-136">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3210d-136">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3210d-137">Spécifie les propriétés et opérations permettant de créer et de localiser les dossiers spéciaux dans une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="3210d-137">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="3210d-138">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3210d-138">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3210d-139">Convertit les objets RFC2445, RFC2446 et RFC2447 de l’IETF, ainsi que les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="3210d-139">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="3210d-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3210d-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3210d-141">Gère l’ordre et le flux des transferts de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="3210d-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3210d-142">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3210d-142">Header files</span></span>

<span data-ttu-id="3210d-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3210d-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="3210d-144">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3210d-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3210d-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3210d-145">See also</span></span>



[<span data-ttu-id="3210d-146">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3210d-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3210d-147">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3210d-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3210d-148">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3210d-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3210d-149">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="3210d-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

