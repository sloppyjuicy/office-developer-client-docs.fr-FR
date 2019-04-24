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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 12cdbfcc140fb5ea3bb15a2db93f3689923d9390
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344967"
---
# <a name="pidlidccattendeesstring-canonical-property"></a><span data-ttu-id="27120-103">Propriété canonique PidLidCcAttendeesString</span><span class="sxs-lookup"><span data-stu-id="27120-103">PidLidCcAttendeesString Canonical Property</span></span>

  
  
<span data-ttu-id="27120-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27120-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27120-105">Contient une liste de tous les participants qui sont également facultatifs.</span><span class="sxs-lookup"><span data-stu-id="27120-105">Contains a list of all the sendable attendees who are also optional attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="27120-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="27120-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27120-107">dispidCCAttendeesString</span><span class="sxs-lookup"><span data-stu-id="27120-107">dispidCCAttendeesString</span></span>  <br/> |
|<span data-ttu-id="27120-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="27120-108">Property set:</span></span>  <br/> |<span data-ttu-id="27120-109">PSETID_Appointment</span><span class="sxs-lookup"><span data-stu-id="27120-109">PSETID_Appointment</span></span>  <br/> |
|<span data-ttu-id="27120-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="27120-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="27120-111">0x0000823C</span><span class="sxs-lookup"><span data-stu-id="27120-111">0x0000823C</span></span>  <br/> |
|<span data-ttu-id="27120-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="27120-112">Data type:</span></span>  <br/> |<span data-ttu-id="27120-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="27120-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="27120-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="27120-114">Area:</span></span>  <br/> |<span data-ttu-id="27120-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="27120-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27120-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="27120-116">Remarks</span></span>

<span data-ttu-id="27120-117">La valeur de chaque participant est la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) du carnet d'adresses du participant.</span><span class="sxs-lookup"><span data-stu-id="27120-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's address book.</span></span> <span data-ttu-id="27120-118">Les entrées distinctes doivent être délimitées par un point-virgule suivi d'un espace.</span><span class="sxs-lookup"><span data-stu-id="27120-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="27120-119">Cette propriété n'est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="27120-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="27120-120">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="27120-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="27120-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="27120-121">Protocol specifications</span></span>

<span data-ttu-id="27120-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27120-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27120-123">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="27120-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="27120-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27120-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27120-125">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="27120-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="27120-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27120-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27120-127">Effectue une conversion entre l'IETF RFC2445, RFC2446 et RFC2447, et les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="27120-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="27120-128">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="27120-128">Header files</span></span>

<span data-ttu-id="27120-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="27120-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="27120-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="27120-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27120-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27120-131">See also</span></span>



[<span data-ttu-id="27120-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="27120-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27120-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="27120-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27120-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="27120-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27120-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="27120-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

