---
title: Propriété canonique PidLidReminderDelta
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderDelta
api_type:
- COM
ms.assetid: 011d73d0-8b38-4a4e-a56f-92dec451946a
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 91cad169157b2dd0ff279e88b69db149c4c7df89
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590749"
---
# <a name="pidlidreminderdelta-canonical-property"></a><span data-ttu-id="2cff5-103">Propriété canonique PidLidReminderDelta</span><span class="sxs-lookup"><span data-stu-id="2cff5-103">PidLidReminderDelta Canonical Property</span></span>

  
  
<span data-ttu-id="2cff5-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2cff5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2cff5-105">Spécifie l’intervalle, en minutes, entre le moment lorsque le rappel est tout d’abord en retard et l’heure de début de l’objet calendar.</span><span class="sxs-lookup"><span data-stu-id="2cff5-105">Specifies the interval, in minutes, between the time when the reminder first becomes overdue and the start time of the calendar object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2cff5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="2cff5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2cff5-107">dispidReminderDelta</span><span class="sxs-lookup"><span data-stu-id="2cff5-107">dispidReminderDelta</span></span>  <br/> |
|<span data-ttu-id="2cff5-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="2cff5-108">Property set:</span></span>  <br/> |<span data-ttu-id="2cff5-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="2cff5-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="2cff5-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="2cff5-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="2cff5-111">0x00008501</span><span class="sxs-lookup"><span data-stu-id="2cff5-111">0x00008501</span></span>  <br/> |
|<span data-ttu-id="2cff5-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="2cff5-112">Data type:</span></span>  <br/> |<span data-ttu-id="2cff5-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2cff5-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2cff5-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="2cff5-114">Area:</span></span>  <br/> |<span data-ttu-id="2cff5-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="2cff5-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2cff5-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="2cff5-116">Remarks</span></span>

<span data-ttu-id="2cff5-117">Cette propriété doit être définie sur des objets de calendrier.</span><span class="sxs-lookup"><span data-stu-id="2cff5-117">This property must be set on calendar objects.</span></span> <span data-ttu-id="2cff5-118">Pour tous les objets autres que du calendrier, cette propriété doit être définie sur « 0 x 00000000 » et est ignorée.</span><span class="sxs-lookup"><span data-stu-id="2cff5-118">For all non-calendar objects, this property should be set to "0x00000000" and is ignored.</span></span> <span data-ttu-id="2cff5-119">Lorsqu’un rappel est rejeté pour une instance d’un objet calendar périodiques, la valeur de cette propriété est utilisée dans le calcul de la durée du signal l’occurrence suivante.</span><span class="sxs-lookup"><span data-stu-id="2cff5-119">When a reminder is dismissed for one instance of a recurring calendar object, the value of this property is used in the calculation of the signal time for the next instance.</span></span> <span data-ttu-id="2cff5-120">Pour plus d’informations sur la création de l’objet calendrier, voir [[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2cff5-120">See [[MS- OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) for details about calendar object creation.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2cff5-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="2cff5-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2cff5-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="2cff5-122">Protocol specifications</span></span>

<span data-ttu-id="2cff5-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2cff5-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2cff5-124">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="2cff5-124">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="2cff5-125">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2cff5-125">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2cff5-126">Spécifie les propriétés et le modèle d’interaction pour la messagerie et autres rappels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2cff5-126">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2cff5-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="2cff5-127">Header files</span></span>

<span data-ttu-id="2cff5-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2cff5-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="2cff5-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="2cff5-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2cff5-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2cff5-130">See also</span></span>



[<span data-ttu-id="2cff5-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="2cff5-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2cff5-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="2cff5-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2cff5-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="2cff5-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2cff5-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="2cff5-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

