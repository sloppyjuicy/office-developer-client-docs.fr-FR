---
title: Propriété canonique PidTagAlternateRecipient
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAlternateRecipient
api_type:
- HeaderDef
ms.assetid: df787b60-2f53-42ac-89b5-1b52c906f472
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7c304de3184e49044d3f83cef1f1ebaac019b2ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360094"
---
# <a name="pidtagalternaterecipient-canonical-property"></a><span data-ttu-id="53011-103">Propriété canonique PidTagAlternateRecipient</span><span class="sxs-lookup"><span data-stu-id="53011-103">PidTagAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="53011-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53011-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53011-105">Contient une liste d'identificateurs d'entrée pour les destinataires suppléant désignés par le destinataire d'origine.</span><span class="sxs-lookup"><span data-stu-id="53011-105">Contains a list of entry identifiers for alternate recipients designated by the original recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="53011-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="53011-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="53011-107">PR_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="53011-107">PR_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="53011-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="53011-108">Identifier:</span></span>  <br/> |<span data-ttu-id="53011-109">0x3A01</span><span class="sxs-lookup"><span data-stu-id="53011-109">0x3A01</span></span>  <br/> |
|<span data-ttu-id="53011-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="53011-110">Data type:</span></span>  <br/> |<span data-ttu-id="53011-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="53011-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="53011-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="53011-112">Area:</span></span>  <br/> |<span data-ttu-id="53011-113">Address</span><span class="sxs-lookup"><span data-stu-id="53011-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53011-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="53011-114">Remarks</span></span>

<span data-ttu-id="53011-115">Cette propriété est utilisée pour les messages transférés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="53011-115">This property is used for auto forwarded messages.</span></span> <span data-ttu-id="53011-116">Il contient une structure [FLATENTRYLIST](flatentrylist.md) de destinataires suppléants.</span><span class="sxs-lookup"><span data-stu-id="53011-116">It contains a [FLATENTRYLIST](flatentrylist.md) structure of alternate recipients.</span></span> <span data-ttu-id="53011-117">Si le transfert d'autodirection n'est pas autorisé ou si aucun autre destinataire n'a été désigné, un rapport de non-remise est généré.</span><span class="sxs-lookup"><span data-stu-id="53011-117">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="53011-118">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="53011-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="53011-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="53011-119">Protocol specifications</span></span>

<span data-ttu-id="53011-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53011-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53011-121">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="53011-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="53011-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53011-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53011-123">Gère l'ordre et le flux de transfert de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="53011-123">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="53011-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53011-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53011-125">Effectue une conversion entre l'IETF RFC2445, RFC2446 et RFC2447, et les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="53011-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="53011-126">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53011-126">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53011-127">Encode et décode les objets message et Attachment en une représentation de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="53011-127">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="53011-128">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="53011-128">Header files</span></span>

<span data-ttu-id="53011-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="53011-129">Mapitags.h</span></span>
  
> <span data-ttu-id="53011-130">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="53011-130">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="53011-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="53011-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="53011-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="53011-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53011-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53011-133">See also</span></span>



[<span data-ttu-id="53011-134">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="53011-134">FLATENTRYLIST</span></span>](flatentrylist.md)


[<span data-ttu-id="53011-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="53011-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="53011-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="53011-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="53011-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="53011-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="53011-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="53011-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

