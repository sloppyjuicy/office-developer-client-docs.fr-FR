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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1e1cba3d927072cb03dbd34eee518c9b0a9e0383
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785470"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a><span data-ttu-id="7e7d8-103">Propriété canonique PidLidTaskMultipleRecipients</span><span class="sxs-lookup"><span data-stu-id="7e7d8-103">PidLidTaskMultipleRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="7e7d8-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7e7d8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7e7d8-105">Fournit des conseils d’optimisation sur les destinataires d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="7e7d8-105">Provides optimization hints about the recipients of a task.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7e7d8-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="7e7d8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7e7d8-107">dispidTaskMultRecips</span><span class="sxs-lookup"><span data-stu-id="7e7d8-107">dispidTaskMultRecips</span></span>  <br/> |
|<span data-ttu-id="7e7d8-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="7e7d8-108">Property set:</span></span>  <br/> |<span data-ttu-id="7e7d8-109">PSETID_Task</span><span class="sxs-lookup"><span data-stu-id="7e7d8-109">PSETID_Task</span></span>  <br/> |
|<span data-ttu-id="7e7d8-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="7e7d8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7e7d8-111">0x00008120</span><span class="sxs-lookup"><span data-stu-id="7e7d8-111">0x00008120</span></span>  <br/> |
|<span data-ttu-id="7e7d8-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="7e7d8-112">Data type:</span></span>  <br/> |<span data-ttu-id="7e7d8-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7e7d8-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7e7d8-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="7e7d8-114">Area:</span></span>  <br/> |<span data-ttu-id="7e7d8-115">Tâche</span><span class="sxs-lookup"><span data-stu-id="7e7d8-115">Task</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e7d8-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="7e7d8-116">Remarks</span></span>

<span data-ttu-id="7e7d8-117">Si vous définissez, cette propriété doit être définie pour une opération de bits **OR** de zéro ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7e7d8-117">If set, this property must be set to a bitwise **OR** operation of zero or more of the following values.</span></span> 
  
|<span data-ttu-id="7e7d8-118">**Nom**</span><span class="sxs-lookup"><span data-stu-id="7e7d8-118">**Name**</span></span>|<span data-ttu-id="7e7d8-119">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="7e7d8-119">**Value**</span></span>|<span data-ttu-id="7e7d8-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="7e7d8-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7e7d8-121">Envoyé</span><span class="sxs-lookup"><span data-stu-id="7e7d8-121">Sent</span></span>  <br/> |<span data-ttu-id="7e7d8-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7e7d8-122">0x00000001</span></span>  <br/> |<span data-ttu-id="7e7d8-123">La tâche a plusieurs destinataires principaux.</span><span class="sxs-lookup"><span data-stu-id="7e7d8-123">The task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="7e7d8-124">Received</span><span class="sxs-lookup"><span data-stu-id="7e7d8-124">Received</span></span>  <br/> |<span data-ttu-id="7e7d8-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7e7d8-125">0x00000002</span></span>  <br/> |<span data-ttu-id="7e7d8-126">Bien que l’indicateur envoyés n’était pas présent, le client a détecté que la tâche a plusieurs destinataires principaux.</span><span class="sxs-lookup"><span data-stu-id="7e7d8-126">Although the Sent hint was not present, the client detected that the task has multiple primary recipients.</span></span>  <br/> |
|<span data-ttu-id="7e7d8-127">Réservé</span><span class="sxs-lookup"><span data-stu-id="7e7d8-127">Reserved</span></span>  <br/> |<span data-ttu-id="7e7d8-128">0 x 00000004</span><span class="sxs-lookup"><span data-stu-id="7e7d8-128">0x00000004</span></span>  <br/> |<span data-ttu-id="7e7d8-129">Cette valeur est réservée.</span><span class="sxs-lookup"><span data-stu-id="7e7d8-129">This value is reserved.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="7e7d8-130">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="7e7d8-130">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7e7d8-131">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="7e7d8-131">Protocol specifications</span></span>

<span data-ttu-id="7e7d8-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e7d8-132">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e7d8-133">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="7e7d8-133">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7e7d8-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7e7d8-134">[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7e7d8-135">Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.</span><span class="sxs-lookup"><span data-stu-id="7e7d8-135">Defines several objects that model the electronic equivalent of tasks, task assignments, and task updates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7e7d8-136">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="7e7d8-136">Header files</span></span>

<span data-ttu-id="7e7d8-137">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7e7d8-137">Mapidefs.h</span></span>
  
> <span data-ttu-id="7e7d8-138">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="7e7d8-138">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7e7d8-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e7d8-139">See also</span></span>



[<span data-ttu-id="7e7d8-140">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="7e7d8-140">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7e7d8-141">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="7e7d8-141">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7e7d8-142">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="7e7d8-142">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7e7d8-143">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="7e7d8-143">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

