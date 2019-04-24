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
ms.openlocfilehash: 33b4fd87f33c26db15e1a6a28f077c393168db91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325759"
---
# <a name="dtblmvddlbox"></a><span data-ttu-id="7f53e-103">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="7f53e-103">DTBLMVDDLBOX</span></span>

  
  
<span data-ttu-id="7f53e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f53e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f53e-105">Décrit une liste déroulante qui sera utilisée dans une boîte de dialogue créée à partir d'une table d'affichage.</span><span class="sxs-lookup"><span data-stu-id="7f53e-105">Describes a drop-down list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f53e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="7f53e-106">Header file:</span></span>  <br/> |<span data-ttu-id="7f53e-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7f53e-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a><span data-ttu-id="7f53e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7f53e-108">Members</span></span>

 <span data-ttu-id="7f53e-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="7f53e-109">**ulFlags**</span></span>
  
> <span data-ttu-id="7f53e-110">MSR doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="7f53e-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="7f53e-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="7f53e-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="7f53e-112">Balise de propriété pour une propriété à valeurs multiples de type PT_MV_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="7f53e-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span> <span data-ttu-id="7f53e-113">Les différentes valeurs de cette propriété sont affichées sous forme d'entrées distinctes dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="7f53e-113">The different values of this property are displayed as distinct entries in the drop-down list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7f53e-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="7f53e-114">Remarks</span></span>

<span data-ttu-id="7f53e-115">Une structure **DTBLMVDDLBOX** décrit une liste déroulante à valeurs multiples, une liste d'éléments en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7f53e-115">A **DTBLMVDDLBOX** structure describes a multi-valued drop-down list a read-only list of items.</span></span> <span data-ttu-id="7f53e-116">À l'aide d'une liste déroulante à valeurs multiples, les valeurs s'affichent lorsqu'un utilisateur clique sur une barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="7f53e-116">By using a multi-valued drop-down list, values are displayed when a user clicks on a scroll bar.</span></span> 
  
<span data-ttu-id="7f53e-117">Les données affichées proviennent de la propriété identifiée dans le membre **ulMVPropTag** .</span><span class="sxs-lookup"><span data-stu-id="7f53e-117">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="7f53e-118">Il n'existe aucun besoin de lire à partir de l'interface de propriétés associée à la table d'affichage.</span><span class="sxs-lookup"><span data-stu-id="7f53e-118">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="7f53e-119">En outre, étant donné que les utilisateurs ne peuvent pas effectuer des sélections à partir de ces types de zones de liste, les données ne sont pas écrites dans l'interface de propriété.</span><span class="sxs-lookup"><span data-stu-id="7f53e-119">Also, because users are not able to make selections from these types of list boxes, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="7f53e-120">Seules les propriétés de chaîne à valeurs multiples sont prises en charge pour la liste déroulante à valeurs multiples; les autres types de propriétés à valeurs multiples ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7f53e-120">Only multi-valued string properties are supported for the multi-valued drop-down list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="7f53e-121">Pour une vue d'ensemble des tables d'affichage, voir [afficher les tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="7f53e-121">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="7f53e-122">Pour plus d'informations sur l'implémentation d'une table d'affichage, voir [Implementing a Display table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="7f53e-122">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7f53e-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f53e-123">See also</span></span>



[<span data-ttu-id="7f53e-124">DTCTL</span><span class="sxs-lookup"><span data-stu-id="7f53e-124">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="7f53e-125">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="7f53e-125">MAPI Structures</span></span>](mapi-structures.md)

