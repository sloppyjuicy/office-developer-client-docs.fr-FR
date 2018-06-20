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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6e74dbb1f8e0e64feb2c86eb04e146e201089a4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785384"
---
# <a name="pidlidremindertime-canonical-property"></a><span data-ttu-id="13a49-103">Propriété canonique PidLidReminderTime</span><span class="sxs-lookup"><span data-stu-id="13a49-103">PidLidReminderTime Canonical Property</span></span>

  
  
<span data-ttu-id="13a49-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="13a49-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="13a49-105">Spécifie la durée du signal initiale pour un rappel.</span><span class="sxs-lookup"><span data-stu-id="13a49-105">Specifies the initial signal time for a reminder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="13a49-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="13a49-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="13a49-107">dispidReminderTime</span><span class="sxs-lookup"><span data-stu-id="13a49-107">dispidReminderTime</span></span>  <br/> |
|<span data-ttu-id="13a49-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="13a49-108">Property set:</span></span>  <br/> |<span data-ttu-id="13a49-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="13a49-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="13a49-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="13a49-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="13a49-111">0x00008502</span><span class="sxs-lookup"><span data-stu-id="13a49-111">0x00008502</span></span>  <br/> |
|<span data-ttu-id="13a49-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="13a49-112">Data type:</span></span>  <br/> |<span data-ttu-id="13a49-113">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="13a49-113">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="13a49-114">Zone :</span><span class="sxs-lookup"><span data-stu-id="13a49-114">Area:</span></span>  <br/> |<span data-ttu-id="13a49-115">Rappel</span><span class="sxs-lookup"><span data-stu-id="13a49-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13a49-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="13a49-116">Remarks</span></span>

<span data-ttu-id="13a49-117">Pour les objets de calendrier, cette propriété représente le temps lorsque l’utilisateur sera en retard qui est l’heure de début du rendez-vous.</span><span class="sxs-lookup"><span data-stu-id="13a49-117">For calendar objects, this property represents the time when the user would be late which is the start time of the appointment.</span></span> <span data-ttu-id="13a49-118">Clients doivent définir la valeur en temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="13a49-118">Clients must set the value in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="13a49-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="13a49-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="13a49-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="13a49-120">Protocol specifications</span></span>

<span data-ttu-id="13a49-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13a49-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13a49-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="13a49-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="13a49-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="13a49-123">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="13a49-124">Spécifie les propriétés et le modèle d’interaction pour la messagerie et autres rappels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="13a49-124">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="13a49-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="13a49-125">Header files</span></span>

<span data-ttu-id="13a49-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="13a49-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="13a49-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="13a49-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="13a49-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13a49-128">See also</span></span>



[<span data-ttu-id="13a49-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="13a49-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="13a49-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="13a49-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="13a49-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="13a49-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="13a49-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="13a49-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

