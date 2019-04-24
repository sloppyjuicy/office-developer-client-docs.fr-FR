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
ms.openlocfilehash: 1db41bc5c7ea71d65d892da520d4258354eb53cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358813"
---
# <a name="pidtagtextattachmentcharset-canonical-property"></a><span data-ttu-id="9ea1e-103">Propriété canonique PidTagTextAttachmentCharset</span><span class="sxs-lookup"><span data-stu-id="9ea1e-103">PidTagTextAttachmentCharset Canonical Property</span></span>

  
  
<span data-ttu-id="9ea1e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ea1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ea1e-105">Contient la valeur du jeu de caractères d'une pièce jointe de message.</span><span class="sxs-lookup"><span data-stu-id="9ea1e-105">Contains a message attachment's character set value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9ea1e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9ea1e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ea1e-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="9ea1e-107">None</span></span>  <br/> |
|<span data-ttu-id="9ea1e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9ea1e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9ea1e-109">0x371B</span><span class="sxs-lookup"><span data-stu-id="9ea1e-109">0x371B</span></span>  <br/> |
|<span data-ttu-id="9ea1e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9ea1e-110">Data type:</span></span>  <br/> |<span data-ttu-id="9ea1e-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9ea1e-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9ea1e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9ea1e-112">Area:</span></span>  <br/> |<span data-ttu-id="9ea1e-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="9ea1e-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ea1e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9ea1e-114">Remarks</span></span>

<span data-ttu-id="9ea1e-115">Les données de cette propriété proviennent d'un champ d'en-tête MIME Content-type qui commence par «Text/», si un paramètre «charset» est présent.</span><span class="sxs-lookup"><span data-stu-id="9ea1e-115">This property's data is derived from a Content-Type MIME header field that starts with "text/", if a "charset" parameter is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9ea1e-116">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="9ea1e-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9ea1e-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="9ea1e-117">Protocol specifications</span></span>

<span data-ttu-id="9ea1e-118">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9ea1e-118">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9ea1e-119">ConVertit des conventions de messagerie standard Internet en objets message.</span><span class="sxs-lookup"><span data-stu-id="9ea1e-119">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9ea1e-120">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="9ea1e-120">Header files</span></span>

<span data-ttu-id="9ea1e-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9ea1e-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ea1e-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9ea1e-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="9ea1e-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="9ea1e-123">Mapitags.h</span></span>
  
> <span data-ttu-id="9ea1e-124">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="9ea1e-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ea1e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ea1e-125">See also</span></span>



[<span data-ttu-id="9ea1e-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9ea1e-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ea1e-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9ea1e-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ea1e-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9ea1e-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ea1e-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9ea1e-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

