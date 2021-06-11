---
title: Propriété canonique PidLidReminderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderSet
api_type:
- COM
ms.assetid: 06b7792c-1b43-4e20-9a3b-44f2664b2125
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 59379b0b1345684a491f2f7f896f2b8fc8fd54c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335153"
---
# <a name="pidlidreminderset-canonical-property"></a><span data-ttu-id="a6a3c-103">Propriété canonique PidLidReminderSet</span><span class="sxs-lookup"><span data-stu-id="a6a3c-103">PidLidReminderSet Canonical Property</span></span>

  
  
<span data-ttu-id="a6a3c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6a3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6a3c-105">Spécifie si un rappel est définie sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="a6a3c-105">Specifies whether a reminder is set on the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a6a3c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a6a3c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a6a3c-107">dispidReminderSet</span><span class="sxs-lookup"><span data-stu-id="a6a3c-107">dispidReminderSet</span></span>  <br/> |
|<span data-ttu-id="a6a3c-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="a6a3c-108">Property set:</span></span>  <br/> |<span data-ttu-id="a6a3c-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a6a3c-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a6a3c-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="a6a3c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a6a3c-111">0x00008503</span><span class="sxs-lookup"><span data-stu-id="a6a3c-111">0x00008503</span></span>  <br/> |
|<span data-ttu-id="a6a3c-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a6a3c-112">Data type:</span></span>  <br/> |<span data-ttu-id="a6a3c-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="a6a3c-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="a6a3c-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a6a3c-114">Area:</span></span>  <br/> |<span data-ttu-id="a6a3c-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="a6a3c-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6a3c-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="a6a3c-116">Remarks</span></span>

<span data-ttu-id="a6a3c-117">Si cette propriété est définie sur TRUE pour un objet calendrier périodique, le client peut remplacer cette valeur pour les exceptions.</span><span class="sxs-lookup"><span data-stu-id="a6a3c-117">If a recurring calendar object has this property set to TRUE, the client can override this value for exceptions.</span></span>
  
<span data-ttu-id="a6a3c-118">Si cette propriété a la valeur FALSE sur un objet calendrier périodique, les rappels sont désactivés pour toute la série, y compris les exceptions.</span><span class="sxs-lookup"><span data-stu-id="a6a3c-118">If this property is FALSE on a recurring calendar object, reminders are disabled for the entire series, including exceptions.</span></span> <span data-ttu-id="a6a3c-119">Pour les objets de tâche périodiques, cette propriété ne peut pas être masquée par des exceptions (voir [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) et [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) pour plus d’informations).</span><span class="sxs-lookup"><span data-stu-id="a6a3c-119">For recurring task objects, this property cannot be overridden by exceptions (see [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) and [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) for details).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a6a3c-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a6a3c-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a6a3c-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="a6a3c-121">Protocol specifications</span></span>

<span data-ttu-id="a6a3c-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6a3c-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6a3c-123">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="a6a3c-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a6a3c-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a6a3c-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a6a3c-125">Spécifie les propriétés et le modèle d’interaction pour les messages électroniques et autres rappels d’objets.</span><span class="sxs-lookup"><span data-stu-id="a6a3c-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a6a3c-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="a6a3c-126">Header files</span></span>

<span data-ttu-id="a6a3c-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a6a3c-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="a6a3c-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a6a3c-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a6a3c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6a3c-129">See also</span></span>



[<span data-ttu-id="a6a3c-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a6a3c-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a6a3c-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a6a3c-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a6a3c-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a6a3c-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a6a3c-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a6a3c-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

