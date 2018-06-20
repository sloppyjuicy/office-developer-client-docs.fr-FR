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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b634f815d2aedecc716227c6525b846db38ca869
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786839"
---
# <a name="pidtagstoreprovider-canonical-property"></a><span data-ttu-id="f19a1-103">Propriété canonique PidTagStoreProvider</span><span class="sxs-lookup"><span data-stu-id="f19a1-103">PidTagStoreProvider Canonical Property</span></span>

  
  
<span data-ttu-id="f19a1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f19a1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f19a1-105">Contient une structure [MAPIUID](mapiuid.md) défini par le fournisseur qui indique le type de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f19a1-105">Contains a provider-defined [MAPIUID](mapiuid.md) structure that indicates the type of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f19a1-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f19a1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f19a1-107">PR_MDB_PROVIDER</span><span class="sxs-lookup"><span data-stu-id="f19a1-107">PR_MDB_PROVIDER</span></span>  <br/> |
|<span data-ttu-id="f19a1-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f19a1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f19a1-109">0x3414</span><span class="sxs-lookup"><span data-stu-id="f19a1-109">0x3414</span></span>  <br/> |
|<span data-ttu-id="f19a1-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f19a1-110">Data type:</span></span>  <br/> |<span data-ttu-id="f19a1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f19a1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f19a1-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="f19a1-112">Area:</span></span>  <br/> |<span data-ttu-id="f19a1-113">Propriétés ID</span><span class="sxs-lookup"><span data-stu-id="f19a1-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f19a1-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f19a1-114">Remarks</span></span>

<span data-ttu-id="f19a1-115">La structure [MAPIUID](mapiuid.md) identifie le type de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="f19a1-115">The [MAPIUID](mapiuid.md) structure identifies the type of message store.</span></span> <span data-ttu-id="f19a1-116">La valeur est calculée par les fournisseurs de banque de messages sur des objets de banque de messages et est unique pour chaque fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f19a1-116">The value is computed by message store providers on message store objects and is unique to each provider.</span></span> <span data-ttu-id="f19a1-117">Il est généralement utilisé pour la navigation par le biais de la table de banque de messages pour rechercher un magasin du type souhaité, tels que les dossiers publics.</span><span class="sxs-lookup"><span data-stu-id="f19a1-117">It is typically used for browsing through the message store table to find a store of the desired type, such as public folders.</span></span> 
  
<span data-ttu-id="f19a1-118">Cette propriété correspond à la propriété **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) pour les carnets d’adresses.</span><span class="sxs-lookup"><span data-stu-id="f19a1-118">This property is analogous to the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property for address books.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f19a1-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f19a1-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f19a1-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f19a1-120">Header files</span></span>

<span data-ttu-id="f19a1-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f19a1-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="f19a1-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f19a1-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="f19a1-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="f19a1-123">Mapitags.h</span></span>
  
> <span data-ttu-id="f19a1-124">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="f19a1-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f19a1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f19a1-125">See also</span></span>



[<span data-ttu-id="f19a1-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f19a1-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f19a1-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f19a1-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f19a1-128">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f19a1-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f19a1-129">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="f19a1-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

