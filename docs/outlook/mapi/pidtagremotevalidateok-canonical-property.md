---
title: Propriété canonique PidTagRemoteValidateOk
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteValidateOk
api_type:
- COM
ms.assetid: e336d2ec-57cb-4d08-bd6e-330ef7d9939e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d8d986554352e05398a843723ee802bb4969e5ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786573"
---
# <a name="pidtagremotevalidateok-canonical-property"></a><span data-ttu-id="9ef87-103">Propriété canonique PidTagRemoteValidateOk</span><span class="sxs-lookup"><span data-stu-id="9ef87-103">PidTagRemoteValidateOk Canonical Property</span></span>

  
  
<span data-ttu-id="9ef87-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9ef87-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9ef87-105">Cette propriété contient la valeur TRUE si la visionneuse à distance est autorisée à appeler la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="9ef87-105">This property contains TRUE if the remote viewer is allowed to call the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ef87-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9ef87-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9ef87-107">PR_REMOTE_VALIDATE_OK</span><span class="sxs-lookup"><span data-stu-id="9ef87-107">PR_REMOTE_VALIDATE_OK</span></span>  <br/> |
|<span data-ttu-id="9ef87-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9ef87-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9ef87-109">0x3E0D</span><span class="sxs-lookup"><span data-stu-id="9ef87-109">0x3E0D</span></span>  <br/> |
|<span data-ttu-id="9ef87-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9ef87-110">Data type:</span></span>  <br/> |<span data-ttu-id="9ef87-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="9ef87-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="9ef87-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="9ef87-112">Area:</span></span>  <br/> |<span data-ttu-id="9ef87-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="9ef87-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ef87-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9ef87-114">Remarks</span></span>

<span data-ttu-id="9ef87-115">Cette propriété s’affiche dans la table d’état et permet de contrôler les performances de transport.</span><span class="sxs-lookup"><span data-stu-id="9ef87-115">This property appears in the status table and offers some control over transport performance.</span></span> <span data-ttu-id="9ef87-116">Il peut être considéré comme un autre moyen de diriger la visionneuse distante inactif.</span><span class="sxs-lookup"><span data-stu-id="9ef87-116">It can be considered as another way of directing the remote viewer to idle.</span></span> <span data-ttu-id="9ef87-117">Lorsqu’elle est définie sur TRUE, la visionneuse à distance peut appeler **IMAPIStatus::ValidateState** aussi souvent que souhaité.</span><span class="sxs-lookup"><span data-stu-id="9ef87-117">When it is set to TRUE, the remote viewer can call **IMAPIStatus::ValidateState** as often as desired.</span></span> <span data-ttu-id="9ef87-118">La valeur FALSE indique que la visionneuse distante ne peut pas émettre des appels plus.</span><span class="sxs-lookup"><span data-stu-id="9ef87-118">A value of FALSE indicates that the remote viewer cannot make any more calls.</span></span> 
  
<span data-ttu-id="9ef87-119">Le fournisseur de transport affecte généralement cette propriété dynamiquement, en définissant la valeur sur FALSE pour désactiver les appels lorsque le fournisseur de transport a suffisamment de traitement à exécuter.</span><span class="sxs-lookup"><span data-stu-id="9ef87-119">The transport provider usually sets this property dynamically, by setting the value to FALSE to disable additional calls when the transport provider has a sufficient amount of processing to perform.</span></span> <span data-ttu-id="9ef87-120">Lorsque le fournisseur de transport est terminé, il définit la valeur sur TRUE pour autoriser l’application cliente à effectuer d’autres appels **IMAPIStatus::ValidateState** .</span><span class="sxs-lookup"><span data-stu-id="9ef87-120">When the transport provider is done, it then sets the value to TRUE to allow the client application to make further **IMAPIStatus::ValidateState** calls.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="9ef87-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9ef87-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9ef87-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="9ef87-122">Header files</span></span>

<span data-ttu-id="9ef87-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9ef87-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="9ef87-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9ef87-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="9ef87-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="9ef87-125">Mapitags.h</span></span>
  
> <span data-ttu-id="9ef87-126">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="9ef87-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ef87-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ef87-127">See also</span></span>



[<span data-ttu-id="9ef87-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9ef87-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9ef87-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9ef87-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9ef87-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9ef87-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9ef87-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="9ef87-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

