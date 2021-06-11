---
title: Propriété canonique PidTagDefaultProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultProfile
api_type:
- HeaderDef
ms.assetid: 47f745a4-5a9c-42af-b076-a72548ef4d31
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8295ae6904f503ca831a00c1f35ac08596b5358c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428773"
---
# <a name="pidtagdefaultprofile-canonical-property"></a><span data-ttu-id="6c5de-103">Propriété canonique PidTagDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c5de-103">PidTagDefaultProfile Canonical Property</span></span>

  
  
<span data-ttu-id="6c5de-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c5de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c5de-105">Contient TRUE si un profil utilisateur de messagerie est le profil mapi par défaut.</span><span class="sxs-lookup"><span data-stu-id="6c5de-105">Contains TRUE if a messaging user profile is the MAPI default profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6c5de-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6c5de-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6c5de-107">PR_DEFAULT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="6c5de-107">PR_DEFAULT_PROFILE</span></span>  <br/> |
|<span data-ttu-id="6c5de-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6c5de-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6c5de-109">0x3D04</span><span class="sxs-lookup"><span data-stu-id="6c5de-109">0x3D04</span></span>  <br/> |
|<span data-ttu-id="6c5de-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6c5de-110">Data type:</span></span>  <br/> |<span data-ttu-id="6c5de-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6c5de-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="6c5de-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="6c5de-112">Area:</span></span>  <br/> |<span data-ttu-id="6c5de-113">Profil MAPI</span><span class="sxs-lookup"><span data-stu-id="6c5de-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c5de-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6c5de-114">Remarks</span></span>

<span data-ttu-id="6c5de-115">Cette propriété n’apparaît pas en tant que propriété d’un objet, mais uniquement en tant que colonne dans une table de profils.</span><span class="sxs-lookup"><span data-stu-id="6c5de-115">This property does not appear as a property of any object but only as a column in a profile table.</span></span> <span data-ttu-id="6c5de-116">Une application cliente peut utiliser [la méthode IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) pour désigner le profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="6c5de-116">A client application can use the [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) method to designate the default profile.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6c5de-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6c5de-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6c5de-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6c5de-118">Header files</span></span>

<span data-ttu-id="6c5de-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6c5de-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="6c5de-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6c5de-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="6c5de-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6c5de-121">Mapitags.h</span></span>
  
> <span data-ttu-id="6c5de-122">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="6c5de-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6c5de-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c5de-123">See also</span></span>



[<span data-ttu-id="6c5de-124">Propriété canonique PidTagDefaultStore</span><span class="sxs-lookup"><span data-stu-id="6c5de-124">PidTagDefaultStore Canonical Property</span></span>](pidtagdefaultstore-canonical-property.md)


[<span data-ttu-id="6c5de-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6c5de-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6c5de-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6c5de-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6c5de-127">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6c5de-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6c5de-128">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="6c5de-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

