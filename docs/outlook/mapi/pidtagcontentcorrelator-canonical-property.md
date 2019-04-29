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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 96e0e3152a70eb2913c4559afd99e25adff48ca9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438525"
---
# <a name="pidtagcontentcorrelator-canonical-property"></a><span data-ttu-id="05133-103">Propriété canonique PidTagContentCorrelator</span><span class="sxs-lookup"><span data-stu-id="05133-103">PidTagContentCorrelator Canonical Property</span></span>

  
  
<span data-ttu-id="05133-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05133-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05133-105">Contient une valeur que l'expéditeur du message peut utiliser pour faire correspondre un rapport avec le message d'origine.</span><span class="sxs-lookup"><span data-stu-id="05133-105">Contains a value the message sender can use to match a report with the original message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="05133-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="05133-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="05133-107">PR_CONTENT_CORRELATOR</span><span class="sxs-lookup"><span data-stu-id="05133-107">PR_CONTENT_CORRELATOR</span></span>  <br/> |
|<span data-ttu-id="05133-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="05133-108">Identifier:</span></span>  <br/> |<span data-ttu-id="05133-109">0x0007</span><span class="sxs-lookup"><span data-stu-id="05133-109">0x0007</span></span>  <br/> |
|<span data-ttu-id="05133-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="05133-110">Data type:</span></span>  <br/> |<span data-ttu-id="05133-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="05133-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="05133-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="05133-112">Area:</span></span>  <br/> |<span data-ttu-id="05133-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="05133-113">Exchange</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05133-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="05133-114">Remarks</span></span>

<span data-ttu-id="05133-115">Le contenu de la chaîne binaire est défini par l'expéditeur du message.</span><span class="sxs-lookup"><span data-stu-id="05133-115">The contents of the binary string are defined by the message originator.</span></span> <span data-ttu-id="05133-116">Si elle est définie sur un message sortant, cette propriété doit être copiée sur tous les rapports générés en réponse au message.</span><span class="sxs-lookup"><span data-stu-id="05133-116">If set on an outgoing message, this property should be copied onto any reports generated in response to the message.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="05133-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="05133-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="05133-118">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="05133-118">Header files</span></span>

<span data-ttu-id="05133-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="05133-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="05133-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="05133-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="05133-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="05133-121">Mapitags.h</span></span>
  
> <span data-ttu-id="05133-122">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="05133-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="05133-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05133-123">See also</span></span>



[<span data-ttu-id="05133-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="05133-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="05133-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="05133-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="05133-126">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="05133-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="05133-127">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="05133-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

