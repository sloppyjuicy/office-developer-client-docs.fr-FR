---
title: Propriété canonique PidLidFExceptionalAttendees
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFExceptionalAttendees
api_type:
- COM
ms.assetid: f1f489a3-e83a-4e96-bf9a-d98bc17d29f5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 544b5b5ac945eeedf787af0e311491da1f9d0217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327474"
---
# <a name="pidlidfexceptionalattendees-canonical-property"></a><span data-ttu-id="8217e-103">Propriété canonique PidLidFExceptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="8217e-103">PidLidFExceptionalAttendees Canonical Property</span></span>

  
  
<span data-ttu-id="8217e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8217e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8217e-105">Indique si cette propriété est un objet calendrier périodique avec une ou plusieurs exceptions, et qu’au moins l’une des exceptions incorporées a au moins un RecipientRow.</span><span class="sxs-lookup"><span data-stu-id="8217e-105">Indicates whether this property is a recurring calendar object with one or more exceptions, and at least one of the exception embedded messages has at least one RecipientRow.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8217e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8217e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8217e-107">dispidFExceptionalAttendees</span><span class="sxs-lookup"><span data-stu-id="8217e-107">dispidFExceptionalAttendees</span></span>  <br/> |
|<span data-ttu-id="8217e-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="8217e-108">Property set:</span></span>  <br/> |<span data-ttu-id="8217e-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="8217e-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="8217e-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="8217e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8217e-111">0x0000822B</span><span class="sxs-lookup"><span data-stu-id="8217e-111">0x0000822B</span></span>  <br/> |
|<span data-ttu-id="8217e-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8217e-112">Data type:</span></span>  <br/> |<span data-ttu-id="8217e-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8217e-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8217e-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="8217e-114">Area:</span></span>  <br/> |<span data-ttu-id="8217e-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="8217e-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8217e-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="8217e-116">Remarks</span></span>

<span data-ttu-id="8217e-117">La valeur FALSE ou l’absence de cette propriété indique que l’objet calendrier n’a pas d’exceptions ou qu’aucun des messages incorporés d’exception n’a RecipientRows.</span><span class="sxs-lookup"><span data-stu-id="8217e-117">A value of FALSE, or the absence of this property, indicates that the calendar object either has no exceptions, or none of the exception embedded messages has RecipientRows.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8217e-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8217e-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8217e-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="8217e-119">Protocol specifications</span></span>

<span data-ttu-id="8217e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8217e-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8217e-121">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="8217e-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8217e-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8217e-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8217e-123">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="8217e-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8217e-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8217e-124">Header files</span></span>

<span data-ttu-id="8217e-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8217e-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="8217e-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8217e-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8217e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8217e-127">See also</span></span>



[<span data-ttu-id="8217e-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8217e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8217e-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8217e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8217e-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8217e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8217e-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="8217e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

