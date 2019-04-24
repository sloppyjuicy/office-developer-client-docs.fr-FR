---
title: Propriété canonique PidTagProviderUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderUid
api_type:
- COM
ms.assetid: 993f5bca-58a6-455d-8a25-6e08b441ad31
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0d79075ea1db451e0c3d327df9a662e5032ebb22
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286414"
---
# <a name="pidtagprovideruid-canonical-property"></a><span data-ttu-id="27296-103">Propriété canonique PidTagProviderUid</span><span class="sxs-lookup"><span data-stu-id="27296-103">PidTagProviderUid Canonical Property</span></span>

  
  
<span data-ttu-id="27296-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27296-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27296-105">Contient une structure **MAPIUID** du fournisseur de services qui gère un message.</span><span class="sxs-lookup"><span data-stu-id="27296-105">Contains a **MAPIUID** structure of the service provider that is handling a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27296-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="27296-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27296-107">PR_PROVIDER_UID</span><span class="sxs-lookup"><span data-stu-id="27296-107">PR_PROVIDER_UID</span></span>  <br/> |
|<span data-ttu-id="27296-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="27296-108">Identifier:</span></span>  <br/> |<span data-ttu-id="27296-109">0x300C</span><span class="sxs-lookup"><span data-stu-id="27296-109">0x300C</span></span>  <br/> |
|<span data-ttu-id="27296-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="27296-110">Data type:</span></span>  <br/> |<span data-ttu-id="27296-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="27296-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="27296-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="27296-112">Area:</span></span>  <br/> |<span data-ttu-id="27296-113">MAPI commun</span><span class="sxs-lookup"><span data-stu-id="27296-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27296-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="27296-114">Remarks</span></span>

<span data-ttu-id="27296-115">Cette propriété est calculée par tous les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="27296-115">This property is computed by all service providers.</span></span> <span data-ttu-id="27296-116">Elle contient une structure [MAPIUID](mapiuid.md) associée à, généralement codée en dur par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="27296-116">It contains a [MAPIUID](mapiuid.md) structure associated with, and usually hard-coded by, the provider.</span></span> <span data-ttu-id="27296-117">Elle est généralement utilisée par une application cliente qui est intéressée uniquement par les conteneurs de carnet d'adresses fournis par un fournisseur particulier.</span><span class="sxs-lookup"><span data-stu-id="27296-117">It is typically used by a client application that is interested in only the address book containers supplied by a particular provider.</span></span> 
  
<span data-ttu-id="27296-118">Cette propriété apparaît uniquement sous la forme d'une entrée de colonne dans la table des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="27296-118">This property appears only as a column entry in the provider table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="27296-119">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="27296-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="27296-120">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="27296-120">Header files</span></span>

<span data-ttu-id="27296-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="27296-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="27296-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="27296-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="27296-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="27296-123">Mapitags.h</span></span>
  
> <span data-ttu-id="27296-124">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="27296-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27296-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27296-125">See also</span></span>



[<span data-ttu-id="27296-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="27296-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27296-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="27296-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27296-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="27296-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27296-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="27296-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

