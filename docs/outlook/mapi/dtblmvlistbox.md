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
ms.openlocfilehash: 0de5bf5d5bb4d8c5606e97bdbc6e70493609a05f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783234"
---
# <a name="dtblmvlistbox"></a><span data-ttu-id="776da-103">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="776da-103">DTBLMVLISTBOX</span></span>

  
  
<span data-ttu-id="776da-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="776da-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="776da-105">Décrit une liste à valeurs multiples qui s’affichera dans la boîte de dialogue qui est générée à partir d’un tableau d’affichage.</span><span class="sxs-lookup"><span data-stu-id="776da-105">Describes a multi-valued list that will be displayed in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="776da-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="776da-106">Header file:</span></span>  <br/> |<span data-ttu-id="776da-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="776da-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a><span data-ttu-id="776da-108">Membres</span><span class="sxs-lookup"><span data-stu-id="776da-108">Members</span></span>

 <span data-ttu-id="776da-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="776da-109">**ulFlags**</span></span>
  
> <span data-ttu-id="776da-110">Réservé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="776da-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="776da-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="776da-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="776da-112">Balise de propriété pour une propriété à valeurs multiples de type PT_MV_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="776da-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="776da-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="776da-113">Remarks</span></span>

<span data-ttu-id="776da-114">Une structure **DTBLMVLISTBOX** décrit une liste à valeurs multiples standard qui comporte une liste en lecture seule d’éléments.</span><span class="sxs-lookup"><span data-stu-id="776da-114">A **DTBLMVLISTBOX** structure describes a standard multi-valued list that has a read-only list of items.</span></span> <span data-ttu-id="776da-115">En utilisant une liste à valeurs multiples standard, les valeurs sont affichées immédiatement.</span><span class="sxs-lookup"><span data-stu-id="776da-115">By using a standard multi-valued list, the values are displayed immediately.</span></span> 
  
<span data-ttu-id="776da-116">Les données qui sont affichées provient de la propriété identifiée dans le membre **ulMVPropTag** .</span><span class="sxs-lookup"><span data-stu-id="776da-116">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="776da-117">Il n’existe aucune exigence pour lire à partir de l’interface de la propriété qui est associé à la table d’affichage.</span><span class="sxs-lookup"><span data-stu-id="776da-117">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="776da-118">En outre, étant donné que les utilisateurs ne sont pas en mesure de réaliser des sélections à partir de ces types de listes, données ne sont pas écrite à l’interface de la propriété.</span><span class="sxs-lookup"><span data-stu-id="776da-118">Also, because users are not able to make selections from these types of lists, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="776da-119">Uniquement les propriétés de type chaîne à valeurs multiples sont pris en charge pour la liste à valeurs multiples ; autres types de propriétés à valeurs multiples ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="776da-119">Only multi-valued string properties are supported for the multi-valued list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="776da-120">Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="776da-120">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="776da-121">Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="776da-121">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="776da-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="776da-122">See also</span></span>



[<span data-ttu-id="776da-123">DTCTL</span><span class="sxs-lookup"><span data-stu-id="776da-123">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="776da-124">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="776da-124">MAPI Structures</span></span>](mapi-structures.md)

