---
title: Propriété canonique PidLidIsRecurring
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidIsRecurring
api_type:
- COM
ms.assetid: 1f8ecc22-badc-4278-a3c6-fcd398f5bf24
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c920cd42a27c03ffcff63bbd2e0049ddb6f81158
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315434"
---
# <a name="pidlidisrecurring-canonical-property"></a><span data-ttu-id="87ae2-103">Propriété canonique PidLidIsRecurring</span><span class="sxs-lookup"><span data-stu-id="87ae2-103">PidLidIsRecurring Canonical Property</span></span>

  
  
<span data-ttu-id="87ae2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87ae2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87ae2-105">Indique si l'objet est associé à une série périodique.</span><span class="sxs-lookup"><span data-stu-id="87ae2-105">Specifies whether or not the object is associated with a recurring series.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="87ae2-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="87ae2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="87ae2-107">LID_IS_RECURRING</span><span class="sxs-lookup"><span data-stu-id="87ae2-107">LID_IS_RECURRING</span></span>  <br/> |
|<span data-ttu-id="87ae2-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="87ae2-108">Property set:</span></span>  <br/> |<span data-ttu-id="87ae2-109">PSETID_Meeting</span><span class="sxs-lookup"><span data-stu-id="87ae2-109">PSETID_Meeting</span></span>  <br/> |
|<span data-ttu-id="87ae2-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="87ae2-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="87ae2-111">0x00000005</span><span class="sxs-lookup"><span data-stu-id="87ae2-111">0x00000005</span></span>  <br/> |
|<span data-ttu-id="87ae2-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="87ae2-112">Data type:</span></span>  <br/> |<span data-ttu-id="87ae2-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="87ae2-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="87ae2-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="87ae2-114">Area:</span></span>  <br/> |<span data-ttu-id="87ae2-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="87ae2-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87ae2-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="87ae2-116">Remarks</span></span>

<span data-ttu-id="87ae2-117">La valeur TRUE indique que l'objet représente une série périodique ou une exception (y compris une instance orpheline).</span><span class="sxs-lookup"><span data-stu-id="87ae2-117">A value of TRUE indicates that the object represents either a recurring series or an exception (including an orphan instance).</span></span> <span data-ttu-id="87ae2-118">La valeur FALSe, ou l'absence de cette propriété, indique que l'objet représente une instance unique.</span><span class="sxs-lookup"><span data-stu-id="87ae2-118">A value of FALSE, or the absence of this property, indicates that the object represents a single instance.</span></span> <span data-ttu-id="87ae2-119">Notez la différence entre cette propriété et la propriété **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="87ae2-119">Note the difference between this property and the **PR_RECURRING** ([PidLidRecurring](pidlidrecurring-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="87ae2-120">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="87ae2-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="87ae2-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="87ae2-121">Protocol specifications</span></span>

<span data-ttu-id="87ae2-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87ae2-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87ae2-123">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="87ae2-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="87ae2-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="87ae2-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="87ae2-125">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="87ae2-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="87ae2-126">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="87ae2-126">Header files</span></span>

<span data-ttu-id="87ae2-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="87ae2-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="87ae2-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="87ae2-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87ae2-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87ae2-129">See also</span></span>



[<span data-ttu-id="87ae2-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="87ae2-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="87ae2-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="87ae2-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="87ae2-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="87ae2-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="87ae2-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="87ae2-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

