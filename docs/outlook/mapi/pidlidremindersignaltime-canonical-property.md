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
ms.openlocfilehash: 3fcfd00f71a308dce625e6636edbe647f3d7258a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350854"
---
# <a name="pidlidremindersignaltime-canonical-property"></a><span data-ttu-id="73a26-103">Propriété canonique PidLidReminderSignalTime</span><span class="sxs-lookup"><span data-stu-id="73a26-103">PidLidReminderSignalTime Canonical Property</span></span>

  
  
<span data-ttu-id="73a26-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73a26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73a26-105">Indique le moment où un rappel passe d'attente à en retard.</span><span class="sxs-lookup"><span data-stu-id="73a26-105">Specifies the point in time when a reminder transitions from pending to overdue.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="73a26-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="73a26-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="73a26-107">dispidReminderNextTime</span><span class="sxs-lookup"><span data-stu-id="73a26-107">dispidReminderNextTime</span></span>  <br/> |
|<span data-ttu-id="73a26-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="73a26-108">Property set:</span></span>  <br/> |<span data-ttu-id="73a26-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="73a26-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="73a26-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="73a26-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="73a26-111">0x00008560</span><span class="sxs-lookup"><span data-stu-id="73a26-111">0x00008560</span></span>  <br/> |
|<span data-ttu-id="73a26-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="73a26-112">Data type:</span></span>  <br/> |<span data-ttu-id="73a26-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="73a26-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="73a26-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="73a26-114">Area:</span></span>  <br/> |<span data-ttu-id="73a26-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="73a26-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73a26-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="73a26-116">Remarks</span></span>

<span data-ttu-id="73a26-117">Cette propriété doit être définie si la propriété **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="73a26-117">This property must be set if the **dispidReminderSet** ([PidLidReminderSet](pidlidreminderset-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="73a26-118">Les clients doivent définir la valeur au format UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="73a26-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="73a26-119">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="73a26-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="73a26-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="73a26-120">Protocol specifications</span></span>

<span data-ttu-id="73a26-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73a26-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73a26-122">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="73a26-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="73a26-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="73a26-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="73a26-124">Spécifie les propriétés et le modèle d'interaction pour les rappels de messagerie et d'objet.</span><span class="sxs-lookup"><span data-stu-id="73a26-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="73a26-125">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="73a26-125">Header files</span></span>

<span data-ttu-id="73a26-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="73a26-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="73a26-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="73a26-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="73a26-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73a26-128">See also</span></span>



[<span data-ttu-id="73a26-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="73a26-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="73a26-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="73a26-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="73a26-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="73a26-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="73a26-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="73a26-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

