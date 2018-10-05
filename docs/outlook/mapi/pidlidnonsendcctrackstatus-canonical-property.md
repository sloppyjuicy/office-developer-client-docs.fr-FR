---
title: Propriété canonique PidLidNonSendCcTrackStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendCcTrackStatus
api_type:
- COM
ms.assetid: e2654fad-444b-45bc-976d-3c5cbbc81b84
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 10b6009bc86df4232c995e7c6bca463f45999528
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383176"
---
# <a name="pidlidnonsendcctrackstatus-canonical-property"></a><span data-ttu-id="023e5-103">Propriété canonique PidLidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="023e5-103">PidLidNonSendCcTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="023e5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="023e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="023e5-105">Contient la valeur de chaque participant répertoriés dans la propriété **dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="023e5-105">Contains the value for each attendee listed in the **dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="023e5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="023e5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="023e5-107">dispidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="023e5-107">dispidNonSendCcTrackStatus</span></span>  <br/> |
|<span data-ttu-id="023e5-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="023e5-108">Property set:</span></span>  <br/> |<span data-ttu-id="023e5-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="023e5-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="023e5-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="023e5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="023e5-111">0x00008544</span><span class="sxs-lookup"><span data-stu-id="023e5-111">0x00008544</span></span>  <br/> |
|<span data-ttu-id="023e5-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="023e5-112">Data type:</span></span>  <br/> |<span data-ttu-id="023e5-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="023e5-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="023e5-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="023e5-114">Area:</span></span>  <br/> |<span data-ttu-id="023e5-115">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="023e5-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="023e5-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="023e5-116">Remarks</span></span>

<span data-ttu-id="023e5-117">Cette propriété est requise uniquement lorsque la valeur de la propriété **dispidNonSendableCC** .</span><span class="sxs-lookup"><span data-stu-id="023e5-117">This property is required only when the **dispidNonSendableCC** property is set.</span></span> <span data-ttu-id="023e5-118">Le nombre de valeurs dans cette propriété doit correspondre au nombre de valeurs dans **dispidNonSendableCC**.</span><span class="sxs-lookup"><span data-stu-id="023e5-118">The number of values in this property must equal the number of values in **dispidNonSendableCC**.</span></span> <span data-ttu-id="023e5-119">Chaque valeur PT_LONG dans cette propriété correspond au participant de la propriété **dispidNonSendableCC** dans le même index.</span><span class="sxs-lookup"><span data-stu-id="023e5-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="023e5-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="023e5-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="023e5-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="023e5-121">Protocol specifications</span></span>

<span data-ttu-id="023e5-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="023e5-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="023e5-123">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="023e5-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="023e5-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="023e5-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="023e5-125">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="023e5-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="023e5-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="023e5-126">Header files</span></span>

<span data-ttu-id="023e5-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="023e5-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="023e5-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="023e5-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="023e5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="023e5-129">See also</span></span>



[<span data-ttu-id="023e5-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="023e5-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="023e5-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="023e5-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="023e5-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="023e5-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="023e5-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="023e5-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

