---
title: Propriété canonique PidLidToAttendeesString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToAttendeesString
api_type:
- COM
ms.assetid: ca1eedba-c617-4403-8490-315ab75f2edb
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 75439fccaf13665c68321cac5d39d0373ca923e1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571093"
---
# <a name="pidlidtoattendeesstring-canonical-property"></a><span data-ttu-id="adbb0-103">Propriété canonique PidLidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="adbb0-103">PidLidToAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="adbb0-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="adbb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="adbb0-105">Contient une liste de tous les participants à envoyer qui sont également des participants obligatoires.</span><span class="sxs-lookup"><span data-stu-id="adbb0-105">Contains a list of all the sendable attendees who are also required attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="adbb0-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="adbb0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="adbb0-107">dispidToAttendeesString</span><span class="sxs-lookup"><span data-stu-id="adbb0-107">dispidToAttendeesString</span></span>  <br/> |
|<span data-ttu-id="adbb0-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="adbb0-108">Property set:</span></span>  <br/> |<span data-ttu-id="adbb0-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="adbb0-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="adbb0-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="adbb0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="adbb0-111">0x0000823B</span><span class="sxs-lookup"><span data-stu-id="adbb0-111">0x0000823B</span></span>  <br/> |
|<span data-ttu-id="adbb0-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="adbb0-112">Data type:</span></span>  <br/> |<span data-ttu-id="adbb0-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="adbb0-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="adbb0-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="adbb0-114">Area:</span></span>  <br/> |<span data-ttu-id="adbb0-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="adbb0-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="adbb0-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="adbb0-116">Remarks</span></span>

<span data-ttu-id="adbb0-117">La valeur de chaque participant est la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de carnet d’adresses du participant.</span><span class="sxs-lookup"><span data-stu-id="adbb0-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="adbb0-118">Des entrées doivent être séparées par un point-virgule suivi d’un espace.</span><span class="sxs-lookup"><span data-stu-id="adbb0-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="adbb0-119">Cette propriété n’est pas requise.</span><span class="sxs-lookup"><span data-stu-id="adbb0-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="adbb0-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="adbb0-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="adbb0-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="adbb0-121">Protocol specifications</span></span>

<span data-ttu-id="adbb0-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="adbb0-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="adbb0-123">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="adbb0-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="adbb0-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="adbb0-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="adbb0-125">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="adbb0-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="adbb0-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="adbb0-126">Header files</span></span>

<span data-ttu-id="adbb0-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="adbb0-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="adbb0-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="adbb0-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="adbb0-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adbb0-129">See also</span></span>



[<span data-ttu-id="adbb0-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="adbb0-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="adbb0-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="adbb0-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="adbb0-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="adbb0-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="adbb0-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="adbb0-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

