---
title: Propriété canonique PidLidClipEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidClipEnd
api_type:
- COM
ms.assetid: 17c8db96-80dd-4a7a-9a1b-ab1b37ba616c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1353289da2b428fb58adecc6f7830a2eea4b519a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785094"
---
# <a name="pidlidclipend-canonical-property"></a><span data-ttu-id="ebedf-103">Propriété canonique PidLidClipEnd</span><span class="sxs-lookup"><span data-stu-id="ebedf-103">PidLidClipEnd Canonical Property</span></span>

  
  
<span data-ttu-id="ebedf-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ebedf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ebedf-105">Spécifie la date de fin et l’heure de l’événement dans le temps universel coordonné (UTC) pour les objets de calendrier d’instance unique.</span><span class="sxs-lookup"><span data-stu-id="ebedf-105">Specifies the end date and time of the event in Coordinated Universal Time (UTC) for single instance calendar objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ebedf-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ebedf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ebedf-107">dispidClipEnd</span><span class="sxs-lookup"><span data-stu-id="ebedf-107">dispidClipEnd</span></span>  <br/> |
|<span data-ttu-id="ebedf-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="ebedf-108">Property set:</span></span>  <br/> |<span data-ttu-id="ebedf-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="ebedf-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="ebedf-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="ebedf-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ebedf-111">0x00008236</span><span class="sxs-lookup"><span data-stu-id="ebedf-111">0x00008236</span></span>  <br/> |
|<span data-ttu-id="ebedf-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ebedf-112">Data type:</span></span>  <br/> |<span data-ttu-id="ebedf-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ebedf-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="ebedf-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="ebedf-114">Area:</span></span>  <br/> |<span data-ttu-id="ebedf-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="ebedf-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ebedf-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="ebedf-116">Remarks</span></span>

<span data-ttu-id="ebedf-117">Pour les objets de calendrier d’instance unique, il spécifie la date de fin et l’heure de l’événement au format UTC.</span><span class="sxs-lookup"><span data-stu-id="ebedf-117">For single instance calendar objects, it specifies the end date and time of the event in UTC.</span></span> <span data-ttu-id="ebedf-118">Pour une série périodique, cette propriété spécifie minuit à la date de la dernière instance de la série périodique au format UTC, sauf si la série périodique n’a aucun effet, auquel cas la valeur doit être le 31 août 4500, 11:59 p.m.</span><span class="sxs-lookup"><span data-stu-id="ebedf-118">For a recurring series, this property specifies midnight on the date of the last instance of the recurring series in UTC, unless the recurring series has no end, in which case the value must be 31 August 4500, 11:59 p.m.</span></span>
  
<span data-ttu-id="ebedf-119">La valeur de cette propriété doit être définie à la valeur de la **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ebedf-119">The value of this property must be set to the value of the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ebedf-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ebedf-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ebedf-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="ebedf-121">Protocol specifications</span></span>

<span data-ttu-id="ebedf-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ebedf-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ebedf-123">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="ebedf-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ebedf-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ebedf-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ebedf-125">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="ebedf-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ebedf-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ebedf-126">Header files</span></span>

<span data-ttu-id="ebedf-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ebedf-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="ebedf-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ebedf-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ebedf-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebedf-129">See also</span></span>



[<span data-ttu-id="ebedf-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ebedf-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ebedf-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ebedf-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ebedf-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ebedf-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ebedf-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="ebedf-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

