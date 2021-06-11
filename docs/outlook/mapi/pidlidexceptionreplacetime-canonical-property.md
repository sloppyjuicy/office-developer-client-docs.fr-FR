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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b364fb91bda7e895b546f9a281ef14ce33b073f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337981"
---
# <a name="pidlidexceptionreplacetime-canonical-property"></a><span data-ttu-id="fd177-103">Propriété canonique PidLidExceptionReplaceTime</span><span class="sxs-lookup"><span data-stu-id="fd177-103">PidLidExceptionReplaceTime Canonical Property</span></span>

  
  
<span data-ttu-id="fd177-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd177-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd177-105">Spécifie la date et l’heure dans la modèle de récurrence que l’exception remplacera.</span><span class="sxs-lookup"><span data-stu-id="fd177-105">Specifies the date and time within the recurrence pattern that the exception will replace.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fd177-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="fd177-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fd177-107">dispidExceptionReplaceTime</span><span class="sxs-lookup"><span data-stu-id="fd177-107">dispidExceptionReplaceTime</span></span>  <br/> |
|<span data-ttu-id="fd177-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="fd177-108">Property set:</span></span>  <br/> |<span data-ttu-id="fd177-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="fd177-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="fd177-110">ID long (LID) :</span><span class="sxs-lookup"><span data-stu-id="fd177-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fd177-111">0x00008228</span><span class="sxs-lookup"><span data-stu-id="fd177-111">0x00008228</span></span>  <br/> |
|<span data-ttu-id="fd177-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="fd177-112">Data type:</span></span>  <br/> |<span data-ttu-id="fd177-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="fd177-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="fd177-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="fd177-114">Area:</span></span>  <br/> |<span data-ttu-id="fd177-115">Calendrier</span><span class="sxs-lookup"><span data-stu-id="fd177-115">Calendar</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd177-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="fd177-116">Remarks</span></span>

<span data-ttu-id="fd177-117">La valeur doit être spécifiée en temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="fd177-117">The value must be specified in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="fd177-118">Cette propriété permet de trouver l’objet pièce jointe d’exception pour une instance particulière.</span><span class="sxs-lookup"><span data-stu-id="fd177-118">This property allows the exception attachment object to be found for a particular instance.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fd177-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="fd177-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fd177-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="fd177-120">Protocol specifications</span></span>

<span data-ttu-id="fd177-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd177-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd177-122">Fournit des définitions de jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fd177-122">Provides property set definitions.</span></span>
    
<span data-ttu-id="fd177-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fd177-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fd177-124">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="fd177-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fd177-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="fd177-125">Header files</span></span>

<span data-ttu-id="fd177-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fd177-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="fd177-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="fd177-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fd177-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd177-128">See also</span></span>



[<span data-ttu-id="fd177-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="fd177-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fd177-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="fd177-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fd177-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="fd177-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fd177-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="fd177-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

