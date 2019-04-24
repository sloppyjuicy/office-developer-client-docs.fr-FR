---
title: Propriété canonique PidLidNonSendableCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidNonSendableCc
api_type:
- COM
ms.assetid: 170afe1f-1223-4689-825c-d21ab14b213b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d9f166b0d1e180fdb087fbf602e6841c3fdac3dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319655"
---
# <a name="pidlidnonsendablecc-canonical-property"></a><span data-ttu-id="f77e0-103">Propriété canonique PidLidNonSendableCc</span><span class="sxs-lookup"><span data-stu-id="f77e0-103">PidLidNonSendableCc Canonical Property</span></span>

  
  
<span data-ttu-id="f77e0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f77e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f77e0-105">Contient une liste de tous les participants non envoyés qui sont également des participants facultatifs.</span><span class="sxs-lookup"><span data-stu-id="f77e0-105">Contains a list of all the unsendable attendees who are also optional attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f77e0-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f77e0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f77e0-107">dispidNonSendableCC</span><span class="sxs-lookup"><span data-stu-id="f77e0-107">dispidNonSendableCC</span></span>  <br/> |
|<span data-ttu-id="f77e0-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="f77e0-108">Property set:</span></span>  <br/> |<span data-ttu-id="f77e0-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="f77e0-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="f77e0-110">ID long (couvercle):</span><span class="sxs-lookup"><span data-stu-id="f77e0-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="f77e0-111">0x00008537</span><span class="sxs-lookup"><span data-stu-id="f77e0-111">0x00008537</span></span>  <br/> |
|<span data-ttu-id="f77e0-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f77e0-112">Data type:</span></span>  <br/> |<span data-ttu-id="f77e0-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f77e0-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f77e0-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f77e0-114">Area:</span></span>  <br/> |<span data-ttu-id="f77e0-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="f77e0-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f77e0-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="f77e0-116">Remarks</span></span>

<span data-ttu-id="f77e0-117">La valeur de chaque participant est la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) du carnet d'adresses du participant.</span><span class="sxs-lookup"><span data-stu-id="f77e0-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="f77e0-118">Les entrées distinctes doivent être délimitées par un point-virgule suivi d'un espace.</span><span class="sxs-lookup"><span data-stu-id="f77e0-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="f77e0-119">Cette propriété n'est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f77e0-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f77e0-120">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="f77e0-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f77e0-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="f77e0-121">Protocol specifications</span></span>

<span data-ttu-id="f77e0-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f77e0-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f77e0-123">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="f77e0-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f77e0-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f77e0-124">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f77e0-125">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="f77e0-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="f77e0-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f77e0-126">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f77e0-127">Effectue une conversion entre l'IETF RFC2445, RFC2446 et RFC2447, et les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="f77e0-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f77e0-128">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="f77e0-128">Header files</span></span>

<span data-ttu-id="f77e0-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f77e0-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="f77e0-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f77e0-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f77e0-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f77e0-131">See also</span></span>



[<span data-ttu-id="f77e0-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f77e0-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f77e0-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f77e0-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f77e0-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f77e0-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f77e0-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f77e0-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

