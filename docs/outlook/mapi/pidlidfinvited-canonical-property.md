---
title: Propriété canonique PidLidFInvited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFInvited
api_type:
- COM
ms.assetid: ca1ea5ec-20d5-4b70-95de-c2246a10beae
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3c2ddb5da9202e9cf0d1c78da1c1ad085ef9687c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357798"
---
# <a name="pidlidfinvited-canonical-property"></a><span data-ttu-id="0181d-103">Propriété canonique PidLidFInvited</span><span class="sxs-lookup"><span data-stu-id="0181d-103">PidLidFInvited Canonical Property</span></span>

  
  
<span data-ttu-id="0181d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0181d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0181d-105">Indique si des invitations ont été envoyées pour la réunion représentée par cette réunion.</span><span class="sxs-lookup"><span data-stu-id="0181d-105">Indicates whether or not invitations have been sent for the meeting that this meeting represents.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0181d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0181d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0181d-107">dispidFInvited</span><span class="sxs-lookup"><span data-stu-id="0181d-107">dispidFInvited</span></span>  <br/> |
|<span data-ttu-id="0181d-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="0181d-108">Property set:</span></span>  <br/> |<span data-ttu-id="0181d-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="0181d-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="0181d-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="0181d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="0181d-111">0x00008229</span><span class="sxs-lookup"><span data-stu-id="0181d-111">0x00008229</span></span>  <br/> |
|<span data-ttu-id="0181d-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0181d-112">Data type:</span></span>  <br/> |<span data-ttu-id="0181d-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0181d-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0181d-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="0181d-114">Area:</span></span>  <br/> |<span data-ttu-id="0181d-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="0181d-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0181d-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="0181d-116">Remarks</span></span>

<span data-ttu-id="0181d-117">La valeur FALSE ou l’absence de cette propriété indique qu’une demande de réunion n’a jamais été envoyée.</span><span class="sxs-lookup"><span data-stu-id="0181d-117">A value of FALSE, or the absence of this property, indicates that a meeting request has never been sent.</span></span> <span data-ttu-id="0181d-118">La valeur TRUE indique qu’une demande de réunion a été envoyée.</span><span class="sxs-lookup"><span data-stu-id="0181d-118">A value of TRUE indicates that a meeting request has been sent.</span></span> <span data-ttu-id="0181d-119">Une fois que cette valeur est définie sur TRUE sur une réunion, elle ne doit pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="0181d-119">Once this value is set to TRUE on a meeting, it must not be changed.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0181d-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0181d-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0181d-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="0181d-121">Protocol specifications</span></span>

<span data-ttu-id="0181d-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0181d-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0181d-123">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="0181d-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0181d-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0181d-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0181d-125">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="0181d-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0181d-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0181d-126">Header files</span></span>

<span data-ttu-id="0181d-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0181d-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="0181d-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0181d-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0181d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0181d-129">See also</span></span>



[<span data-ttu-id="0181d-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0181d-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0181d-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0181d-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0181d-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0181d-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0181d-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="0181d-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

