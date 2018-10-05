---
title: Propriété canonique PidLidForwardInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidForwardInstance
api_type:
- COM
ms.assetid: 055bdcaf-5002-44a6-b2b6-87244b2bea93
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 585e1a5400965288aa4a4c321888a570270021c8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394775"
---
# <a name="pidlidforwardinstance-canonical-property"></a><span data-ttu-id="007e8-103">Propriété canonique PidLidForwardInstance</span><span class="sxs-lookup"><span data-stu-id="007e8-103">PidLidForwardInstance Canonical Property</span></span>

  
  
<span data-ttu-id="007e8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="007e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="007e8-105">Indique que la demande de réunion représente une exception à une série périodique, et il a été transféré (même si transmis par l’organisateur) au lieu d’une invitation envoyée par l’organisateur.</span><span class="sxs-lookup"><span data-stu-id="007e8-105">Indicates that the meeting request represents an exception to a recurring series, and it was forwarded (even when forwarded by the organizer) rather than being an invitation sent by the organizer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="007e8-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="007e8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="007e8-107">dispidFwrdInstance</span><span class="sxs-lookup"><span data-stu-id="007e8-107">dispidFwrdInstance</span></span>  <br/> |
|<span data-ttu-id="007e8-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="007e8-108">Property set:</span></span>  <br/> |<span data-ttu-id="007e8-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="007e8-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="007e8-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="007e8-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="007e8-111">0x0000820A</span><span class="sxs-lookup"><span data-stu-id="007e8-111">0x0000820A</span></span>  <br/> |
|<span data-ttu-id="007e8-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="007e8-112">Data type:</span></span>  <br/> |<span data-ttu-id="007e8-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="007e8-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="007e8-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="007e8-114">Area:</span></span>  <br/> |<span data-ttu-id="007e8-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="007e8-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="007e8-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="007e8-116">Remarks</span></span>

<span data-ttu-id="007e8-117">La valeur FALSE pour cette propriété indique que la demande de réunion n’est pas une instance transférée.</span><span class="sxs-lookup"><span data-stu-id="007e8-117">A value of FALSE for this property indicates that the meeting request is not a forwarded instance.</span></span> <span data-ttu-id="007e8-118">Cette propriété n’est pas requise.</span><span class="sxs-lookup"><span data-stu-id="007e8-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="007e8-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="007e8-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="007e8-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="007e8-120">Protocol specifications</span></span>

<span data-ttu-id="007e8-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="007e8-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="007e8-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="007e8-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="007e8-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="007e8-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="007e8-124">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="007e8-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="007e8-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="007e8-125">Header files</span></span>

<span data-ttu-id="007e8-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="007e8-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="007e8-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="007e8-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="007e8-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="007e8-128">See also</span></span>



[<span data-ttu-id="007e8-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="007e8-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="007e8-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="007e8-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="007e8-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="007e8-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="007e8-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="007e8-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

