---
title: Propriété canonique PidTagMiniIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMiniIcon
api_type:
- HeaderDef
ms.assetid: a436b590-63f3-413c-a9c2-7664567e0ff0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 04d78bddc7bae27ba23cccf676eb6e7412ffc0db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786252"
---
# <a name="pidtagminiicon-canonical-property"></a><span data-ttu-id="33899-103">Propriété canonique PidTagMiniIcon</span><span class="sxs-lookup"><span data-stu-id="33899-103">PidTagMiniIcon Canonical Property</span></span>

  
  
<span data-ttu-id="33899-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="33899-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="33899-105">Contient un bitmap d’une icône demi pour un formulaire.</span><span class="sxs-lookup"><span data-stu-id="33899-105">Contains a bitmap of a half-size icon for a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="33899-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="33899-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="33899-107">PR_MINI_ICON</span><span class="sxs-lookup"><span data-stu-id="33899-107">PR_MINI_ICON</span></span>  <br/> |
|<span data-ttu-id="33899-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="33899-108">Identifier:</span></span>  <br/> |<span data-ttu-id="33899-109">0x0FFC</span><span class="sxs-lookup"><span data-stu-id="33899-109">0x0FFC</span></span>  <br/> |
|<span data-ttu-id="33899-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="33899-110">Data type:</span></span>  <br/> |<span data-ttu-id="33899-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="33899-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="33899-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="33899-112">Area:</span></span>  <br/> |<span data-ttu-id="33899-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="33899-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33899-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="33899-114">Remarks</span></span>

<span data-ttu-id="33899-115">Cette propriété contient une image de 32 x 32 pixels d’une icône, le même que le contenu d’un. Fichier ICO, mais seuls les pixels du coin supérieur gauche de 16 x 16 sont considérées comme importantes.</span><span class="sxs-lookup"><span data-stu-id="33899-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file, but only the upper left 16 × 16 pixels are considered significant.</span></span> <span data-ttu-id="33899-116">Cette propriété est normalement copiée à partir de la. Fichier ICO spécifié dans la ligne SmallIcon de la section [Description] appropriée du fichier de configuration du formulaire.</span><span class="sxs-lookup"><span data-stu-id="33899-116">This property is normally copied from the .ICO file specified in the SmallIcon line of the appropriate [Description] section of the form configuration file.</span></span>
  
 <span data-ttu-id="33899-117">**Remarque** Certaines plateformes de ne pas les icônes prise en charge 16 x 16 pixels.</span><span class="sxs-lookup"><span data-stu-id="33899-117">**Note** Some platforms do not support 16 × 16 pixel icons.</span></span> <span data-ttu-id="33899-118">Le format de 32 x 32 de cette propriété est utile dans ce cas, mais les applications clientes doivent être conscients de l’affichage incohérences.</span><span class="sxs-lookup"><span data-stu-id="33899-118">The 32 × 32 format of this property is usable in such a case but client applications should be aware of display inconsistencies.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="33899-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="33899-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="33899-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="33899-120">Header files</span></span>

<span data-ttu-id="33899-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="33899-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="33899-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="33899-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="33899-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="33899-123">Mapitags.h</span></span>
  
> <span data-ttu-id="33899-124">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="33899-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="33899-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33899-125">See also</span></span>



[<span data-ttu-id="33899-126">Propriété canonique PidTagIcon</span><span class="sxs-lookup"><span data-stu-id="33899-126">PidTagIcon Canonical Property</span></span>](pidtagicon-canonical-property.md)


[<span data-ttu-id="33899-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="33899-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="33899-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="33899-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="33899-129">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="33899-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="33899-130">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="33899-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

