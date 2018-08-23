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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: eabcaaf1db6149ef200e640f5af152758261581b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582250"
---
# <a name="pidtagserviceuid-canonical-property"></a><span data-ttu-id="4e49f-103">Propriété canonique PidTagServiceUid</span><span class="sxs-lookup"><span data-stu-id="4e49f-103">PidTagServiceUid Canonical Property</span></span>

  
  
<span data-ttu-id="4e49f-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e49f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e49f-105">Contient la structure [MAPIUID](mapiuid.md) d’un service de message.</span><span class="sxs-lookup"><span data-stu-id="4e49f-105">Contains the [MAPIUID](mapiuid.md) structure for a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4e49f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4e49f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4e49f-107">PR_SERVICE_UID</span><span class="sxs-lookup"><span data-stu-id="4e49f-107">PR_SERVICE_UID</span></span>  <br/> |
|<span data-ttu-id="4e49f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="4e49f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4e49f-109">0x3D0C</span><span class="sxs-lookup"><span data-stu-id="4e49f-109">0x3D0C</span></span>  <br/> |
|<span data-ttu-id="4e49f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4e49f-110">Data type:</span></span>  <br/> |<span data-ttu-id="4e49f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="4e49f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="4e49f-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="4e49f-112">Area:</span></span>  <br/> |<span data-ttu-id="4e49f-113">Profil MAPI</span><span class="sxs-lookup"><span data-stu-id="4e49f-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e49f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4e49f-114">Remarks</span></span>

<span data-ttu-id="4e49f-115">Cette propriété est calculée par MAPI sur les objets section de profil.</span><span class="sxs-lookup"><span data-stu-id="4e49f-115">This property is computed by MAPI on profile section objects.</span></span> <span data-ttu-id="4e49f-116">MAPI utilise pour tous les fournisseurs qui appartiennent au même service de message de groupe.</span><span class="sxs-lookup"><span data-stu-id="4e49f-116">MAPI uses it to group all the providers that belong to the same message service.</span></span> <span data-ttu-id="4e49f-117">Cette propriété est fournie en tant que paramètre à la plupart des méthodes [IMsgServiceAdmin](imsgserviceadminiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="4e49f-117">This property is supplied as a parameter to most of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) methods.</span></span> <span data-ttu-id="4e49f-118">Il ne doit pas apparaître dans le fichier Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="4e49f-118">It must not appear in Mapisvc.inf.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4e49f-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="4e49f-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4e49f-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="4e49f-120">Header files</span></span>

<span data-ttu-id="4e49f-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4e49f-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="4e49f-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4e49f-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="4e49f-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="4e49f-123">Mapitags.h</span></span>
  
> <span data-ttu-id="4e49f-124">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="4e49f-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4e49f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e49f-125">See also</span></span>



[<span data-ttu-id="4e49f-126">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4e49f-126">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="4e49f-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4e49f-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4e49f-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4e49f-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4e49f-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4e49f-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4e49f-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="4e49f-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

