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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7635dd24f4fbc5128d3d96556802ab2e3fe56e35
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571842"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a><span data-ttu-id="2ce5c-103">Propriété canonique PidTagImplicitConversionProhibited</span><span class="sxs-lookup"><span data-stu-id="2ce5c-103">PidTagImplicitConversionProhibited Canonical Property</span></span>

  
  
<span data-ttu-id="2ce5c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ce5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ce5c-105">Contient la valeur TRUE si un message transfert agent d’est interdite d’effectuer des conversions de texte message implicite.</span><span class="sxs-lookup"><span data-stu-id="2ce5c-105">Contains TRUE if a message transfer agent (MTA) is prohibited from making implicit message text conversions.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ce5c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="2ce5c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2ce5c-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span><span class="sxs-lookup"><span data-stu-id="2ce5c-107">PR_IMPLICIT_CONVERSION_PROHIBITED</span></span>  <br/> |
|<span data-ttu-id="2ce5c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="2ce5c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2ce5c-109">0x0016</span><span class="sxs-lookup"><span data-stu-id="2ce5c-109">0x0016</span></span>  <br/> |
|<span data-ttu-id="2ce5c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="2ce5c-110">Data type:</span></span>  <br/> |<span data-ttu-id="2ce5c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="2ce5c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="2ce5c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="2ce5c-112">Area:</span></span>  <br/> |<span data-ttu-id="2ce5c-113">Serveur</span><span class="sxs-lookup"><span data-stu-id="2ce5c-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ce5c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="2ce5c-114">Remarks</span></span>

<span data-ttu-id="2ce5c-115">Si cette propriété a la valeur TRUE, le système de messagerie doit effectuent pas de conversion de contenu dans le message, sauf si elle est demandée explicitement sur une base par destinataire avec la propriété **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="2ce5c-115">If this property is TRUE, the messaging system must not perform any content conversion on the message unless it is explicitly requested on a per-recipient basis with the **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="2ce5c-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="2ce5c-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="2ce5c-117">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="2ce5c-117">Header files</span></span>

<span data-ttu-id="2ce5c-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ce5c-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="2ce5c-119">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="2ce5c-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="2ce5c-120">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="2ce5c-120">Mapitags.h</span></span>
  
> <span data-ttu-id="2ce5c-121">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="2ce5c-121">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ce5c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ce5c-122">See also</span></span>



[<span data-ttu-id="2ce5c-123">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="2ce5c-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2ce5c-124">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="2ce5c-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2ce5c-125">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="2ce5c-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2ce5c-126">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="2ce5c-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

