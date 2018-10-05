---
title: Propriété canonique PidLidIsException
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsException
api_type:
- COM
ms.assetid: 802321fb-4261-4c3e-9de3-8b4f490dae13
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 18dfa8a5936902afe0272274f7a48d01b28f94f3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386249"
---
# <a name="pidlidisexception-canonical-property"></a><span data-ttu-id="f5dd4-103">Propriété canonique PidLidIsException</span><span class="sxs-lookup"><span data-stu-id="f5dd4-103">PidLidIsException Canonical Property</span></span>

  
  
<span data-ttu-id="f5dd4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5dd4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5dd4-105">Indique que l’objet qui représente une exception (y compris une instance orpheline).</span><span class="sxs-lookup"><span data-stu-id="f5dd4-105">Indicates that the object that represents an exception (including an orphan instance).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f5dd4-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f5dd4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5dd4-107">LID_IS_EXCEPTION</span><span class="sxs-lookup"><span data-stu-id="f5dd4-107">LID_IS_EXCEPTION</span></span>  <br/> |
|<span data-ttu-id="f5dd4-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="f5dd4-108">Property set:</span></span>  <br/> |<span data-ttu-id="f5dd4-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="f5dd4-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="f5dd4-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="f5dd4-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f5dd4-111">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="f5dd4-111">0x0000000A</span></span>  <br/> |
|<span data-ttu-id="f5dd4-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f5dd4-112">Data type:</span></span>  <br/> |<span data-ttu-id="f5dd4-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f5dd4-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f5dd4-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f5dd4-114">Area:</span></span>  <br/> |<span data-ttu-id="f5dd4-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="f5dd4-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5dd4-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="f5dd4-116">Remarks</span></span>

<span data-ttu-id="f5dd4-117">La valeur FALSE indique que l’objet qui représente une série périodique ou une instance unique.</span><span class="sxs-lookup"><span data-stu-id="f5dd4-117">A value of FALSE indicates that the object that represents a recurring series or a single instance.</span></span> <span data-ttu-id="f5dd4-118">L’absence de cette propriété pour tout objet indique la valeur FALSE à l’exception du message incorporé exception qui suppose que la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="f5dd4-118">The absence of this property for any object indicates a value of FALSE except for the exception embedded message, which assumes a value of TRUE.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f5dd4-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f5dd4-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f5dd4-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="f5dd4-120">Protocol specifications</span></span>

<span data-ttu-id="f5dd4-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5dd4-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5dd4-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="f5dd4-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f5dd4-123">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5dd4-123">[[MS-OXOCAL] ](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5dd4-124">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="f5dd4-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f5dd4-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f5dd4-125">Header files</span></span>

<span data-ttu-id="f5dd4-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5dd4-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5dd4-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f5dd4-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5dd4-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5dd4-128">See also</span></span>



[<span data-ttu-id="f5dd4-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f5dd4-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5dd4-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f5dd4-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5dd4-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f5dd4-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5dd4-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f5dd4-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

