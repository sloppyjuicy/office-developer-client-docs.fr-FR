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
ms.openlocfilehash: ea7f9e0ed57c56b48399b9ffd1ea42db28daf249
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356230"
---
# <a name="pidtagminiicon-canonical-property"></a><span data-ttu-id="df34e-103">Propriété canonique PidTagMiniIcon</span><span class="sxs-lookup"><span data-stu-id="df34e-103">PidTagMiniIcon Canonical Property</span></span>

  
  
<span data-ttu-id="df34e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df34e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df34e-105">Contient une image bitmap d'une icône de demi-taille pour un formulaire.</span><span class="sxs-lookup"><span data-stu-id="df34e-105">Contains a bitmap of a half-size icon for a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="df34e-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="df34e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="df34e-107">PR_MINI_ICON</span><span class="sxs-lookup"><span data-stu-id="df34e-107">PR_MINI_ICON</span></span>  <br/> |
|<span data-ttu-id="df34e-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="df34e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="df34e-109">0x0FFC</span><span class="sxs-lookup"><span data-stu-id="df34e-109">0x0FFC</span></span>  <br/> |
|<span data-ttu-id="df34e-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="df34e-110">Data type:</span></span>  <br/> |<span data-ttu-id="df34e-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="df34e-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="df34e-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="df34e-112">Area:</span></span>  <br/> |<span data-ttu-id="df34e-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="df34e-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df34e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="df34e-114">Remarks</span></span>

<span data-ttu-id="df34e-115">Cette propriété contient une image 32 × 32 pixels d'une icône, le même que le contenu d'un. Fichier. ICO, mais seuls les 16 × 16 pixels du coin supérieur gauche sont considérés comme significatifs.</span><span class="sxs-lookup"><span data-stu-id="df34e-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file, but only the upper left 16 × 16 pixels are considered significant.</span></span> <span data-ttu-id="df34e-116">Cette propriété est généralement copiée à partir du. Fichier. ICO spécifié dans la ligne SmallIcon de la section [Description] appropriée du fichier de configuration du formulaire.</span><span class="sxs-lookup"><span data-stu-id="df34e-116">This property is normally copied from the .ICO file specified in the SmallIcon line of the appropriate [Description] section of the form configuration file.</span></span>
  
 <span data-ttu-id="df34e-117">**Note** Certaines plateformes ne prennent pas en charge les icônes 16 x 16 pixels.</span><span class="sxs-lookup"><span data-stu-id="df34e-117">**Note** Some platforms do not support 16 × 16 pixel icons.</span></span> <span data-ttu-id="df34e-118">Le format 32 × 32 de cette propriété est utilisable dans ce cas, mais les applications clientes doivent être conscientes des incohérences d'affichage.</span><span class="sxs-lookup"><span data-stu-id="df34e-118">The 32 × 32 format of this property is usable in such a case but client applications should be aware of display inconsistencies.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="df34e-119">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="df34e-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="df34e-120">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="df34e-120">Header files</span></span>

<span data-ttu-id="df34e-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="df34e-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="df34e-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="df34e-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="df34e-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="df34e-123">Mapitags.h</span></span>
  
> <span data-ttu-id="df34e-124">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="df34e-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="df34e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df34e-125">See also</span></span>



[<span data-ttu-id="df34e-126">Propriété canonique PidTagIcon</span><span class="sxs-lookup"><span data-stu-id="df34e-126">PidTagIcon Canonical Property</span></span>](pidtagicon-canonical-property.md)


[<span data-ttu-id="df34e-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="df34e-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="df34e-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="df34e-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="df34e-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="df34e-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="df34e-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="df34e-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

