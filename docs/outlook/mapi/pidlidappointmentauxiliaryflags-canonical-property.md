---
title: Propriété canonique PidLidAppointmentAuxiliaryFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentAuxiliaryFlags
api_type:
- COM
ms.assetid: 56c64e23-4a99-4f80-ba06-dfae2a5fe961
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4414ae866dece0654131d1575fe699676892709f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345429"
---
# <a name="pidlidappointmentauxiliaryflags-canonical-property"></a><span data-ttu-id="e25b8-103">Propriété canonique PidLidAppointmentAuxiliaryFlags</span><span class="sxs-lookup"><span data-stu-id="e25b8-103">PidLidAppointmentAuxiliaryFlags Canonical Property</span></span>

  
  
<span data-ttu-id="e25b8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e25b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e25b8-105">Spécifie un champ de bits qui décrit l'État auxiliaire de l'objet.</span><span class="sxs-lookup"><span data-stu-id="e25b8-105">Specifies a bit field that describes the auxiliary state of the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e25b8-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e25b8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e25b8-107">dispidApptAuxFlags</span><span class="sxs-lookup"><span data-stu-id="e25b8-107">dispidApptAuxFlags</span></span>  <br/> |
|<span data-ttu-id="e25b8-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="e25b8-108">Property set:</span></span>  <br/> |<span data-ttu-id="e25b8-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="e25b8-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="e25b8-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="e25b8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e25b8-111">0x00008207</span><span class="sxs-lookup"><span data-stu-id="e25b8-111">0x00008207</span></span>  <br/> |
|<span data-ttu-id="e25b8-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e25b8-112">Data type:</span></span>  <br/> |<span data-ttu-id="e25b8-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e25b8-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e25b8-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e25b8-114">Area:</span></span>  <br/> |<span data-ttu-id="e25b8-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="e25b8-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e25b8-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="e25b8-116">Remarks</span></span>

<span data-ttu-id="e25b8-117">Cette propriété n'est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e25b8-117">This property is not required.</span></span> <span data-ttu-id="e25b8-118">Vous trouverez ci-dessous les indicateurs individuels qui peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="e25b8-118">Below are the individual flags that can be set.</span></span>
  
<span data-ttu-id="e25b8-119">C (auxApptFlagCopied, 0x00000001)</span><span class="sxs-lookup"><span data-stu-id="e25b8-119">C (auxApptFlagCopied, 0x00000001)</span></span>
  
> <span data-ttu-id="e25b8-120">Cet indicateur indique que l'objet de calendrier a été copié à partir d'un autre dossier de calendrier.</span><span class="sxs-lookup"><span data-stu-id="e25b8-120">This flag indicates that the calendar object was copied from another calendar folder.</span></span>
    
<span data-ttu-id="e25b8-121">R (auxApptFlagForceMtgResponse, 0x00000002)</span><span class="sxs-lookup"><span data-stu-id="e25b8-121">R (auxApptFlagForceMtgResponse, 0x00000002)</span></span>
  
> <span data-ttu-id="e25b8-122">Cet indicateur sur une demande de réunion indique que le client ou le serveur doit renvoyer une réponse à la réunion à l'organisateur lorsqu'une réponse est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="e25b8-122">This flag on a meeting request indicates that the client or server should send a meeting response back to the organizer when a response is chosen.</span></span>
    
<span data-ttu-id="e25b8-123">F (auxApptFlagForwarded, 0x00000004)</span><span class="sxs-lookup"><span data-stu-id="e25b8-123">F (auxApptFlagForwarded, 0x00000004)</span></span>
  
> <span data-ttu-id="e25b8-124">Cet indicateur sur une demande de réunion indique qu'il a été transféré (y compris en cours de transfert par l'organisateur), au lieu d'être une invitation de l'organisateur.</span><span class="sxs-lookup"><span data-stu-id="e25b8-124">This flag on a meeting request indicates that it was forwarded (including being forwarded by the organizer), rather than being an invitation from the organizer.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="e25b8-125">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="e25b8-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e25b8-126">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="e25b8-126">Protocol specifications</span></span>

<span data-ttu-id="e25b8-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e25b8-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e25b8-128">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="e25b8-128">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e25b8-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e25b8-129">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e25b8-130">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="e25b8-130">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e25b8-131">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="e25b8-131">Header files</span></span>

<span data-ttu-id="e25b8-132">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e25b8-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="e25b8-133">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e25b8-133">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e25b8-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e25b8-134">See also</span></span>



[<span data-ttu-id="e25b8-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e25b8-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e25b8-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e25b8-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e25b8-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e25b8-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e25b8-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e25b8-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

