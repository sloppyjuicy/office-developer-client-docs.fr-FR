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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 32d150e508f5c208e15d5ee5f0b8c800a1e597f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429858"
---
# <a name="pidtagresourcepath-canonical-property"></a><span data-ttu-id="9d11c-103">Propriété canonique PidTagResourcePath</span><span class="sxs-lookup"><span data-stu-id="9d11c-103">PidTagResourcePath Canonical Property</span></span>

  
  
<span data-ttu-id="9d11c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d11c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d11c-105">Contient un chemin d'accès au serveur du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="9d11c-105">Contains a path to the service provider's server.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9d11c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9d11c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d11c-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span><span class="sxs-lookup"><span data-stu-id="9d11c-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span></span>  <br/> |
|<span data-ttu-id="9d11c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9d11c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9d11c-109">0x3E07</span><span class="sxs-lookup"><span data-stu-id="9d11c-109">0x3E07</span></span>  <br/> |
|<span data-ttu-id="9d11c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9d11c-110">Data type:</span></span>  <br/> |<span data-ttu-id="9d11c-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9d11c-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="9d11c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9d11c-112">Area:</span></span>  <br/> |<span data-ttu-id="9d11c-113">État MAPI</span><span class="sxs-lookup"><span data-stu-id="9d11c-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d11c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9d11c-114">Remarks</span></span>

<span data-ttu-id="9d11c-115">Le chemin d'accès contenu dans ces propriétés représente le chemin d'accès suggéré dans lequel l'utilisateur peut trouver des ressources.</span><span class="sxs-lookup"><span data-stu-id="9d11c-115">The path contained in these properties represents the suggested path where the user can find resources.</span></span> <span data-ttu-id="9d11c-116">La définition de ces propriétés est spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9d11c-116">The definition of these properties is provider specific.</span></span> <span data-ttu-id="9d11c-117">Par exemple, une application de planification utilise ces propriétés pour spécifier l'emplacement suggéré pour ses fichiers d'application de planification.</span><span class="sxs-lookup"><span data-stu-id="9d11c-117">For example, a scheduling application uses these properties to specify the suggested location for its scheduling application files.</span></span>
  
<span data-ttu-id="9d11c-118">Le profil utilisateur de messagerie fournit ces propriétés pour qu'une application cliente n'ait pas besoin d'inviter l'utilisateur de messagerie à indiquer un chemin d'accès réseau ou une lettre de lecteur réseau.</span><span class="sxs-lookup"><span data-stu-id="9d11c-118">The messaging user profile furnishes these properties as a convenience so that a client application does not have to prompt the messaging user for a network path or network drive letter.</span></span>
  
<span data-ttu-id="9d11c-119">MAPI ne fonctionne qu'avec les noms de fichier dans le jeu de caractères ANSI (American National Standards Institute).</span><span class="sxs-lookup"><span data-stu-id="9d11c-119">MAPI works only with filenames in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="9d11c-120">Les applications qui utilisent des noms de fichier dans un jeu de caractères OEM (Original Equipment Manufacturer) doivent les convertir en ANSI avant d'appeler MAPI.</span><span class="sxs-lookup"><span data-stu-id="9d11c-120">Applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9d11c-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="9d11c-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="9d11c-122">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="9d11c-122">Header files</span></span>

<span data-ttu-id="9d11c-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9d11c-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d11c-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9d11c-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="9d11c-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="9d11c-125">Mapitags.h</span></span>
  
> <span data-ttu-id="9d11c-126">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="9d11c-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d11c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d11c-127">See also</span></span>



[<span data-ttu-id="9d11c-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9d11c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d11c-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9d11c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d11c-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9d11c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d11c-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9d11c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

