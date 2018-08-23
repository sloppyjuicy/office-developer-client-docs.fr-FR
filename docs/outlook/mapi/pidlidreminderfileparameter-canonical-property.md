---
title: Propriété canonique PidLidReminderFileParameter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderFileParameter
api_type:
- COM
ms.assetid: 1009f0ea-6f35-484d-b04d-5b6e844c14dd
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 07653bea747e6e697cb1edb5669ae106c9e213fe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591477"
---
# <a name="pidlidreminderfileparameter-canonical-property"></a><span data-ttu-id="e8882-103">Propriété canonique PidLidReminderFileParameter</span><span class="sxs-lookup"><span data-stu-id="e8882-103">PidLidReminderFileParameter Canonical Property</span></span>

  
  
<span data-ttu-id="e8882-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8882-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8882-105">Spécifie le nom de fichier du son un client doit être lu lorsque le rappel pour cet objet est en retard.</span><span class="sxs-lookup"><span data-stu-id="e8882-105">Specifies the filename of the sound that a client should play when the reminder for that object becomes overdue.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e8882-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e8882-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e8882-107">dispidReminderFileParam</span><span class="sxs-lookup"><span data-stu-id="e8882-107">dispidReminderFileParam</span></span>  <br/> |
|<span data-ttu-id="e8882-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="e8882-108">Property set:</span></span>  <br/> |<span data-ttu-id="e8882-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="e8882-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="e8882-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="e8882-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e8882-111">0x0000851F</span><span class="sxs-lookup"><span data-stu-id="e8882-111">0x0000851F</span></span>  <br/> |
|<span data-ttu-id="e8882-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e8882-112">Data type:</span></span>  <br/> |<span data-ttu-id="e8882-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e8882-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e8882-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e8882-114">Area:</span></span>  <br/> |<span data-ttu-id="e8882-115">Reminder</span><span class="sxs-lookup"><span data-stu-id="e8882-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8882-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="e8882-116">Remarks</span></span>

<span data-ttu-id="e8882-117">Si cette propriété n’est pas présente, le client peut utiliser une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="e8882-117">If this property is not present, the client may use a default value.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e8882-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e8882-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e8882-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="e8882-119">Protocol specifications</span></span>

<span data-ttu-id="e8882-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8882-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8882-121">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="e8882-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e8882-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8882-122">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8882-123">Spécifie les propriétés et le modèle d’interaction pour la messagerie et autres rappels de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e8882-123">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e8882-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e8882-124">Header files</span></span>

<span data-ttu-id="e8882-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e8882-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="e8882-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e8882-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e8882-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8882-127">See also</span></span>



[<span data-ttu-id="e8882-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e8882-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e8882-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e8882-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e8882-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e8882-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e8882-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e8882-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

