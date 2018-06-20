---
title: Propriété canonique PidTagContentCorrelator
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentCorrelator
api_type:
- HeaderDef
ms.assetid: 0bf78879-2f9f-4c29-b1f4-2f4882d8464d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2290e6751778f17defc8d1007ff62c88f1b75465
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785847"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a><span data-ttu-id="1647f-103">Propriété canonique PidTagContentCorrelator</span><span class="sxs-lookup"><span data-stu-id="1647f-103">PidTagContentCorrelator Canonical Property</span></span>

  
  
<span data-ttu-id="1647f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1647f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1647f-105">Contient une valeur de que l’expéditeur du message peut utiliser pour correspondre à un rapport avec le message d’origine.</span><span class="sxs-lookup"><span data-stu-id="1647f-105">Contains a value the message sender can use to match a report with the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1647f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1647f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1647f-107">PR_CONTENT_CORRELATOR</span><span class="sxs-lookup"><span data-stu-id="1647f-107">PR_CONTENT_CORRELATOR</span></span>  <br/> |
|<span data-ttu-id="1647f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1647f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1647f-109">0 x 0007</span><span class="sxs-lookup"><span data-stu-id="1647f-109">0x0007</span></span>  <br/> |
|<span data-ttu-id="1647f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1647f-110">Data type:</span></span>  <br/> |<span data-ttu-id="1647f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1647f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1647f-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="1647f-112">Area:</span></span>  <br/> |<span data-ttu-id="1647f-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="1647f-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1647f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1647f-114">Remarks</span></span>

<span data-ttu-id="1647f-115">Le contenu de la chaîne binaire est défini par l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="1647f-115">The contents of the binary string are defined by the message originator.</span></span> <span data-ttu-id="1647f-116">Si défini sur un message sortant, cette propriété doit être copié sur tous les rapports générés en réponse au message.</span><span class="sxs-lookup"><span data-stu-id="1647f-116">If set on an outgoing message, this property should be copied onto any reports generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1647f-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1647f-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1647f-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1647f-118">Header files</span></span>

<span data-ttu-id="1647f-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1647f-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="1647f-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1647f-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="1647f-121">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="1647f-121">Mapitags.h</span></span>
  
> <span data-ttu-id="1647f-122">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="1647f-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1647f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1647f-123">See also</span></span>



[<span data-ttu-id="1647f-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1647f-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1647f-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1647f-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1647f-126">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1647f-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1647f-127">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="1647f-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

