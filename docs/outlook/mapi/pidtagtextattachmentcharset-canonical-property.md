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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1db41bc5c7ea71d65d892da520d4258354eb53cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358813"
---
# <a name="pidtagtextattachmentcharset-canonical-property"></a><span data-ttu-id="d46cf-103">Propriété canonique PidTagTextAttachmentCharset</span><span class="sxs-lookup"><span data-stu-id="d46cf-103">PidTagTextAttachmentCharset Canonical Property</span></span>

  
  
<span data-ttu-id="d46cf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d46cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d46cf-105">Contient la valeur du jeu de caractères d’une pièce jointe d’un message.</span><span class="sxs-lookup"><span data-stu-id="d46cf-105">Contains a message attachment's character set value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d46cf-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d46cf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d46cf-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="d46cf-107">None</span></span>  <br/> |
|<span data-ttu-id="d46cf-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d46cf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d46cf-109">0x371B</span><span class="sxs-lookup"><span data-stu-id="d46cf-109">0x371B</span></span>  <br/> |
|<span data-ttu-id="d46cf-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d46cf-110">Data type:</span></span>  <br/> |<span data-ttu-id="d46cf-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d46cf-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d46cf-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d46cf-112">Area:</span></span>  <br/> |<span data-ttu-id="d46cf-113">Pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="d46cf-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d46cf-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d46cf-114">Remarks</span></span>

<span data-ttu-id="d46cf-115">Les données de cette propriété sont dérivées d’un champ d’en-tête MIME content-type qui commence par « text/ », si un paramètre « charset » est présent.</span><span class="sxs-lookup"><span data-stu-id="d46cf-115">This property's data is derived from a Content-Type MIME header field that starts with "text/", if a "charset" parameter is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d46cf-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d46cf-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d46cf-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="d46cf-117">Protocol specifications</span></span>

<span data-ttu-id="d46cf-118">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d46cf-118">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d46cf-119">Convertit des conventions de messagerie standard Internet en objets de message.</span><span class="sxs-lookup"><span data-stu-id="d46cf-119">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d46cf-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d46cf-120">Header files</span></span>

<span data-ttu-id="d46cf-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d46cf-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="d46cf-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d46cf-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="d46cf-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d46cf-123">Mapitags.h</span></span>
  
> <span data-ttu-id="d46cf-124">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="d46cf-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d46cf-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d46cf-125">See also</span></span>



[<span data-ttu-id="d46cf-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d46cf-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d46cf-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d46cf-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d46cf-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d46cf-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d46cf-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="d46cf-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

