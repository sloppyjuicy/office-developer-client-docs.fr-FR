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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bc511ea4b3ec4eea9e38f744bcb8f277108085cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413856"
---
# <a name="flatentrylist"></a><span data-ttu-id="b8221-103">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="b8221-103">FLATENTRYLIST</span></span>

<span data-ttu-id="b8221-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8221-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8221-105">Contient un tableau de structures [FLATENTRY.](flatentry.md)</span><span class="sxs-lookup"><span data-stu-id="b8221-105">Contains an array of [FLATENTRY](flatentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b8221-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b8221-106">Header file:</span></span>  <br/> |<span data-ttu-id="b8221-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b8221-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b8221-108">Macros associées :</span><span class="sxs-lookup"><span data-stu-id="b8221-108">Related macros:</span></span>  <br/> |<span data-ttu-id="b8221-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span><span class="sxs-lookup"><span data-stu-id="b8221-109">[CbFLATENTRYLIST](cbflatentrylist.md), [CbNewFLATENTRYLIST](cbnewflatentrylist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cEntries;
  ULONG cbEntries;
  BYTE abEntries[MAPI_DIM];
} FLATENTRYLIST, FAR *LPFLATENTRYLIST;

```

## <a name="members"></a><span data-ttu-id="b8221-110">Members</span><span class="sxs-lookup"><span data-stu-id="b8221-110">Members</span></span>

<span data-ttu-id="b8221-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="b8221-111">**cEntries**</span></span>
  
> <span data-ttu-id="b8221-112">Nombre de structures **FLATENTRY** dans le tableau décrit par le **membre abEntries.**</span><span class="sxs-lookup"><span data-stu-id="b8221-112">Count of **FLATENTRY** structures in the array described by the **abEntries** member.</span></span> 
    
<span data-ttu-id="b8221-113">**cbEntries**</span><span class="sxs-lookup"><span data-stu-id="b8221-113">**cbEntries**</span></span>
  
> <span data-ttu-id="b8221-114">Nombre d’octets dans le tableau décrit par **abEntries**.</span><span class="sxs-lookup"><span data-stu-id="b8221-114">Count of bytes in the array described by **abEntries**.</span></span> 
    
<span data-ttu-id="b8221-115">**abEntries**</span><span class="sxs-lookup"><span data-stu-id="b8221-115">**abEntries**</span></span>
  
> <span data-ttu-id="b8221-116">Tableau d’bytes qui contient une ou plusieurs structures **FLATENTRY,** organisées de bout en bout.</span><span class="sxs-lookup"><span data-stu-id="b8221-116">Byte array that contains one or more **FLATENTRY** structures, arranged end to end.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b8221-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="b8221-117">Remarks</span></span>

<span data-ttu-id="b8221-118">Dans le **tableau abEntries,** chaque structure **FLATENTRY** est alignée sur une limite alignée naturellement.</span><span class="sxs-lookup"><span data-stu-id="b8221-118">In the **abEntries** array, each **FLATENTRY** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="b8221-119">Des octets supplémentaires sont inclus comme remplissage pour assurer un alignement naturel entre deux structures **FLATENTRY.**</span><span class="sxs-lookup"><span data-stu-id="b8221-119">Extra bytes are included as padding to make sure natural alignment between any two **FLATENTRY** structures.</span></span> <span data-ttu-id="b8221-120">La première structure **FLATENTRY** du tableau est toujours alignée correctement, car le décalage du membre **abEntries** est 8.</span><span class="sxs-lookup"><span data-stu-id="b8221-120">The first **FLATENTRY** structure in the array is always aligned correctly because the offset of the **abEntries** member is 8.</span></span> <span data-ttu-id="b8221-121">Pour calculer le décalage de la structure suivante, utilisez la taille de la première entrée arrondie au multiple suivant de 4.</span><span class="sxs-lookup"><span data-stu-id="b8221-121">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="b8221-122">Utilisez la macro [CbFLATENTRY](cbflatentry.md) pour calculer la taille d’une structure **FLATENTRY.**</span><span class="sxs-lookup"><span data-stu-id="b8221-122">Use the [CbFLATENTRY](cbflatentry.md) macro to compute the size of a **FLATENTRY** structure.</span></span> 
  
<span data-ttu-id="b8221-123">Par exemple, la deuxième structure **FLATENTRY** commence par un décalage qui se compose du décalage de la première entrée plus la longueur de la première entrée arrondie aux quatre octets suivants.</span><span class="sxs-lookup"><span data-stu-id="b8221-123">For example, the second **FLATENTRY** structure starts at an offset that consists of the offset of the first entry plus the length of the first entry rounded to the next four bytes.</span></span> <span data-ttu-id="b8221-124">La longueur de la première entrée est la longueur de son membre **cb** ainsi que la longueur de son **membre abEntry.**</span><span class="sxs-lookup"><span data-stu-id="b8221-124">The length of the first entry is the length of its **cb** member plus the length of its **abEntry** member.</span></span> 
  
<span data-ttu-id="b8221-125">L’exemple de code suivant indique comment calculer des décalages dans une structure **FLATENTRYLIST.**</span><span class="sxs-lookup"><span data-stu-id="b8221-125">The following code sample indicates how to compute offsets in a **FLATENTRYLIST** structure.</span></span> <span data-ttu-id="b8221-126">Supposons  _que lpFlatEntry_ est un pointeur vers la première structure de la liste.</span><span class="sxs-lookup"><span data-stu-id="b8221-126">Assume that  _lpFlatEntry_ is a pointer to the first structure in the list.</span></span> 
  
```cpp
(offsetof(lpFlatEntry->ab) // for example, 4
+ lpFlatEntry->cb // size of lpFlatEntry->ab 
+ 4) & ~3 // round to next 4 byte boundary
```

## <a name="see-also"></a><span data-ttu-id="b8221-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8221-127">See also</span></span>

- [<span data-ttu-id="b8221-128">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="b8221-128">FLATENTRY</span></span>](flatentry.md)
- [<span data-ttu-id="b8221-129">Propriété canonique PidTagReplyRecipientEntries</span><span class="sxs-lookup"><span data-stu-id="b8221-129">PidTagReplyRecipientEntries Canonical Property</span></span>](pidtagreplyrecipiententries-canonical-property.md)
- [<span data-ttu-id="b8221-130">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="b8221-130">MAPI Structures</span></span>](mapi-structures.md)

