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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 10b6009bc86df4232c995e7c6bca463f45999528
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319669"
---
# <a name="pidlidnonsendcctrackstatus-canonical-property"></a><span data-ttu-id="910cd-103">Propriété canonique PidLidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="910cd-103">PidLidNonSendCcTrackStatus Canonical Property</span></span>

  
  
<span data-ttu-id="910cd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="910cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="910cd-105">Contient la valeur de chaque participant figurant dans la propriété **dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="910cd-105">Contains the value for each attendee listed in the **dispidNonSendableCC** ([PidLidNonSendableCc](pidlidnonsendablecc-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="910cd-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="910cd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="910cd-107">dispidNonSendCcTrackStatus</span><span class="sxs-lookup"><span data-stu-id="910cd-107">dispidNonSendCcTrackStatus</span></span>  <br/> |
|<span data-ttu-id="910cd-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="910cd-108">Property set:</span></span>  <br/> |<span data-ttu-id="910cd-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="910cd-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="910cd-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="910cd-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="910cd-111">0x00008544</span><span class="sxs-lookup"><span data-stu-id="910cd-111">0x00008544</span></span>  <br/> |
|<span data-ttu-id="910cd-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="910cd-112">Data type:</span></span>  <br/> |<span data-ttu-id="910cd-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="910cd-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="910cd-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="910cd-114">Area:</span></span>  <br/> |<span data-ttu-id="910cd-115">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="910cd-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="910cd-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="910cd-116">Remarks</span></span>

<span data-ttu-id="910cd-117">Cette propriété est requise uniquement lorsque la propriété **dispidNonSendableCC** est définie.</span><span class="sxs-lookup"><span data-stu-id="910cd-117">This property is required only when the **dispidNonSendableCC** property is set.</span></span> <span data-ttu-id="910cd-118">Le nombre de valeurs de cette propriété doit être égal au nombre de valeurs dans **dispidNonSendableCC**.</span><span class="sxs-lookup"><span data-stu-id="910cd-118">The number of values in this property must equal the number of values in **dispidNonSendableCC**.</span></span> <span data-ttu-id="910cd-119">Chaque valeur PT_LONG de cette propriété correspond au participant dans la propriété **dispidNonSendableCC** au même index.</span><span class="sxs-lookup"><span data-stu-id="910cd-119">Each PT_LONG value in this property corresponds to the attendee in the **dispidNonSendableCC** property at the same index.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="910cd-120">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="910cd-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="910cd-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="910cd-121">Protocol specifications</span></span>

<span data-ttu-id="910cd-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="910cd-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="910cd-123">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="910cd-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="910cd-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="910cd-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="910cd-125">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="910cd-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="910cd-126">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="910cd-126">Header files</span></span>

<span data-ttu-id="910cd-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="910cd-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="910cd-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="910cd-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="910cd-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="910cd-129">See also</span></span>



[<span data-ttu-id="910cd-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="910cd-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="910cd-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="910cd-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="910cd-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="910cd-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="910cd-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="910cd-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

