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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 02d2c30fede7e554910a1bedb01b79c488447bb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595355"
---
# <a name="pidtagstoreprovider-canonical-property"></a><span data-ttu-id="282a6-103">Propriété canonique PidTagStoreProvider</span><span class="sxs-lookup"><span data-stu-id="282a6-103">PidTagStoreProvider Canonical Property</span></span>

  
  
<span data-ttu-id="282a6-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="282a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="282a6-105">Contient une structure [MAPIUID](mapiuid.md) défini par le fournisseur qui indique le type de la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="282a6-105">Contains a provider-defined [MAPIUID](mapiuid.md) structure that indicates the type of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="282a6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="282a6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="282a6-107">PR_MDB_PROVIDER</span><span class="sxs-lookup"><span data-stu-id="282a6-107">PR_MDB_PROVIDER</span></span>  <br/> |
|<span data-ttu-id="282a6-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="282a6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="282a6-109">0x3414</span><span class="sxs-lookup"><span data-stu-id="282a6-109">0x3414</span></span>  <br/> |
|<span data-ttu-id="282a6-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="282a6-110">Data type:</span></span>  <br/> |<span data-ttu-id="282a6-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="282a6-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="282a6-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="282a6-112">Area:</span></span>  <br/> |<span data-ttu-id="282a6-113">Propriétés ID</span><span class="sxs-lookup"><span data-stu-id="282a6-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="282a6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="282a6-114">Remarks</span></span>

<span data-ttu-id="282a6-115">La structure [MAPIUID](mapiuid.md) identifie le type de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="282a6-115">The [MAPIUID](mapiuid.md) structure identifies the type of message store.</span></span> <span data-ttu-id="282a6-116">La valeur est calculée par les fournisseurs de banque de messages sur des objets de banque de messages et est unique pour chaque fournisseur.</span><span class="sxs-lookup"><span data-stu-id="282a6-116">The value is computed by message store providers on message store objects and is unique to each provider.</span></span> <span data-ttu-id="282a6-117">Il est généralement utilisé pour la navigation par le biais de la table de banque de messages pour rechercher un magasin du type souhaité, tels que les dossiers publics.</span><span class="sxs-lookup"><span data-stu-id="282a6-117">It is typically used for browsing through the message store table to find a store of the desired type, such as public folders.</span></span> 
  
<span data-ttu-id="282a6-118">Cette propriété correspond à la propriété **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) pour les carnets d’adresses.</span><span class="sxs-lookup"><span data-stu-id="282a6-118">This property is analogous to the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property for address books.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="282a6-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="282a6-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="282a6-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="282a6-120">Header files</span></span>

<span data-ttu-id="282a6-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="282a6-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="282a6-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="282a6-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="282a6-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="282a6-123">Mapitags.h</span></span>
  
> <span data-ttu-id="282a6-124">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="282a6-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="282a6-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="282a6-125">See also</span></span>



[<span data-ttu-id="282a6-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="282a6-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="282a6-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="282a6-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="282a6-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="282a6-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="282a6-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="282a6-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

