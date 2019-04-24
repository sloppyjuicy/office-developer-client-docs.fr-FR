---
title: Propriété canonique PidLidAllAttendeesString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAllAttendeesString
api_type:
- COM
ms.assetid: 2ffc0609-341d-4e35-8f53-ed3096c6fa7f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 96ad0727797475effd0563e4753070cb3bac4b37
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334775"
---
# <a name="pidlidallattendeesstring-canonical-property"></a><span data-ttu-id="784ec-103">Propriété canonique PidLidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="784ec-103">PidLidAllAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="784ec-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="784ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="784ec-105">Spécifie une liste de tous les participants à l'exception de l'organisateur, y compris les ressources et les participants non envoisables.</span><span class="sxs-lookup"><span data-stu-id="784ec-105">Specifies a list of all the attendees except for the organizer, including resources and unsendable attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="784ec-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="784ec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="784ec-107">dispidAllAttendeesString</span><span class="sxs-lookup"><span data-stu-id="784ec-107">dispidAllAttendeesString</span></span>  <br/> |
|<span data-ttu-id="784ec-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="784ec-108">Property set:</span></span>  <br/> |<span data-ttu-id="784ec-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="784ec-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="784ec-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="784ec-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="784ec-111">0x00008238</span><span class="sxs-lookup"><span data-stu-id="784ec-111">0x00008238</span></span>  <br/> |
|<span data-ttu-id="784ec-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="784ec-112">Data type:</span></span>  <br/> |<span data-ttu-id="784ec-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="784ec-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="784ec-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="784ec-114">Area:</span></span>  <br/> |<span data-ttu-id="784ec-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="784ec-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="784ec-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="784ec-116">Remarks</span></span>

<span data-ttu-id="784ec-117">La valeur de chaque participant est le nom d'affichage du participant.</span><span class="sxs-lookup"><span data-stu-id="784ec-117">The value for each attendee is the attendee's display name.</span></span> <span data-ttu-id="784ec-118">Les entrées distinctes doivent être délimitées par un point-virgule suivi d'un espace.</span><span class="sxs-lookup"><span data-stu-id="784ec-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="784ec-119">Cette propriété n'est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="784ec-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="784ec-120">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="784ec-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="784ec-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="784ec-121">Protocol specifications</span></span>

<span data-ttu-id="784ec-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="784ec-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="784ec-123">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="784ec-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="784ec-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="784ec-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="784ec-125">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="784ec-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="784ec-126">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="784ec-126">Header files</span></span>

<span data-ttu-id="784ec-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="784ec-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="784ec-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="784ec-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="784ec-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="784ec-129">See also</span></span>



[<span data-ttu-id="784ec-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="784ec-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="784ec-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="784ec-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="784ec-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="784ec-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="784ec-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="784ec-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

