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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 6398acf71e62157cf5a6eb7e6caf22130fa9f9d0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568804"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a><span data-ttu-id="5c3bd-103">Propriété canonique PidTagContentCorrelator</span><span class="sxs-lookup"><span data-stu-id="5c3bd-103">PidTagContentCorrelator Canonical Property</span></span>

  
  
<span data-ttu-id="5c3bd-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c3bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c3bd-105">Contient une valeur de que l’expéditeur du message peut utiliser pour correspondre à un rapport avec le message d’origine.</span><span class="sxs-lookup"><span data-stu-id="5c3bd-105">Contains a value the message sender can use to match a report with the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5c3bd-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5c3bd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5c3bd-107">PR_CONTENT_CORRELATOR</span><span class="sxs-lookup"><span data-stu-id="5c3bd-107">PR_CONTENT_CORRELATOR</span></span>  <br/> |
|<span data-ttu-id="5c3bd-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5c3bd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5c3bd-109">0 x 0007</span><span class="sxs-lookup"><span data-stu-id="5c3bd-109">0x0007</span></span>  <br/> |
|<span data-ttu-id="5c3bd-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5c3bd-110">Data type:</span></span>  <br/> |<span data-ttu-id="5c3bd-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5c3bd-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5c3bd-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5c3bd-112">Area:</span></span>  <br/> |<span data-ttu-id="5c3bd-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="5c3bd-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c3bd-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5c3bd-114">Remarks</span></span>

<span data-ttu-id="5c3bd-115">Le contenu de la chaîne binaire est défini par l’expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="5c3bd-115">The contents of the binary string are defined by the message originator.</span></span> <span data-ttu-id="5c3bd-116">Si défini sur un message sortant, cette propriété doit être copié sur tous les rapports générés en réponse au message.</span><span class="sxs-lookup"><span data-stu-id="5c3bd-116">If set on an outgoing message, this property should be copied onto any reports generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="5c3bd-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5c3bd-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5c3bd-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5c3bd-118">Header files</span></span>

<span data-ttu-id="5c3bd-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5c3bd-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="5c3bd-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5c3bd-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="5c3bd-121">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="5c3bd-121">Mapitags.h</span></span>
  
> <span data-ttu-id="5c3bd-122">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="5c3bd-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c3bd-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c3bd-123">See also</span></span>



[<span data-ttu-id="5c3bd-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5c3bd-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5c3bd-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5c3bd-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5c3bd-126">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5c3bd-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5c3bd-127">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5c3bd-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

