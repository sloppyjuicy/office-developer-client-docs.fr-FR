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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e42bbf23ea8cf4e6196017a962329366e168420d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784911"
---
# <a name="mtsid"></a><span data-ttu-id="9731f-103">MTSID</span><span class="sxs-lookup"><span data-stu-id="9731f-103">MTSID</span></span>

  
  
<span data-ttu-id="9731f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9731f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9731f-105">Contient un identificateur d’entrée X.400 message transport système (MTS).</span><span class="sxs-lookup"><span data-stu-id="9731f-105">Contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9731f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="9731f-106">Header file:</span></span>  <br/> |<span data-ttu-id="9731f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9731f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="9731f-108">Macros connexes :</span><span class="sxs-lookup"><span data-stu-id="9731f-108">Related macros:</span></span>  <br/> |<span data-ttu-id="9731f-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span><span class="sxs-lookup"><span data-stu-id="9731f-109">[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a><span data-ttu-id="9731f-110">Membres</span><span class="sxs-lookup"><span data-stu-id="9731f-110">Members</span></span>

 <span data-ttu-id="9731f-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="9731f-111">**cb**</span></span>
  
> <span data-ttu-id="9731f-112">Nombre d’octets dans le tableau indiqué par le membre **abEntry** .</span><span class="sxs-lookup"><span data-stu-id="9731f-112">Count of bytes in the array described by the **abEntry** member.</span></span> 
    
 <span data-ttu-id="9731f-113">**abEntry**</span><span class="sxs-lookup"><span data-stu-id="9731f-113">**abEntry**</span></span>
  
> <span data-ttu-id="9731f-114">Tableau d’octets qui contient les données d’identificateur MTS entrée.</span><span class="sxs-lookup"><span data-stu-id="9731f-114">Byte array that contains the MTS entry identifier data.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9731f-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="9731f-115">Remarks</span></span>

<span data-ttu-id="9731f-116">La structure **MTSID** est utilisée uniquement pour les mappages X.400 d’identificateurs d’entrée MAPI.</span><span class="sxs-lookup"><span data-stu-id="9731f-116">The **MTSID** structure is used only for X.400 mappings of MAPI entry identifiers.</span></span> <span data-ttu-id="9731f-117">Il correspond à la structure MAPI [FLATENTRY](flatentry.md) .</span><span class="sxs-lookup"><span data-stu-id="9731f-117">It corresponds to the MAPI [FLATENTRY](flatentry.md) structure.</span></span> 
  
<span data-ttu-id="9731f-118">Un identificateur MTS a le même format qu’un identificateur d’entrée MAPI ou une valeur de propriété binaire.</span><span class="sxs-lookup"><span data-stu-id="9731f-118">An MTS identifier has the same format as a MAPI entry identifier or a binary property value.</span></span> <span data-ttu-id="9731f-119">Les identificateurs MTS peuvent être particulièrement utiles pour l’annulation de messages différés.</span><span class="sxs-lookup"><span data-stu-id="9731f-119">MTS identifiers can be particularly useful for canceling deferred messages.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9731f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9731f-120">See also</span></span>



[<span data-ttu-id="9731f-121">FLATENTRY</span><span class="sxs-lookup"><span data-stu-id="9731f-121">FLATENTRY</span></span>](flatentry.md)
  
[<span data-ttu-id="9731f-122">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="9731f-122">FLATMTSIDLIST</span></span>](flatmtsidlist.md)


[<span data-ttu-id="9731f-123">Structures MAPI</span><span class="sxs-lookup"><span data-stu-id="9731f-123">MAPI Structures</span></span>](mapi-structures.md)

