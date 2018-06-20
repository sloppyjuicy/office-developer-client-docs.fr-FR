---
title: Propriété canonique PidTagAttachFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFlags
api_type:
- HeaderDef
ms.assetid: 47e01131-f399-43cb-9815-aba69638c3fb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b934f9694061e17118be35e3fabeeff3bbc61a37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785713"
---
# <a name="pidtagattachflags-canonical-property"></a><span data-ttu-id="1e04a-103">Propriété canonique PidTagAttachFlags</span><span class="sxs-lookup"><span data-stu-id="1e04a-103">PidTagAttachFlags Canonical Property</span></span>

  
  
<span data-ttu-id="1e04a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1e04a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1e04a-105">Contient un masque binaire composé des indicateurs d’une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="1e04a-105">Contains a bitmask of flags for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1e04a-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1e04a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1e04a-107">PR_ATTACH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="1e04a-107">PR_ATTACH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="1e04a-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1e04a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1e04a-109">0x3714</span><span class="sxs-lookup"><span data-stu-id="1e04a-109">0x3714</span></span>  <br/> |
|<span data-ttu-id="1e04a-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1e04a-110">Data type:</span></span>  <br/> |<span data-ttu-id="1e04a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1e04a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1e04a-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="1e04a-112">Area:</span></span>  <br/> |<span data-ttu-id="1e04a-113">Pièce jointe du message</span><span class="sxs-lookup"><span data-stu-id="1e04a-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e04a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1e04a-114">Remarks</span></span>

<span data-ttu-id="1e04a-115">Cette propriété est utilisée pour la prise en charge MHTML.</span><span class="sxs-lookup"><span data-stu-id="1e04a-115">This property is used for MHTML support.</span></span> 
  
<span data-ttu-id="1e04a-116">Un ou plusieurs des indicateurs suivants peuvent être définies pour le masque de bits **PR_ATTACH_FLAGS** :</span><span class="sxs-lookup"><span data-stu-id="1e04a-116">One or more of the following flags can be set for the **PR_ATTACH_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="1e04a-117">ATT_INVISIBLE_IN_HTML</span><span class="sxs-lookup"><span data-stu-id="1e04a-117">ATT_INVISIBLE_IN_HTML</span></span> 
  
> <span data-ttu-id="1e04a-118">Indique que cette pièce jointe n’est pas disponible pour les applications de rendu HTML et doit être ignorée dans Multipurpose Internet Mail Extensions (MIME) de traitement.</span><span class="sxs-lookup"><span data-stu-id="1e04a-118">Indicates that this attachment is not available to HTML rendering applications and should be ignored in Multipurpose Internet Mail Extensions (MIME) processing.</span></span> 
    
<span data-ttu-id="1e04a-119">ATT_INVISIBLE_IN_RTF</span><span class="sxs-lookup"><span data-stu-id="1e04a-119">ATT_INVISIBLE_IN_RTF</span></span> 
  
> <span data-ttu-id="1e04a-120">Indique que cette pièce jointe n’est pas disponible pour les applications rendu au format RTF (RICH Text Format) et doit être ignorée par MAPI.</span><span class="sxs-lookup"><span data-stu-id="1e04a-120">Indicates that this attachment is not available to applications rendering in Rich Text Format (RTF) and should be ignored by MAPI.</span></span>
    
<span data-ttu-id="1e04a-121">Si la propriété **PR_ATTACH_FLAGS** est égale à zéro ou absent, la pièce jointe doit être traité par toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="1e04a-121">If the **PR_ATTACH_FLAGS** property is zero or absent, the attachment is to be processed by all applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1e04a-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1e04a-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1e04a-123">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="1e04a-123">Protocol specifications</span></span>

<span data-ttu-id="1e04a-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e04a-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e04a-125">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="1e04a-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1e04a-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1e04a-126">Header files</span></span>

<span data-ttu-id="1e04a-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1e04a-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="1e04a-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1e04a-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="1e04a-129">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="1e04a-129">Mapitags.h</span></span>
  
> <span data-ttu-id="1e04a-130">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="1e04a-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e04a-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e04a-131">See also</span></span>



[<span data-ttu-id="1e04a-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1e04a-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1e04a-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1e04a-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1e04a-134">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1e04a-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1e04a-135">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="1e04a-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

