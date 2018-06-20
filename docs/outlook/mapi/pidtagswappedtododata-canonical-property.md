---
title: Propriété canonique PidTagSwappedToDoData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoData
api_type:
- COM
ms.assetid: d2a82fc8-de5d-4819-906e-b8314fd06ea0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: dedb60c5356e1dbb6d35f27372a09c152da0fed0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786867"
---
# <a name="pidtagswappedtododata-canonical-property"></a><span data-ttu-id="956c0-103">Propriété canonique PidTagSwappedToDoData</span><span class="sxs-lookup"><span data-stu-id="956c0-103">PidTagSwappedToDoData Canonical Property</span></span>

  
  
<span data-ttu-id="956c0-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="956c0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="956c0-105">Gère un second ensemble de valeurs de propriété qui n’affectent pas l’état de l’objet du Message avec indicateur.</span><span class="sxs-lookup"><span data-stu-id="956c0-105">Maintains a second set of property values that do not affect the flagged state of the Message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="956c0-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="956c0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="956c0-107">PR_SWAPPED_TODO_DATA</span><span class="sxs-lookup"><span data-stu-id="956c0-107">PR_SWAPPED_TODO_DATA</span></span>  <br/> |
|<span data-ttu-id="956c0-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="956c0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="956c0-109">0x0E2D</span><span class="sxs-lookup"><span data-stu-id="956c0-109">0x0E2D</span></span>  <br/> |
|<span data-ttu-id="956c0-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="956c0-110">Data type:</span></span>  <br/> |<span data-ttu-id="956c0-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="956c0-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="956c0-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="956c0-112">Area:</span></span>  <br/> |<span data-ttu-id="956c0-113">MAPI non transmissible</span><span class="sxs-lookup"><span data-stu-id="956c0-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="956c0-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="956c0-114">Remarks</span></span>

<span data-ttu-id="956c0-115">Agir comme l’emplacement de stockage indicateur secondaire si indicateurs de l’expéditeur ou les rappels de l’expéditeur sont pris en charge, cette structure fournit un emplacement dans lequel stocker toutes les propriétés relatives au protocole de signalisation d’information qui sont prises en charge dans les indicateurs de l’expéditeur et tous les propriétés relatives au protocole de paramètres de rappel sont prises en charge dans les rappels de l’expéditeur sans exposer les indicateur de l’expéditeur ou les informations de rappel de l’expéditeur pour les destinataires d’un message.</span><span class="sxs-lookup"><span data-stu-id="956c0-115">Acting as the secondary flag storage location if sender flags or sender reminders are supported, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in sender flags, and all properties relating to the Reminder Settings Protocol that are supported in sender reminders without exposing the sender flag or sender reminder information to the recipients of a message.</span></span>
  
<span data-ttu-id="956c0-116">De même, cette structure fournit un emplacement dans lequel stocker toutes les propriétés relatives au protocole de signalisation d’information qui sont prises en charge dans les indicateurs de destinataires et relative au protocole de paramètres de rappel qui sont prises en charge dans un destinataire rappels sur un message envoyé précédemment.</span><span class="sxs-lookup"><span data-stu-id="956c0-116">Similarly, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in recipient flags and properties relating to the Reminder Settings Protocol that are supported in recipient reminders on a previously sent message.</span></span>
  
<span data-ttu-id="956c0-117">Pour plus d’informations sur cette propriété, voir [[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="956c0-117">For more information about this property, see [[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="956c0-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="956c0-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="956c0-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="956c0-119">Protocol specifications</span></span>

<span data-ttu-id="956c0-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="956c0-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="956c0-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="956c0-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="956c0-122">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="956c0-122">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="956c0-123">Spécifie les propriétés et les opérations liées aux marquage.</span><span class="sxs-lookup"><span data-stu-id="956c0-123">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="956c0-124">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="956c0-124">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="956c0-125">Spécifie les propriétés et le modèle d’interaction pour la messagerie et autres rappels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="956c0-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="956c0-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="956c0-126">Header files</span></span>

<span data-ttu-id="956c0-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="956c0-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="956c0-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="956c0-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="956c0-129">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="956c0-129">Mapitags.h</span></span>
  
> <span data-ttu-id="956c0-130">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="956c0-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="956c0-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="956c0-131">See also</span></span>



[<span data-ttu-id="956c0-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="956c0-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="956c0-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="956c0-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="956c0-134">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="956c0-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="956c0-135">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="956c0-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

