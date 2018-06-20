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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6cd255c60987ec7a279e509aa2925a8029cce62e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785895"
---
# <a name="pidtagdefaultprofile-canonical-property"></a><span data-ttu-id="ac8b6-103">Propriété canonique PidTagDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac8b6-103">PidTagDefaultProfile Canonical Property</span></span>

  
  
<span data-ttu-id="ac8b6-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ac8b6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ac8b6-105">Contient la valeur TRUE si un profil utilisateur de messagerie est le profil par défaut MAPI.</span><span class="sxs-lookup"><span data-stu-id="ac8b6-105">Contains TRUE if a messaging user profile is the MAPI default profile.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ac8b6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ac8b6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac8b6-107">PR_DEFAULT_PROFILE</span><span class="sxs-lookup"><span data-stu-id="ac8b6-107">PR_DEFAULT_PROFILE</span></span>  <br/> |
|<span data-ttu-id="ac8b6-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ac8b6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ac8b6-109">0x3D04</span><span class="sxs-lookup"><span data-stu-id="ac8b6-109">0x3D04</span></span>  <br/> |
|<span data-ttu-id="ac8b6-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ac8b6-110">Data type:</span></span>  <br/> |<span data-ttu-id="ac8b6-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="ac8b6-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="ac8b6-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="ac8b6-112">Area:</span></span>  <br/> |<span data-ttu-id="ac8b6-113">Profil MAPI</span><span class="sxs-lookup"><span data-stu-id="ac8b6-113">MAPI profile</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac8b6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ac8b6-114">Remarks</span></span>

<span data-ttu-id="ac8b6-115">Cette propriété n’apparaît pas en tant que propriété de tout objet, mais uniquement en tant que colonne dans une table de profil.</span><span class="sxs-lookup"><span data-stu-id="ac8b6-115">This property does not appear as a property of any object but only as a column in a profile table.</span></span> <span data-ttu-id="ac8b6-116">Une application cliente peut utiliser la méthode [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) pour désigner le profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="ac8b6-116">A client application can use the [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md) method to designate the default profile.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ac8b6-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ac8b6-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ac8b6-118">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ac8b6-118">Header files</span></span>

<span data-ttu-id="ac8b6-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac8b6-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac8b6-120">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ac8b6-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="ac8b6-121">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="ac8b6-121">Mapitags.h</span></span>
  
> <span data-ttu-id="ac8b6-122">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="ac8b6-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac8b6-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac8b6-123">See also</span></span>



[<span data-ttu-id="ac8b6-124">Propriété canonique PidTagDefaultStore</span><span class="sxs-lookup"><span data-stu-id="ac8b6-124">PidTagDefaultStore Canonical Property</span></span>](pidtagdefaultstore-canonical-property.md)


[<span data-ttu-id="ac8b6-125">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ac8b6-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ac8b6-126">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ac8b6-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac8b6-127">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ac8b6-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac8b6-128">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="ac8b6-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

