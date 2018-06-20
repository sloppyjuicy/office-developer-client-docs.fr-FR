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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1546ee1aa970be71d853dba59ce0fab7cc5a4dac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786453"
---
# <a name="pidtagproviderdisplay-canonical-property"></a><span data-ttu-id="05d1f-103">Propriété canonique PidTagProviderDisplay</span><span class="sxs-lookup"><span data-stu-id="05d1f-103">PidTagProviderDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="05d1f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="05d1f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="05d1f-105">Contient le nom d’affichage définies par le fournisseur pour un fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="05d1f-105">Contains the vendor-defined display name for a service provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="05d1f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="05d1f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="05d1f-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="05d1f-107">PR_PROVIDER_DISPLAY, PR_PROVIDER_DISPLAY_A, PR_PROVIDER_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="05d1f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="05d1f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="05d1f-109">0x3006</span><span class="sxs-lookup"><span data-stu-id="05d1f-109">0x3006</span></span>  <br/> |
|<span data-ttu-id="05d1f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="05d1f-110">Data type:</span></span>  <br/> |<span data-ttu-id="05d1f-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="05d1f-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="05d1f-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="05d1f-112">Area:</span></span>  <br/> |<span data-ttu-id="05d1f-113">MAPI courantes</span><span class="sxs-lookup"><span data-stu-id="05d1f-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05d1f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="05d1f-114">Remarks</span></span>

<span data-ttu-id="05d1f-115">Ces propriétés et **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) sont définis uniquement sur les sections profil appartenant aux fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="05d1f-115">These properties and **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) are defined only on profile sections belonging to service providers.</span></span> <span data-ttu-id="05d1f-116">Ils doivent être présents dans le fichier MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="05d1f-116">They must be present in MAPISVC.INF.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="05d1f-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="05d1f-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="05d1f-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="05d1f-118">Header files</span></span>

<span data-ttu-id="05d1f-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="05d1f-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="05d1f-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="05d1f-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="05d1f-121">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="05d1f-121">Mapitags.h</span></span>
  
> <span data-ttu-id="05d1f-122">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="05d1f-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="05d1f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05d1f-123">See also</span></span>



[<span data-ttu-id="05d1f-124">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="05d1f-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="05d1f-125">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="05d1f-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="05d1f-126">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="05d1f-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="05d1f-127">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="05d1f-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

