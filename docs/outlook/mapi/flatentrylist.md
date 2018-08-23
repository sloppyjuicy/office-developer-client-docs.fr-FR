---
title: FLATENTRYLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATENTRYLIST
api_type:
- COM
ms.assetid: b465d015-9b62-4986-b0df-118121f60602
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 371d0305f8f00e66704bae03f93857c7275b6a10
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589818"
---
# <a name="flatentrylist"></a><span data-ttu-id="92109-103">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="92109-103">FLATENTRYLIST</span></span>

<span data-ttu-id="92109-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92109-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92109-105">Contient un tableau de structures [FLATENTRY](flatentry.md) .</span><span class="sxs-lookup"><span data-stu-id="92109-105">Contains an array of [FLATENTRY](flatentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92109-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="92109-106">Header file:</span></span>  <br/> |<span data-ttu-id="92109-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="92109-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="92109-108">Macros connexes :</span><span class="sxs-lookup"><span data-stu-id="92109-108">Related macros:</span></span>  <br/> |<span data-ttu-id="92109-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span><span class="sxs-lookup"><span data-stu-id="92109-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a><span data-ttu-id="92109-110">Members</span><span class="sxs-lookup"><span data-stu-id="92109-110">Members</span></span>

<span data-ttu-id="92109-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="92109-111">**cEntries**</span></span>
  
> <span data-ttu-id="92109-112">Nombre de structures **FLATENTRY** dans le tableau indiqué par le membre **abEntries** .</span><span class="sxs-lookup"><span data-stu-id="92109-112">Count of **FLATENTRY** structures in the array described by the **abEntries** member.</span></span> 
    
<span data-ttu-id="92109-113">**cbEntries**</span><span class="sxs-lookup"><span data-stu-id="92109-113">**cbEntries**</span></span>
  
> <span data-ttu-id="92109-114">Nombre d’octets dans le tableau décrit par **abEntries**.</span><span class="sxs-lookup"><span data-stu-id="92109-114">Count of bytes in the array described by **abEntries**.</span></span> 
    
<span data-ttu-id="92109-115">**abEntries**</span><span class="sxs-lookup"><span data-stu-id="92109-115">**abEntries**</span></span>
  
> <span data-ttu-id="92109-116">Tableau d’octets qui contient une ou plusieurs structures **FLATENTRY** , organisées de bout en bout.</span><span class="sxs-lookup"><span data-stu-id="92109-116">Byte array that contains one or more **FLATENTRY** structures, arranged end to end.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="92109-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="92109-117">Remarks</span></span>

<span data-ttu-id="92109-118">Dans le tableau **abEntries** , chaque structure **FLATENTRY** est aligné sur une limite alignée naturellement.</span><span class="sxs-lookup"><span data-stu-id="92109-118">In the **abEntries** array, each **FLATENTRY** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="92109-119">Octets supplémentaires sont inclus comme remplissage pour rendre l’alignement que naturel entre les deux structures **FLATENTRY** .</span><span class="sxs-lookup"><span data-stu-id="92109-119">Extra bytes are included as padding to make sure natural alignment between any two **FLATENTRY** structures.</span></span> <span data-ttu-id="92109-120">La première structure **FLATENTRY** dans le tableau est toujours alignée correctement, car le décalage du membre **abEntries** est 8.</span><span class="sxs-lookup"><span data-stu-id="92109-120">The first **FLATENTRY** structure in the array is always aligned correctly because the offset of the **abEntries** member is 8.</span></span> <span data-ttu-id="92109-121">Pour calculer le décalage de la structure suivante, utilisez la taille de la première entrée d’arrondi au multiple prochain de 4.</span><span class="sxs-lookup"><span data-stu-id="92109-121">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="92109-122">Utilisez la macro [CbFLATENTRY](cbflatentry.md) pour calculer la taille d’une structure **FLATENTRY** .</span><span class="sxs-lookup"><span data-stu-id="92109-122">Use the [CbFLATENTRY](cbflatentry.md) macro to compute the size of a **FLATENTRY** structure.</span></span> 
  
<span data-ttu-id="92109-123">Par exemple, la deuxième structure **FLATENTRY** commence à un décalage qui comprend le décalage de la première entrée ainsi que la longueur de la première entrée d’arrondi pour les quatre octets.</span><span class="sxs-lookup"><span data-stu-id="92109-123">For example, the second **FLATENTRY** structure starts at an offset that consists of the offset of the first entry plus the length of the first entry rounded to the next four bytes.</span></span> <span data-ttu-id="92109-124">La longueur de la première entrée est la longueur de ses membres **cb** ainsi que la longueur de ses membres **abEntry** .</span><span class="sxs-lookup"><span data-stu-id="92109-124">The length of the first entry is the length of its **cb** member plus the length of its **abEntry** member.</span></span> 
  
<span data-ttu-id="92109-125">L’exemple de code suivant indique comment calculer les décalages dans une structure **FLATENTRYLIST** .</span><span class="sxs-lookup"><span data-stu-id="92109-125">The following code sample indicates how to compute offsets in a **FLATENTRYLIST** structure.</span></span> <span data-ttu-id="92109-126">Supposons que _lpFlatEntry_ est un pointeur vers la première structure dans la liste.</span><span class="sxs-lookup"><span data-stu-id="92109-126">Assume that  _lpFlatEntry_ is a pointer to the first structure in the list.</span></span> 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a><span data-ttu-id="92109-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92109-127">See also</span></span>

- [<span data-ttu-id="92109-128">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="92109-128">FLATENTRY</span></span>](flatentry.md)
- [<span data-ttu-id="92109-129">Propriété canonique PidTagReplyRecipientEntries</span><span class="sxs-lookup"><span data-stu-id="92109-129">PidTagReplyRecipientEntries Canonical Property</span></span>](pidtagreplyrecipiententries-canonical-property.md)
- [<span data-ttu-id="92109-130">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="92109-130">MAPI Structures</span></span>](mapi-structures.md)

