---
title: Propriété canonique PidTagTextAttachmentCharset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTextAttachmentCharset
api_type:
- COM
ms.assetid: d347c949-d0c3-4a36-8447-3fa01111cdc1
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c728799832b10ad2d4533a9a040582b67054baad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786888"
---
# <a name="pidtagtextattachmentcharset-canonical-property"></a><span data-ttu-id="aae58-103">Propriété canonique PidTagTextAttachmentCharset</span><span class="sxs-lookup"><span data-stu-id="aae58-103">PidTagTextAttachmentCharset Canonical Property</span></span>

  
  
<span data-ttu-id="aae58-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aae58-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aae58-105">Contient la valeur de jeu de caractères d’une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="aae58-105">Contains a message attachment's character set value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aae58-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="aae58-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aae58-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="aae58-107">None</span></span>  <br/> |
|<span data-ttu-id="aae58-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="aae58-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aae58-109">0x371B</span><span class="sxs-lookup"><span data-stu-id="aae58-109">0x371B</span></span>  <br/> |
|<span data-ttu-id="aae58-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="aae58-110">Data type:</span></span>  <br/> |<span data-ttu-id="aae58-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="aae58-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="aae58-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="aae58-112">Area:</span></span>  <br/> |<span data-ttu-id="aae58-113">Pièce jointe du message</span><span class="sxs-lookup"><span data-stu-id="aae58-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aae58-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="aae58-114">Remarks</span></span>

<span data-ttu-id="aae58-115">Données de cette propriété sont dérivées d’un champ d’en-tête MIME Content-Type qui commence par « texte / », s’il existe un paramètre « charset ».</span><span class="sxs-lookup"><span data-stu-id="aae58-115">This property's data is derived from a Content-Type MIME header field that starts with "text/", if a "charset" parameter is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="aae58-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="aae58-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aae58-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="aae58-117">Protocol specifications</span></span>

<span data-ttu-id="aae58-118">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aae58-118">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aae58-119">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="aae58-119">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aae58-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="aae58-120">Header files</span></span>

<span data-ttu-id="aae58-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aae58-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="aae58-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="aae58-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="aae58-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="aae58-123">Mapitags.h</span></span>
  
> <span data-ttu-id="aae58-124">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="aae58-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aae58-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aae58-125">See also</span></span>



[<span data-ttu-id="aae58-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="aae58-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aae58-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="aae58-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aae58-128">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="aae58-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aae58-129">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="aae58-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

