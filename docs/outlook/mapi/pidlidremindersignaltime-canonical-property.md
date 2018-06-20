---
title: Propriété canonique PidLidReminderSignalTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderSignalTime
api_type:
- COM
ms.assetid: 58f6432e-6e88-420b-959f-7f365899f7eb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 375cde94d0ecd989908fccbdd69710c1961fba17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785375"
---
# <a name="pidlidremindersignaltime-canonical-property"></a><span data-ttu-id="a7f44-103">Propriété canonique PidLidReminderSignalTime</span><span class="sxs-lookup"><span data-stu-id="a7f44-103">PidLidReminderSignalTime Canonical Property</span></span>

  
  
<span data-ttu-id="a7f44-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a7f44-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a7f44-105">Spécifie le point dans le temps lorsqu’un rappel passe d’en attente en retard.</span><span class="sxs-lookup"><span data-stu-id="a7f44-105">Specifies the point in time when a reminder transitions from pending to overdue.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a7f44-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a7f44-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a7f44-107">dispidReminderNextTime</span><span class="sxs-lookup"><span data-stu-id="a7f44-107">dispidReminderNextTime</span></span>  <br/> |
|<span data-ttu-id="a7f44-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="a7f44-108">Property set:</span></span>  <br/> |<span data-ttu-id="a7f44-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a7f44-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a7f44-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="a7f44-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a7f44-111">0x00008560</span><span class="sxs-lookup"><span data-stu-id="a7f44-111">0x00008560</span></span>  <br/> |
|<span data-ttu-id="a7f44-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a7f44-112">Data type:</span></span>  <br/> |<span data-ttu-id="a7f44-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="a7f44-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="a7f44-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="a7f44-114">Area:</span></span>  <br/> |<span data-ttu-id="a7f44-115">Rappel</span><span class="sxs-lookup"><span data-stu-id="a7f44-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7f44-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="a7f44-116">Remarks</span></span>

<span data-ttu-id="a7f44-117">Si la propriété **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) a la valeur TRUE, cette propriété doit être définie.</span><span class="sxs-lookup"><span data-stu-id="a7f44-117">This property must be set if the **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="a7f44-118">Clients doivent définir la valeur en temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="a7f44-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a7f44-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a7f44-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a7f44-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="a7f44-120">Protocol specifications</span></span>

<span data-ttu-id="a7f44-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7f44-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7f44-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="a7f44-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a7f44-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7f44-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7f44-124">Spécifie les propriétés et le modèle d’interaction pour la messagerie et autres rappels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a7f44-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a7f44-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="a7f44-125">Header files</span></span>

<span data-ttu-id="a7f44-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a7f44-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a7f44-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a7f44-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7f44-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7f44-128">See also</span></span>



[<span data-ttu-id="a7f44-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a7f44-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a7f44-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a7f44-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a7f44-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a7f44-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a7f44-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="a7f44-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

