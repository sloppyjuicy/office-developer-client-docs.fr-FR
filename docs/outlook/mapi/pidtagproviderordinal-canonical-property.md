---
title: Propriété canonique PidTagProviderOrdinal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderOrdinal
api_type:
- COM
ms.assetid: d062b54d-7c32-4369-ab69-f7193773a1c0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fbeb63bbae23f8f7f78c92d3abed6bea1c3ac85d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286438"
---
# <a name="pidtagproviderordinal-canonical-property"></a><span data-ttu-id="e0783-103">Propriété canonique PidTagProviderOrdinal</span><span class="sxs-lookup"><span data-stu-id="e0783-103">PidTagProviderOrdinal Canonical Property</span></span>

  
  
<span data-ttu-id="e0783-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0783-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0783-105">Contient l'index de base zéro de la position d'un fournisseur de services dans la table des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="e0783-105">Contains the zero-based index of a service provider's position in the provider table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e0783-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e0783-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e0783-107">PR_PROVIDER_ORDINAL</span><span class="sxs-lookup"><span data-stu-id="e0783-107">PR_PROVIDER_ORDINAL</span></span>  <br/> |
|<span data-ttu-id="e0783-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="e0783-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e0783-109">0x300D</span><span class="sxs-lookup"><span data-stu-id="e0783-109">0x300D</span></span>  <br/> |
|<span data-ttu-id="e0783-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e0783-110">Data type:</span></span>  <br/> |<span data-ttu-id="e0783-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e0783-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e0783-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e0783-112">Area:</span></span>  <br/> |<span data-ttu-id="e0783-113">MAPI commun</span><span class="sxs-lookup"><span data-stu-id="e0783-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0783-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e0783-114">Remarks</span></span>

<span data-ttu-id="e0783-115">Cette propriété est calculée par MAPI.</span><span class="sxs-lookup"><span data-stu-id="e0783-115">This property is computed by MAPI.</span></span>
  
<span data-ttu-id="e0783-116">Obtenez la table du fournisseur en appelant la méthode [IMsgServiceAdmin:: GetProviderTable](imsgserviceadmin-getprovidertable.md) .</span><span class="sxs-lookup"><span data-stu-id="e0783-116">Obtain the provider table by calling the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="e0783-117">Triez la table des fournisseurs sur cette propriété pour afficher l'ordre de transport.</span><span class="sxs-lookup"><span data-stu-id="e0783-117">Sort the provider table on this property to display the transport order.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e0783-118">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="e0783-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e0783-119">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="e0783-119">Header files</span></span>

<span data-ttu-id="e0783-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e0783-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="e0783-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e0783-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="e0783-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e0783-122">Mapitags.h</span></span>
  
> <span data-ttu-id="e0783-123">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="e0783-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e0783-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0783-124">See also</span></span>



[<span data-ttu-id="e0783-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e0783-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e0783-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e0783-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e0783-127">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e0783-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e0783-128">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e0783-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

