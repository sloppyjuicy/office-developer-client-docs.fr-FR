---
title: Propriété canonique PidLidTaskStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStatus
api_type:
- COM
ms.assetid: 809776b7-ff00-4a52-84b9-8b5fb5f5c3e3
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: a89cf096e3775b57035be60cab01e3d687770cf8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582573"
---
# <a name="pidlidtaskstatus-canonical-property"></a><span data-ttu-id="20d7f-103">Propriété canonique PidLidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="20d7f-103">PidLidTaskStatus Canonical Property</span></span>

  
  
<span data-ttu-id="20d7f-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20d7f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20d7f-105">Spécifie l’état d’avancement de l’utilisateur sur la tâche.</span><span class="sxs-lookup"><span data-stu-id="20d7f-105">Specifies the status of the user's progress on the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="20d7f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="20d7f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="20d7f-107">dispidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="20d7f-107">dispidTaskStatus</span></span>  <br/> |
|<span data-ttu-id="20d7f-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="20d7f-108">Property set:</span></span>  <br/> |<span data-ttu-id="20d7f-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="20d7f-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="20d7f-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="20d7f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="20d7f-111">0x00008101</span><span class="sxs-lookup"><span data-stu-id="20d7f-111">0x00008101</span></span>  <br/> |
|<span data-ttu-id="20d7f-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="20d7f-112">Data type:</span></span>  <br/> |<span data-ttu-id="20d7f-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="20d7f-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="20d7f-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="20d7f-114">Area:</span></span>  <br/> |<span data-ttu-id="20d7f-115">Task</span><span class="sxs-lookup"><span data-stu-id="20d7f-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20d7f-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="20d7f-116">Remarks</span></span>

<span data-ttu-id="20d7f-117">La valeur de cette propriété doit avoir une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="20d7f-117">The value of this property must be set to one of the following.</span></span>
  
|<span data-ttu-id="20d7f-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="20d7f-118">**Value**</span></span>|<span data-ttu-id="20d7f-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="20d7f-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="20d7f-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="20d7f-120">0x00000000</span></span>  <br/> |<span data-ttu-id="20d7f-121">L’utilisateur n’a pas démarré travail sur la tâche.</span><span class="sxs-lookup"><span data-stu-id="20d7f-121">The user has not started work on the task.</span></span> <span data-ttu-id="20d7f-122">Si cette valeur est définie, **dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) doit être 0.0.</span><span class="sxs-lookup"><span data-stu-id="20d7f-122">If this value is set, **dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) must be 0.0.</span></span>  <br/> |
|<span data-ttu-id="20d7f-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="20d7f-123">0x00000001</span></span>  <br/> |<span data-ttu-id="20d7f-124">À exécuter l’utilisateur cette tâche est en cours.</span><span class="sxs-lookup"><span data-stu-id="20d7f-124">The user's work on this task is in progress.</span></span> <span data-ttu-id="20d7f-125">Si cette valeur est définie, **dispidPercentComplete** doit être supérieure à 0,0 et inférieur à 1,0.</span><span class="sxs-lookup"><span data-stu-id="20d7f-125">If this value is set, **dispidPercentComplete** must be greater than 0.0 and less than 1.0.</span></span>  <br/> |
|<span data-ttu-id="20d7f-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="20d7f-126">0x00000002</span></span>  <br/> |<span data-ttu-id="20d7f-127">À exécuter l’utilisateur cette tâche est terminée.</span><span class="sxs-lookup"><span data-stu-id="20d7f-127">The user's work on this task is complete.</span></span> <span data-ttu-id="20d7f-128">Si cette valeur est définie, **dispidPercentComplete** doit être 1.0, **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) doit être la date actuelle, et **dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) doit avoir la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="20d7f-128">If this value is set, **dispidPercentComplete** must be 1.0, **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) must be the current date, and **dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) must be TRUE.</span></span>  <br/> |
|<span data-ttu-id="20d7f-129">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="20d7f-129">0x00000003</span></span>  <br/> |<span data-ttu-id="20d7f-130">L’utilisateur est en attente de quelqu'un d’autre.</span><span class="sxs-lookup"><span data-stu-id="20d7f-130">The user is waiting on somebody else.</span></span>  <br/> |
|<span data-ttu-id="20d7f-131">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="20d7f-131">0x00000004</span></span>  <br/> |<span data-ttu-id="20d7f-132">L’utilisateur a différé le travail sur la tâche.</span><span class="sxs-lookup"><span data-stu-id="20d7f-132">The user has deferred work on the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="20d7f-133">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="20d7f-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="20d7f-134">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="20d7f-134">Protocol specifications</span></span>

<span data-ttu-id="20d7f-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20d7f-135">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20d7f-136">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="20d7f-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="20d7f-137">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20d7f-137">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20d7f-138">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="20d7f-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="20d7f-139">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20d7f-139">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20d7f-140">Spécifie les propriétés et les opérations liées aux marquage.</span><span class="sxs-lookup"><span data-stu-id="20d7f-140">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="20d7f-141">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20d7f-141">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20d7f-142">Spécifie les propriétés et opérations pour la création et la localisation des dossiers spéciaux dans une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="20d7f-142">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="20d7f-143">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20d7f-143">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20d7f-144">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="20d7f-144">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="20d7f-145">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20d7f-145">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20d7f-146">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="20d7f-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="20d7f-147">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20d7f-147">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20d7f-148">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="20d7f-148">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="20d7f-149">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="20d7f-149">Header files</span></span>

<span data-ttu-id="20d7f-150">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="20d7f-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="20d7f-151">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="20d7f-151">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="20d7f-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20d7f-152">See also</span></span>



[<span data-ttu-id="20d7f-153">Propriété canonique PidLidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="20d7f-153">PidLidPercentComplete Canonical Property</span></span>](pidlidpercentcomplete-canonical-property.md)
  
[<span data-ttu-id="20d7f-154">Propriété canonique PidLidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="20d7f-154">PidLidTaskDateCompleted Canonical Property</span></span>](pidlidtaskdatecompleted-canonical-property.md)
  
[<span data-ttu-id="20d7f-155">Propriété canonique PidLidTaskComplete</span><span class="sxs-lookup"><span data-stu-id="20d7f-155">PidLidTaskComplete Canonical Property</span></span>](pidlidtaskcomplete-canonical-property.md)


[<span data-ttu-id="20d7f-156">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="20d7f-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="20d7f-157">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="20d7f-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="20d7f-158">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="20d7f-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="20d7f-159">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="20d7f-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

