---
title: Propriété canonique PidTagCorrelate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelate
api_type:
- HeaderDef
ms.assetid: be34993e-ffcc-47f5-b2d4-95ffa707bc5c
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 063e41bf9fe306b3862e302abb4495ca56e3087b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575454"
---
# <a name="pidtagcorrelate-canonical-property"></a><span data-ttu-id="987f3-103">Propriété canonique PidTagCorrelate</span><span class="sxs-lookup"><span data-stu-id="987f3-103">PidTagCorrelate Canonical Property</span></span>

  
  
<span data-ttu-id="987f3-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="987f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="987f3-105">Contient la valeur TRUE si l’expéditeur d’un message de demande de la fonctionnalité de corrélation du système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="987f3-105">Contains TRUE if the sender of a message requests the correlation feature of the messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="987f3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="987f3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="987f3-107">PR_CORRELATE</span><span class="sxs-lookup"><span data-stu-id="987f3-107">PR_CORRELATE</span></span>  <br/> |
|<span data-ttu-id="987f3-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="987f3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="987f3-109">0x0E0C</span><span class="sxs-lookup"><span data-stu-id="987f3-109">0x0E0C</span></span>  <br/> |
|<span data-ttu-id="987f3-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="987f3-110">Data type:</span></span>  <br/> |<span data-ttu-id="987f3-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="987f3-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="987f3-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="987f3-112">Area:</span></span>  <br/> |<span data-ttu-id="987f3-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="987f3-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="987f3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="987f3-114">Remarks</span></span>

<span data-ttu-id="987f3-115">Cette propriété est utilisée pour demander la corrélation de rapports entrants avec le message d’origine envoyé.</span><span class="sxs-lookup"><span data-stu-id="987f3-115">This property is used to request the correlation of incoming reports with the original sent message.</span></span> <span data-ttu-id="987f3-116">Lorsqu’un fournisseur de transport rencontre un message envoyé avec set **PR_CORRELATE** sur TRUE, il définit la propriété **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) à l’identificateur de système (MTS) de transfert de message pour le message.</span><span class="sxs-lookup"><span data-stu-id="987f3-116">When a transport provider encounters a submitted message with **PR_CORRELATE** set to TRUE, it sets the **PR_CORRELATE_MTSID** ([PidTagCorrelateMtsid](pidtagcorrelatemtsid-canonical-property.md)) property to the message transfer system (MTS) identifier for that message.</span></span>
  
 <span data-ttu-id="987f3-117">**PR_CORRELATE** doit être utilisé avec les systèmes qui prennent en charge la corrélation de messagerie par identificateur MTS, tels que X.400.</span><span class="sxs-lookup"><span data-stu-id="987f3-117">**PR_CORRELATE** should be used with messaging systems that support correlation by MTS identifier, such as X.400.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="987f3-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="987f3-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="987f3-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="987f3-119">Header files</span></span>

<span data-ttu-id="987f3-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="987f3-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="987f3-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="987f3-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="987f3-122">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="987f3-122">Mapitags.h</span></span>
  
> <span data-ttu-id="987f3-123">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="987f3-123">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="987f3-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="987f3-124">See also</span></span>



[<span data-ttu-id="987f3-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="987f3-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="987f3-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="987f3-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="987f3-127">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="987f3-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="987f3-128">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="987f3-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

