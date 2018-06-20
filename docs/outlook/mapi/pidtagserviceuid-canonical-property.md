---
title: Propriété canonique PidTagServiceUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceUid
api_type:
- COM
ms.assetid: 9d99a3b6-d0b4-4e8a-8f08-f46fdeb6b3e7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 304efc3f4ea903f9ed0e9fcf95c7100fa6ebfc95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786799"
---
# <a name="pidtagserviceuid-canonical-property"></a><span data-ttu-id="30705-103">Propriété canonique PidTagServiceUid</span><span class="sxs-lookup"><span data-stu-id="30705-103">PidTagServiceUid Canonical Property</span></span>

  
  
<span data-ttu-id="30705-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="30705-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="30705-105">Contient la structure [MAPIUID](mapiuid.md) d’un service de message.</span><span class="sxs-lookup"><span data-stu-id="30705-105">Contains the [MAPIUID](mapiuid.md) structure for a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30705-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="30705-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="30705-107">PR_SERVICE_UID</span><span class="sxs-lookup"><span data-stu-id="30705-107">PR_SERVICE_UID</span></span>  <br/> |
|<span data-ttu-id="30705-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="30705-108">Identifier:</span></span>  <br/> |<span data-ttu-id="30705-109">0x3D0C</span><span class="sxs-lookup"><span data-stu-id="30705-109">0x3D0C</span></span>  <br/> |
|<span data-ttu-id="30705-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="30705-110">Data type:</span></span>  <br/> |<span data-ttu-id="30705-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="30705-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="30705-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="30705-112">Area:</span></span>  <br/> |<span data-ttu-id="30705-113">Profil MAPI</span><span class="sxs-lookup"><span data-stu-id="30705-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30705-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="30705-114">Remarks</span></span>

<span data-ttu-id="30705-115">Cette propriété est calculée par MAPI sur les objets section de profil.</span><span class="sxs-lookup"><span data-stu-id="30705-115">This property is computed by MAPI on profile section objects.</span></span> <span data-ttu-id="30705-116">MAPI utilise pour tous les fournisseurs qui appartiennent au même service de message de groupe.</span><span class="sxs-lookup"><span data-stu-id="30705-116">MAPI uses it to group all the providers that belong to the same message service.</span></span> <span data-ttu-id="30705-117">Cette propriété est fournie en tant que paramètre à la plupart des méthodes [IMsgServiceAdmin](imsgserviceadminiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="30705-117">This property is supplied as a parameter to most of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) methods.</span></span> <span data-ttu-id="30705-118">Il ne doit pas apparaître dans le fichier Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="30705-118">It must not appear in Mapisvc.inf.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="30705-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="30705-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="30705-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="30705-120">Header files</span></span>

<span data-ttu-id="30705-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="30705-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="30705-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="30705-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="30705-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="30705-123">Mapitags.h</span></span>
  
> <span data-ttu-id="30705-124">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="30705-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="30705-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30705-125">See also</span></span>



[<span data-ttu-id="30705-126">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="30705-126">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="30705-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="30705-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="30705-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="30705-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="30705-129">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="30705-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="30705-130">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="30705-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

