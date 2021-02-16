---
title: Propriété canonique PidLidTaskMultipleRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMultipleRecipients
api_type:
- COM
ms.assetid: 28ba9997-72dd-465f-94a7-35a317a361ef
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3b260917e107086dee6176f73b6c82c3a1825327
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360066"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a><span data-ttu-id="5da6d-103">Propriété canonique PidLidTaskMultipleRecipients</span><span class="sxs-lookup"><span data-stu-id="5da6d-103">PidLidTaskMultipleRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="5da6d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5da6d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5da6d-105">Fournit des conseils d’optimisation sur les destinataires d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="5da6d-105">Provides optimization hints about the recipients of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5da6d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5da6d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5da6d-107">dispidTaskMultRecips</span><span class="sxs-lookup"><span data-stu-id="5da6d-107">dispidTaskMultRecips</span></span>  <br/> |
|<span data-ttu-id="5da6d-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="5da6d-108">Property set:</span></span>  <br/> |<span data-ttu-id="5da6d-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="5da6d-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="5da6d-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="5da6d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="5da6d-111">0x00008120</span><span class="sxs-lookup"><span data-stu-id="5da6d-111">0x00008120</span></span>  <br/> |
|<span data-ttu-id="5da6d-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5da6d-112">Data type:</span></span>  <br/> |<span data-ttu-id="5da6d-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5da6d-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5da6d-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5da6d-114">Area:</span></span>  <br/> |<span data-ttu-id="5da6d-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="5da6d-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5da6d-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="5da6d-116">Remarks</span></span>

<span data-ttu-id="5da6d-117">Si elle est définie, cette propriété doit être définie sur une opération **OR** au niveau du bit de zéro ou de plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="5da6d-117">If set, this property must be set to a bitwise **OR** operation of zero or more of the following values.</span></span> 
  
|<span data-ttu-id="5da6d-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="5da6d-118">**Name**</span></span>|<span data-ttu-id="5da6d-119">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="5da6d-119">**Value**</span></span>|<span data-ttu-id="5da6d-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="5da6d-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5da6d-121">Sent</span><span class="sxs-lookup"><span data-stu-id="5da6d-121">Sent</span></span>  <br/> |<span data-ttu-id="5da6d-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5da6d-122">0x00000001</span></span>  <br/> |<span data-ttu-id="5da6d-123">La tâche a plusieurs destinataires principaux.</span><span class="sxs-lookup"><span data-stu-id="5da6d-123">The task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="5da6d-124">Received</span><span class="sxs-lookup"><span data-stu-id="5da6d-124">Received</span></span>  <br/> |<span data-ttu-id="5da6d-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5da6d-125">0x00000002</span></span>  <br/> |<span data-ttu-id="5da6d-126">Bien que l’indication Envoyée ne soit pas présente, le client a détecté que la tâche a plusieurs destinataires principaux.</span><span class="sxs-lookup"><span data-stu-id="5da6d-126">Although the Sent hint was not present, the client detected that the task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="5da6d-127">Reserved</span><span class="sxs-lookup"><span data-stu-id="5da6d-127">Reserved</span></span>  <br/> |<span data-ttu-id="5da6d-128">0x00000004</span><span class="sxs-lookup"><span data-stu-id="5da6d-128">0x00000004</span></span>  <br/> |<span data-ttu-id="5da6d-129">Cette valeur est réservée.</span><span class="sxs-lookup"><span data-stu-id="5da6d-129">This value is reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5da6d-130">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5da6d-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5da6d-131">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="5da6d-131">Protocol specifications</span></span>

<span data-ttu-id="5da6d-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5da6d-132">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5da6d-133">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="5da6d-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5da6d-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5da6d-134">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5da6d-135">Définit plusieurs objets qui modélisent l’équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.</span><span class="sxs-lookup"><span data-stu-id="5da6d-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5da6d-136">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5da6d-136">Header files</span></span>

<span data-ttu-id="5da6d-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5da6d-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="5da6d-138">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5da6d-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5da6d-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5da6d-139">See also</span></span>



[<span data-ttu-id="5da6d-140">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5da6d-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5da6d-141">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5da6d-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5da6d-142">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5da6d-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5da6d-143">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5da6d-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

