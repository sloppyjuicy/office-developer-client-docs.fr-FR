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
ms.openlocfilehash: efccd75cce04e4e392a7fbd9feecc7c8b49ab57e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339332"
---
# <a name="pidtagattachflags-canonical-property"></a><span data-ttu-id="f5a29-103">Propriété canonique PidTagAttachFlags</span><span class="sxs-lookup"><span data-stu-id="f5a29-103">PidTagAttachFlags Canonical Property</span></span>

  
  
<span data-ttu-id="f5a29-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5a29-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5a29-105">Contient un masque de masque des indicateurs d'une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="f5a29-105">Contains a bitmask of flags for an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f5a29-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f5a29-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5a29-107">PR_ATTACH_FLAGS</span><span class="sxs-lookup"><span data-stu-id="f5a29-107">PR_ATTACH_FLAGS</span></span>  <br/> |
|<span data-ttu-id="f5a29-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f5a29-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f5a29-109">0x3714</span><span class="sxs-lookup"><span data-stu-id="f5a29-109">0x3714</span></span>  <br/> |
|<span data-ttu-id="f5a29-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f5a29-110">Data type:</span></span>  <br/> |<span data-ttu-id="f5a29-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f5a29-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f5a29-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f5a29-112">Area:</span></span>  <br/> |<span data-ttu-id="f5a29-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="f5a29-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5a29-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f5a29-114">Remarks</span></span>

<span data-ttu-id="f5a29-115">Cette propriété est utilisée pour la prise en charge de MHTML.</span><span class="sxs-lookup"><span data-stu-id="f5a29-115">This property is used for MHTML support.</span></span> 
  
<span data-ttu-id="f5a29-116">Un ou plusieurs des indicateurs suivants peuvent être définis pour le masque de masque **PR_ATTACH_FLAGS** :</span><span class="sxs-lookup"><span data-stu-id="f5a29-116">One or more of the following flags can be set for the **PR_ATTACH_FLAGS** bitmask:</span></span> 
  
<span data-ttu-id="f5a29-117">ATT_INVISIBLE_IN_HTML</span><span class="sxs-lookup"><span data-stu-id="f5a29-117">ATT_INVISIBLE_IN_HTML</span></span> 
  
> <span data-ttu-id="f5a29-118">Indique que cette pièce jointe n'est pas disponible pour les applications de rendu HTML et qu'elle doit être ignorée dans le traitement MIME (Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="f5a29-118">Indicates that this attachment is not available to HTML rendering applications and should be ignored in Multipurpose Internet Mail Extensions (MIME) processing.</span></span> 
    
<span data-ttu-id="f5a29-119">ATT_INVISIBLE_IN_RTF</span><span class="sxs-lookup"><span data-stu-id="f5a29-119">ATT_INVISIBLE_IN_RTF</span></span> 
  
> <span data-ttu-id="f5a29-120">Indique que cette pièce jointe n'est pas disponible pour le rendu des applications au format RTF (Rich Text Format) et qu'elle doit être ignorée par MAPI.</span><span class="sxs-lookup"><span data-stu-id="f5a29-120">Indicates that this attachment is not available to applications rendering in Rich Text Format (RTF) and should be ignored by MAPI.</span></span>
    
<span data-ttu-id="f5a29-121">Si la propriété **PR_ATTACH_FLAGS** est nulle ou absente, la pièce jointe doit être traitée par toutes les applications.</span><span class="sxs-lookup"><span data-stu-id="f5a29-121">If the **PR_ATTACH_FLAGS** property is zero or absent, the attachment is to be processed by all applications.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f5a29-122">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="f5a29-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f5a29-123">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="f5a29-123">Protocol specifications</span></span>

<span data-ttu-id="f5a29-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5a29-124">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5a29-125">Gère les objets message et Attachment.</span><span class="sxs-lookup"><span data-stu-id="f5a29-125">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f5a29-126">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="f5a29-126">Header files</span></span>

<span data-ttu-id="f5a29-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="f5a29-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5a29-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f5a29-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="f5a29-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="f5a29-129">Mapitags.h</span></span>
  
> <span data-ttu-id="f5a29-130">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="f5a29-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5a29-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5a29-131">See also</span></span>



[<span data-ttu-id="f5a29-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f5a29-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5a29-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f5a29-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5a29-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f5a29-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5a29-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f5a29-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

