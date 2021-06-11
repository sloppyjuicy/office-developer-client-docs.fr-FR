---
title: Propri t canonique PidLidCalendarType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCalendarType
api_type:
- COM
ms.assetid: 06e066f1-2b7d-4a6b-b88c-85a9bfa83bd3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6a33559a3e047890153f6a8e0ab40e49c2bf80cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341992"
---
# <a name="pidlidcalendartype-canonical-property"></a><span data-ttu-id="03358-103">Propri t canonique PidLidCalendarType</span><span class="sxs-lookup"><span data-stu-id="03358-103">PidLidCalendarType Canonical Property</span></span>

  
  
<span data-ttu-id="03358-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03358-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03358-105">Spécifie la valeur du champ CalendarType à partir de la propriété **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="03358-105">Specifies the value of the CalendarType field from the **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="03358-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="03358-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="03358-107">LID_CALENDAR_TYPE</span><span class="sxs-lookup"><span data-stu-id="03358-107">LID_CALENDAR_TYPE</span></span>  <br/> |
|<span data-ttu-id="03358-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="03358-108">Property set:</span></span>  <br/> |<span data-ttu-id="03358-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="03358-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="03358-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="03358-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="03358-111">0x0000001C</span><span class="sxs-lookup"><span data-stu-id="03358-111">0x0000001C</span></span>  <br/> |
|<span data-ttu-id="03358-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="03358-112">Data type:</span></span>  <br/> |<span data-ttu-id="03358-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="03358-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="03358-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="03358-114">Area:</span></span>  <br/> |<span data-ttu-id="03358-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="03358-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03358-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="03358-116">Remarks</span></span>

<span data-ttu-id="03358-117">Lorsque la demande de réunion représente une série périodique ou une exception, il s’agit de la valeur du champ CalendarType de la propriété **dispidApptRecur.**</span><span class="sxs-lookup"><span data-stu-id="03358-117">When the meeting request represents a recurring series or an exception, this is the value of the CalendarType field from the **dispidApptRecur** property.</span></span> <span data-ttu-id="03358-118">Sinon, cette propriété n’est pas définie et est supposée être 0.</span><span class="sxs-lookup"><span data-stu-id="03358-118">Otherwise, this property is not set and assumed to be 0.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="03358-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="03358-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="03358-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="03358-120">Protocol specifications</span></span>

<span data-ttu-id="03358-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03358-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03358-122">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="03358-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="03358-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03358-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03358-124">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="03358-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="03358-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="03358-125">Header files</span></span>

<span data-ttu-id="03358-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03358-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="03358-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="03358-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03358-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03358-128">See also</span></span>



[<span data-ttu-id="03358-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="03358-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="03358-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="03358-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="03358-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="03358-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="03358-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="03358-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

