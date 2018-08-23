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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 910f779f3463ee5dccd052655a442ef24c2cce58
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570680"
---
# <a name="dtblmvddlbox"></a><span data-ttu-id="3a560-103">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="3a560-103">DTBLMVDDLBOX</span></span>

  
  
<span data-ttu-id="3a560-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a560-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a560-105">Décrit une liste déroulante qui sera utilisée dans une boîte de dialogue qui est générée à partir d’un tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="3a560-105">Describes a drop-down list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3a560-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="3a560-106">Header file:</span></span>  <br/> |<span data-ttu-id="3a560-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3a560-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a><span data-ttu-id="3a560-108">Members</span><span class="sxs-lookup"><span data-stu-id="3a560-108">Members</span></span>

 <span data-ttu-id="3a560-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="3a560-109">**ulFlags**</span></span>
  
> <span data-ttu-id="3a560-110">Réservé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="3a560-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="3a560-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="3a560-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="3a560-112">Balise de propriété pour une propriété à valeurs multiples de type PT_MV_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="3a560-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span> <span data-ttu-id="3a560-113">Les différentes valeurs de cette propriété sont affichent comme des entrées distinctes dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="3a560-113">The different values of this property are displayed as distinct entries in the drop-down list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3a560-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="3a560-114">Remarks</span></span>

<span data-ttu-id="3a560-115">Une structure **DTBLMVDDLBOX** décrit une liste déroulante à valeurs multiples une liste en lecture seule d’éléments.</span><span class="sxs-lookup"><span data-stu-id="3a560-115">A **DTBLMVDDLBOX** structure describes a multi-valued drop-down list a read-only list of items.</span></span> <span data-ttu-id="3a560-116">En utilisant une liste déroulante à valeurs multiples, les valeurs sont affichées lorsqu’un utilisateur clique sur une barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="3a560-116">By using a multi-valued drop-down list, values are displayed when a user clicks on a scroll bar.</span></span> 
  
<span data-ttu-id="3a560-117">Les données qui sont affichées provient de la propriété identifiée dans le membre **ulMVPropTag** .</span><span class="sxs-lookup"><span data-stu-id="3a560-117">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="3a560-118">Il n’existe aucune exigence pour lire à partir de l’interface de la propriété qui est associé à la table d’affichage.</span><span class="sxs-lookup"><span data-stu-id="3a560-118">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="3a560-119">En outre, étant donné que les utilisateurs ne sont pas en mesure de réaliser des sélections à partir de ces types de zones de liste, données ne sont pas écrite à l’interface de la propriété.</span><span class="sxs-lookup"><span data-stu-id="3a560-119">Also, because users are not able to make selections from these types of list boxes, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="3a560-120">Uniquement les propriétés de type chaîne à valeurs multiples sont pris en charge pour la liste déroulante à valeurs multiples ; autres types de propriétés à valeurs multiples ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3a560-120">Only multi-valued string properties are supported for the multi-valued drop-down list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="3a560-121">Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="3a560-121">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="3a560-122">Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="3a560-122">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3a560-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a560-123">See also</span></span>



[<span data-ttu-id="3a560-124">DTCTL</span><span class="sxs-lookup"><span data-stu-id="3a560-124">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="3a560-125">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="3a560-125">MAPI Structures</span></span>](mapi-structures.md)

