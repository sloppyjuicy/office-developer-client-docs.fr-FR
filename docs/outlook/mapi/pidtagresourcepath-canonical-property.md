---
title: Propriété canonique PidTagResourcePath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourcePath
api_type:
- COM
ms.assetid: ac49538e-6ee8-4ab4-9d79-88a83c7d0149
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d7385ea403e7ea45c97f6fd98e422ad7eb762c4c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786604"
---
# <a name="pidtagresourcepath-canonical-property"></a><span data-ttu-id="3088b-103">Propriété canonique PidTagResourcePath</span><span class="sxs-lookup"><span data-stu-id="3088b-103">PidTagResourcePath Canonical Property</span></span>

  
  
<span data-ttu-id="3088b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3088b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3088b-105">Contient un chemin d’accès au serveur du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="3088b-105">Contains a path to the service provider's server.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3088b-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="3088b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3088b-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span><span class="sxs-lookup"><span data-stu-id="3088b-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span></span>  <br/> |
|<span data-ttu-id="3088b-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="3088b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3088b-109">0x3E07</span><span class="sxs-lookup"><span data-stu-id="3088b-109">0x3E07</span></span>  <br/> |
|<span data-ttu-id="3088b-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3088b-110">Data type:</span></span>  <br/> |<span data-ttu-id="3088b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3088b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3088b-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="3088b-112">Area:</span></span>  <br/> |<span data-ttu-id="3088b-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="3088b-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3088b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3088b-114">Remarks</span></span>

<span data-ttu-id="3088b-115">Le chemin d’accès contenue dans ces propriétés représente le chemin d’accès suggéré dans laquelle l’utilisateur peut trouver des ressources.</span><span class="sxs-lookup"><span data-stu-id="3088b-115">The path contained in these properties represents the suggested path where the user can find resources.</span></span> <span data-ttu-id="3088b-116">La définition de ces propriétés est spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3088b-116">The definition of these properties is provider specific.</span></span> <span data-ttu-id="3088b-117">Par exemple, une application de planification utilise ces propriétés pour spécifier l’emplacement proposé pour ses fichiers d’application de planification.</span><span class="sxs-lookup"><span data-stu-id="3088b-117">For example, a scheduling application uses these properties to specify the suggested location for its scheduling application files.</span></span>
  
<span data-ttu-id="3088b-118">Le profil utilisateur de messagerie fournit ces propriétés commodité afin qu’une application cliente n’a pas demander à l’utilisateur de messagerie pour un chemin d’accès réseau ou d’une lettre de lecteur réseau.</span><span class="sxs-lookup"><span data-stu-id="3088b-118">The messaging user profile furnishes these properties as a convenience so that a client application does not have to prompt the messaging user for a network path or network drive letter.</span></span>
  
<span data-ttu-id="3088b-119">MAPI ne fonctionne qu’avec les noms de fichiers dans le jeu de caractères National Institute ANSI (American Standards).</span><span class="sxs-lookup"><span data-stu-id="3088b-119">MAPI works only with filenames in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="3088b-120">Les applications qui utilisent des noms de fichiers dans un jeu de caractères OEM (OEM) doivent les convertir au format ANSI avant l’appel de MAPI.</span><span class="sxs-lookup"><span data-stu-id="3088b-120">Applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3088b-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="3088b-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3088b-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="3088b-122">Header files</span></span>

<span data-ttu-id="3088b-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3088b-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="3088b-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="3088b-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="3088b-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="3088b-125">Mapitags.h</span></span>
  
> <span data-ttu-id="3088b-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="3088b-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3088b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3088b-127">See also</span></span>



[<span data-ttu-id="3088b-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="3088b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3088b-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="3088b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3088b-130">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="3088b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3088b-131">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="3088b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

