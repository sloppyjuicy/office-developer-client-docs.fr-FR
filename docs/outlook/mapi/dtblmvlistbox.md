---
title: DTBLMVLISTBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVLISTBOX
api_type:
- COM
ms.assetid: 1c22f842-d0e7-44f0-a7d5-c9c2aa6b8820
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ae8f3ab28837bf0579549ead46c28477f815f35c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338275"
---
# <a name="dtblmvlistbox"></a><span data-ttu-id="35472-103">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="35472-103">DTBLMVLISTBOX</span></span>

  
  
<span data-ttu-id="35472-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35472-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35472-105">Décrit une liste à plusieurs valeurs qui s'affiche dans une boîte de dialogue créée à partir d'une table d'affichage.</span><span class="sxs-lookup"><span data-stu-id="35472-105">Describes a multi-valued list that will be displayed in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="35472-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="35472-106">Header file:</span></span>  <br/> |<span data-ttu-id="35472-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="35472-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a><span data-ttu-id="35472-108">Membres</span><span class="sxs-lookup"><span data-stu-id="35472-108">Members</span></span>

 <span data-ttu-id="35472-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="35472-109">**ulFlags**</span></span>
  
> <span data-ttu-id="35472-110">MSR doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="35472-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="35472-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="35472-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="35472-112">Balise de propriété pour une propriété à valeurs multiples de type PT_MV_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="35472-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="35472-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="35472-113">Remarks</span></span>

<span data-ttu-id="35472-114">Une structure **DTBLMVLISTBOX** décrit une liste à plusieurs valeurs standard qui contient une liste d'éléments en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="35472-114">A **DTBLMVLISTBOX** structure describes a standard multi-valued list that has a read-only list of items.</span></span> <span data-ttu-id="35472-115">À l'aide d'une liste à plusieurs valeurs standard, les valeurs s'affichent immédiatement.</span><span class="sxs-lookup"><span data-stu-id="35472-115">By using a standard multi-valued list, the values are displayed immediately.</span></span> 
  
<span data-ttu-id="35472-116">Les données affichées proviennent de la propriété identifiée dans le membre **ulMVPropTag** .</span><span class="sxs-lookup"><span data-stu-id="35472-116">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="35472-117">Il n'existe aucun besoin de lire à partir de l'interface de propriétés associée à la table d'affichage.</span><span class="sxs-lookup"><span data-stu-id="35472-117">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="35472-118">En outre, étant donné que les utilisateurs ne peuvent pas effectuer des sélections à partir de ces types de listes, les données ne sont pas écrites dans l'interface de propriété.</span><span class="sxs-lookup"><span data-stu-id="35472-118">Also, because users are not able to make selections from these types of lists, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="35472-119">Seules les propriétés de chaîne à valeurs multiples sont prises en charge pour la liste à valeurs multiples; les autres types de propriétés à valeurs multiples ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="35472-119">Only multi-valued string properties are supported for the multi-valued list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="35472-120">Pour une vue d'ensemble des tables d'affichage, voir [afficher les tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="35472-120">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="35472-121">Pour plus d'informations sur l'implémentation d'une table d'affichage, voir [Implementing a Display table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="35472-121">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="35472-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35472-122">See also</span></span>



[<span data-ttu-id="35472-123">DTCTL</span><span class="sxs-lookup"><span data-stu-id="35472-123">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="35472-124">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="35472-124">MAPI Structures</span></span>](mapi-structures.md)

