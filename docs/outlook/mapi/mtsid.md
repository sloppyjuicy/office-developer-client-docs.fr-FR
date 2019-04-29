---
title: MTSID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MTSID
api_type:
- COM
ms.assetid: 3d9bc643-332f-4c8e-83e6-ce9b15711945
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 96da91acec741322e6c07c64555171d35f0f7e00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435172"
---
# <a name="mtsid"></a><span data-ttu-id="b3c3d-103">MTSID</span><span class="sxs-lookup"><span data-stu-id="b3c3d-103">MTSID</span></span>

  
  
<span data-ttu-id="b3c3d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3c3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3c3d-105">Contient un identificateur d'entrée de système de transport de messages (MTS) X. 400.</span><span class="sxs-lookup"><span data-stu-id="b3c3d-105">Contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3c3d-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b3c3d-106">Header file:</span></span>  <br/> |<span data-ttu-id="b3c3d-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b3c3d-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b3c3d-108">Macros connexes:</span><span class="sxs-lookup"><span data-stu-id="b3c3d-108">Related macros:</span></span>  <br/> |<span data-ttu-id="b3c3d-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span><span class="sxs-lookup"><span data-stu-id="b3c3d-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a><span data-ttu-id="b3c3d-110">Members</span><span class="sxs-lookup"><span data-stu-id="b3c3d-110">Members</span></span>

 <span data-ttu-id="b3c3d-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="b3c3d-111">**cb**</span></span>
  
> <span data-ttu-id="b3c3d-112">Nombre d'octets dans le tableau décrit par le membre **abEntry** .</span><span class="sxs-lookup"><span data-stu-id="b3c3d-112">Count of bytes in the array described by the **abEntry** member.</span></span> 
    
 <span data-ttu-id="b3c3d-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="b3c3d-113">**abEntry**</span></span>
  
> <span data-ttu-id="b3c3d-114">Tableau d'octets qui contient les données de l'identificateur de l'entrée MTS.</span><span class="sxs-lookup"><span data-stu-id="b3c3d-114">Byte array that contains the MTS entry identifier data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b3c3d-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="b3c3d-115">Remarks</span></span>

<span data-ttu-id="b3c3d-116">La structure **MTSID** est utilisée uniquement pour les mappages X. 400 des identificateurs d'entrée MAPI.</span><span class="sxs-lookup"><span data-stu-id="b3c3d-116">The **MTSID** structure is used only for X.400 mappings of MAPI entry identifiers.</span></span> <span data-ttu-id="b3c3d-117">Elle correspond à la structure [FLATENTRY](flatentry.md) MAPI.</span><span class="sxs-lookup"><span data-stu-id="b3c3d-117">It corresponds to the MAPI [FLATENTRY](flatentry.md) structure.</span></span> 
  
<span data-ttu-id="b3c3d-118">Un identificateur MTS a le même format qu'un identificateur d'entrée MAPI ou une valeur de propriété binaire.</span><span class="sxs-lookup"><span data-stu-id="b3c3d-118">An MTS identifier has the same format as a MAPI entry identifier or a binary property value.</span></span> <span data-ttu-id="b3c3d-119">Les identificateurs MTS peuvent être particulièrement utiles pour annuler les messages différés.</span><span class="sxs-lookup"><span data-stu-id="b3c3d-119">MTS identifiers can be particularly useful for canceling deferred messages.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b3c3d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3c3d-120">See also</span></span>



[<span data-ttu-id="b3c3d-121">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="b3c3d-121">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="b3c3d-122">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="b3c3d-122">FLATMTSIDLIST</span></span>](flatmtsidlist.md)


[<span data-ttu-id="b3c3d-123">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="b3c3d-123">MAPI Structures</span></span>](mapi-structures.md)

