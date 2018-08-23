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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 76ea38db86f678c250016c2f5e2feea3a173bb5c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589384"
---
# <a name="pidlidnonsendablecc-canonical-property"></a><span data-ttu-id="fc565-103">Propriété canonique PidLidNonSendableCc</span><span class="sxs-lookup"><span data-stu-id="fc565-103">PidLidNonSendableCc Canonical Property</span></span>

  
  
<span data-ttu-id="fc565-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc565-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc565-105">Contient une liste de tous les participants de rédaction qui sont également des participants facultatifs.</span><span class="sxs-lookup"><span data-stu-id="fc565-105">Contains a list of all the unsendable attendees who are also optional attendees.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fc565-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="fc565-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fc565-107">dispidNonSendableCC</span><span class="sxs-lookup"><span data-stu-id="fc565-107">dispidNonSendableCC</span></span>  <br/> |
|<span data-ttu-id="fc565-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="fc565-108">Property set:</span></span>  <br/> |<span data-ttu-id="fc565-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="fc565-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="fc565-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="fc565-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="fc565-111">0x00008537</span><span class="sxs-lookup"><span data-stu-id="fc565-111">0x00008537</span></span>  <br/> |
|<span data-ttu-id="fc565-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="fc565-112">Data type:</span></span>  <br/> |<span data-ttu-id="fc565-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fc565-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fc565-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="fc565-114">Area:</span></span>  <br/> |<span data-ttu-id="fc565-115">Réunions</span><span class="sxs-lookup"><span data-stu-id="fc565-115">Meetings</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fc565-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="fc565-116">Remarks</span></span>

<span data-ttu-id="fc565-117">La valeur de chaque participant est la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de carnet d’adresses du participant.</span><span class="sxs-lookup"><span data-stu-id="fc565-117">The value for each attendee is the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property of the attendee's Address Book.</span></span> <span data-ttu-id="fc565-118">Des entrées doivent être séparées par un point-virgule suivi d’un espace.</span><span class="sxs-lookup"><span data-stu-id="fc565-118">Separate entries must be delimited by a semicolon followed by a space.</span></span> <span data-ttu-id="fc565-119">Cette propriété n’est pas requise.</span><span class="sxs-lookup"><span data-stu-id="fc565-119">This property is not required.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fc565-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="fc565-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fc565-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="fc565-121">Protocol specifications</span></span>

<span data-ttu-id="fc565-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc565-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc565-123">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="fc565-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fc565-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc565-124">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc565-125">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="fc565-125">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="fc565-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fc565-126">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fc565-127">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="fc565-127">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fc565-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="fc565-128">Header files</span></span>

<span data-ttu-id="fc565-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fc565-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="fc565-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="fc565-130">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fc565-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc565-131">See also</span></span>



[<span data-ttu-id="fc565-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="fc565-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fc565-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="fc565-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fc565-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="fc565-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fc565-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="fc565-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

