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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8b5c9e5bb2aa915d4b76d9998baaf504e7929b78
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424223"
---
# <a name="pidtagremotevalidateok-canonical-property"></a><span data-ttu-id="af302-103">Propriété canonique PidTagRemoteValidateOk</span><span class="sxs-lookup"><span data-stu-id="af302-103">PidTagRemoteValidateOk Canonical Property</span></span>

  
  
<span data-ttu-id="af302-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af302-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af302-105">Cette propriété contient TRUE si la visionneuse distante est autorisée à appeler la méthode [IMAPIStatus::ValidateState.](imapistatus-validatestate.md)</span><span class="sxs-lookup"><span data-stu-id="af302-105">This property contains TRUE if the remote viewer is allowed to call the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="af302-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="af302-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="af302-107">PR_REMOTE_VALIDATE_OK</span><span class="sxs-lookup"><span data-stu-id="af302-107">PR_REMOTE_VALIDATE_OK</span></span>  <br/> |
|<span data-ttu-id="af302-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="af302-108">Identifier:</span></span>  <br/> |<span data-ttu-id="af302-109">0x3E0D</span><span class="sxs-lookup"><span data-stu-id="af302-109">0x3E0D</span></span>  <br/> |
|<span data-ttu-id="af302-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="af302-110">Data type:</span></span>  <br/> |<span data-ttu-id="af302-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="af302-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="af302-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="af302-112">Area:</span></span>  <br/> |<span data-ttu-id="af302-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="af302-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af302-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="af302-114">Remarks</span></span>

<span data-ttu-id="af302-115">Cette propriété apparaît dans le tableau d’état et offre un certain contrôle sur les performances de transport.</span><span class="sxs-lookup"><span data-stu-id="af302-115">This property appears in the status table and offers some control over transport performance.</span></span> <span data-ttu-id="af302-116">Il peut être considéré comme un autre moyen de diriger la visionneuse à distance vers l’inactivité.</span><span class="sxs-lookup"><span data-stu-id="af302-116">It can be considered as another way of directing the remote viewer to idle.</span></span> <span data-ttu-id="af302-117">Lorsqu’elle est définie sur TRUE, la visionneuse distante peut appeler **IMAPIStatus::ValidateState** aussi souvent que vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="af302-117">When it is set to TRUE, the remote viewer can call **IMAPIStatus::ValidateState** as often as desired.</span></span> <span data-ttu-id="af302-118">La valeur FALSE indique que la visionneuse distante ne peut plus effectuer d’appels.</span><span class="sxs-lookup"><span data-stu-id="af302-118">A value of FALSE indicates that the remote viewer cannot make any more calls.</span></span> 
  
<span data-ttu-id="af302-119">En règle générale, le fournisseur de transport définit cette propriété dynamiquement, en lui activant la valeur FALSE pour désactiver les appels supplémentaires lorsque le fournisseur de transport dispose d’un volume de traitement suffisant.</span><span class="sxs-lookup"><span data-stu-id="af302-119">The transport provider usually sets this property dynamically, by setting the value to FALSE to disable additional calls when the transport provider has a sufficient amount of processing to perform.</span></span> <span data-ttu-id="af302-120">Une fois le fournisseur de transport terminé, il définit la valeur sur TRUE pour permettre à l’application cliente d’effectuer d’autres **appels IMAPIStatus::ValidateState.**</span><span class="sxs-lookup"><span data-stu-id="af302-120">When the transport provider is done, it then sets the value to TRUE to allow the client application to make further **IMAPIStatus::ValidateState** calls.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="af302-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="af302-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="af302-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="af302-122">Header files</span></span>

<span data-ttu-id="af302-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="af302-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="af302-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="af302-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="af302-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="af302-125">Mapitags.h</span></span>
  
> <span data-ttu-id="af302-126">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="af302-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af302-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af302-127">See also</span></span>



[<span data-ttu-id="af302-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="af302-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af302-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="af302-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af302-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="af302-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af302-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="af302-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

