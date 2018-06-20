---
title: Propriété canonique PidTagServiceExtraUids
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceExtraUids
api_type:
- COM
ms.assetid: 4838a9af-7818-49aa-ace8-cb94dda8471f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 71f802014200d4b767c346c14df53f1193d44b0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786783"
---
# <a name="pidtagserviceextrauids-canonical-property"></a><span data-ttu-id="0341f-103">Propriété canonique PidTagServiceExtraUids</span><span class="sxs-lookup"><span data-stu-id="0341f-103">PidTagServiceExtraUids Canonical Property</span></span>

  
  
<span data-ttu-id="0341f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0341f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0341f-105">Contient une liste des structures [MAPIUID](mapiuid.md) qui identifient les sections de profil supplémentaires pour le service de message.</span><span class="sxs-lookup"><span data-stu-id="0341f-105">Contains a list of [MAPIUID](mapiuid.md) structures that identify additional profile sections for the message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0341f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0341f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0341f-107">PR_SERVICE_EXTRA_UIDS</span><span class="sxs-lookup"><span data-stu-id="0341f-107">PR_SERVICE_EXTRA_UIDS</span></span>  <br/> |
|<span data-ttu-id="0341f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="0341f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0341f-109">0x3D0D</span><span class="sxs-lookup"><span data-stu-id="0341f-109">0x3D0D</span></span>  <br/> |
|<span data-ttu-id="0341f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0341f-110">Data type:</span></span>  <br/> |<span data-ttu-id="0341f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0341f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0341f-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="0341f-112">Area:</span></span>  <br/> |<span data-ttu-id="0341f-113">Profil MAPI</span><span class="sxs-lookup"><span data-stu-id="0341f-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0341f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0341f-114">Remarks</span></span>

<span data-ttu-id="0341f-115">Nouvelles sections profil peuvent être créées pour chaque filtre de message.</span><span class="sxs-lookup"><span data-stu-id="0341f-115">New profile sections can be created for each message filter.</span></span> <span data-ttu-id="0341f-116">Lorsque les informations sur le service de message doit être copié vers un autre profil, il est important de copier les sections de profil supplémentaires pour les filtres ainsi.</span><span class="sxs-lookup"><span data-stu-id="0341f-116">When the information about the message service is to be copied to another profile, it is important to copy the additional profile sections for the filters as well.</span></span> <span data-ttu-id="0341f-117">Un fournisseur de services qui utilise des sections de profil supplémentaires peut stocker les structures **MAPIUID** de ces sections profil dans **PR_SERVICE_EXTRA_UIDS**, qui permet de MAPI copier les informations de service de message supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="0341f-117">A service provider that uses additional profile sections can store the **MAPIUID** structures of those profile sections in **PR_SERVICE_EXTRA_UIDS**, which allows MAPI to copy the additional message service information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0341f-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0341f-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0341f-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0341f-119">Header files</span></span>

<span data-ttu-id="0341f-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0341f-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="0341f-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0341f-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="0341f-122">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="0341f-122">Mapitags.h</span></span>
  
> <span data-ttu-id="0341f-123">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="0341f-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0341f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0341f-124">See also</span></span>



[<span data-ttu-id="0341f-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0341f-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0341f-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0341f-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0341f-127">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0341f-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0341f-128">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="0341f-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

