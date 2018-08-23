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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f20c3e988c0a0461a966a109a8d345c22e1fccee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585737"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a><span data-ttu-id="e1ba9-103">Propriété canonique PidLidTaskMultipleRecipients</span><span class="sxs-lookup"><span data-stu-id="e1ba9-103">PidLidTaskMultipleRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="e1ba9-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1ba9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1ba9-105">Fournit des conseils d’optimisation sur les destinataires d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="e1ba9-105">Provides optimization hints about the recipients of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1ba9-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e1ba9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e1ba9-107">dispidTaskMultRecips</span><span class="sxs-lookup"><span data-stu-id="e1ba9-107">dispidTaskMultRecips</span></span>  <br/> |
|<span data-ttu-id="e1ba9-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="e1ba9-108">Property set:</span></span>  <br/> |<span data-ttu-id="e1ba9-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="e1ba9-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="e1ba9-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="e1ba9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e1ba9-111">0x00008120</span><span class="sxs-lookup"><span data-stu-id="e1ba9-111">0x00008120</span></span>  <br/> |
|<span data-ttu-id="e1ba9-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e1ba9-112">Data type:</span></span>  <br/> |<span data-ttu-id="e1ba9-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e1ba9-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e1ba9-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e1ba9-114">Area:</span></span>  <br/> |<span data-ttu-id="e1ba9-115">Task</span><span class="sxs-lookup"><span data-stu-id="e1ba9-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1ba9-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="e1ba9-116">Remarks</span></span>

<span data-ttu-id="e1ba9-117">Si vous définissez, cette propriété doit être définie pour une opération de bits **OR** de zéro ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e1ba9-117">If set, this property must be set to a bitwise **OR** operation of zero or more of the following values.</span></span> 
  
|<span data-ttu-id="e1ba9-118">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e1ba9-118">**Name**</span></span>|<span data-ttu-id="e1ba9-119">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="e1ba9-119">**Value**</span></span>|<span data-ttu-id="e1ba9-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="e1ba9-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e1ba9-121">Envoyé</span><span class="sxs-lookup"><span data-stu-id="e1ba9-121">Sent</span></span>  <br/> |<span data-ttu-id="e1ba9-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e1ba9-122">0x00000001</span></span>  <br/> |<span data-ttu-id="e1ba9-123">La tâche a plusieurs destinataires principaux.</span><span class="sxs-lookup"><span data-stu-id="e1ba9-123">The task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="e1ba9-124">Received</span><span class="sxs-lookup"><span data-stu-id="e1ba9-124">Received</span></span>  <br/> |<span data-ttu-id="e1ba9-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e1ba9-125">0x00000002</span></span>  <br/> |<span data-ttu-id="e1ba9-126">Bien que l’indicateur envoyés n’était pas présent, le client a détecté que la tâche a plusieurs destinataires principaux.</span><span class="sxs-lookup"><span data-stu-id="e1ba9-126">Although the Sent hint was not present, the client detected that the task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="e1ba9-127">Réservé</span><span class="sxs-lookup"><span data-stu-id="e1ba9-127">Reserved</span></span>  <br/> |<span data-ttu-id="e1ba9-128">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="e1ba9-128">0x00000004</span></span>  <br/> |<span data-ttu-id="e1ba9-129">Cette valeur est réservée.</span><span class="sxs-lookup"><span data-stu-id="e1ba9-129">This value is reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="e1ba9-130">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e1ba9-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e1ba9-131">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="e1ba9-131">Protocol specifications</span></span>

<span data-ttu-id="e1ba9-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1ba9-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1ba9-133">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="e1ba9-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e1ba9-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1ba9-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1ba9-135">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="e1ba9-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e1ba9-136">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e1ba9-136">Header files</span></span>

<span data-ttu-id="e1ba9-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e1ba9-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1ba9-138">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e1ba9-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1ba9-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1ba9-139">See also</span></span>



[<span data-ttu-id="e1ba9-140">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e1ba9-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1ba9-141">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e1ba9-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1ba9-142">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e1ba9-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1ba9-143">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e1ba9-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

