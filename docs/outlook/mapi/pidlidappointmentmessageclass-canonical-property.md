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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7149ba5a4a0378951942df790003b6d09c1155f5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393417"
---
# <a name="pidlidappointmentmessageclass-canonical-property"></a><span data-ttu-id="08208-103">Propriété canonique PidLidAppointmentMessageClass</span><span class="sxs-lookup"><span data-stu-id="08208-103">PidLidAppointmentMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="08208-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08208-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08208-105">Indique la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) de la réunion doit être généré à partir de la demande de réunion.</span><span class="sxs-lookup"><span data-stu-id="08208-105">Indicates the **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property of the meeting that is to be generated from the meeting request.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="08208-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="08208-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08208-107">dispidApptMessageClass</span><span class="sxs-lookup"><span data-stu-id="08208-107">dispidApptMessageClass</span></span>  <br/> |
|<span data-ttu-id="08208-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="08208-108">Property set:</span></span>  <br/> |<span data-ttu-id="08208-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="08208-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="08208-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="08208-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="08208-111">0 x 00000024</span><span class="sxs-lookup"><span data-stu-id="08208-111">0x00000024</span></span>  <br/> |
|<span data-ttu-id="08208-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="08208-112">Data type:</span></span>  <br/> |<span data-ttu-id="08208-113">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="08208-113">PT_TSTRING</span></span>  <br/> |
|<span data-ttu-id="08208-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="08208-114">Area:</span></span>  <br/> |<span data-ttu-id="08208-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="08208-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08208-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="08208-116">Remarks</span></span>

<span data-ttu-id="08208-117">La valeur de cette propriété doit être « IPM. Rendez-vous » ou doit être signalée par « IPM. Rendez-vous. ».</span><span class="sxs-lookup"><span data-stu-id="08208-117">The value of this property must either be "IPM.Appointment" or be prefixed with "IPM.Appointment.".</span></span> <span data-ttu-id="08208-118">Cette propriété n’est pas requise.</span><span class="sxs-lookup"><span data-stu-id="08208-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="08208-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="08208-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="08208-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="08208-120">Protocol specifications</span></span>

<span data-ttu-id="08208-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08208-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08208-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="08208-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="08208-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08208-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08208-124">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="08208-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="08208-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="08208-125">Header files</span></span>

<span data-ttu-id="08208-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="08208-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="08208-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="08208-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08208-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08208-128">See also</span></span>



[<span data-ttu-id="08208-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="08208-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08208-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="08208-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08208-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="08208-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08208-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="08208-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

