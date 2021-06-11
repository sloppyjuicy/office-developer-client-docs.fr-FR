---
title: Propriété canonique PidTagAbProviderId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagAbProviderId
api_type:
- HeaderDef
ms.assetid: 23cfd1d0-8e9d-4508-93dd-a88c0ef77c51
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 820df61ec23e2dd1459582e5a7bb35ad9525e0b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422242"
---
# <a name="pidtagabproviderid-canonical-property"></a><span data-ttu-id="5e09d-103">Propriété canonique PidTagAbProviderId</span><span class="sxs-lookup"><span data-stu-id="5e09d-103">PidTagAbProviderId Canonical Property</span></span>

  
  
<span data-ttu-id="5e09d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e09d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e09d-105">Contient la structure [MAPIUID](mapiuid.md) d’un fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="5e09d-105">Contains an address book provider's [MAPIUID](mapiuid.md) structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5e09d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5e09d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5e09d-107">PR_AB_PROVIDER_ID</span><span class="sxs-lookup"><span data-stu-id="5e09d-107">PR_AB_PROVIDER_ID</span></span>  <br/> |
|<span data-ttu-id="5e09d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5e09d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5e09d-109">0x3615</span><span class="sxs-lookup"><span data-stu-id="5e09d-109">0x3615</span></span>  <br/> |
|<span data-ttu-id="5e09d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5e09d-110">Data type:</span></span>  <br/> |<span data-ttu-id="5e09d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5e09d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5e09d-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5e09d-112">Area:</span></span>  <br/> |<span data-ttu-id="5e09d-113">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="5e09d-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e09d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5e09d-114">Remarks</span></span>

<span data-ttu-id="5e09d-115">La structure **MAPIUID** identifie le fournisseur de carnet d’adresses qui fournit ce conteneur particulier dans la hiérarchie de conteneurs.</span><span class="sxs-lookup"><span data-stu-id="5e09d-115">The **MAPIUID** structure identifies which address book provider supplies this particular container in the container hierarchy.</span></span> <span data-ttu-id="5e09d-116">La valeur est propre à chaque fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5e09d-116">The value is unique to each provider.</span></span> 
  
<span data-ttu-id="5e09d-117">Un fournisseur de carnet d’adresses peut fournir plusieurs identificateurs.</span><span class="sxs-lookup"><span data-stu-id="5e09d-117">An address book provider can provide more than one identifier.</span></span> <span data-ttu-id="5e09d-118">Par exemple, un fournisseur qui fournit  deux conteneurs différents peut publier dans PR_AB_PROVIDER_ID identificateurs uniques pour chaque conteneur.</span><span class="sxs-lookup"><span data-stu-id="5e09d-118">For example, a provider that supplies two different containers can publish in **PR_AB_PROVIDER_ID** unique identifiers for each container.</span></span> 
  
 <span data-ttu-id="5e09d-119">**PR_AB_PROVIDER_ID** est analogue à la propriété **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) pour les magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="5e09d-119">**PR_AB_PROVIDER_ID** is analogous to the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for message stores.</span></span> <span data-ttu-id="5e09d-120">Les applications clientes peuvent **utiliser PR_AB_PROVIDER_ID** pour rechercher des lignes associées dans une table de hiérarchie de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="5e09d-120">Client applications can use **PR_AB_PROVIDER_ID** to find related rows in an address book hierarchy table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5e09d-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5e09d-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="5e09d-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5e09d-122">Header files</span></span>

<span data-ttu-id="5e09d-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5e09d-123">Mapitags.h</span></span>
  
> <span data-ttu-id="5e09d-124">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="5e09d-124">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="5e09d-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5e09d-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="5e09d-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5e09d-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e09d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e09d-127">See also</span></span>



[<span data-ttu-id="5e09d-128">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="5e09d-128">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="5e09d-129">Propriété canonique PidTagStoreProvider</span><span class="sxs-lookup"><span data-stu-id="5e09d-129">PidTagStoreProvider Canonical Property</span></span>](pidtagstoreprovider-canonical-property.md)


[<span data-ttu-id="5e09d-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5e09d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5e09d-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5e09d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5e09d-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5e09d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

