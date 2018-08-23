---
title: Propriété canonique PidTagProviderDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDisplay
api_type:
- COM
ms.assetid: 62e96db8-4c3e-4f73-b695-99eb4b2396fd
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 9a37382cda1a96025f950d941f83fb5b6a0497bb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565500"
---
# <a name="pidtagproviderdisplay-canonical-property"></a><span data-ttu-id="91194-103">Propriété canonique PidTagProviderDisplay</span><span class="sxs-lookup"><span data-stu-id="91194-103">PidTagProviderDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="91194-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="91194-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="91194-105">Contient le nom d’affichage définies par le fournisseur pour un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="91194-105">Contains the vendor-defined display name for a service provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="91194-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="91194-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="91194-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="91194-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="91194-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="91194-108">Identifier:</span></span>  <br/> |<span data-ttu-id="91194-109">0x3006</span><span class="sxs-lookup"><span data-stu-id="91194-109">0x3006</span></span>  <br/> |
|<span data-ttu-id="91194-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="91194-110">Data type:</span></span>  <br/> |<span data-ttu-id="91194-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="91194-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="91194-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="91194-112">Area:</span></span>  <br/> |<span data-ttu-id="91194-113">MAPI courantes</span><span class="sxs-lookup"><span data-stu-id="91194-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="91194-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="91194-114">Remarks</span></span>

<span data-ttu-id="91194-115">Ces propriétés et **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) sont définis uniquement sur les sections profil appartenant aux fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="91194-115">These properties and **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) are defined only on profile sections belonging to service providers.</span></span> <span data-ttu-id="91194-116">Ils doivent être présents dans le fichier MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="91194-116">They must be present in MAPISVC.INF.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="91194-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="91194-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="91194-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="91194-118">Header files</span></span>

<span data-ttu-id="91194-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="91194-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="91194-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="91194-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="91194-121">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="91194-121">Mapitags.h</span></span>
  
> <span data-ttu-id="91194-122">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="91194-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="91194-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91194-123">See also</span></span>



[<span data-ttu-id="91194-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="91194-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="91194-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="91194-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="91194-126">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="91194-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="91194-127">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="91194-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

