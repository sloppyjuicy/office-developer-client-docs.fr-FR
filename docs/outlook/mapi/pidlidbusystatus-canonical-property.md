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
ms.openlocfilehash: cb73a0e09436177b8b53a05588508886ee28a0a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342027"
---
# <a name="pidlidbusystatus-canonical-property"></a><span data-ttu-id="1632d-103">Propriété canonique PidLidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="1632d-103">PidLidBusyStatus Canonical Property</span></span>

  
  
<span data-ttu-id="1632d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1632d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1632d-105">Représente la disponibilité de l'utilisateur pour un rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="1632d-105">Represents the user's availability for an appointment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1632d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1632d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1632d-107">dispidBusyStatus</span><span class="sxs-lookup"><span data-stu-id="1632d-107">dispidBusyStatus</span></span>  <br/> |
|<span data-ttu-id="1632d-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="1632d-108">Property set:</span></span>  <br/> |<span data-ttu-id="1632d-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="1632d-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="1632d-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="1632d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="1632d-111">0x00008205</span><span class="sxs-lookup"><span data-stu-id="1632d-111">0x00008205</span></span>  <br/> |
|<span data-ttu-id="1632d-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1632d-112">Data type:</span></span>  <br/> |<span data-ttu-id="1632d-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1632d-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1632d-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="1632d-114">Area:</span></span>  <br/> |<span data-ttu-id="1632d-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="1632d-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1632d-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="1632d-116">Remarks</span></span>

<span data-ttu-id="1632d-117">Cette propriété spécifie la disponibilité d'un utilisateur pour l'événement décrit par l'objet et doit être l'une des valeurs indiquées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="1632d-117">This property specifies the availability of a user for the event described by the object and must be one of the values specified below.</span></span>
  
|<span data-ttu-id="1632d-118">**Value**</span><span class="sxs-lookup"><span data-stu-id="1632d-118">**Value**</span></span>|<span data-ttu-id="1632d-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="1632d-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1632d-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="1632d-120">0x00000000</span></span>  <br/> |<span data-ttu-id="1632d-121">L'utilisateur est disponible.</span><span class="sxs-lookup"><span data-stu-id="1632d-121">The user is available.</span></span>  <br/> |
|<span data-ttu-id="1632d-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="1632d-122">0x00000001</span></span>  <br/> |<span data-ttu-id="1632d-123">Un événement provisoire est planifié pour l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1632d-123">The user has a tentative event scheduled.</span></span>  <br/> |
|<span data-ttu-id="1632d-124">0x00000002</span><span class="sxs-lookup"><span data-stu-id="1632d-124">0x00000002</span></span>  <br/> |<span data-ttu-id="1632d-125">L'utilisateur est occupé.</span><span class="sxs-lookup"><span data-stu-id="1632d-125">The user is busy.</span></span>  <br/> |
|<span data-ttu-id="1632d-126">0x00000003</span><span class="sxs-lookup"><span data-stu-id="1632d-126">0x00000003</span></span>  <br/> |<span data-ttu-id="1632d-127">L'utilisateur est absent du bureau.</span><span class="sxs-lookup"><span data-stu-id="1632d-127">The user is out of office.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1632d-128">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="1632d-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1632d-129">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="1632d-129">Protocol specifications</span></span>

<span data-ttu-id="1632d-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1632d-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1632d-131">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="1632d-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1632d-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1632d-132">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1632d-133">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="1632d-133">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1632d-134">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="1632d-134">Header files</span></span>

<span data-ttu-id="1632d-135">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="1632d-135">Mapidefs.h</span></span>
  
> <span data-ttu-id="1632d-136">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1632d-136">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1632d-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1632d-137">See also</span></span>



[<span data-ttu-id="1632d-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1632d-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1632d-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1632d-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1632d-140">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1632d-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1632d-141">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="1632d-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

