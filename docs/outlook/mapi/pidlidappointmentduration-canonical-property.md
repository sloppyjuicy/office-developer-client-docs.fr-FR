---
title: Propriété canonique PidLidAppointmentDuration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentDuration
api_type:
- COM
ms.assetid: 92c07a81-9dec-4118-af1f-02ecad340f07
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8ce9df6290fe6e50e52c632f0a14f226c4d715d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345394"
---
# <a name="pidlidappointmentduration-canonical-property"></a><span data-ttu-id="08caf-103">Propriété canonique PidLidAppointmentDuration</span><span class="sxs-lookup"><span data-stu-id="08caf-103">PidLidAppointmentDuration Canonical Property</span></span>

  
  
<span data-ttu-id="08caf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08caf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08caf-105">Représente la durée, en minutes, de planification d'un rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="08caf-105">Represents the length of time, in minutes, when an appointment is scheduled.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="08caf-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="08caf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08caf-107">dispidApptDuration</span><span class="sxs-lookup"><span data-stu-id="08caf-107">dispidApptDuration</span></span>  <br/> |
|<span data-ttu-id="08caf-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="08caf-108">Property set:</span></span>  <br/> |<span data-ttu-id="08caf-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="08caf-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="08caf-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="08caf-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="08caf-111">0x00008213</span><span class="sxs-lookup"><span data-stu-id="08caf-111">0x00008213</span></span>  <br/> |
|<span data-ttu-id="08caf-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="08caf-112">Data type:</span></span>  <br/> |<span data-ttu-id="08caf-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="08caf-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="08caf-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="08caf-114">Area:</span></span>  <br/> |<span data-ttu-id="08caf-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="08caf-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08caf-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="08caf-116">Remarks</span></span>

<span data-ttu-id="08caf-117">La valeur doit être le nombre de minutes entre la valeur des propriétés **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) et **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="08caf-117">The value must be the number of minutes between the value of the **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) and the **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="08caf-118">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="08caf-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="08caf-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="08caf-119">Protocol specifications</span></span>

<span data-ttu-id="08caf-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08caf-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08caf-121">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="08caf-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="08caf-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08caf-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08caf-123">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="08caf-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="08caf-124">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="08caf-124">Header files</span></span>

<span data-ttu-id="08caf-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="08caf-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="08caf-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="08caf-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08caf-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08caf-127">See also</span></span>



[<span data-ttu-id="08caf-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="08caf-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08caf-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="08caf-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08caf-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="08caf-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08caf-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="08caf-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

