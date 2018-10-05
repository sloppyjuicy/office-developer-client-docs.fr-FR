---
title: Propriété canonique PidTagDeleteAfterSubmit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeleteAfterSubmit
api_type:
- HeaderDef
ms.assetid: ba69a557-120c-4b1e-bbb7-0e901e7d1ebf
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2708d89e2572e8820de0b525b4f53ccd309ae2a0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383869"
---
# <a name="pidtagdeleteaftersubmit-canonical-property"></a><span data-ttu-id="b3004-103">Propriété canonique PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="b3004-103">PidTagDeleteAfterSubmit Canonical Property</span></span>

  
  
<span data-ttu-id="b3004-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3004-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3004-105">Contient la valeur TRUE si une application cliente souhaite MAPI pour supprimer le message associé après l’envoi.</span><span class="sxs-lookup"><span data-stu-id="b3004-105">Contains TRUE if a client application wants MAPI to delete the associated message after submission.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3004-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b3004-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b3004-107">PR_DELETE_AFTER_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="b3004-107">PR_DELETE_AFTER_SUBMIT</span></span>  <br/> |
|<span data-ttu-id="b3004-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b3004-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b3004-109">0x0E01</span><span class="sxs-lookup"><span data-stu-id="b3004-109">0x0E01</span></span>  <br/> |
|<span data-ttu-id="b3004-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b3004-110">Data type:</span></span>  <br/> |<span data-ttu-id="b3004-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="b3004-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="b3004-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="b3004-112">Area:</span></span>  <br/> |<span data-ttu-id="b3004-113">MAPI non transmissible</span><span class="sxs-lookup"><span data-stu-id="b3004-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3004-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b3004-114">Remarks</span></span>

<span data-ttu-id="b3004-115">Une application cliente utilise cette propriété avec la propriété **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) pour contrôler que se passe-t-il à un message après son envoi.</span><span class="sxs-lookup"><span data-stu-id="b3004-115">A client application uses this property with the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="b3004-116">Une ou l’autre doit être ensemble, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="b3004-116">Either one or the other should be set, but not both.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b3004-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b3004-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b3004-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="b3004-118">Protocol specifications</span></span>

<span data-ttu-id="b3004-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b3004-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b3004-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="b3004-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b3004-121">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b3004-121">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b3004-122">Spécifie les opérations autorisées pour les objets de banque de messages principale.</span><span class="sxs-lookup"><span data-stu-id="b3004-122">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="b3004-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b3004-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b3004-124">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="b3004-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b3004-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b3004-125">Header files</span></span>

<span data-ttu-id="b3004-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b3004-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="b3004-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b3004-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="b3004-128">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="b3004-128">Mapitags.h</span></span>
  
> <span data-ttu-id="b3004-129">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="b3004-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b3004-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3004-130">See also</span></span>



[<span data-ttu-id="b3004-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b3004-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b3004-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b3004-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b3004-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b3004-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b3004-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="b3004-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

