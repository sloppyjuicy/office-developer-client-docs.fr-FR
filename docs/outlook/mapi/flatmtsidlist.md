---
title: FLATMTSIDLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATMTSIDLIST
api_type:
- COM
ms.assetid: b66c2815-72bc-4535-b34c-899bb830f29e
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 0f1495549df751c59ab84e2b16fffbaf2f4f9fa5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574719"
---
# <a name="flatmtsidlist"></a><span data-ttu-id="a98f5-103">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="a98f5-103">FLATMTSIDLIST</span></span>

  
  
<span data-ttu-id="a98f5-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a98f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a98f5-105">Contient un tableau de structures [MTSID](mtsid.md) , chacun d'entre eux contient un identificateur d’entrée X.400 message transport système (MTS).</span><span class="sxs-lookup"><span data-stu-id="a98f5-105">Contains an array of [MTSID](mtsid.md) structures, each of which contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a98f5-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="a98f5-106">Header file:</span></span>  <br/> |<span data-ttu-id="a98f5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a98f5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a98f5-108">Macros connexes :</span><span class="sxs-lookup"><span data-stu-id="a98f5-108">Related macros:</span></span>  <br/> |<span data-ttu-id="a98f5-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span><span class="sxs-lookup"><span data-stu-id="a98f5-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a><span data-ttu-id="a98f5-110">Members</span><span class="sxs-lookup"><span data-stu-id="a98f5-110">Members</span></span>

 <span data-ttu-id="a98f5-111">**cMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="a98f5-111">**cMTSIDs**</span></span>
  
> <span data-ttu-id="a98f5-112">Nombre de structures **MTSID** dans le tableau indiqué par le membre **abMTSIDs** .</span><span class="sxs-lookup"><span data-stu-id="a98f5-112">Count of **MTSID** structures in the array described by the **abMTSIDs** member.</span></span> 
    
 <span data-ttu-id="a98f5-113">**cbMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="a98f5-113">**cbMTSIDs**</span></span>
  
> <span data-ttu-id="a98f5-114">Nombre d’octets dans le tableau décrit par **abMTSIDs**.</span><span class="sxs-lookup"><span data-stu-id="a98f5-114">Count of bytes in the array described by **abMTSIDs**.</span></span>
    
 <span data-ttu-id="a98f5-115">**abMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="a98f5-115">**abMTSIDs**</span></span>
  
> <span data-ttu-id="a98f5-116">Tableau d’octets qui contient une ou plusieurs structures **MTSID** .</span><span class="sxs-lookup"><span data-stu-id="a98f5-116">Byte array that contains one or more **MTSID** structures.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a98f5-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="a98f5-117">Remarks</span></span>

<span data-ttu-id="a98f5-118">Utilisation de la structure **FLATMTSIDLIST** messagerie X.400 correspond à l’utilisation de la structure [FLATENTRYLIST](flatentrylist.md) de messagerie MAPI.</span><span class="sxs-lookup"><span data-stu-id="a98f5-118">The **FLATMTSIDLIST** structure's use in X.400 messaging corresponds to the [FLATENTRYLIST](flatentrylist.md) structure's use in MAPI messaging.</span></span> <span data-ttu-id="a98f5-119">MAPI utilise des structures **FLATMTSIDLIST** pour mettre à jour les propriétés X.400 lors de la gestion du message.</span><span class="sxs-lookup"><span data-stu-id="a98f5-119">MAPI uses **FLATMTSIDLIST** structures to maintain X.400 properties during message handling.</span></span> <span data-ttu-id="a98f5-120">Fournisseurs de services utilisent des structures **FLATMTSIDLIST** lors de la gestion des messages X.400 entrants et sortants.</span><span class="sxs-lookup"><span data-stu-id="a98f5-120">Service providers use **FLATMTSIDLIST** structures when handling incoming and outgoing X.400 messages.</span></span> 
  
<span data-ttu-id="a98f5-121">Dans le tableau **abMTSIDs** , chaque structure **MTSID** est aligné sur une limite alignée naturellement.</span><span class="sxs-lookup"><span data-stu-id="a98f5-121">In the **abMTSIDs** array, each **MTSID** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="a98f5-122">Octets supplémentaires sont inclus comme remplissage pour rendre l’alignement que naturel entre les deux structures **MTSID** .</span><span class="sxs-lookup"><span data-stu-id="a98f5-122">Extra bytes are included as padding to make sure natural alignment between any two **MTSID** structures.</span></span> <span data-ttu-id="a98f5-123">La première structure **MTSID** dans le tableau est toujours alignée correctement, car le décalage du membre **abMTSIDs** est 8.</span><span class="sxs-lookup"><span data-stu-id="a98f5-123">The first **MTSID** structure in the array is always aligned correctly because the offset of the **abMTSIDs** member is 8.</span></span> <span data-ttu-id="a98f5-124">Pour calculer le décalage de la structure suivante, utilisez la taille de la première entrée d’arrondi au multiple prochain de 4.</span><span class="sxs-lookup"><span data-stu-id="a98f5-124">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="a98f5-125">Utilisez la macro [CbNewMTSID](cbnewmtsid.md) pour calculer la taille d’une structure **MTSID** .</span><span class="sxs-lookup"><span data-stu-id="a98f5-125">Use the [CbNewMTSID](cbnewmtsid.md) macro to compute the size of an **MTSID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a98f5-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a98f5-126">See also</span></span>



[<span data-ttu-id="a98f5-127">CbNewFLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="a98f5-127">CbNewFLATMTSIDLIST</span></span>](cbnewflatmtsidlist.md)
  
[<span data-ttu-id="a98f5-128">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="a98f5-128">FLATENTRYLIST</span></span>](flatentrylist.md)
  
[<span data-ttu-id="a98f5-129">MTSID</span><span class="sxs-lookup"><span data-stu-id="a98f5-129">MTSID</span></span>](mtsid.md)


[<span data-ttu-id="a98f5-130">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="a98f5-130">MAPI Structures</span></span>](mapi-structures.md)

