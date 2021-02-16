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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ae8f3ab28837bf0579549ead46c28477f815f35c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439701"
---
# <a name="dtblmvlistbox"></a><span data-ttu-id="53a80-103">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="53a80-103">DTBLMVLISTBOX</span></span>

  
  
<span data-ttu-id="53a80-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53a80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53a80-105">Décrit une liste à valeurs multiples qui sera affichée dans une boîte de dialogue qui est conçue à partir d’un tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="53a80-105">Describes a multi-valued list that will be displayed in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="53a80-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="53a80-106">Header file:</span></span>  <br/> |<span data-ttu-id="53a80-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53a80-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a><span data-ttu-id="53a80-108">Membres</span><span class="sxs-lookup"><span data-stu-id="53a80-108">Members</span></span>

 <span data-ttu-id="53a80-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="53a80-109">**ulFlags**</span></span>
  
> <span data-ttu-id="53a80-110">Réservé ; doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="53a80-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="53a80-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="53a80-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="53a80-112">Balise de propriété pour une propriété à valeurs multiples de type PT_MV_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="53a80-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="53a80-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="53a80-113">Remarks</span></span>

<span data-ttu-id="53a80-114">Une structure **DTBLMVLISTBOX** décrit une liste à valeurs multiples standard avec une liste d’éléments en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="53a80-114">A **DTBLMVLISTBOX** structure describes a standard multi-valued list that has a read-only list of items.</span></span> <span data-ttu-id="53a80-115">À l’aide d’une liste à valeurs multiples standard, les valeurs sont affichées immédiatement.</span><span class="sxs-lookup"><span data-stu-id="53a80-115">By using a standard multi-valued list, the values are displayed immediately.</span></span> 
  
<span data-ttu-id="53a80-116">Les données affichées proviennent de la propriété identifiée dans le **membre ulMVPropTag.**</span><span class="sxs-lookup"><span data-stu-id="53a80-116">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="53a80-117">Il n’est pas nécessaire de lire l’interface de propriétés associée au tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="53a80-117">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="53a80-118">En outre, étant donné que les utilisateurs ne sont pas en mesure d’effectuer des sélections à partir de ces types de listes, les données ne sont pas écrites dans l’interface des propriétés.</span><span class="sxs-lookup"><span data-stu-id="53a80-118">Also, because users are not able to make selections from these types of lists, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="53a80-119">Seules les propriétés de chaîne à valeurs multiples sont pris en charge pour la liste à valeurs multiples ; les autres types de propriétés à valeurs multiples ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="53a80-119">Only multi-valued string properties are supported for the multi-valued list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="53a80-120">Pour obtenir une vue d’ensemble des tableaux d’affichage, voir [Tableaux d’affichage.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="53a80-120">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="53a80-121">Pour plus d’informations sur l’implémentation d’un tableau d’affichage, voir [Implementing a Display Table](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="53a80-121">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="53a80-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53a80-122">See also</span></span>



[<span data-ttu-id="53a80-123">DTCTL</span><span class="sxs-lookup"><span data-stu-id="53a80-123">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="53a80-124">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="53a80-124">MAPI Structures</span></span>](mapi-structures.md)

