---
title: Propriété canonique PidTagSentMailEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentMailEntryId
api_type:
- COM
ms.assetid: 8f14dc15-d7d7-4894-b6a8-0d589f576c42
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b53275d3bf26aa8bee3aeaef2148f5ead961e471
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591652"
---
# <a name="pidtagsentmailentryid-canonical-property"></a><span data-ttu-id="6c6fc-103">Propriété canonique PidTagSentMailEntryId</span><span class="sxs-lookup"><span data-stu-id="6c6fc-103">PidTagSentMailEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="6c6fc-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c6fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c6fc-105">Contient l’identificateur d’entrée du dossier dans lequel le message doit être déplacé après l’envoi.</span><span class="sxs-lookup"><span data-stu-id="6c6fc-105">Contains the entry identifier of the folder where the message should be moved after submission.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6c6fc-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6c6fc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c6fc-107">PR_SENTMAIL_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="6c6fc-107">PR_SENTMAIL_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="6c6fc-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6c6fc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6c6fc-109">0x0E0A</span><span class="sxs-lookup"><span data-stu-id="6c6fc-109">0x0E0A</span></span>  <br/> |
|<span data-ttu-id="6c6fc-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6c6fc-110">Data type:</span></span>  <br/> |<span data-ttu-id="6c6fc-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6c6fc-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6c6fc-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6c6fc-112">Area:</span></span>  <br/> |<span data-ttu-id="6c6fc-113">MAPI non transmissible</span><span class="sxs-lookup"><span data-stu-id="6c6fc-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c6fc-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6c6fc-114">Remarks</span></span>

<span data-ttu-id="6c6fc-115">Cette propriété est souvent copiée à partir de la propriété **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)), dossier éléments envoyés standard de l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="6c6fc-115">This property is often copied from the **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) property, the client application's standard Sent Items folder.</span></span>
  
<span data-ttu-id="6c6fc-116">L’application cliente utilise cette propriété avec la propriété **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) pour contrôler que se passe-t-il à un message après son envoi.</span><span class="sxs-lookup"><span data-stu-id="6c6fc-116">The client application uses this property with the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="6c6fc-117">Une ou l’autre doit être ensemble, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="6c6fc-117">Either one or the other should be set, but not both.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6c6fc-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6c6fc-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6c6fc-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="6c6fc-119">Protocol specifications</span></span>

<span data-ttu-id="6c6fc-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c6fc-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c6fc-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="6c6fc-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6c6fc-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c6fc-122">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c6fc-123">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="6c6fc-123">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="6c6fc-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6c6fc-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6c6fc-125">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="6c6fc-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6c6fc-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6c6fc-126">Header files</span></span>

<span data-ttu-id="6c6fc-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6c6fc-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c6fc-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6c6fc-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="6c6fc-129">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="6c6fc-129">Mapitags.h</span></span>
  
> <span data-ttu-id="6c6fc-130">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="6c6fc-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c6fc-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c6fc-131">See also</span></span>



[<span data-ttu-id="6c6fc-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6c6fc-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c6fc-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6c6fc-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c6fc-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6c6fc-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c6fc-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6c6fc-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

