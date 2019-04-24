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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d058b42ad7d1a1b8387aa5b9a1a65ea160d90b02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316666"
---
# <a name="pidlidtaskstatus-canonical-property"></a><span data-ttu-id="a0189-103">Propriété canonique PidLidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="a0189-103">PidLidTaskStatus Canonical Property</span></span>

  
  
<span data-ttu-id="a0189-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a0189-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a0189-105">Spécifie l'état d'avancement de l'utilisateur sur la tâche.</span><span class="sxs-lookup"><span data-stu-id="a0189-105">Specifies the status of the user's progress on the task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a0189-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a0189-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a0189-107">dispidTaskStatus</span><span class="sxs-lookup"><span data-stu-id="a0189-107">dispidTaskStatus</span></span>  <br/> |
|<span data-ttu-id="a0189-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="a0189-108">Property set:</span></span>  <br/> |<span data-ttu-id="a0189-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="a0189-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="a0189-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="a0189-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a0189-111">0x00008101</span><span class="sxs-lookup"><span data-stu-id="a0189-111">0x00008101</span></span>  <br/> |
|<span data-ttu-id="a0189-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a0189-112">Data type:</span></span>  <br/> |<span data-ttu-id="a0189-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a0189-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a0189-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a0189-114">Area:</span></span>  <br/> |<span data-ttu-id="a0189-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="a0189-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0189-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="a0189-116">Remarks</span></span>

<span data-ttu-id="a0189-117">La valeur de cette propriété doit être définie sur l'une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a0189-117">The value of this property must be set to one of the following.</span></span>
  
|<span data-ttu-id="a0189-118">**Value**</span><span class="sxs-lookup"><span data-stu-id="a0189-118">**Value**</span></span>|<span data-ttu-id="a0189-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="a0189-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a0189-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a0189-120">0x00000000</span></span>  <br/> |<span data-ttu-id="a0189-121">L'utilisateur n'a pas commencé à travailler sur la tâche.</span><span class="sxs-lookup"><span data-stu-id="a0189-121">The user has not started work on the task.</span></span> <span data-ttu-id="a0189-122">Si cette valeur est définie, **dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) doit être 0,0.</span><span class="sxs-lookup"><span data-stu-id="a0189-122">If this value is set, **dispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) must be 0.0.</span></span>  <br/> |
|<span data-ttu-id="a0189-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a0189-123">0x00000001</span></span>  <br/> |<span data-ttu-id="a0189-124">L'activité de l'utilisateur sur cette tâche est en cours.</span><span class="sxs-lookup"><span data-stu-id="a0189-124">The user's work on this task is in progress.</span></span> <span data-ttu-id="a0189-125">Si cette valeur est définie, **dispidPercentComplete** doit être supérieur à 0,0 et inférieur à 1,0.</span><span class="sxs-lookup"><span data-stu-id="a0189-125">If this value is set, **dispidPercentComplete** must be greater than 0.0 and less than 1.0.</span></span>  <br/> |
|<span data-ttu-id="a0189-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a0189-126">0x00000002</span></span>  <br/> |<span data-ttu-id="a0189-127">L'activité de l'utilisateur sur cette tâche est terminée.</span><span class="sxs-lookup"><span data-stu-id="a0189-127">The user's work on this task is complete.</span></span> <span data-ttu-id="a0189-128">Si cette valeur est définie, **dispidPercentComplete** doit être 1,0, **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) doit être la date actuelle et **dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) doit être true.</span><span class="sxs-lookup"><span data-stu-id="a0189-128">If this value is set, **dispidPercentComplete** must be 1.0, **dispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) must be the current date, and **dispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) must be TRUE.</span></span>  <br/> |
|<span data-ttu-id="a0189-129">0x00000003</span><span class="sxs-lookup"><span data-stu-id="a0189-129">0x00000003</span></span>  <br/> |<span data-ttu-id="a0189-130">L'utilisateur attend une autre personne.</span><span class="sxs-lookup"><span data-stu-id="a0189-130">The user is waiting on somebody else.</span></span>  <br/> |
|<span data-ttu-id="a0189-131">0x00000004</span><span class="sxs-lookup"><span data-stu-id="a0189-131">0x00000004</span></span>  <br/> |<span data-ttu-id="a0189-132">L'utilisateur a différé le travail sur la tâche.</span><span class="sxs-lookup"><span data-stu-id="a0189-132">The user has deferred work on the task.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="a0189-133">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="a0189-133">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a0189-134">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="a0189-134">Protocol specifications</span></span>

<span data-ttu-id="a0189-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0189-135">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0189-136">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="a0189-136">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a0189-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0189-137">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0189-138">Définit plusieurs objets qui modélisent l'équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.</span><span class="sxs-lookup"><span data-stu-id="a0189-138">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
<span data-ttu-id="a0189-139">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0189-139">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0189-140">Spécifie les propriétés et les opérations relatives au marquage.</span><span class="sxs-lookup"><span data-stu-id="a0189-140">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="a0189-141">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0189-141">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0189-142">Spécifie les propriétés et les opérations de création et de localisation des dossiers spéciaux dans une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="a0189-142">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="a0189-143">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0189-143">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0189-144">ConVertit des conventions de messagerie standard Internet en objets message.</span><span class="sxs-lookup"><span data-stu-id="a0189-144">Converts from Internet standard email conventions to message objects.</span></span>
    
<span data-ttu-id="a0189-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0189-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0189-146">Effectue une conversion entre l'IETF RFC2445, RFC2446 et RFC2447, et les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="a0189-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="a0189-147">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a0189-147">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a0189-148">Gère l'ordre et le flux de transfert de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="a0189-148">Handles the order and flow for data transfers between a client and server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a0189-149">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="a0189-149">Header files</span></span>

<span data-ttu-id="a0189-150">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a0189-150">Mapidefs.h</span></span>
  
> <span data-ttu-id="a0189-151">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a0189-151">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a0189-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0189-152">See also</span></span>



[<span data-ttu-id="a0189-153">Propriété canonique PidLidPercentComplete</span><span class="sxs-lookup"><span data-stu-id="a0189-153">PidLidPercentComplete Canonical Property</span></span>](pidlidpercentcomplete-canonical-property.md)
  
[<span data-ttu-id="a0189-154">Propriété canonique PidLidTaskDateCompleted</span><span class="sxs-lookup"><span data-stu-id="a0189-154">PidLidTaskDateCompleted Canonical Property</span></span>](pidlidtaskdatecompleted-canonical-property.md)
  
[<span data-ttu-id="a0189-155">Propriété canonique PidLidTaskComplete</span><span class="sxs-lookup"><span data-stu-id="a0189-155">PidLidTaskComplete Canonical Property</span></span>](pidlidtaskcomplete-canonical-property.md)


[<span data-ttu-id="a0189-156">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a0189-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a0189-157">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a0189-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a0189-158">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a0189-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a0189-159">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a0189-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

