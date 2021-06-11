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
ms.openlocfilehash: ea7f9e0ed57c56b48399b9ffd1ea42db28daf249
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405414"
---
# <a name="pidtagminiicon-canonical-property"></a><span data-ttu-id="093fd-103">Propriété canonique PidTagMiniIcon</span><span class="sxs-lookup"><span data-stu-id="093fd-103">PidTagMiniIcon Canonical Property</span></span>

  
  
<span data-ttu-id="093fd-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="093fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="093fd-105">Contient une image bitmap d’une icône à demi-taille pour un formulaire.</span><span class="sxs-lookup"><span data-stu-id="093fd-105">Contains a bitmap of a half-size icon for a form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="093fd-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="093fd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="093fd-107">PR_MINI_ICON</span><span class="sxs-lookup"><span data-stu-id="093fd-107">PR_MINI_ICON</span></span>  <br/> |
|<span data-ttu-id="093fd-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="093fd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="093fd-109">0x0FFC</span><span class="sxs-lookup"><span data-stu-id="093fd-109">0x0FFC</span></span>  <br/> |
|<span data-ttu-id="093fd-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="093fd-110">Data type:</span></span>  <br/> |<span data-ttu-id="093fd-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="093fd-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="093fd-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="093fd-112">Area:</span></span>  <br/> |<span data-ttu-id="093fd-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="093fd-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="093fd-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="093fd-114">Remarks</span></span>

<span data-ttu-id="093fd-115">Cette propriété contient une image de 32 × 32 pixels d’une icône, identique au contenu d’un . Le fichier ICO, mais seul le coin supérieur gauche de 16 × 16 pixels est considéré comme significatif.</span><span class="sxs-lookup"><span data-stu-id="093fd-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file, but only the upper left 16 × 16 pixels are considered significant.</span></span> <span data-ttu-id="093fd-116">Cette propriété est normalement copiée à partir du . Fichier ICO spécifié dans la ligne SmallIcon de la section [Description] appropriée du fichier de configuration du formulaire.</span><span class="sxs-lookup"><span data-stu-id="093fd-116">This property is normally copied from the .ICO file specified in the SmallIcon line of the appropriate [Description] section of the form configuration file.</span></span>
  
 <span data-ttu-id="093fd-117">**Remarque** Certaines plateformes ne supportent pas les icônes de 16 × 16 pixels.</span><span class="sxs-lookup"><span data-stu-id="093fd-117">**Note** Some platforms do not support 16 × 16 pixel icons.</span></span> <span data-ttu-id="093fd-118">Le format 32 × 32 de cette propriété est utilisable dans ce cas, mais les applications clientes doivent être sensibles aux incohérences d’affichage.</span><span class="sxs-lookup"><span data-stu-id="093fd-118">The 32 × 32 format of this property is usable in such a case but client applications should be aware of display inconsistencies.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="093fd-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="093fd-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="093fd-120">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="093fd-120">Header files</span></span>

<span data-ttu-id="093fd-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="093fd-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="093fd-122">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="093fd-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="093fd-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="093fd-123">Mapitags.h</span></span>
  
> <span data-ttu-id="093fd-124">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="093fd-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="093fd-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="093fd-125">See also</span></span>



[<span data-ttu-id="093fd-126">Propriété canonique PidTagIcon</span><span class="sxs-lookup"><span data-stu-id="093fd-126">PidTagIcon Canonical Property</span></span>](pidtagicon-canonical-property.md)


[<span data-ttu-id="093fd-127">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="093fd-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="093fd-128">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="093fd-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="093fd-129">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="093fd-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="093fd-130">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="093fd-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

