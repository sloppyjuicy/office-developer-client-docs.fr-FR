---
title: Propriété canonique PidLidReminderTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderTime
api_type:
- COM
ms.assetid: f4068ff0-2aa2-4332-be7d-ecebda30dfff
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8371418aabc557f48c74039320305df59624d7ac
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382469"
---
# <a name="pidlidremindertime-canonical-property"></a><span data-ttu-id="f1b5e-103">Propriété canonique PidLidReminderTime</span><span class="sxs-lookup"><span data-stu-id="f1b5e-103">PidLidReminderTime Canonical Property</span></span>

  
  
<span data-ttu-id="f1b5e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1b5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1b5e-105">Spécifie la durée du signal initiale pour un rappel.</span><span class="sxs-lookup"><span data-stu-id="f1b5e-105">Specifies the initial signal time for a reminder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f1b5e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f1b5e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f1b5e-107">dispidReminderTime</span><span class="sxs-lookup"><span data-stu-id="f1b5e-107">dispidReminderTime</span></span>  <br/> |
|<span data-ttu-id="f1b5e-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="f1b5e-108">Property set:</span></span>  <br/> |<span data-ttu-id="f1b5e-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="f1b5e-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="f1b5e-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="f1b5e-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f1b5e-111">0x00008502</span><span class="sxs-lookup"><span data-stu-id="f1b5e-111">0x00008502</span></span>  <br/> |
|<span data-ttu-id="f1b5e-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f1b5e-112">Data type:</span></span>  <br/> |<span data-ttu-id="f1b5e-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="f1b5e-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="f1b5e-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f1b5e-114">Area:</span></span>  <br/> |<span data-ttu-id="f1b5e-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="f1b5e-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1b5e-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="f1b5e-116">Remarks</span></span>

<span data-ttu-id="f1b5e-117">Pour les objets de calendrier, cette propriété représente le temps lorsque l’utilisateur sera en retard qui est l’heure de début du rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="f1b5e-117">For calendar objects, this property represents the time when the user would be late which is the start time of the appointment.</span></span> <span data-ttu-id="f1b5e-118">Clients doivent définir la valeur en temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="f1b5e-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f1b5e-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f1b5e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f1b5e-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="f1b5e-120">Protocol specifications</span></span>

<span data-ttu-id="f1b5e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1b5e-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1b5e-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="f1b5e-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f1b5e-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f1b5e-123">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f1b5e-124">Spécifie les propriétés et le modèle d’interaction pour la messagerie et autres rappels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f1b5e-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f1b5e-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f1b5e-125">Header files</span></span>

<span data-ttu-id="f1b5e-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f1b5e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="f1b5e-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f1b5e-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f1b5e-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1b5e-128">See also</span></span>



[<span data-ttu-id="f1b5e-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f1b5e-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f1b5e-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f1b5e-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f1b5e-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f1b5e-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f1b5e-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f1b5e-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

