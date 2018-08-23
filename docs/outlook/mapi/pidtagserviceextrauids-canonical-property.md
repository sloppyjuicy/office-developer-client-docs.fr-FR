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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 0deb1b34a437d47ab53cdb2e13cda006d9116f65
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570120"
---
# <a name="pidtagserviceextrauids-canonical-property"></a><span data-ttu-id="ef154-103">Propriété canonique PidTagServiceExtraUids</span><span class="sxs-lookup"><span data-stu-id="ef154-103">PidTagServiceExtraUids Canonical Property</span></span>

  
  
<span data-ttu-id="ef154-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef154-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef154-105">Contient une liste des structures [MAPIUID](mapiuid.md) qui identifient les sections de profil supplémentaires pour le service de message.</span><span class="sxs-lookup"><span data-stu-id="ef154-105">Contains a list of [MAPIUID](mapiuid.md) structures that identify additional profile sections for the message service.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ef154-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ef154-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ef154-107">PR_SERVICE_EXTRA_UIDS</span><span class="sxs-lookup"><span data-stu-id="ef154-107">PR_SERVICE_EXTRA_UIDS</span></span>  <br/> |
|<span data-ttu-id="ef154-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ef154-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ef154-109">0x3D0D</span><span class="sxs-lookup"><span data-stu-id="ef154-109">0x3D0D</span></span>  <br/> |
|<span data-ttu-id="ef154-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ef154-110">Data type:</span></span>  <br/> |<span data-ttu-id="ef154-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ef154-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ef154-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ef154-112">Area:</span></span>  <br/> |<span data-ttu-id="ef154-113">Profil MAPI</span><span class="sxs-lookup"><span data-stu-id="ef154-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef154-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ef154-114">Remarks</span></span>

<span data-ttu-id="ef154-115">Nouvelles sections profil peuvent être créées pour chaque filtre de message.</span><span class="sxs-lookup"><span data-stu-id="ef154-115">New profile sections can be created for each message filter.</span></span> <span data-ttu-id="ef154-116">Lorsque les informations sur le service de message doit être copié vers un autre profil, il est important de copier les sections de profil supplémentaires pour les filtres ainsi.</span><span class="sxs-lookup"><span data-stu-id="ef154-116">When the information about the message service is to be copied to another profile, it is important to copy the additional profile sections for the filters as well.</span></span> <span data-ttu-id="ef154-117">Un fournisseur de services qui utilise des sections de profil supplémentaires peut stocker les structures **MAPIUID** de ces sections profil dans **PR_SERVICE_EXTRA_UIDS**, qui permet de MAPI copier les informations de service de message supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="ef154-117">A service provider that uses additional profile sections can store the **MAPIUID** structures of those profile sections in **PR_SERVICE_EXTRA_UIDS**, which allows MAPI to copy the additional message service information.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ef154-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ef154-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ef154-119">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ef154-119">Header files</span></span>

<span data-ttu-id="ef154-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ef154-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="ef154-121">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ef154-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="ef154-122">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ef154-122">Mapitags.h</span></span>
  
> <span data-ttu-id="ef154-123">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="ef154-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ef154-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef154-124">See also</span></span>



[<span data-ttu-id="ef154-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ef154-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ef154-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ef154-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ef154-127">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ef154-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ef154-128">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ef154-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

