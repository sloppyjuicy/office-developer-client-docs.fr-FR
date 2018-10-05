---
title: Propriété canonique PidTagExpiryNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryNumber
api_type:
- HeaderDef
ms.assetid: 644e8d3d-1792-4417-95a1-e978d0e6cd8e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: da90347f5aacdb2fcac8547eddd5b89a0a44820d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385822"
---
# <a name="pidtagexpirynumber-canonical-property"></a><span data-ttu-id="18be5-103">Propriété canonique PidTagExpiryNumber</span><span class="sxs-lookup"><span data-stu-id="18be5-103">PidTagExpiryNumber Canonical Property</span></span>

  
  
<span data-ttu-id="18be5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18be5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18be5-105">Définit le délai d’expiration envoi conjointement avec la propriété **PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="18be5-105">Defines the expiry send time in conjunction with the **PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="18be5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="18be5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18be5-107">PR_EXPIRY_NUMBER</span><span class="sxs-lookup"><span data-stu-id="18be5-107">PR_EXPIRY_NUMBER</span></span>  <br/> |
|<span data-ttu-id="18be5-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="18be5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="18be5-109">0x3FED</span><span class="sxs-lookup"><span data-stu-id="18be5-109">0x3FED</span></span>  <br/> |
|<span data-ttu-id="18be5-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="18be5-110">Data type:</span></span>  <br/> |<span data-ttu-id="18be5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="18be5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="18be5-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="18be5-112">Area:</span></span>  <br/> |<span data-ttu-id="18be5-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="18be5-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18be5-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="18be5-114">Remarks</span></span>

<span data-ttu-id="18be5-115">Valeur de cette propriété doit être définie entre 0 et 999 inclus, s’il est présent.</span><span class="sxs-lookup"><span data-stu-id="18be5-115">This property's value must be set between 0 and 999 inclusive, if it is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="18be5-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="18be5-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="18be5-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="18be5-117">Protocol specifications</span></span>

<span data-ttu-id="18be5-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18be5-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18be5-119">Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="18be5-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="18be5-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="18be5-120">Header files</span></span>

<span data-ttu-id="18be5-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18be5-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="18be5-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="18be5-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="18be5-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="18be5-123">Mapitags.h</span></span>
  
> <span data-ttu-id="18be5-124">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="18be5-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18be5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18be5-125">See also</span></span>



[<span data-ttu-id="18be5-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="18be5-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18be5-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="18be5-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18be5-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="18be5-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18be5-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="18be5-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

