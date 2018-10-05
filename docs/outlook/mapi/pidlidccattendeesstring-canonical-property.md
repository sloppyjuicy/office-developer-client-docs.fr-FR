---
title: Propriété canonique PidLidCcAttendeesString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCcAttendeesString
api_type:
- COM
ms.assetid: 697d5c93-ec7f-4608-9866-9e249a093dbc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 12cdbfcc140fb5ea3bb15a2db93f3689923d9390
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386585"
---
# <a name="pidlidccattendeesstring-canonical-property"></a><span data-ttu-id="8f18f-103">Propriété canonique PidLidCcAttendeesString</span><span class="sxs-lookup"><span data-stu-id="8f18f-103">PidLidCcAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="8f18f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f18f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f18f-105">Contient une liste de tous les participants à envoyer qui sont également des participants facultatifs.</span><span class="sxs-lookup"><span data-stu-id="8f18f-105">Contains a list of all the sendable attendees who are also optional attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8f18f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8f18f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8f18f-107">dispidCCAttendeesString</span><span class="sxs-lookup"><span data-stu-id="8f18f-107">dispidCCAttendeesString</span></span>  <br/> |
|<span data-ttu-id="8f18f-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="8f18f-108">Property set:</span></span>  <br/> |<span data-ttu-id="8f18f-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="8f18f-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="8f18f-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="8f18f-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="8f18f-111">0x0000823C</span><span class="sxs-lookup"><span data-stu-id="8f18f-111">0x0000823C</span></span>  <br/> |
|<span data-ttu-id="8f18f-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8f18f-112">Data type:</span></span>  <br/> |<span data-ttu-id="8f18f-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8f18f-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8f18f-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="8f18f-114">Area:</span></span>  <br/> |<span data-ttu-id="8f18f-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="8f18f-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8f18f-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="8f18f-116">Remarks</span></span>

<span data-ttu-id="8f18f-117">La valeur de chaque participant est la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de carnet d’adresses du participant.</span><span class="sxs-lookup"><span data-stu-id="8f18f-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's address book.</span></span> <span data-ttu-id="8f18f-118">Des entrées doivent être séparées par un point-virgule suivi d’un espace.</span><span class="sxs-lookup"><span data-stu-id="8f18f-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="8f18f-119">Cette propriété n’est pas requise.</span><span class="sxs-lookup"><span data-stu-id="8f18f-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8f18f-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8f18f-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8f18f-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="8f18f-121">Protocol specifications</span></span>

<span data-ttu-id="8f18f-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f18f-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f18f-123">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="8f18f-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8f18f-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f18f-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f18f-125">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="8f18f-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="8f18f-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f18f-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8f18f-127">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="8f18f-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8f18f-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8f18f-128">Header files</span></span>

<span data-ttu-id="8f18f-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8f18f-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="8f18f-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8f18f-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8f18f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f18f-131">See also</span></span>



[<span data-ttu-id="8f18f-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8f18f-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8f18f-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8f18f-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8f18f-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8f18f-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8f18f-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="8f18f-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

