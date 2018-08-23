---
title: Propriété canonique PidTagProfileName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProfileName
api_type:
- COM
ms.assetid: 13ca726d-ae7a-4da9-9c8e-3db3c479f839
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 708e77e4df097f5a0de008e09808ffcbc0289f61
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574579"
---
# <a name="pidtagprofilename-canonical-property"></a><span data-ttu-id="6e999-103">Propriété canonique PidTagProfileName</span><span class="sxs-lookup"><span data-stu-id="6e999-103">PidTagProfileName Canonical Property</span></span>

  
  
<span data-ttu-id="6e999-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e999-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e999-105">Contient le nom du profil.</span><span class="sxs-lookup"><span data-stu-id="6e999-105">Contains the name of the profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6e999-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6e999-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6e999-107">PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W</span><span class="sxs-lookup"><span data-stu-id="6e999-107">PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W</span></span>  <br/> |
|<span data-ttu-id="6e999-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6e999-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6e999-109">0x3D12</span><span class="sxs-lookup"><span data-stu-id="6e999-109">0x3D12</span></span>  <br/> |
|<span data-ttu-id="6e999-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6e999-110">Data type:</span></span>  <br/> |<span data-ttu-id="6e999-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6e999-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6e999-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6e999-112">Area:</span></span>  <br/> |<span data-ttu-id="6e999-113">Configuration d’un profil MAPI</span><span class="sxs-lookup"><span data-stu-id="6e999-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6e999-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6e999-114">Remarks</span></span>

<span data-ttu-id="6e999-115">Ces propriétés sont calculées par les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="6e999-115">These properties are computed by service providers.</span></span> <span data-ttu-id="6e999-116">Implémentation d’un fournisseur de la fonction **ServiceEntry** peut utiliser ces propriétés pour découvrir le nom du profil.</span><span class="sxs-lookup"><span data-stu-id="6e999-116">A provider's implementation of the **ServiceEntry** function can use these properties to discover the profile name.</span></span> 
  
<span data-ttu-id="6e999-117">Applications clientes peuvent utiliser ces propriétés comme une alternative pratique pour obtenir le nom du profil en examinant la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) dans la ligne table d’état du sous-système MAPI.</span><span class="sxs-lookup"><span data-stu-id="6e999-117">Client applications can use these properties as a convenient alternative to obtaining the profile name by examining the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property in the MAPI subsystem's status table row.</span></span>
  
<span data-ttu-id="6e999-118">Ces propriétés ne peuvent pas être uniques au fil du temps, par exemple où un profil est supprimé et recréé ultérieurement portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="6e999-118">These properties may not be unique across time, for example where a profile is deleted and later recreated with the same name.</span></span> <span data-ttu-id="6e999-119">MAPI apporte une propriété **clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) unique dans une section de profil codé en dur appelée **MUID_PROFILE_INSTANCE.**</span><span class="sxs-lookup"><span data-stu-id="6e999-119">MAPI furnishes a totally unique **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property in a hard-coded profile section called **MUID_PROFILE_INSTANCE.**</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6e999-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6e999-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6e999-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6e999-121">Header files</span></span>

<span data-ttu-id="6e999-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6e999-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="6e999-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6e999-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="6e999-124">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="6e999-124">Mapitags.h</span></span>
  
> <span data-ttu-id="6e999-125">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="6e999-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e999-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e999-126">See also</span></span>



[<span data-ttu-id="6e999-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6e999-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6e999-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6e999-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6e999-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6e999-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6e999-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6e999-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

