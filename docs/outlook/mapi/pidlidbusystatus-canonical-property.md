---
title: Propriété canonique PidLidBusyStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusyStatus
api_type:
- COM
ms.assetid: 50c91fe6-2a61-4348-a16d-fd5c501b0715
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 926f0425a4a59cad4280917573c974375c94f50b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785079"
---
# <a name="pidlidbusystatus-canonical-property"></a><span data-ttu-id="b1a42-103">Propriété canonique PidLidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="b1a42-103">PidLidBusyStatus Canonical Property</span></span>

  
  
<span data-ttu-id="b1a42-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b1a42-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b1a42-105">Représente la disponibilité de l’utilisateur pour un rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="b1a42-105">Represents the user's availability for an appointment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b1a42-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b1a42-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b1a42-107">dispidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="b1a42-107">dispidBusyStatus</span></span>  <br/> |
|<span data-ttu-id="b1a42-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="b1a42-108">Property set:</span></span>  <br/> |<span data-ttu-id="b1a42-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="b1a42-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="b1a42-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="b1a42-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b1a42-111">0x00008205</span><span class="sxs-lookup"><span data-stu-id="b1a42-111">0x00008205</span></span>  <br/> |
|<span data-ttu-id="b1a42-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b1a42-112">Data type:</span></span>  <br/> |<span data-ttu-id="b1a42-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b1a42-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b1a42-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="b1a42-114">Area:</span></span>  <br/> |<span data-ttu-id="b1a42-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="b1a42-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1a42-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="b1a42-116">Remarks</span></span>

<span data-ttu-id="b1a42-117">Cette propriété spécifie la disponibilité d’un utilisateur pour l’événement décrit par l’objet et doit être une des valeurs ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b1a42-117">This property specifies the availability of a user for the event described by the object and must be one of the values specified below.</span></span>
  
|<span data-ttu-id="b1a42-118">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="b1a42-118">**Value**</span></span>|<span data-ttu-id="b1a42-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="b1a42-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b1a42-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="b1a42-120">0x00000000</span></span>  <br/> |<span data-ttu-id="b1a42-121">L'utilisateur est disponible.</span><span class="sxs-lookup"><span data-stu-id="b1a42-121">The user is available.</span></span>  <br/> |
|<span data-ttu-id="b1a42-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b1a42-122">0x00000001</span></span>  <br/> |<span data-ttu-id="b1a42-123">L’utilisateur dispose d’un événement provisoire de prévu.</span><span class="sxs-lookup"><span data-stu-id="b1a42-123">The user has a tentative event scheduled.</span></span>  <br/> |
|<span data-ttu-id="b1a42-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b1a42-124">0x00000002</span></span>  <br/> |<span data-ttu-id="b1a42-125">L'utilisateur est occupé.</span><span class="sxs-lookup"><span data-stu-id="b1a42-125">The user is busy.</span></span>  <br/> |
|<span data-ttu-id="b1a42-126">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="b1a42-126">0x00000003</span></span>  <br/> |<span data-ttu-id="b1a42-127">L'utilisateur est absent du bureau.</span><span class="sxs-lookup"><span data-stu-id="b1a42-127">The user is out of office.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="b1a42-128">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b1a42-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b1a42-129">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="b1a42-129">Protocol specifications</span></span>

<span data-ttu-id="b1a42-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1a42-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1a42-131">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="b1a42-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b1a42-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b1a42-132">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b1a42-133">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="b1a42-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b1a42-134">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b1a42-134">Header files</span></span>

<span data-ttu-id="b1a42-135">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b1a42-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="b1a42-136">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b1a42-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b1a42-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1a42-137">See also</span></span>



[<span data-ttu-id="b1a42-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b1a42-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b1a42-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b1a42-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b1a42-140">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b1a42-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b1a42-141">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="b1a42-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

