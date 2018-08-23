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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: bf92e62dc572a81b6e0aab4cb1b0fc8afe97800d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573095"
---
# <a name="pidtagattachflags-canonical-property"></a><span data-ttu-id="319d4-103">Propriété canonique PidTagAttachFlags</span><span class="sxs-lookup"><span data-stu-id="319d4-103">PidTagAttachFlags Canonical Property</span></span>

  
  
<span data-ttu-id="319d4-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="319d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="319d4-105">Contient un masque binaire composé des indicateurs d’une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="319d4-105">Contains a bitmask of flags for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="319d4-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="319d4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="319d4-107">PR_ATTACH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="319d4-107">PR_ATTACH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="319d4-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="319d4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="319d4-109">0x3714</span><span class="sxs-lookup"><span data-stu-id="319d4-109">0x3714</span></span>  <br/> |
|<span data-ttu-id="319d4-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="319d4-110">Data type:</span></span>  <br/> |<span data-ttu-id="319d4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="319d4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="319d4-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="319d4-112">Area:</span></span>  <br/> |<span data-ttu-id="319d4-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="319d4-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="319d4-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="319d4-114">Remarks</span></span>

<span data-ttu-id="319d4-115">Cette propriété est utilisée pour la prise en charge MHTML.</span><span class="sxs-lookup"><span data-stu-id="319d4-115">This property is used for MHTML support.</span></span> 
  
<span data-ttu-id="319d4-116">Un ou plusieurs des indicateurs suivants peuvent être définies pour le masque de bits **PR_ATTACH_FLAGS** :</span><span class="sxs-lookup"><span data-stu-id="319d4-116">One or more of the following flags can be set for the **PR_ATTACH_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="319d4-117">ATT_INVISIBLE_IN_HTML</span><span class="sxs-lookup"><span data-stu-id="319d4-117">ATT_INVISIBLE_IN_HTML</span></span> 
  
> <span data-ttu-id="319d4-118">Indique que cette pièce jointe n’est pas disponible pour les applications de rendu HTML et doit être ignorée dans Multipurpose Internet Mail Extensions (MIME) de traitement.</span><span class="sxs-lookup"><span data-stu-id="319d4-118">Indicates that this attachment is not available to HTML rendering applications and should be ignored in Multipurpose Internet Mail Extensions (MIME) processing.</span></span> 
    
<span data-ttu-id="319d4-119">ATT_INVISIBLE_IN_RTF</span><span class="sxs-lookup"><span data-stu-id="319d4-119">ATT_INVISIBLE_IN_RTF</span></span> 
  
> <span data-ttu-id="319d4-120">Indique que cette pièce jointe n’est pas disponible pour les applications rendu au format RTF (RICH Text Format) et doit être ignorée par MAPI.</span><span class="sxs-lookup"><span data-stu-id="319d4-120">Indicates that this attachment is not available to applications rendering in Rich Text Format (RTF) and should be ignored by MAPI.</span></span>
    
<span data-ttu-id="319d4-121">Si la propriété **PR_ATTACH_FLAGS** est égale à zéro ou absent, la pièce jointe doit être traité par toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="319d4-121">If the **PR_ATTACH_FLAGS** property is zero or absent, the attachment is to be processed by all applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="319d4-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="319d4-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="319d4-123">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="319d4-123">Protocol specifications</span></span>

<span data-ttu-id="319d4-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="319d4-124">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="319d4-125">Gère les objets de message et la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="319d4-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="319d4-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="319d4-126">Header files</span></span>

<span data-ttu-id="319d4-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="319d4-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="319d4-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="319d4-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="319d4-129">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="319d4-129">Mapitags.h</span></span>
  
> <span data-ttu-id="319d4-130">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="319d4-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="319d4-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="319d4-131">See also</span></span>



[<span data-ttu-id="319d4-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="319d4-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="319d4-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="319d4-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="319d4-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="319d4-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="319d4-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="319d4-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

