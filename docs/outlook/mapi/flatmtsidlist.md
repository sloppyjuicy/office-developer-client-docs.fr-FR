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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bd9bfe4d1411b84a7811235aa68728afaefe64ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439218"
---
# <a name="flatmtsidlist"></a><span data-ttu-id="9ff96-103">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="9ff96-103">FLATMTSIDLIST</span></span>

  
  
<span data-ttu-id="9ff96-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ff96-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ff96-105">Contient un tableau de structures [MTSID,](mtsid.md) chacune contenant un identificateur d’entrée de système de transport de messages (MTS) X.400.</span><span class="sxs-lookup"><span data-stu-id="9ff96-105">Contains an array of [MTSID](mtsid.md) structures, each of which contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ff96-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="9ff96-106">Header file:</span></span>  <br/> |<span data-ttu-id="9ff96-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9ff96-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9ff96-108">Macros associées :</span><span class="sxs-lookup"><span data-stu-id="9ff96-108">Related macros:</span></span>  <br/> |<span data-ttu-id="9ff96-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span><span class="sxs-lookup"><span data-stu-id="9ff96-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a><span data-ttu-id="9ff96-110">Members</span><span class="sxs-lookup"><span data-stu-id="9ff96-110">Members</span></span>

 <span data-ttu-id="9ff96-111">**cMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="9ff96-111">**cMTSIDs**</span></span>
  
> <span data-ttu-id="9ff96-112">Nombre de structures **MTSID** dans le tableau décrit par le membre **abMTSIDs.**</span><span class="sxs-lookup"><span data-stu-id="9ff96-112">Count of **MTSID** structures in the array described by the **abMTSIDs** member.</span></span> 
    
 <span data-ttu-id="9ff96-113">**cbMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="9ff96-113">**cbMTSIDs**</span></span>
  
> <span data-ttu-id="9ff96-114">Nombre d’octets dans le tableau décrit par **abMTSIDs**.</span><span class="sxs-lookup"><span data-stu-id="9ff96-114">Count of bytes in the array described by **abMTSIDs**.</span></span>
    
 <span data-ttu-id="9ff96-115">**abMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="9ff96-115">**abMTSIDs**</span></span>
  
> <span data-ttu-id="9ff96-116">Tableau d’bytes qui contient une ou plusieurs structures **MTSID.**</span><span class="sxs-lookup"><span data-stu-id="9ff96-116">Byte array that contains one or more **MTSID** structures.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9ff96-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="9ff96-117">Remarks</span></span>

<span data-ttu-id="9ff96-118">L’utilisation de la structure **FLATMTSIDLIST** dans la messagerie X.400 correspond à l’utilisation de la structure [FLATENTRYLIST](flatentrylist.md) dans la messagerie MAPI.</span><span class="sxs-lookup"><span data-stu-id="9ff96-118">The **FLATMTSIDLIST** structure's use in X.400 messaging corresponds to the [FLATENTRYLIST](flatentrylist.md) structure's use in MAPI messaging.</span></span> <span data-ttu-id="9ff96-119">MAPI utilise des structures **FLATMTSIDLIST** pour gérer les propriétés X.400 lors de la gestion des messages.</span><span class="sxs-lookup"><span data-stu-id="9ff96-119">MAPI uses **FLATMTSIDLIST** structures to maintain X.400 properties during message handling.</span></span> <span data-ttu-id="9ff96-120">Les fournisseurs de services utilisent des structures **FLATMTSIDLIST** lors de la gestion des messages X.400 entrants et sortants.</span><span class="sxs-lookup"><span data-stu-id="9ff96-120">Service providers use **FLATMTSIDLIST** structures when handling incoming and outgoing X.400 messages.</span></span> 
  
<span data-ttu-id="9ff96-121">Dans le **tableau abMTSIDs,** chaque structure **MTSID** est alignée sur une limite alignée naturellement.</span><span class="sxs-lookup"><span data-stu-id="9ff96-121">In the **abMTSIDs** array, each **MTSID** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="9ff96-122">Des octets supplémentaires sont inclus comme remplissage pour assurer un alignement naturel entre deux structures **MTSID.**</span><span class="sxs-lookup"><span data-stu-id="9ff96-122">Extra bytes are included as padding to make sure natural alignment between any two **MTSID** structures.</span></span> <span data-ttu-id="9ff96-123">La première structure **MTSID** du tableau est toujours alignée correctement, car le décalage du membre **abMTSIDs** est 8.</span><span class="sxs-lookup"><span data-stu-id="9ff96-123">The first **MTSID** structure in the array is always aligned correctly because the offset of the **abMTSIDs** member is 8.</span></span> <span data-ttu-id="9ff96-124">Pour calculer le décalage de la structure suivante, utilisez la taille de la première entrée arrondie au multiple suivant de 4.</span><span class="sxs-lookup"><span data-stu-id="9ff96-124">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="9ff96-125">Utilisez la macro [CbNewMTSID](cbnewmtsid.md) pour calculer la taille d’une structure **MTSID.**</span><span class="sxs-lookup"><span data-stu-id="9ff96-125">Use the [CbNewMTSID](cbnewmtsid.md) macro to compute the size of an **MTSID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9ff96-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ff96-126">See also</span></span>



[<span data-ttu-id="9ff96-127">CbNewFLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="9ff96-127">CbNewFLATMTSIDLIST</span></span>](cbnewflatmtsidlist.md)
  
[<span data-ttu-id="9ff96-128">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="9ff96-128">FLATENTRYLIST</span></span>](flatentrylist.md)
  
[<span data-ttu-id="9ff96-129">MTSID</span><span class="sxs-lookup"><span data-stu-id="9ff96-129">MTSID</span></span>](mtsid.md)


[<span data-ttu-id="9ff96-130">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="9ff96-130">MAPI Structures</span></span>](mapi-structures.md)

