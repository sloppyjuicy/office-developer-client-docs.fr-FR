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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 84a2d5517d405ac6deb61f7c4679d6816e802404
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785647"
---
# <a name="pidtagabproviderid-canonical-property"></a><span data-ttu-id="835e9-103">Propriété canonique PidTagAbProviderId</span><span class="sxs-lookup"><span data-stu-id="835e9-103">PidTagAbProviderId Canonical Property</span></span>

  
  
<span data-ttu-id="835e9-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="835e9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="835e9-105">Contient la structure [MAPIUID](mapiuid.md) d’un fournisseur de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="835e9-105">Contains an address book provider's [MAPIUID](mapiuid.md) structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="835e9-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="835e9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="835e9-107">PR_AB_PROVIDER_ID</span><span class="sxs-lookup"><span data-stu-id="835e9-107">PR_AB_PROVIDER_ID</span></span>  <br/> |
|<span data-ttu-id="835e9-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="835e9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="835e9-109">0x3615</span><span class="sxs-lookup"><span data-stu-id="835e9-109">0x3615</span></span>  <br/> |
|<span data-ttu-id="835e9-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="835e9-110">Data type:</span></span>  <br/> |<span data-ttu-id="835e9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="835e9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="835e9-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="835e9-112">Area:</span></span>  <br/> |<span data-ttu-id="835e9-113">Carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="835e9-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="835e9-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="835e9-114">Remarks</span></span>

<span data-ttu-id="835e9-115">La structure **MAPIUID** identifie le fournisseur de carnet d’adresses fournit ce conteneur particulier dans la hiérarchie des conteneurs.</span><span class="sxs-lookup"><span data-stu-id="835e9-115">The **MAPIUID** structure identifies which address book provider supplies this particular container in the container hierarchy.</span></span> <span data-ttu-id="835e9-116">La valeur est unique pour chaque fournisseur.</span><span class="sxs-lookup"><span data-stu-id="835e9-116">The value is unique to each provider.</span></span> 
  
<span data-ttu-id="835e9-117">Un fournisseur de carnet d’adresses peut fournir plusieurs identificateurs.</span><span class="sxs-lookup"><span data-stu-id="835e9-117">An address book provider can provide more than one identifier.</span></span> <span data-ttu-id="835e9-118">Par exemple, un fournisseur qui fournit deux différents conteneurs peut publier dans **PR_AB_PROVIDER_ID** des identificateurs uniques pour chaque conteneur.</span><span class="sxs-lookup"><span data-stu-id="835e9-118">For example, a provider that supplies two different containers can publish in **PR_AB_PROVIDER_ID** unique identifiers for each container.</span></span> 
  
 <span data-ttu-id="835e9-119">**PR_AB_PROVIDER_ID** correspond à la propriété **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) pour les banques de messages.</span><span class="sxs-lookup"><span data-stu-id="835e9-119">**PR_AB_PROVIDER_ID** is analogous to the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for message stores.</span></span> <span data-ttu-id="835e9-120">Les applications de client peuvent utiliser **PR_AB_PROVIDER_ID** pour rechercher des lignes dans une table de hiérarchie adresse téléchargeable.</span><span class="sxs-lookup"><span data-stu-id="835e9-120">Client applications can use **PR_AB_PROVIDER_ID** to find related rows in an address book hierarchy table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="835e9-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="835e9-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="835e9-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="835e9-122">Header files</span></span>

<span data-ttu-id="835e9-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="835e9-123">Mapitags.h</span></span>
  
> <span data-ttu-id="835e9-124">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="835e9-124">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="835e9-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="835e9-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="835e9-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="835e9-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="835e9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="835e9-127">See also</span></span>



[<span data-ttu-id="835e9-128">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="835e9-128">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="835e9-129">Propriété canonique PidTagStoreProvider</span><span class="sxs-lookup"><span data-stu-id="835e9-129">PidTagStoreProvider Canonical Property</span></span>](pidtagstoreprovider-canonical-property.md)


[<span data-ttu-id="835e9-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="835e9-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="835e9-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="835e9-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="835e9-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="835e9-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

