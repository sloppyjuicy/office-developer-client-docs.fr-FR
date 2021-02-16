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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359912"
---
# <a name="pidtagdeleteaftersubmit-canonical-property"></a><span data-ttu-id="e1bbc-103">Propriété canonique PidTagDeleteAfterSubmit</span><span class="sxs-lookup"><span data-stu-id="e1bbc-103">PidTagDeleteAfterSubmit Canonical Property</span></span>

  
  
<span data-ttu-id="e1bbc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1bbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1bbc-105">Contient TRUE si une application cliente souhaite que MAPI supprime le message associé après l’envoi.</span><span class="sxs-lookup"><span data-stu-id="e1bbc-105">Contains TRUE if a client application wants MAPI to delete the associated message after submission.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e1bbc-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e1bbc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e1bbc-107">PR_DELETE_AFTER_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="e1bbc-107">PR_DELETE_AFTER_SUBMIT</span></span>  <br/> |
|<span data-ttu-id="e1bbc-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="e1bbc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e1bbc-109">0x0E01</span><span class="sxs-lookup"><span data-stu-id="e1bbc-109">0x0E01</span></span>  <br/> |
|<span data-ttu-id="e1bbc-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e1bbc-110">Data type:</span></span>  <br/> |<span data-ttu-id="e1bbc-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e1bbc-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e1bbc-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e1bbc-112">Area:</span></span>  <br/> |<span data-ttu-id="e1bbc-113">MAPI non transmetteable</span><span class="sxs-lookup"><span data-stu-id="e1bbc-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1bbc-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e1bbc-114">Remarks</span></span>

<span data-ttu-id="e1bbc-115">Une application cliente utilise cette propriété avec la **propriété PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) pour contrôler ce qu’il advient d’un message après qu’il a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="e1bbc-115">A client application uses this property with the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property to control what happens to a message after it is submitted.</span></span> <span data-ttu-id="e1bbc-116">L’une ou l’autre doit être définie, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="e1bbc-116">Either one or the other should be set, but not both.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e1bbc-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e1bbc-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e1bbc-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="e1bbc-118">Protocol specifications</span></span>

<span data-ttu-id="e1bbc-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1bbc-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1bbc-120">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="e1bbc-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e1bbc-121">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1bbc-121">[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1bbc-122">Spécifie les opérations autorisées pour les objets principaux de la boutique de messages.</span><span class="sxs-lookup"><span data-stu-id="e1bbc-122">Specifies permissible operations for the core message store objects.</span></span>
    
<span data-ttu-id="e1bbc-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1bbc-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1bbc-124">Spécifie les propriétés et opérations autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="e1bbc-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e1bbc-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e1bbc-125">Header files</span></span>

<span data-ttu-id="e1bbc-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e1bbc-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1bbc-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e1bbc-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="e1bbc-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e1bbc-128">Mapitags.h</span></span>
  
> <span data-ttu-id="e1bbc-129">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="e1bbc-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1bbc-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1bbc-130">See also</span></span>



[<span data-ttu-id="e1bbc-131">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e1bbc-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1bbc-132">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e1bbc-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1bbc-133">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e1bbc-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1bbc-134">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e1bbc-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

