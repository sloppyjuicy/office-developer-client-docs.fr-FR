---
title: Propriété canonique PidLidLogFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidLogFlags
api_type:
- COM
ms.assetid: 3174d931-e045-44db-a203-a27c9c00f4fc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a407c065a51870ba9908fbd9b626d7f287a1df4e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387236"
---
# <a name="pidlidlogflags-canonical-property"></a><span data-ttu-id="55298-103">Propriété canonique PidLidLogFlags</span><span class="sxs-lookup"><span data-stu-id="55298-103">PidLidLogFlags Canonical Property</span></span>

  
  
<span data-ttu-id="55298-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55298-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55298-105">Contient des métadonnées sur la feuille.</span><span class="sxs-lookup"><span data-stu-id="55298-105">Contains metadata about the journal.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55298-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="55298-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="55298-107">dispidLogFlags</span><span class="sxs-lookup"><span data-stu-id="55298-107">dispidLogFlags</span></span>  <br/> |
|<span data-ttu-id="55298-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="55298-108">Property set:</span></span>  <br/> |<span data-ttu-id="55298-109">PSETID_Log</span><span class="sxs-lookup"><span data-stu-id="55298-109">PSETID_Log</span></span>  <br/> |
|<span data-ttu-id="55298-110">ID de type long (capot) :</span><span class="sxs-lookup"><span data-stu-id="55298-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="55298-111">0x0000870C</span><span class="sxs-lookup"><span data-stu-id="55298-111">0x0000870C</span></span>  <br/> |
|<span data-ttu-id="55298-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="55298-112">Data type:</span></span>  <br/> |<span data-ttu-id="55298-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="55298-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="55298-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="55298-114">Area:</span></span>  <br/> |<span data-ttu-id="55298-115">Journal</span><span class="sxs-lookup"><span data-stu-id="55298-115">Journal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55298-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="55298-116">Remarks</span></span>

<span data-ttu-id="55298-117">Le champ de bits qui contient des métadonnées relatives à la feuille doit être égale à zéro ou « 0 x 40000000 ».</span><span class="sxs-lookup"><span data-stu-id="55298-117">The bit field that contains metadata about the journal must be either zero or "0x40000000".</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="55298-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="55298-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="55298-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="55298-119">Protocol specifications</span></span>

<span data-ttu-id="55298-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55298-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55298-121">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="55298-121">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="55298-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="55298-122">[[MS-OXOJRNL]](https://msdn.microsoft.com/library/2aa04fd2-0f36-4ce4-9178-c0fc70aa8d43%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="55298-123">Spécifie les propriétés et les opérations qui sont autorisées pour les journaux.</span><span class="sxs-lookup"><span data-stu-id="55298-123">Specifies the properties and operations that are permissible for journals.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="55298-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="55298-124">Header files</span></span>

<span data-ttu-id="55298-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="55298-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="55298-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="55298-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="55298-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55298-127">See also</span></span>



[<span data-ttu-id="55298-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="55298-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="55298-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="55298-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="55298-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="55298-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="55298-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="55298-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

