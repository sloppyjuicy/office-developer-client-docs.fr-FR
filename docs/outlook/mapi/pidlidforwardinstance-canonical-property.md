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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0c32a60c7655f4e468a03013cb3979bde228ea3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785231"
---
# <a name="pidlidforwardinstance-canonical-property"></a><span data-ttu-id="b503c-103">Propriété canonique PidLidForwardInstance</span><span class="sxs-lookup"><span data-stu-id="b503c-103">PidLidForwardInstance Canonical Property</span></span>

  
  
<span data-ttu-id="b503c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b503c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b503c-105">Indique que la demande de réunion représente une exception à une série périodique, et il a été transféré (même si transmis par l’organisateur) au lieu d’une invitation envoyée par l’organisateur.</span><span class="sxs-lookup"><span data-stu-id="b503c-105">Indicates that the meeting request represents an exception to a recurring series, and it was forwarded (even when forwarded by the organizer) rather than being an invitation sent by the organizer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b503c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b503c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b503c-107">dispidFwrdInstance</span><span class="sxs-lookup"><span data-stu-id="b503c-107">dispidFwrdInstance</span></span>  <br/> |
|<span data-ttu-id="b503c-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="b503c-108">Property set:</span></span>  <br/> |<span data-ttu-id="b503c-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="b503c-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="b503c-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="b503c-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="b503c-111">0x0000820A</span><span class="sxs-lookup"><span data-stu-id="b503c-111">0x0000820A</span></span>  <br/> |
|<span data-ttu-id="b503c-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b503c-112">Data type:</span></span>  <br/> |<span data-ttu-id="b503c-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b503c-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b503c-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="b503c-114">Area:</span></span>  <br/> |<span data-ttu-id="b503c-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="b503c-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b503c-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="b503c-116">Remarks</span></span>

<span data-ttu-id="b503c-117">La valeur FALSE pour cette propriété indique que la demande de réunion n’est pas une instance transférée.</span><span class="sxs-lookup"><span data-stu-id="b503c-117">A value of FALSE for this property indicates that the meeting request is not a forwarded instance.</span></span> <span data-ttu-id="b503c-118">Cette propriété n’est pas requise.</span><span class="sxs-lookup"><span data-stu-id="b503c-118">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b503c-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b503c-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b503c-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="b503c-120">Protocol specifications</span></span>

<span data-ttu-id="b503c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b503c-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b503c-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="b503c-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b503c-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b503c-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b503c-124">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="b503c-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b503c-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b503c-125">Header files</span></span>

<span data-ttu-id="b503c-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b503c-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b503c-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b503c-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b503c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b503c-128">See also</span></span>



[<span data-ttu-id="b503c-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b503c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b503c-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b503c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b503c-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b503c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b503c-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="b503c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

