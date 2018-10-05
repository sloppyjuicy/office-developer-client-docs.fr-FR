---
title: Propriété canonique PidTagIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIcon
api_type:
- HeaderDef
ms.assetid: 815dabf3-3cac-40e1-b6ff-51db2ff5096a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ad8d6934b5e57429de5039e9420742caa9dd4294
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397694"
---
# <a name="pidtagicon-canonical-property"></a><span data-ttu-id="f6b1d-103">Propriété canonique PidTagIcon</span><span class="sxs-lookup"><span data-stu-id="f6b1d-103">PidTagIcon Canonical Property</span></span>

  
  
<span data-ttu-id="f6b1d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f6b1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f6b1d-105">Contient un bitmap d’une icône de toute taille d’un formulaire.</span><span class="sxs-lookup"><span data-stu-id="f6b1d-105">Contains a bitmap of a full size icon for a form.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6b1d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f6b1d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f6b1d-107">PR_ICON</span><span class="sxs-lookup"><span data-stu-id="f6b1d-107">PR_ICON</span></span>  <br/> |
|<span data-ttu-id="f6b1d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f6b1d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f6b1d-109">0x0FFD</span><span class="sxs-lookup"><span data-stu-id="f6b1d-109">0x0FFD</span></span>  <br/> |
|<span data-ttu-id="f6b1d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f6b1d-110">Data type:</span></span>  <br/> |<span data-ttu-id="f6b1d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f6b1d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f6b1d-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f6b1d-112">Area:</span></span>  <br/> |<span data-ttu-id="f6b1d-113">MAPI non transmissible</span><span class="sxs-lookup"><span data-stu-id="f6b1d-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6b1d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f6b1d-114">Remarks</span></span>

<span data-ttu-id="f6b1d-115">Cette propriété contient une image de 32 x 32 pixels d’une icône, le même que le contenu d’un. Fichier ICO.</span><span class="sxs-lookup"><span data-stu-id="f6b1d-115">This property contains a 32 × 32 pixel image of an icon, the same as the contents of a .ICO file.</span></span> <span data-ttu-id="f6b1d-116">Cette propriété est normalement copiée à partir de la. Fichier ICO spécifié dans la ligne LargeIcon de la section [Description] appropriée du fichier de configuration du formulaire.</span><span class="sxs-lookup"><span data-stu-id="f6b1d-116">This property is normally copied from the .ICO file specified in the LargeIcon line of the appropriate [Description] section of the form configuration file.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f6b1d-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f6b1d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f6b1d-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="f6b1d-118">Protocol specifications</span></span>

<span data-ttu-id="f6b1d-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f6b1d-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f6b1d-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="f6b1d-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f6b1d-121">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f6b1d-121">Header files</span></span>

<span data-ttu-id="f6b1d-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f6b1d-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="f6b1d-123">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f6b1d-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="f6b1d-124">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="f6b1d-124">Mapitags.h</span></span>
  
> <span data-ttu-id="f6b1d-125">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="f6b1d-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f6b1d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6b1d-126">See also</span></span>



[<span data-ttu-id="f6b1d-127">Propriété canonique PidTagMiniIcon</span><span class="sxs-lookup"><span data-stu-id="f6b1d-127">PidTagMiniIcon Canonical Property</span></span>](pidtagminiicon-canonical-property.md)


[<span data-ttu-id="f6b1d-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f6b1d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f6b1d-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f6b1d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f6b1d-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f6b1d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f6b1d-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f6b1d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

