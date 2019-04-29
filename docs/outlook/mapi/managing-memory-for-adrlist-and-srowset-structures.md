---
title: Gestion de la mémoire des structures ADRLIST et SRowSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a5636cad7cad23bb5114bdbd34aff48c3639773b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407864"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a><span data-ttu-id="5b073-103">Gestion de la mémoire pour les structures ADRLIST et SRowSet</span><span class="sxs-lookup"><span data-stu-id="5b073-103">Managing memory for ADRLIST and SRowSet structures"</span></span>

<span data-ttu-id="5b073-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b073-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b073-105">La nécessité d'allouer toute la mémoire d'une mémoire tampon dans la mesure du possible avec un seul appel **MAPIAllocateBuffer** ne s'applique pas lorsque vous utilisez la liste d'adresses, ou **ADRLIST**et le jeu de lignes, ou **SRowSet**, structures.</span><span class="sxs-lookup"><span data-stu-id="5b073-105">The requirement to allocate all memory for a buffer whenever possible with a single **MAPIAllocateBuffer** call does not apply when using the address list, or **ADRLIST**, and row set, or **SRowSet**, structures.</span></span> 
  
<span data-ttu-id="5b073-106">Ces deux structures sont des exceptions aux règles standard d'allocation et de libération de mémoire.</span><span class="sxs-lookup"><span data-stu-id="5b073-106">These two structures are exceptions to the standard rules for allocating and releasing memory.</span></span> <span data-ttu-id="5b073-107">Elles contiennent plusieurs niveaux de structures et sont conçues pour permettre l'ajout ou la suppression de membres individuels.</span><span class="sxs-lookup"><span data-stu-id="5b073-107">They contain multiple levels of structures and are designed to enable individual members to be added or removed.</span></span> <span data-ttu-id="5b073-108">Par conséquent, chaque propriété doit être une allocation distincte.</span><span class="sxs-lookup"><span data-stu-id="5b073-108">Therefore, each property must be a separate allocation.</span></span> 

<span data-ttu-id="5b073-109">Lorsque la plupart des structures sont libérées à l'aide d'un appel à **MAPIFreeBuffer**, chaque entrée individuelle d'une structure **ADRLIST** ou **SRowSet** doit être libérée avec son propre appel à **MAPIFreeBuffer** ou un seul appel à **FreeProws** ou \*\* FreePadrlist\*\*.</span><span class="sxs-lookup"><span data-stu-id="5b073-109">Where most structures are freed with one call to **MAPIFreeBuffer**, each individual entry in an **ADRLIST** or **SRowSet** structure must be freed with its own call to **MAPIFreeBuffer** or a single call to either **FreeProws** or **FreePadrlist**.</span></span> <span data-ttu-id="5b073-110">Pour plus d'informations, voir [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md)et [SRowSet](srowset.md).</span><span class="sxs-lookup"><span data-stu-id="5b073-110">For more information, see [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md), and [SRowSet](srowset.md).</span></span> 

<span data-ttu-id="5b073-111">**FreeProws** et **FreePadrlist** sont des fonctions fournies par MAPI pour simplifier la libération de ces structures de données.</span><span class="sxs-lookup"><span data-stu-id="5b073-111">**FreeProws** and **FreePadrlist** are functions provided by MAPI for simplifying the freeing of these data structures.</span></span> <span data-ttu-id="5b073-112">Pour plus d'informations, voir [FreeProws](freeprows.md) et [FreePadrlist](freepadrlist.md).</span><span class="sxs-lookup"><span data-stu-id="5b073-112">For more information, see [FreeProws](freeprows.md) and [FreePadrlist](freepadrlist.md).</span></span> <span data-ttu-id="5b073-113">**FreePadrlist** libère la mémoire de la structure **ADRLIST** plus l'ensemble de la mémoire associée aux membres de la structure; **FreeProws** effectue la même opération pour la structure **SRowSet** .</span><span class="sxs-lookup"><span data-stu-id="5b073-113">**FreePadrlist** frees the memory for the **ADRLIST** structure plus all associated memory for the structure members; **FreeProws** does the same for the **SRowSet** structure.</span></span> 
  
<span data-ttu-id="5b073-114">Le diagramme suivant montre la disposition d'une structure de données **ADRLIST** , indiquant les allocations de mémoire distinctes requises.</span><span class="sxs-lookup"><span data-stu-id="5b073-114">The following diagram shows the layout of an **ADRLIST** data structure, indicating the separate memory allocations required.</span></span> <span data-ttu-id="5b073-115">Les cases gris affichent de la mémoire qui peut être allouée et libérée en un seul appel.</span><span class="sxs-lookup"><span data-stu-id="5b073-115">The gray boxes show memory that can be allocated and released with one call.</span></span> 
  
<span data-ttu-id="5b073-116">**Allocation de mémoire ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="5b073-116">**ADRLIST memory allocation**</span></span>
  
<span data-ttu-id="5b073-117">![Allocation de mémoire ADRLIST] (media/amapi_52.gif "Allocation de mémoire ADRLIST")</span><span class="sxs-lookup"><span data-stu-id="5b073-117">![ADRLIST memory allocation](media/amapi_52.gif "ADRLIST memory allocation")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5b073-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b073-118">See also</span></span>

- [<span data-ttu-id="5b073-119">Gestion de la mémoire dans MAPI</span><span class="sxs-lookup"><span data-stu-id="5b073-119">Managing Memory in MAPI</span></span>](managing-memory-in-mapi.md)

