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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f2cd536a2f287e880388457586f6bdfa9f67f2b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590847"
---
# <a name="pidlidtaskstate-canonical-property"></a><span data-ttu-id="61d25-103">Propriété canonique PidLidTaskState</span><span class="sxs-lookup"><span data-stu-id="61d25-103">PidLidTaskState Canonical Property</span></span>

  
  
<span data-ttu-id="61d25-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61d25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61d25-105">Indique l’état d’affectation en cours de la tâche.</span><span class="sxs-lookup"><span data-stu-id="61d25-105">Indicates the current assignment state of the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="61d25-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="61d25-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="61d25-107">dispidTaskState</span><span class="sxs-lookup"><span data-stu-id="61d25-107">dispidTaskState</span></span>  <br/> |
|<span data-ttu-id="61d25-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="61d25-108">Property set:</span></span>  <br/> |<span data-ttu-id="61d25-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="61d25-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="61d25-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="61d25-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="61d25-111">0x00008113</span><span class="sxs-lookup"><span data-stu-id="61d25-111">0x00008113</span></span>  <br/> |
|<span data-ttu-id="61d25-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="61d25-112">Data type:</span></span>  <br/> |<span data-ttu-id="61d25-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="61d25-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="61d25-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="61d25-114">Area:</span></span>  <br/> |<span data-ttu-id="61d25-115">Task</span><span class="sxs-lookup"><span data-stu-id="61d25-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61d25-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="61d25-116">Remarks</span></span>

<span data-ttu-id="61d25-117">La valeur de cette propriété doit être une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="61d25-117">The value of this property must be one of the following.</span></span>
  
|<span data-ttu-id="61d25-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="61d25-118">**Value**</span></span>|<span data-ttu-id="61d25-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="61d25-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="61d25-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="61d25-120">0x00000000</span></span>  <br/> |<span data-ttu-id="61d25-121">Cette tâche a été créée pour correspondre à une tâche qui a été incorporée dans un refus de tâche, mais ne peut pas être trouvée localement.</span><span class="sxs-lookup"><span data-stu-id="61d25-121">This task was created to correspond to a task that was embedded in a task rejection but could not be found locally.</span></span>  <br/> |
|<span data-ttu-id="61d25-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="61d25-122">0x00000001</span></span>  <br/> |<span data-ttu-id="61d25-123">La tâche n’est pas affectée.</span><span class="sxs-lookup"><span data-stu-id="61d25-123">The task is not assigned.</span></span>  <br/> |
|<span data-ttu-id="61d25-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="61d25-124">0x00000002</span></span>  <br/> |<span data-ttu-id="61d25-125">La tâche est copie du destinataire de la tâche d’une tâche affectée.</span><span class="sxs-lookup"><span data-stu-id="61d25-125">The task is the task assignee's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="61d25-126">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="61d25-126">0x00000003</span></span>  <br/> |<span data-ttu-id="61d25-127">La tâche est la copie d’assigne la tâche d’une tâche affectée.</span><span class="sxs-lookup"><span data-stu-id="61d25-127">The task is the task assigner's copy of an assigned task.</span></span>  <br/> |
|<span data-ttu-id="61d25-128">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="61d25-128">0x00000004</span></span>  <br/> |<span data-ttu-id="61d25-129">La tâche est la copie d’assigne la tâche d’une tâche refusée.</span><span class="sxs-lookup"><span data-stu-id="61d25-129">The task is the task assigner's copy of a rejected task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="61d25-130">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="61d25-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="61d25-131">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="61d25-131">Protocol specifications</span></span>

<span data-ttu-id="61d25-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="61d25-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="61d25-133">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="61d25-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="61d25-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="61d25-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="61d25-135">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="61d25-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="61d25-136">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="61d25-136">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="61d25-137">Spécifie les propriétés et opérations pour la création et la localisation des dossiers spéciaux dans une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="61d25-137">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="61d25-138">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="61d25-138">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="61d25-139">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="61d25-139">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="61d25-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="61d25-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="61d25-141">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="61d25-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="61d25-142">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="61d25-142">Header files</span></span>

<span data-ttu-id="61d25-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="61d25-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="61d25-144">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="61d25-144">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="61d25-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61d25-145">See also</span></span>



[<span data-ttu-id="61d25-146">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="61d25-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="61d25-147">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="61d25-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="61d25-148">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="61d25-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="61d25-149">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="61d25-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

