---
title: Propriété canonique PidLidExceptionReplaceTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidExceptionReplaceTime
api_type:
- COM
ms.assetid: c3aae4f5-7f00-45bf-b007-370041ba360e
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e28bde9571081d61b37f6939a991c11ddeb75a4c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566046"
---
# <a name="pidlidexceptionreplacetime-canonical-property"></a><span data-ttu-id="7894d-103">Propriété canonique PidLidExceptionReplaceTime</span><span class="sxs-lookup"><span data-stu-id="7894d-103">PidLidExceptionReplaceTime Canonical Property</span></span>

  
  
<span data-ttu-id="7894d-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7894d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7894d-105">Spécifie la date et l’heure au sein de la périodicité qui remplace l’exception.</span><span class="sxs-lookup"><span data-stu-id="7894d-105">Specifies the date and time within the recurrence pattern that the exception will replace.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7894d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="7894d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7894d-107">dispidExceptionReplaceTime</span><span class="sxs-lookup"><span data-stu-id="7894d-107">dispidExceptionReplaceTime</span></span>  <br/> |
|<span data-ttu-id="7894d-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="7894d-108">Property set:</span></span>  <br/> |<span data-ttu-id="7894d-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="7894d-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="7894d-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="7894d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="7894d-111">0x00008228</span><span class="sxs-lookup"><span data-stu-id="7894d-111">0x00008228</span></span>  <br/> |
|<span data-ttu-id="7894d-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="7894d-112">Data type:</span></span>  <br/> |<span data-ttu-id="7894d-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="7894d-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="7894d-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="7894d-114">Area:</span></span>  <br/> |<span data-ttu-id="7894d-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="7894d-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7894d-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="7894d-116">Remarks</span></span>

<span data-ttu-id="7894d-117">La valeur doit être spécifiée dans le temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="7894d-117">The value must be specified in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="7894d-118">Cette propriété permet à l’objet de pièce jointe exception doit être localisé pour une instance spécifique.</span><span class="sxs-lookup"><span data-stu-id="7894d-118">This property allows the exception attachment object to be found for a particular instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7894d-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="7894d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7894d-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="7894d-120">Protocol specifications</span></span>

<span data-ttu-id="7894d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7894d-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7894d-122">Fournit des définitions de jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="7894d-122">Provides property set definitions.</span></span>
    
<span data-ttu-id="7894d-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7894d-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7894d-124">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="7894d-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7894d-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="7894d-125">Header files</span></span>

<span data-ttu-id="7894d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7894d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="7894d-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="7894d-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7894d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7894d-128">See also</span></span>



[<span data-ttu-id="7894d-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="7894d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7894d-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="7894d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7894d-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="7894d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7894d-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="7894d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

