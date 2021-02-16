---
title: Propriété canonique PidTagDeferredSendUnits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendUnits
api_type:
- HeaderDef
ms.assetid: 2386be9f-18c9-4949-a2aa-efc8e212801c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: becc076efe0f4f805eb2a8db071b70ad731ee256
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359905"
---
# <a name="pidtagdeferredsendunits-canonical-property"></a><span data-ttu-id="4036c-103">Propriété canonique PidTagDeferredSendUnits</span><span class="sxs-lookup"><span data-stu-id="4036c-103">PidTagDeferredSendUnits Canonical Property</span></span>

  
  
<span data-ttu-id="4036c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4036c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4036c-105">Spécifie l’unité de temps à laquelle la valeur de PR_DEFERRED_SEND_NUMBER **(** [PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) doit être multipliée.</span><span class="sxs-lookup"><span data-stu-id="4036c-105">Specifies the unit of time by which the **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) property value should be multiplied.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4036c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4036c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4036c-107">PR_DEFERRED_SEND_UNITS</span><span class="sxs-lookup"><span data-stu-id="4036c-107">PR_DEFERRED_SEND_UNITS</span></span>  <br/> |
|<span data-ttu-id="4036c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="4036c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4036c-109">0x3FEC</span><span class="sxs-lookup"><span data-stu-id="4036c-109">0x3FEC</span></span>  <br/> |
|<span data-ttu-id="4036c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4036c-110">Data type:</span></span>  <br/> |<span data-ttu-id="4036c-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4036c-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4036c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="4036c-112">Area:</span></span>  <br/> |<span data-ttu-id="4036c-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="4036c-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4036c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4036c-114">Remarks</span></span>

<span data-ttu-id="4036c-115">Si elle est définie, cette propriété doit avoir l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="4036c-115">If set, this property must have one of the following values:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4036c-116">**PidTagDeferredSendUnits**</span><span class="sxs-lookup"><span data-stu-id="4036c-116">**PidTagDeferredSendUnits**</span></span> <br/> |<span data-ttu-id="4036c-117">Description</span><span class="sxs-lookup"><span data-stu-id="4036c-117">Description</span></span>  <br/> |
|<span data-ttu-id="4036c-118">0</span><span class="sxs-lookup"><span data-stu-id="4036c-118">0</span></span>  <br/> |<span data-ttu-id="4036c-119">Minutes, par exemple 60 secondes</span><span class="sxs-lookup"><span data-stu-id="4036c-119">Minutes, for example 60 seconds</span></span>  <br/> |
|<span data-ttu-id="4036c-120">1 </span><span class="sxs-lookup"><span data-stu-id="4036c-120">1</span></span>  <br/> |<span data-ttu-id="4036c-121">Heures, par exemple 60 x 60 secondes</span><span class="sxs-lookup"><span data-stu-id="4036c-121">Hours, for example 60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="4036c-122">2 </span><span class="sxs-lookup"><span data-stu-id="4036c-122">2</span></span>  <br/> |<span data-ttu-id="4036c-123">Jour, par exemple 24 x 60 x 60 secondes</span><span class="sxs-lookup"><span data-stu-id="4036c-123">Day, for example 24x60x60 seconds</span></span>  <br/> |
|<span data-ttu-id="4036c-124">3 </span><span class="sxs-lookup"><span data-stu-id="4036c-124">3</span></span>  <br/> |<span data-ttu-id="4036c-125">Semaine, par exemple 7 x 24 x 60 x 60 secondes</span><span class="sxs-lookup"><span data-stu-id="4036c-125">Week, for example 7x24x60x60 seconds</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4036c-126">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="4036c-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4036c-127">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="4036c-127">Protocol specifications</span></span>

<span data-ttu-id="4036c-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4036c-128">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4036c-129">Spécifie les propriétés et opérations autorisées pour les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="4036c-129">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4036c-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="4036c-130">Header files</span></span>

<span data-ttu-id="4036c-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4036c-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="4036c-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4036c-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="4036c-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4036c-133">Mapitags.h</span></span>
  
> <span data-ttu-id="4036c-134">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="4036c-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4036c-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4036c-135">See also</span></span>



[<span data-ttu-id="4036c-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4036c-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4036c-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4036c-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4036c-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4036c-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4036c-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="4036c-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

