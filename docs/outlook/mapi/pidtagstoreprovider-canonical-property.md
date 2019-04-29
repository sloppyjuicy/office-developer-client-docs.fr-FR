---
title: Propriété canonique PidTagStoreProvider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreProvider
api_type:
- COM
ms.assetid: 6f6cc66f-a08e-4f8e-b33a-d3674319248e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6266c9293f54ce764c5b5b0e41d43767490abcf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412050"
---
# <a name="pidtagstoreprovider-canonical-property"></a><span data-ttu-id="d7f33-103">Propriété canonique PidTagStoreProvider</span><span class="sxs-lookup"><span data-stu-id="d7f33-103">PidTagStoreProvider Canonical Property</span></span>

  
  
<span data-ttu-id="d7f33-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7f33-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7f33-105">Contient une structure [MAPIUID](mapiuid.md) définie par le fournisseur qui indique le type de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="d7f33-105">Contains a provider-defined [MAPIUID](mapiuid.md) structure that indicates the type of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d7f33-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d7f33-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d7f33-107">PR_MDB_PROVIDER</span><span class="sxs-lookup"><span data-stu-id="d7f33-107">PR_MDB_PROVIDER</span></span>  <br/> |
|<span data-ttu-id="d7f33-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d7f33-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d7f33-109">0x3414</span><span class="sxs-lookup"><span data-stu-id="d7f33-109">0x3414</span></span>  <br/> |
|<span data-ttu-id="d7f33-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d7f33-110">Data type:</span></span>  <br/> |<span data-ttu-id="d7f33-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d7f33-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d7f33-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d7f33-112">Area:</span></span>  <br/> |<span data-ttu-id="d7f33-113">Propriétés ID</span><span class="sxs-lookup"><span data-stu-id="d7f33-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7f33-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d7f33-114">Remarks</span></span>

<span data-ttu-id="d7f33-115">La structure [MAPIUID](mapiuid.md) identifie le type de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="d7f33-115">The [MAPIUID](mapiuid.md) structure identifies the type of message store.</span></span> <span data-ttu-id="d7f33-116">La valeur est calculée par les fournisseurs de banque de messages sur les objets de banque de messages et est unique pour chaque fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d7f33-116">The value is computed by message store providers on message store objects and is unique to each provider.</span></span> <span data-ttu-id="d7f33-117">Il est généralement utilisé pour parcourir la table de banque de messages afin de trouver une banque du type souhaité, comme des dossiers publics.</span><span class="sxs-lookup"><span data-stu-id="d7f33-117">It is typically used for browsing through the message store table to find a store of the desired type, such as public folders.</span></span> 
  
<span data-ttu-id="d7f33-118">Cette propriété est analogue à la propriété **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) pour les carnets d'adresses.</span><span class="sxs-lookup"><span data-stu-id="d7f33-118">This property is analogous to the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property for address books.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d7f33-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d7f33-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d7f33-120">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="d7f33-120">Header files</span></span>

<span data-ttu-id="d7f33-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d7f33-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="d7f33-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d7f33-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="d7f33-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="d7f33-123">Mapitags.h</span></span>
  
> <span data-ttu-id="d7f33-124">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="d7f33-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d7f33-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7f33-125">See also</span></span>



[<span data-ttu-id="d7f33-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d7f33-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d7f33-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d7f33-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d7f33-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d7f33-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d7f33-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="d7f33-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

