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
ms.openlocfilehash: ea78d9487e4929c2df3d49a9b85ba4aefac90a59
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785684"
---
# <a name="pidtagalternaterecipient-canonical-property"></a><span data-ttu-id="75a98-103">Propriété canonique PidTagAlternateRecipient</span><span class="sxs-lookup"><span data-stu-id="75a98-103">PidTagAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="75a98-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="75a98-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="75a98-105">Contient une liste d’identificateurs d’entrée pour les autres destinataires désignés par le destinataire d’origine.</span><span class="sxs-lookup"><span data-stu-id="75a98-105">Contains a list of entry identifiers for alternate recipients designated by the original recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="75a98-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="75a98-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="75a98-107">PR_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="75a98-107">PR_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="75a98-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="75a98-108">Identifier:</span></span>  <br/> |<span data-ttu-id="75a98-109">0x3A01</span><span class="sxs-lookup"><span data-stu-id="75a98-109">0x3A01</span></span>  <br/> |
|<span data-ttu-id="75a98-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="75a98-110">Data type:</span></span>  <br/> |<span data-ttu-id="75a98-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="75a98-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="75a98-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="75a98-112">Area:</span></span>  <br/> |<span data-ttu-id="75a98-113">Address</span><span class="sxs-lookup"><span data-stu-id="75a98-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75a98-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="75a98-114">Remarks</span></span>

<span data-ttu-id="75a98-115">Cette propriété est utilisée pour automatique des messages transmis.</span><span class="sxs-lookup"><span data-stu-id="75a98-115">This property is used for auto forwarded messages.</span></span> <span data-ttu-id="75a98-116">Il contient une structure [FLATENTRYLIST](flatentrylist.md) des autres destinataires.</span><span class="sxs-lookup"><span data-stu-id="75a98-116">It contains a [FLATENTRYLIST](flatentrylist.md) structure of alternate recipients.</span></span> <span data-ttu-id="75a98-117">Si le transfert automatique n’est pas autorisée ou si aucun autre destinataire n’a été désigné, un rapport de non-remise est généré.</span><span class="sxs-lookup"><span data-stu-id="75a98-117">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="75a98-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="75a98-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="75a98-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="75a98-119">Protocol specifications</span></span>

<span data-ttu-id="75a98-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75a98-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75a98-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="75a98-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="75a98-122">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75a98-122">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75a98-123">Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="75a98-123">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="75a98-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75a98-124">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75a98-125">La conversion entre IETF RFC2445, RFC2446, RFC2447 et rendez-vous et des objets de la conférence.</span><span class="sxs-lookup"><span data-stu-id="75a98-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="75a98-126">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="75a98-126">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="75a98-127">Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="75a98-127">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="75a98-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="75a98-128">Header files</span></span>

<span data-ttu-id="75a98-129">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="75a98-129">Mapitags.h</span></span>
  
> <span data-ttu-id="75a98-130">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="75a98-130">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="75a98-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="75a98-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="75a98-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="75a98-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="75a98-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75a98-133">See also</span></span>



[<span data-ttu-id="75a98-134">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="75a98-134">FLATENTRYLIST</span></span>](flatentrylist.md)


[<span data-ttu-id="75a98-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="75a98-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="75a98-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="75a98-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="75a98-137">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="75a98-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="75a98-138">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="75a98-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

