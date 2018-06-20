---
title: Propriété canonique PidTagImplicitConversionProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImplicitConversionProhibited
api_type:
- HeaderDef
ms.assetid: c6cb5a86-0105-4743-9f8e-b832e898da52
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: dcfaf9f4e71a13a8697da0cac98f7ea9cc3d8708
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786101"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a><span data-ttu-id="bc7cf-103">Propriété canonique PidTagImplicitConversionProhibited</span><span class="sxs-lookup"><span data-stu-id="bc7cf-103">PidTagImplicitConversionProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="bc7cf-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bc7cf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bc7cf-105">Contient la valeur TRUE si un message transfert agent d’est interdite d’effectuer des conversions de texte message implicite.</span><span class="sxs-lookup"><span data-stu-id="bc7cf-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making implicit message text conversions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bc7cf-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="bc7cf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bc7cf-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="bc7cf-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="bc7cf-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="bc7cf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bc7cf-109">0x0016</span><span class="sxs-lookup"><span data-stu-id="bc7cf-109">0x0016</span></span>  <br/> |
|<span data-ttu-id="bc7cf-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="bc7cf-110">Data type:</span></span>  <br/> |<span data-ttu-id="bc7cf-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="bc7cf-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="bc7cf-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="bc7cf-112">Area:</span></span>  <br/> |<span data-ttu-id="bc7cf-113">Serveur</span><span class="sxs-lookup"><span data-stu-id="bc7cf-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc7cf-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="bc7cf-114">Remarks</span></span>

<span data-ttu-id="bc7cf-115">Si cette propriété a la valeur TRUE, le système de messagerie doit effectuent pas de conversion de contenu dans le message, sauf si elle est demandée explicitement sur une base par destinataire avec la propriété **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="bc7cf-115">If this property is TRUE, the messaging system must not perform any content conversion on the message unless it is explicitly requested on a per-recipient basis with the **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bc7cf-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="bc7cf-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="bc7cf-117">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="bc7cf-117">Header files</span></span>

<span data-ttu-id="bc7cf-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bc7cf-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="bc7cf-119">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="bc7cf-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="bc7cf-120">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="bc7cf-120">Mapitags.h</span></span>
  
> <span data-ttu-id="bc7cf-121">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="bc7cf-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bc7cf-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc7cf-122">See also</span></span>



[<span data-ttu-id="bc7cf-123">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="bc7cf-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bc7cf-124">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="bc7cf-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bc7cf-125">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="bc7cf-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bc7cf-126">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="bc7cf-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

