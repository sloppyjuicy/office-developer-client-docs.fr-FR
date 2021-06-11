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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d5c6e1dc30c3ee7862341bce204b4a78bd6d379b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426526"
---
# <a name="pidtagserviceuid-canonical-property"></a><span data-ttu-id="79bed-103">Propriété canonique PidTagServiceUid</span><span class="sxs-lookup"><span data-stu-id="79bed-103">PidTagServiceUid Canonical Property</span></span>

  
  
<span data-ttu-id="79bed-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79bed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79bed-105">Contient la structure [MAPIUID](mapiuid.md) pour un service de message.</span><span class="sxs-lookup"><span data-stu-id="79bed-105">Contains the [MAPIUID](mapiuid.md) structure for a message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="79bed-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="79bed-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="79bed-107">PR_SERVICE_UID</span><span class="sxs-lookup"><span data-stu-id="79bed-107">PR_SERVICE_UID</span></span>  <br/> |
|<span data-ttu-id="79bed-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="79bed-108">Identifier:</span></span>  <br/> |<span data-ttu-id="79bed-109">0x3D0C</span><span class="sxs-lookup"><span data-stu-id="79bed-109">0x3D0C</span></span>  <br/> |
|<span data-ttu-id="79bed-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="79bed-110">Data type:</span></span>  <br/> |<span data-ttu-id="79bed-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="79bed-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="79bed-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="79bed-112">Area:</span></span>  <br/> |<span data-ttu-id="79bed-113">Profil MAPI</span><span class="sxs-lookup"><span data-stu-id="79bed-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79bed-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="79bed-114">Remarks</span></span>

<span data-ttu-id="79bed-115">Cette propriété est calculée par MAPI sur les objets de section de profil.</span><span class="sxs-lookup"><span data-stu-id="79bed-115">This property is computed by MAPI on profile section objects.</span></span> <span data-ttu-id="79bed-116">MAPI l’utilise pour grouper tous les fournisseurs qui appartiennent au même service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="79bed-116">MAPI uses it to group all the providers that belong to the same message service.</span></span> <span data-ttu-id="79bed-117">Cette propriété est fournie en tant que paramètre pour la plupart des méthodes [IMsgServiceAdmin.](imsgserviceadminiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="79bed-117">This property is supplied as a parameter to most of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) methods.</span></span> <span data-ttu-id="79bed-118">Elle ne doit pas apparaître dans Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="79bed-118">It must not appear in Mapisvc.inf.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="79bed-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="79bed-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="79bed-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="79bed-120">Header files</span></span>

<span data-ttu-id="79bed-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="79bed-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="79bed-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="79bed-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="79bed-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="79bed-123">Mapitags.h</span></span>
  
> <span data-ttu-id="79bed-124">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="79bed-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="79bed-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79bed-125">See also</span></span>



[<span data-ttu-id="79bed-126">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="79bed-126">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="79bed-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="79bed-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="79bed-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="79bed-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="79bed-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="79bed-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="79bed-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="79bed-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

