---
title: Propriété canonique PidTagFreeBusyCountMonths
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyCountMonths
api_type:
- HeaderDef
ms.assetid: 278a77f2-65ec-4281-b406-942cc416a476
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 610e9d396442f981b7bcbf126e3086e6885399d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316190"
---
# <a name="pidtagfreebusycountmonths-canonical-property"></a><span data-ttu-id="091da-103">Propriété canonique PidTagFreeBusyCountMonths</span><span class="sxs-lookup"><span data-stu-id="091da-103">PidTagFreeBusyCountMonths Canonical Property</span></span>

  
  
<span data-ttu-id="091da-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="091da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="091da-105">Contient la valeur pour le calcul des dates de début et de fin de la plage de données de libre/occupé à publier dans les dossiers publics.</span><span class="sxs-lookup"><span data-stu-id="091da-105">Contains the value for calculating the start and end dates of the range of free/busy data to be published to public folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="091da-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="091da-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="091da-107">PR_FREEBUSY_COUNT_MONTHS</span><span class="sxs-lookup"><span data-stu-id="091da-107">PR_FREEBUSY_COUNT_MONTHS</span></span>  <br/> |
|<span data-ttu-id="091da-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="091da-108">Identifier:</span></span>  <br/> |<span data-ttu-id="091da-109">0x6869</span><span class="sxs-lookup"><span data-stu-id="091da-109">0x6869</span></span>  <br/> |
|<span data-ttu-id="091da-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="091da-110">Data type:</span></span>  <br/> |<span data-ttu-id="091da-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="091da-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="091da-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="091da-112">Area:</span></span>  <br/> |<span data-ttu-id="091da-113">Message définissable par la classe de message</span><span class="sxs-lookup"><span data-stu-id="091da-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="091da-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="091da-114">Remarks</span></span>

<span data-ttu-id="091da-115">La valeur de cette propriété doit être supérieure ou égale à 0 et inférieure ou égale à 36.</span><span class="sxs-lookup"><span data-stu-id="091da-115">This property's value must be greater than or equal to 0 and less than or equal to 36.</span></span> <span data-ttu-id="091da-116">Il ne s’agit pas d’une propriété obligatoire.</span><span class="sxs-lookup"><span data-stu-id="091da-116">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="091da-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="091da-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="091da-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="091da-118">Protocol specifications</span></span>

<span data-ttu-id="091da-119">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="091da-119">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="091da-120">Publie la disponibilité d’un utilisateur ou d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="091da-120">Publishes the availability of a user or resource.</span></span>
    
<span data-ttu-id="091da-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="091da-121">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="091da-122">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="091da-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="091da-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="091da-123">Header files</span></span>

<span data-ttu-id="091da-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="091da-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="091da-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="091da-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="091da-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="091da-126">Mapitags.h</span></span>
  
> <span data-ttu-id="091da-127">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="091da-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="091da-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="091da-128">See also</span></span>



[<span data-ttu-id="091da-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="091da-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="091da-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="091da-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="091da-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="091da-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="091da-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="091da-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

