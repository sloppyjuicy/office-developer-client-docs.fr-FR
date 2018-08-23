---
title: Propriété canonique PidLidAppointmentMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentMessageClass
api_type:
- COM
ms.assetid: 8b8c8484-0cb4-4842-8b11-de42d97e0140
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 4b26266e58a201b13aa178534039c9e07c900de0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569497"
---
# <a name="pidlidappointmentmessageclass-canonical-property"></a><span data-ttu-id="d1a95-103">Propriété canonique PidLidAppointmentMessageClass</span><span class="sxs-lookup"><span data-stu-id="d1a95-103">PidLidAppointmentMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="d1a95-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d1a95-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d1a95-105">Indique la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) de la réunion doit être généré à partir de la demande de réunion.</span><span class="sxs-lookup"><span data-stu-id="d1a95-105">Indicates the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the meeting that is to be generated from the meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d1a95-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d1a95-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d1a95-107">dispidApptMessageClass</span><span class="sxs-lookup"><span data-stu-id="d1a95-107">dispidApptMessageClass</span></span>  <br/> |
|<span data-ttu-id="d1a95-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="d1a95-108">Property set:</span></span>  <br/> |<span data-ttu-id="d1a95-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="d1a95-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="d1a95-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="d1a95-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d1a95-111">0 x 00000024</span><span class="sxs-lookup"><span data-stu-id="d1a95-111">0x00000024</span></span>  <br/> |
|<span data-ttu-id="d1a95-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d1a95-112">Data type:</span></span>  <br/> |<span data-ttu-id="d1a95-113">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="d1a95-113">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="d1a95-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d1a95-114">Area:</span></span>  <br/> |<span data-ttu-id="d1a95-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="d1a95-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1a95-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="d1a95-116">Remarks</span></span>

<span data-ttu-id="d1a95-117">La valeur de cette propriété doit être « IPM. Rendez-vous » ou doit être signalée par « IPM. Rendez-vous. ».</span><span class="sxs-lookup"><span data-stu-id="d1a95-117">The value of this property must either be "IPM.Appointment" or be prefixed with "IPM.Appointment.".</span></span> <span data-ttu-id="d1a95-118">Cette propriété n’est pas requise.</span><span class="sxs-lookup"><span data-stu-id="d1a95-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d1a95-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d1a95-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d1a95-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="d1a95-120">Protocol specifications</span></span>

<span data-ttu-id="d1a95-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1a95-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1a95-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="d1a95-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d1a95-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d1a95-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d1a95-124">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="d1a95-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d1a95-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d1a95-125">Header files</span></span>

<span data-ttu-id="d1a95-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d1a95-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="d1a95-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d1a95-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d1a95-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1a95-128">See also</span></span>



[<span data-ttu-id="d1a95-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d1a95-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d1a95-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d1a95-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d1a95-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d1a95-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d1a95-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="d1a95-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

