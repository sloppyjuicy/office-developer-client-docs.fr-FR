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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316365"
---
# <a name="pidtagexpirynumber-canonical-property"></a><span data-ttu-id="7fe18-103">Propriété canonique PidTagExpiryNumber</span><span class="sxs-lookup"><span data-stu-id="7fe18-103">PidTagExpiryNumber Canonical Property</span></span>

  
  
<span data-ttu-id="7fe18-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7fe18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7fe18-105">Définit l’heure d’envoi d’expiration conjointement avec **la propriété PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7fe18-105">Defines the expiry send time in conjunction with the **PR_EXPIRY_UNITS** ([PidTagExpiryUnits](pidtagexpiryunits-canonical-property.md)) property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7fe18-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="7fe18-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7fe18-107">PR_EXPIRY_NUMBER</span><span class="sxs-lookup"><span data-stu-id="7fe18-107">PR_EXPIRY_NUMBER</span></span>  <br/> |
|<span data-ttu-id="7fe18-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="7fe18-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7fe18-109">0x3FED</span><span class="sxs-lookup"><span data-stu-id="7fe18-109">0x3FED</span></span>  <br/> |
|<span data-ttu-id="7fe18-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="7fe18-110">Data type:</span></span>  <br/> |<span data-ttu-id="7fe18-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="7fe18-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="7fe18-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="7fe18-112">Area:</span></span>  <br/> |<span data-ttu-id="7fe18-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="7fe18-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7fe18-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="7fe18-114">Remarks</span></span>

<span data-ttu-id="7fe18-115">La valeur de cette propriété doit être définie entre 0 et 999 inclus, si elle est présente.</span><span class="sxs-lookup"><span data-stu-id="7fe18-115">This property's value must be set between 0 and 999 inclusive, if it is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7fe18-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="7fe18-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7fe18-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="7fe18-117">Protocol specifications</span></span>

<span data-ttu-id="7fe18-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7fe18-118">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7fe18-119">Spécifie les propriétés et opérations autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="7fe18-119">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7fe18-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="7fe18-120">Header files</span></span>

<span data-ttu-id="7fe18-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7fe18-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="7fe18-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="7fe18-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="7fe18-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7fe18-123">Mapitags.h</span></span>
  
> <span data-ttu-id="7fe18-124">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="7fe18-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7fe18-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fe18-125">See also</span></span>



[<span data-ttu-id="7fe18-126">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="7fe18-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7fe18-127">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="7fe18-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7fe18-128">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="7fe18-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7fe18-129">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="7fe18-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

