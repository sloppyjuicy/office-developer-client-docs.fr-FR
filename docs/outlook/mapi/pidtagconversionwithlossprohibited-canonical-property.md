---
title: Propriété canonique PidTagConversionWithLossProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversionWithLossProhibited
api_type:
- HeaderDef
ms.assetid: a18b560a-e054-45b3-946d-6504465db5b7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 972df747e0ee459996b9b4da5732be1490fbd08a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417125"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a><span data-ttu-id="8b7c3-103">Propriété canonique PidTagConversionWithLossProhibited</span><span class="sxs-lookup"><span data-stu-id="8b7c3-103">PidTagConversionWithLossProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="8b7c3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b7c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b7c3-105">Contient TRUE si un agent de transfert de messages (MTA) ne peut pas effectuer de conversions de texte de message qui perdent des informations.</span><span class="sxs-lookup"><span data-stu-id="8b7c3-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making message text conversions that lose information.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8b7c3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8b7c3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8b7c3-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="8b7c3-107">PR_CONVERSION_WITH_LOSS_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="8b7c3-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="8b7c3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8b7c3-109">0x000D</span><span class="sxs-lookup"><span data-stu-id="8b7c3-109">0x000D</span></span>  <br/> |
|<span data-ttu-id="8b7c3-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8b7c3-110">Data type:</span></span>  <br/> |<span data-ttu-id="8b7c3-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8b7c3-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8b7c3-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="8b7c3-112">Area:</span></span>  <br/> |<span data-ttu-id="8b7c3-113">Configuration générale</span><span class="sxs-lookup"><span data-stu-id="8b7c3-113">General configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b7c3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8b7c3-114">Remarks</span></span>

<span data-ttu-id="8b7c3-115">Un exemple du type de conversion interdit est le mappage « perte » d’Unicode (deux octets par caractère) en un jeu de caractères à un octet.</span><span class="sxs-lookup"><span data-stu-id="8b7c3-115">An example of the type of conversion being prohibited is the "lossy" mapping from Unicode (two bytes per character) to a single-byte character set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8b7c3-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8b7c3-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8b7c3-117">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8b7c3-117">Header files</span></span>

<span data-ttu-id="8b7c3-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8b7c3-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="8b7c3-119">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8b7c3-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="8b7c3-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8b7c3-120">Mapitags.h</span></span>
  
> <span data-ttu-id="8b7c3-121">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="8b7c3-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b7c3-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b7c3-122">See also</span></span>



[<span data-ttu-id="8b7c3-123">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8b7c3-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8b7c3-124">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8b7c3-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8b7c3-125">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8b7c3-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8b7c3-126">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="8b7c3-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

