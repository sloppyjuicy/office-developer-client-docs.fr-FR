---
title: Propriété canonique PidTagInitialDetailsPane
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInitialDetailsPane
api_type:
- HeaderDef
ms.assetid: c4712133-6fbd-4c50-a258-5f4317120476
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 884bbad509e459d4f329e6468dd99124cec6c7d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786090"
---
# <a name="pidtaginitialdetailspane-canonical-property"></a><span data-ttu-id="90e3d-103">Propriété canonique PidTagInitialDetailsPane</span><span class="sxs-lookup"><span data-stu-id="90e3d-103">PidTagInitialDetailsPane Canonical Property</span></span>

  
  
<span data-ttu-id="90e3d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="90e3d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="90e3d-105">Indique la page d’un modèle d’affichage pour afficher le premier.</span><span class="sxs-lookup"><span data-stu-id="90e3d-105">Indicates the page of a display template to display first.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="90e3d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="90e3d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="90e3d-107">PR_INITIAL_DETAILS_PANE</span><span class="sxs-lookup"><span data-stu-id="90e3d-107">PR_INITIAL_DETAILS_PANE</span></span>  <br/> |
|<span data-ttu-id="90e3d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="90e3d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="90e3d-109">0x3F08</span><span class="sxs-lookup"><span data-stu-id="90e3d-109">0x3F08</span></span>  <br/> |
|<span data-ttu-id="90e3d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="90e3d-110">Data type:</span></span>  <br/> |<span data-ttu-id="90e3d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="90e3d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="90e3d-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="90e3d-112">Area:</span></span>  <br/> |<span data-ttu-id="90e3d-113">Afficher des Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="90e3d-113">MAPI Display Tables</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90e3d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="90e3d-114">Remarks</span></span>

<span data-ttu-id="90e3d-115">Il doit être présent sur tous les objets de carnet d’adresses sur un serveur du Service fournisseur Interface NSPI (Name) et doit avoir la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="90e3d-115">It must be present on all address book objects on an Name Service Provider Interface (NSPI) server, and must have the value zero (0).</span></span> <span data-ttu-id="90e3d-116">Il ne doit pas être défini pour tous les objets dans un carnet d’adresses en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="90e3d-116">It must not be defined for any objects in an Offline Address Book.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="90e3d-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="90e3d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="90e3d-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="90e3d-118">Protocol specifications</span></span>

<span data-ttu-id="90e3d-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90e3d-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90e3d-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="90e3d-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="90e3d-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90e3d-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90e3d-122">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="90e3d-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="90e3d-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="90e3d-123">Header files</span></span>

<span data-ttu-id="90e3d-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="90e3d-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="90e3d-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="90e3d-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="90e3d-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="90e3d-126">Mapitags.h</span></span>
  
> <span data-ttu-id="90e3d-127">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="90e3d-127">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90e3d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90e3d-128">See also</span></span>



[<span data-ttu-id="90e3d-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="90e3d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="90e3d-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="90e3d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="90e3d-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="90e3d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="90e3d-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="90e3d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

