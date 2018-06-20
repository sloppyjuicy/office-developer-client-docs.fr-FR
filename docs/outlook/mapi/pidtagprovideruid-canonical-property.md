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
ms.openlocfilehash: 7a42a3b50cfa5630ac66cb03caac06dd7cb00e6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786458"
---
# <a name="pidtagprovideruid-canonical-property"></a><span data-ttu-id="4b749-103">Propriété canonique PidTagProviderUid</span><span class="sxs-lookup"><span data-stu-id="4b749-103">PidTagProviderUid Canonical Property</span></span>

  
  
<span data-ttu-id="4b749-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4b749-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4b749-105">Contient une structure **MAPIUID** du fournisseur de services qui gère un message.</span><span class="sxs-lookup"><span data-stu-id="4b749-105">Contains a **MAPIUID** structure of the service provider that is handling a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4b749-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4b749-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4b749-107">PR_PROVIDER_UID</span><span class="sxs-lookup"><span data-stu-id="4b749-107">PR_PROVIDER_UID</span></span>  <br/> |
|<span data-ttu-id="4b749-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="4b749-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4b749-109">0x300C</span><span class="sxs-lookup"><span data-stu-id="4b749-109">0x300C</span></span>  <br/> |
|<span data-ttu-id="4b749-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4b749-110">Data type:</span></span>  <br/> |<span data-ttu-id="4b749-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4b749-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4b749-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="4b749-112">Area:</span></span>  <br/> |<span data-ttu-id="4b749-113">MAPI courantes</span><span class="sxs-lookup"><span data-stu-id="4b749-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b749-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4b749-114">Remarks</span></span>

<span data-ttu-id="4b749-115">Cette propriété est calculée par tous les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="4b749-115">This property is computed by all service providers.</span></span> <span data-ttu-id="4b749-116">Il contient une structure [MAPIUID](mapiuid.md) associée et généralement codée en dur par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4b749-116">It contains a [MAPIUID](mapiuid.md) structure associated with, and usually hard-coded by, the provider.</span></span> <span data-ttu-id="4b749-117">Il est généralement utilisé par une application cliente qui intéresse dans uniquement les conteneurs de carnet d’adresse fournies par un fournisseur spécifique.</span><span class="sxs-lookup"><span data-stu-id="4b749-117">It is typically used by a client application that is interested in only the address book containers supplied by a particular provider.</span></span> 
  
<span data-ttu-id="4b749-118">Cette propriété s’affiche uniquement en tant qu’une entrée de la colonne dans la table fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4b749-118">This property appears only as a column entry in the provider table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4b749-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="4b749-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4b749-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="4b749-120">Header files</span></span>

<span data-ttu-id="4b749-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4b749-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="4b749-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4b749-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="4b749-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="4b749-123">Mapitags.h</span></span>
  
> <span data-ttu-id="4b749-124">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="4b749-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4b749-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b749-125">See also</span></span>



[<span data-ttu-id="4b749-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4b749-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4b749-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4b749-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4b749-128">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4b749-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4b749-129">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="4b749-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

