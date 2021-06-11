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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3ecfa1e89688ae525a28e221424fb4a8194fc217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359135"
---
# <a name="pidtagswappedtododata-canonical-property"></a><span data-ttu-id="9cbfb-103">Propriété canonique PidTagSwappedToDoData</span><span class="sxs-lookup"><span data-stu-id="9cbfb-103">PidTagSwappedToDoData Canonical Property</span></span>

  
  
<span data-ttu-id="9cbfb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9cbfb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9cbfb-105">Conserve un deuxième ensemble de valeurs de propriété qui n’affectent pas l’état marqué de l’objet Message.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-105">Maintains a second set of property values that do not affect the flagged state of the Message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9cbfb-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9cbfb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9cbfb-107">PR_SWAPPED_TODO_DATA</span><span class="sxs-lookup"><span data-stu-id="9cbfb-107">PR_SWAPPED_TODO_DATA</span></span>  <br/> |
|<span data-ttu-id="9cbfb-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9cbfb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9cbfb-109">0x0E2D</span><span class="sxs-lookup"><span data-stu-id="9cbfb-109">0x0E2D</span></span>  <br/> |
|<span data-ttu-id="9cbfb-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9cbfb-110">Data type:</span></span>  <br/> |<span data-ttu-id="9cbfb-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9cbfb-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9cbfb-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9cbfb-112">Area:</span></span>  <br/> |<span data-ttu-id="9cbfb-113">MAPI non transmetteable</span><span class="sxs-lookup"><span data-stu-id="9cbfb-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9cbfb-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9cbfb-114">Remarks</span></span>

<span data-ttu-id="9cbfb-115">Agissant en tant qu’emplacement de stockage d’indicateur secondaire si les indicateurs de l’expéditeur ou les rappels d’expéditeur sont pris en charge, cette structure fournit un emplacement dans lequel stocker toutes les propriétés relatives au protocole Informational Flagging qui sont pris en charge dans les indicateurs d’expéditeur, ainsi que toutes les propriétés relatives au protocole reminder Paramètres qui sont pris en charge dans les rappels d’expéditeur sans exposer les informations de rappel de l’expéditeur ou de l’expéditeur aux destinataires d’un message.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-115">Acting as the secondary flag storage location if sender flags or sender reminders are supported, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in sender flags, and all properties relating to the Reminder Settings Protocol that are supported in sender reminders without exposing the sender flag or sender reminder information to the recipients of a message.</span></span>
  
<span data-ttu-id="9cbfb-116">De même, cette structure fournit un emplacement dans lequel stocker toutes les propriétés relatives au protocole Informational Flagging qui sont pris en charge dans les indicateurs de destinataire et les propriétés relatives au protocole reminder Paramètres qui sont pris en charge dans les rappels de destinataire sur un message précédemment envoyé.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-116">Similarly, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in recipient flags and properties relating to the Reminder Settings Protocol that are supported in recipient reminders on a previously sent message.</span></span>
  
<span data-ttu-id="9cbfb-117">Pour plus d’informations sur cette propriété, [voir [MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9cbfb-117">For more information about this property, see [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9cbfb-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9cbfb-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9cbfb-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="9cbfb-119">Protocol specifications</span></span>

<span data-ttu-id="9cbfb-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cbfb-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9cbfb-121">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9cbfb-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cbfb-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9cbfb-123">Spécifie les propriétés et les opérations liées au marquage.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-123">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="9cbfb-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9cbfb-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9cbfb-125">Spécifie les propriétés et le modèle d’interaction pour les messages électroniques et autres rappels d’objets.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9cbfb-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9cbfb-126">Header files</span></span>

<span data-ttu-id="9cbfb-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9cbfb-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="9cbfb-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="9cbfb-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="9cbfb-129">Mapitags.h</span></span>
  
> <span data-ttu-id="9cbfb-130">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="9cbfb-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9cbfb-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9cbfb-131">See also</span></span>



[<span data-ttu-id="9cbfb-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9cbfb-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9cbfb-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9cbfb-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9cbfb-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9cbfb-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9cbfb-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9cbfb-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

