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
# <a name="pidtagstoreprovider-canonical-property"></a><span data-ttu-id="d269d-103">Propriété canonique PidTagStoreProvider</span><span class="sxs-lookup"><span data-stu-id="d269d-103">PidTagStoreProvider Canonical Property</span></span>

  
  
<span data-ttu-id="d269d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d269d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d269d-105">Contient une structure [MAPIUID](mapiuid.md) définie par un fournisseur qui indique le type de la magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="d269d-105">Contains a provider-defined [MAPIUID](mapiuid.md) structure that indicates the type of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d269d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d269d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d269d-107">PR_MDB_PROVIDER</span><span class="sxs-lookup"><span data-stu-id="d269d-107">PR_MDB_PROVIDER</span></span>  <br/> |
|<span data-ttu-id="d269d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d269d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d269d-109">0x3414</span><span class="sxs-lookup"><span data-stu-id="d269d-109">0x3414</span></span>  <br/> |
|<span data-ttu-id="d269d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d269d-110">Data type:</span></span>  <br/> |<span data-ttu-id="d269d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d269d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d269d-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d269d-112">Area:</span></span>  <br/> |<span data-ttu-id="d269d-113">Propriétés de l’ID</span><span class="sxs-lookup"><span data-stu-id="d269d-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d269d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d269d-114">Remarks</span></span>

<span data-ttu-id="d269d-115">La structure [MAPIUID](mapiuid.md) identifie le type de magasin de messages.</span><span class="sxs-lookup"><span data-stu-id="d269d-115">The [MAPIUID](mapiuid.md) structure identifies the type of message store.</span></span> <span data-ttu-id="d269d-116">La valeur est calculée par les fournisseurs de magasins de messages sur les objets de la boutique de messages et est propre à chaque fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d269d-116">The value is computed by message store providers on message store objects and is unique to each provider.</span></span> <span data-ttu-id="d269d-117">Il est généralement utilisé pour parcourir la table de la boutique de messages afin de trouver une boutique du type souhaité, par exemple des dossiers publics.</span><span class="sxs-lookup"><span data-stu-id="d269d-117">It is typically used for browsing through the message store table to find a store of the desired type, such as public folders.</span></span> 
  
<span data-ttu-id="d269d-118">Cette propriété est analogue à la propriété **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) pour les carnets d’adresses.</span><span class="sxs-lookup"><span data-stu-id="d269d-118">This property is analogous to the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property for address books.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d269d-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="d269d-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d269d-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d269d-120">Header files</span></span>

<span data-ttu-id="d269d-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d269d-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="d269d-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d269d-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="d269d-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d269d-123">Mapitags.h</span></span>
  
> <span data-ttu-id="d269d-124">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="d269d-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d269d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d269d-125">See also</span></span>



[<span data-ttu-id="d269d-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d269d-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d269d-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d269d-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d269d-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d269d-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d269d-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="d269d-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

