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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7c304de3184e49044d3f83cef1f1ebaac019b2ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360094"
---
# <a name="pidtagalternaterecipient-canonical-property"></a><span data-ttu-id="5d7a8-103">Propriété canonique PidTagAlternateRecipient</span><span class="sxs-lookup"><span data-stu-id="5d7a8-103">PidTagAlternateRecipient Canonical Property</span></span>

  
  
<span data-ttu-id="5d7a8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d7a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d7a8-105">Contient une liste d’identificateurs d’entrée pour d’autres destinataires désignés par le destinataire d’origine.</span><span class="sxs-lookup"><span data-stu-id="5d7a8-105">Contains a list of entry identifiers for alternate recipients designated by the original recipient.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5d7a8-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5d7a8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5d7a8-107">PR_ALTERNATE_RECIPIENT</span><span class="sxs-lookup"><span data-stu-id="5d7a8-107">PR_ALTERNATE_RECIPIENT</span></span>  <br/> |
|<span data-ttu-id="5d7a8-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5d7a8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5d7a8-109">0x3A01</span><span class="sxs-lookup"><span data-stu-id="5d7a8-109">0x3A01</span></span>  <br/> |
|<span data-ttu-id="5d7a8-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5d7a8-110">Data type:</span></span>  <br/> |<span data-ttu-id="5d7a8-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5d7a8-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5d7a8-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5d7a8-112">Area:</span></span>  <br/> |<span data-ttu-id="5d7a8-113">Adresse</span><span class="sxs-lookup"><span data-stu-id="5d7a8-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d7a8-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5d7a8-114">Remarks</span></span>

<span data-ttu-id="5d7a8-115">Cette propriété est utilisée pour les messages transmis automatiquement.</span><span class="sxs-lookup"><span data-stu-id="5d7a8-115">This property is used for auto forwarded messages.</span></span> <span data-ttu-id="5d7a8-116">Il contient une structure [FLATENTRYLIST](flatentrylist.md) de destinataires de remplacement.</span><span class="sxs-lookup"><span data-stu-id="5d7a8-116">It contains a [FLATENTRYLIST](flatentrylist.md) structure of alternate recipients.</span></span> <span data-ttu-id="5d7a8-117">Si laforwarding automatique n’est pas autorisée ou si aucun autre destinataire n’a été désigné, un rapport de non-demande est généré.</span><span class="sxs-lookup"><span data-stu-id="5d7a8-117">If autoforwarding is not permitted or if no alternate recipient has been designated, a nondelivery report is generated.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5d7a8-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5d7a8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5d7a8-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="5d7a8-119">Protocol specifications</span></span>

<span data-ttu-id="5d7a8-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d7a8-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d7a8-121">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="5d7a8-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5d7a8-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d7a8-122">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d7a8-123">Gère l’ordre et le flux des transferts de données entre un client et un serveur.</span><span class="sxs-lookup"><span data-stu-id="5d7a8-123">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="5d7a8-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d7a8-124">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d7a8-125">Convertit les objets RFC2445, RFC2446 et RFC2447 de l’IETF, ainsi que les objets de rendez-vous et de réunion.</span><span class="sxs-lookup"><span data-stu-id="5d7a8-125">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="5d7a8-126">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5d7a8-126">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5d7a8-127">Code et décode les objets de message et de pièce jointe dans une représentation de flux efficace.</span><span class="sxs-lookup"><span data-stu-id="5d7a8-127">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5d7a8-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5d7a8-128">Header files</span></span>

<span data-ttu-id="5d7a8-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5d7a8-129">Mapitags.h</span></span>
  
> <span data-ttu-id="5d7a8-130">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="5d7a8-130">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="5d7a8-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5d7a8-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="5d7a8-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5d7a8-132">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5d7a8-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d7a8-133">See also</span></span>



[<span data-ttu-id="5d7a8-134">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="5d7a8-134">FLATENTRYLIST</span></span>](flatentrylist.md)


[<span data-ttu-id="5d7a8-135">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5d7a8-135">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5d7a8-136">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5d7a8-136">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5d7a8-137">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5d7a8-137">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5d7a8-138">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5d7a8-138">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

