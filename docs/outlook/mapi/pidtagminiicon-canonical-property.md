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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5514e0553f719e2e875aad7001bb38a6a52e8e08
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589776"
---
# <a name="pidtagminiicon-canonical-property"></a><span data-ttu-id="1b188-103">Propriété canonique PidTagMiniIcon</span><span class="sxs-lookup"><span data-stu-id="1b188-103">PidTagMiniIcon Canonical Property</span></span>

  
  
<span data-ttu-id="1b188-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b188-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b188-105">Contient un bitmap d’une icône demi pour un formulaire.</span><span class="sxs-lookup"><span data-stu-id="1b188-105">Contains a bitmap of a half-size icon for a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1b188-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="1b188-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1b188-107">PR_MINI_ICON</span><span class="sxs-lookup"><span data-stu-id="1b188-107">PR_MINI_ICON</span></span>  <br/> |
|<span data-ttu-id="1b188-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="1b188-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1b188-109">0x0FFC</span><span class="sxs-lookup"><span data-stu-id="1b188-109">0x0FFC</span></span>  <br/> |
|<span data-ttu-id="1b188-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1b188-110">Data type:</span></span>  <br/> |<span data-ttu-id="1b188-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1b188-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1b188-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="1b188-112">Area:</span></span>  <br/> |<span data-ttu-id="1b188-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="1b188-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b188-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1b188-114">Remarks</span></span>

<span data-ttu-id="1b188-115">Cette propriété contient une image de 32 x 32 pixels d’une icône, le même que le contenu d’un. Fichier ICO, mais seuls les pixels du coin supérieur gauche de 16 x 16 sont considérées comme importantes.</span><span class="sxs-lookup"><span data-stu-id="1b188-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file, but only the upper left 16 × 16 pixels are considered significant.</span></span> <span data-ttu-id="1b188-116">Cette propriété est normalement copiée à partir de la. Fichier ICO spécifié dans la ligne SmallIcon de la section [Description] appropriée du fichier de configuration du formulaire.</span><span class="sxs-lookup"><span data-stu-id="1b188-116">This property is normally copied from the .ICO file specified in the SmallIcon line of the appropriate [Description] section of the form configuration file.</span></span>
  
 <span data-ttu-id="1b188-117">**Remarque** Certaines plateformes de ne pas les icônes prise en charge 16 x 16 pixels.</span><span class="sxs-lookup"><span data-stu-id="1b188-117">**Note** Some platforms do not support 16 × 16 pixel icons.</span></span> <span data-ttu-id="1b188-118">Le format de 32 x 32 de cette propriété est utile dans ce cas, mais les applications clientes doivent être conscients de l’affichage incohérences.</span><span class="sxs-lookup"><span data-stu-id="1b188-118">The 32 × 32 format of this property is usable in such a case but client applications should be aware of display inconsistencies.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1b188-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1b188-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1b188-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1b188-120">Header files</span></span>

<span data-ttu-id="1b188-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1b188-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="1b188-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1b188-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="1b188-123">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="1b188-123">Mapitags.h</span></span>
  
> <span data-ttu-id="1b188-124">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="1b188-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b188-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b188-125">See also</span></span>



[<span data-ttu-id="1b188-126">Propriété canonique PidTagIcon</span><span class="sxs-lookup"><span data-stu-id="1b188-126">PidTagIcon Canonical Property</span></span>](pidtagicon-canonical-property.md)


[<span data-ttu-id="1b188-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1b188-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1b188-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1b188-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1b188-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1b188-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1b188-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="1b188-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

