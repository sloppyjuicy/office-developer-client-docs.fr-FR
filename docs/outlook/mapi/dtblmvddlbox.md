---
title: DTBLMVDDLBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVDDLBOX
api_type:
- COM
ms.assetid: 0e6283dc-9a08-460f-9400-03f0ceb4081c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ede0a448a32565446e614fc2d14f2a72a9549dad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783236"
---
# <a name="dtblmvddlbox"></a><span data-ttu-id="c9906-103">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="c9906-103">DTBLMVDDLBOX</span></span>

  
  
<span data-ttu-id="c9906-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c9906-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c9906-105">Décrit une liste déroulante qui sera utilisée dans une boîte de dialogue qui est générée à partir d’un tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c9906-105">Describes a drop-down list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c9906-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c9906-106">Header file:</span></span>  <br/> |<span data-ttu-id="c9906-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9906-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a><span data-ttu-id="c9906-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c9906-108">Members</span></span>

 <span data-ttu-id="c9906-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="c9906-109">**ulFlags**</span></span>
  
> <span data-ttu-id="c9906-110">Réservé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="c9906-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="c9906-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="c9906-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="c9906-112">Balise de propriété pour une propriété à valeurs multiples de type PT_MV_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="c9906-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span> <span data-ttu-id="c9906-113">Les différentes valeurs de cette propriété sont affichent comme des entrées distinctes dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="c9906-113">The different values of this property are displayed as distinct entries in the drop-down list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c9906-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c9906-114">Remarks</span></span>

<span data-ttu-id="c9906-115">Une structure **DTBLMVDDLBOX** décrit une liste déroulante à valeurs multiples une liste en lecture seule d’éléments.</span><span class="sxs-lookup"><span data-stu-id="c9906-115">A **DTBLMVDDLBOX** structure describes a multi-valued drop-down list a read-only list of items.</span></span> <span data-ttu-id="c9906-116">En utilisant une liste déroulante à valeurs multiples, les valeurs sont affichées lorsqu’un utilisateur clique sur une barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="c9906-116">By using a multi-valued drop-down list, values are displayed when a user clicks on a scroll bar.</span></span> 
  
<span data-ttu-id="c9906-117">Les données qui sont affichées provient de la propriété identifiée dans le membre **ulMVPropTag** .</span><span class="sxs-lookup"><span data-stu-id="c9906-117">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="c9906-118">Il n’existe aucune exigence pour lire à partir de l’interface de la propriété qui est associé à la table d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c9906-118">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="c9906-119">En outre, étant donné que les utilisateurs ne sont pas en mesure de réaliser des sélections à partir de ces types de zones de liste, données ne sont pas écrite à l’interface de la propriété.</span><span class="sxs-lookup"><span data-stu-id="c9906-119">Also, because users are not able to make selections from these types of list boxes, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="c9906-120">Uniquement les propriétés de type chaîne à valeurs multiples sont pris en charge pour la liste déroulante à valeurs multiples ; autres types de propriétés à valeurs multiples ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c9906-120">Only multi-valued string properties are supported for the multi-valued drop-down list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="c9906-121">Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c9906-121">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="c9906-122">Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="c9906-122">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c9906-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9906-123">See also</span></span>



[<span data-ttu-id="c9906-124">DTCTL</span><span class="sxs-lookup"><span data-stu-id="c9906-124">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="c9906-125">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="c9906-125">MAPI Structures</span></span>](mapi-structures.md)

