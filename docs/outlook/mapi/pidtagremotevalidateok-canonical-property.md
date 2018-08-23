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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 9b06ebbe8cb162d77d60cfffa866438567c84c27
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576833"
---
# <a name="pidtagremotevalidateok-canonical-property"></a><span data-ttu-id="f4039-103">Propriété canonique PidTagRemoteValidateOk</span><span class="sxs-lookup"><span data-stu-id="f4039-103">PidTagRemoteValidateOk Canonical Property</span></span>

  
  
<span data-ttu-id="f4039-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4039-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4039-105">Cette propriété contient la valeur TRUE si la visionneuse à distance est autorisée à appeler la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) .</span><span class="sxs-lookup"><span data-stu-id="f4039-105">This property contains TRUE if the remote viewer is allowed to call the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4039-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f4039-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f4039-107">PR_REMOTE_VALIDATE_OK</span><span class="sxs-lookup"><span data-stu-id="f4039-107">PR_REMOTE_VALIDATE_OK</span></span>  <br/> |
|<span data-ttu-id="f4039-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f4039-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f4039-109">0x3E0D</span><span class="sxs-lookup"><span data-stu-id="f4039-109">0x3E0D</span></span>  <br/> |
|<span data-ttu-id="f4039-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f4039-110">Data type:</span></span>  <br/> |<span data-ttu-id="f4039-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f4039-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f4039-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f4039-112">Area:</span></span>  <br/> |<span data-ttu-id="f4039-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="f4039-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f4039-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f4039-114">Remarks</span></span>

<span data-ttu-id="f4039-115">Cette propriété s’affiche dans la table d’état et permet de contrôler les performances de transport.</span><span class="sxs-lookup"><span data-stu-id="f4039-115">This property appears in the status table and offers some control over transport performance.</span></span> <span data-ttu-id="f4039-116">Il peut être considéré comme un autre moyen de diriger la visionneuse distante inactif.</span><span class="sxs-lookup"><span data-stu-id="f4039-116">It can be considered as another way of directing the remote viewer to idle.</span></span> <span data-ttu-id="f4039-117">Lorsqu’elle est définie sur TRUE, la visionneuse à distance peut appeler **IMAPIStatus::ValidateState** aussi souvent que souhaité.</span><span class="sxs-lookup"><span data-stu-id="f4039-117">When it is set to TRUE, the remote viewer can call **IMAPIStatus::ValidateState** as often as desired.</span></span> <span data-ttu-id="f4039-118">La valeur FALSE indique que la visionneuse distante ne peut pas émettre des appels plus.</span><span class="sxs-lookup"><span data-stu-id="f4039-118">A value of FALSE indicates that the remote viewer cannot make any more calls.</span></span> 
  
<span data-ttu-id="f4039-119">Le fournisseur de transport affecte généralement cette propriété dynamiquement, en définissant la valeur sur FALSE pour désactiver les appels lorsque le fournisseur de transport a suffisamment de traitement à exécuter.</span><span class="sxs-lookup"><span data-stu-id="f4039-119">The transport provider usually sets this property dynamically, by setting the value to FALSE to disable additional calls when the transport provider has a sufficient amount of processing to perform.</span></span> <span data-ttu-id="f4039-120">Lorsque le fournisseur de transport est terminé, il définit la valeur sur TRUE pour autoriser l’application cliente à effectuer d’autres appels **IMAPIStatus::ValidateState** .</span><span class="sxs-lookup"><span data-stu-id="f4039-120">When the transport provider is done, it then sets the value to TRUE to allow the client application to make further **IMAPIStatus::ValidateState** calls.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f4039-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f4039-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f4039-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f4039-122">Header files</span></span>

<span data-ttu-id="f4039-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4039-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f4039-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f4039-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f4039-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="f4039-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f4039-126">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="f4039-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f4039-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4039-127">See also</span></span>



[<span data-ttu-id="f4039-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f4039-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f4039-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f4039-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f4039-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f4039-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f4039-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f4039-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

