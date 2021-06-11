---
title: Propriété canonique PidTagOriginalDisplayBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayBcc
api_type:
- COM
ms.assetid: 7bf66f0c-3095-4b4a-a32e-db278e1adc5a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3fbd7205901616695bcdcd012601afd252ac05f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355642"
---
# <a name="pidtagoriginaldisplaybcc-canonical-property"></a><span data-ttu-id="739b8-103">Propriété canonique PidTagOriginalDisplayBcc</span><span class="sxs-lookup"><span data-stu-id="739b8-103">PidTagOriginalDisplayBcc Canonical Property</span></span>

  
  
<span data-ttu-id="739b8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="739b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="739b8-105">Contient les noms d’affichage des destinataires en copie carbone non voyante (Bc) du message d’origine.</span><span class="sxs-lookup"><span data-stu-id="739b8-105">Contains the display names of any blind carbon copy (BCC) recipients of the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="739b8-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="739b8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="739b8-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span><span class="sxs-lookup"><span data-stu-id="739b8-107">PR_ORIGINAL_DISPLAY_BCC, PR_ORIGINAL_DISPLAY_BCC_A, PR_ORIGINAL_DISPLAY_BCC_W</span></span>  <br/> |
|<span data-ttu-id="739b8-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="739b8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="739b8-109">0x0072</span><span class="sxs-lookup"><span data-stu-id="739b8-109">0x0072</span></span>  <br/> |
|<span data-ttu-id="739b8-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="739b8-110">Data type:</span></span>  <br/> |<span data-ttu-id="739b8-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="739b8-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="739b8-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="739b8-112">Area:</span></span>  <br/> |<span data-ttu-id="739b8-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="739b8-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="739b8-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="739b8-114">Remarks</span></span>

<span data-ttu-id="739b8-115">Ces propriétés contiennent une liste séparée par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="739b8-115">These properties contain a list separated by semicolons.</span></span> <span data-ttu-id="739b8-116">Ils sont fournis par MAPI et sont copiés directement à partir de **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) lorsqu’un rapport de remise ou non remise ou un rapport en lecture ou non lu est généré.</span><span class="sxs-lookup"><span data-stu-id="739b8-116">They is furnished by MAPI and are copied directly from **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) when a delivery or nondelivery report or a read or nonread report is generated.</span></span> <span data-ttu-id="739b8-117">Ces propriétés peuvent être présentes sur d’autres messages tels que définis par leurs classes de messages.</span><span class="sxs-lookup"><span data-stu-id="739b8-117">These properties may be present on other messages as defined by their message classes.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="739b8-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="739b8-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="739b8-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="739b8-119">Protocol specifications</span></span>

<span data-ttu-id="739b8-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="739b8-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="739b8-121">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="739b8-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="739b8-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="739b8-122">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="739b8-123">Spécifie les propriétés et opérations autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="739b8-123">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="739b8-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="739b8-124">Header files</span></span>

<span data-ttu-id="739b8-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="739b8-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="739b8-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="739b8-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="739b8-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="739b8-127">Mapitags.h</span></span>
  
> <span data-ttu-id="739b8-128">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="739b8-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="739b8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="739b8-129">See also</span></span>



[<span data-ttu-id="739b8-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="739b8-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="739b8-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="739b8-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="739b8-132">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="739b8-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="739b8-133">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="739b8-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

