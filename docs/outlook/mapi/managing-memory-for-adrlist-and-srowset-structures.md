---
title: Gestion de la mémoire pour les structures ADRLIST et SRowSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ef20cf8460aa7d3d160208109e42b2de66658d54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589727"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a><span data-ttu-id="de2d0-103">Gestion de la mémoire pour les structures ADRLIST et SRowSet »</span><span class="sxs-lookup"><span data-stu-id="de2d0-103">Managing memory for ADRLIST and SRowSet structures"</span></span>

<span data-ttu-id="de2d0-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de2d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de2d0-105">La condition requise pour allouer toute la mémoire pour une mémoire tampon de la mesure du possible avec un seul appel **MAPIAllocateBuffer** ne s’applique pas à l’aide de la liste d’adresses ou **ADRLIST**et jeu de lignes ou **SRowSet**, structures.</span><span class="sxs-lookup"><span data-stu-id="de2d0-105">The requirement to allocate all memory for a buffer whenever possible with a single **MAPIAllocateBuffer** call does not apply when using the address list, or **ADRLIST**, and row set, or **SRowSet**, structures.</span></span> 
  
<span data-ttu-id="de2d0-106">Ces deux structures sont des exceptions pour les règles standards d’allouer et de libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="de2d0-106">These two structures are exceptions to the standard rules for allocating and releasing memory.</span></span> <span data-ttu-id="de2d0-107">Ils contiennent plusieurs niveaux de structures et sont conçues pour permettre aux membres individuels être ajouté ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="de2d0-107">They contain multiple levels of structures and are designed to enable individual members to be added or removed.</span></span> <span data-ttu-id="de2d0-108">Par conséquent, chaque propriété doit être une affectation distincte.</span><span class="sxs-lookup"><span data-stu-id="de2d0-108">Therefore, each property must be a separate allocation.</span></span> 

<span data-ttu-id="de2d0-109">Où la plupart des structures sont libérées par un appel à **MAPIFreeBuffer**, chaque entrée individuelle dans une structure **ADRLIST** ou **SRowSet** doivent être libérée avec son propre appel à **MAPIFreeBuffer** ou un seul appel **FreeProws** ou ** FreePadrlist**.</span><span class="sxs-lookup"><span data-stu-id="de2d0-109">Where most structures are freed with one call to **MAPIFreeBuffer**, each individual entry in an **ADRLIST** or **SRowSet** structure must be freed with its own call to **MAPIFreeBuffer** or a single call to either **FreeProws** or **FreePadrlist**.</span></span> <span data-ttu-id="de2d0-110">Pour plus d’informations, voir [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md)et [SRowSet](srowset.md).</span><span class="sxs-lookup"><span data-stu-id="de2d0-110">For more information, see [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md), and [SRowSet](srowset.md).</span></span> 

<span data-ttu-id="de2d0-111">**FreeProws** et **FreePadrlist** sont des fonctions fournies par MAPI pour simplifier la libération de ces structures de données.</span><span class="sxs-lookup"><span data-stu-id="de2d0-111">**FreeProws** and **FreePadrlist** are functions provided by MAPI for simplifying the freeing of these data structures.</span></span> <span data-ttu-id="de2d0-112">Pour plus d’informations, voir [FreeProws](freeprows.md) et [FreePadrlist](freepadrlist.md).</span><span class="sxs-lookup"><span data-stu-id="de2d0-112">For more information, see [FreeProws](freeprows.md) and [FreePadrlist](freepadrlist.md).</span></span> <span data-ttu-id="de2d0-113">**FreePadrlist** libère de la mémoire pour la structure **ADRLIST** plus de mémoire tous les membres de la structure ; **FreeProws** effectue la même pour la structure **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="de2d0-113">**FreePadrlist** frees the memory for the **ADRLIST** structure plus all associated memory for the structure members; **FreeProws** does the same for the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="de2d0-114">Le diagramme suivant illustre la disposition d’une structure de données **ADRLIST** , indiquant les allocations de mémoire distinct requises.</span><span class="sxs-lookup"><span data-stu-id="de2d0-114">The following diagram shows the layout of an **ADRLIST** data structure, indicating the separate memory allocations required.</span></span> <span data-ttu-id="de2d0-115">Les zones grisées indiquent la mémoire pouvant être allouée et publié avec un seul appel.</span><span class="sxs-lookup"><span data-stu-id="de2d0-115">The gray boxes show memory that can be allocated and released with one call.</span></span> 
  
<span data-ttu-id="de2d0-116">**Allocation de mémoire ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="de2d0-116">**ADRLIST memory allocation**</span></span>
  
<span data-ttu-id="de2d0-117">![Allocation de mémoire ADRLIST] (media/amapi_52.gif "Allocation de mémoire ADRLIST")</span><span class="sxs-lookup"><span data-stu-id="de2d0-117">![ADRLIST memory allocation](media/amapi_52.gif "ADRLIST memory allocation")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="de2d0-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de2d0-118">See also</span></span>

- [<span data-ttu-id="de2d0-119">Gestion de la mémoire dans MAPI</span><span class="sxs-lookup"><span data-stu-id="de2d0-119">Managing Memory in MAPI</span></span>](managing-memory-in-mapi.md)

