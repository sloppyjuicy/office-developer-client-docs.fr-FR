---
title: Propriété canonique PidLidRecurring
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRecurring
api_type:
- COM
ms.assetid: 3d39a053-277f-4d59-ab2e-cee81710f2ab
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 36bf204823711e87ac6250f0997445f2745fbc19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785353"
---
# <a name="pidlidrecurring-canonical-property"></a><span data-ttu-id="0f42e-103">Propriété canonique PidLidRecurring</span><span class="sxs-lookup"><span data-stu-id="0f42e-103">PidLidRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="0f42e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0f42e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0f42e-105">Indique si un message d’un rendez-vous périodique.</span><span class="sxs-lookup"><span data-stu-id="0f42e-105">Specifies whether an appointment message is recurrent.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0f42e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0f42e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0f42e-107">dispidRecurring</span><span class="sxs-lookup"><span data-stu-id="0f42e-107">dispidRecurring</span></span>  <br/> |
|<span data-ttu-id="0f42e-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="0f42e-108">Property set:</span></span>  <br/> |<span data-ttu-id="0f42e-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="0f42e-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="0f42e-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="0f42e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0f42e-111">0x00008223</span><span class="sxs-lookup"><span data-stu-id="0f42e-111">0x00008223</span></span>  <br/> |
|<span data-ttu-id="0f42e-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0f42e-112">Data type:</span></span>  <br/> |<span data-ttu-id="0f42e-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0f42e-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0f42e-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="0f42e-114">Area:</span></span>  <br/> |<span data-ttu-id="0f42e-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="0f42e-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f42e-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="0f42e-116">Remarks</span></span>

<span data-ttu-id="0f42e-117">Cette propriété a la valeur TRUE si le rendez-vous est un rendez-vous périodique et a la valeur FALSE si elle n’est pas périodique.</span><span class="sxs-lookup"><span data-stu-id="0f42e-117">This property is TRUE if the appointment is a recurring appointment, and is FALSE if it is not recurring.</span></span>
  
<span data-ttu-id="0f42e-118">Cette propriété spécifie si l’objet représente une série périodique.</span><span class="sxs-lookup"><span data-stu-id="0f42e-118">This property specifies whether or not the object represents a recurring series.</span></span> <span data-ttu-id="0f42e-119">La valeur TRUE indique que l’objet représente une série périodique.</span><span class="sxs-lookup"><span data-stu-id="0f42e-119">A value of TRUE indicates that the object represents a recurring series.</span></span> <span data-ttu-id="0f42e-120">La valeur FALSE, ou l’absence de cette propriété, indique que l’objet représente une instance unique ou une exception (y compris une instance orpheline).</span><span class="sxs-lookup"><span data-stu-id="0f42e-120">A value of FALSE, or the absence of this property, indicates that the object represents either a single instance or an exception (including an orphan instance).</span></span> <span data-ttu-id="0f42e-121">Notez la différence entre cette propriété et la propriété **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0f42e-121">Note the difference between this property and the **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0f42e-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0f42e-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0f42e-123">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="0f42e-123">Protocol specifications</span></span>

<span data-ttu-id="0f42e-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f42e-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f42e-125">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="0f42e-125">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0f42e-126">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0f42e-126">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0f42e-127">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="0f42e-127">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0f42e-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0f42e-128">Header files</span></span>

<span data-ttu-id="0f42e-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0f42e-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="0f42e-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0f42e-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0f42e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f42e-131">See also</span></span>



[<span data-ttu-id="0f42e-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0f42e-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0f42e-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0f42e-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0f42e-134">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0f42e-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0f42e-135">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="0f42e-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

