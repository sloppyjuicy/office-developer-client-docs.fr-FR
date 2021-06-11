---
title: ISocialPersonGetPicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: Obtient un tableau d’octets qui contient la ressource d’image de la personne.
ms.openlocfilehash: 755e2138378136a3c1d810a1957923f4e8db721d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406709"
---
# <a name="isocialpersongetpicture"></a><span data-ttu-id="20317-103">ISocialPerson::GetPicture</span><span class="sxs-lookup"><span data-stu-id="20317-103">ISocialPerson::GetPicture</span></span>

<span data-ttu-id="20317-104">Obtient un tableau d’octets qui contient la ressource d’image de la personne.</span><span class="sxs-lookup"><span data-stu-id="20317-104">Gets an array of bytes that contains the picture resource for the person.</span></span> 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a><span data-ttu-id="20317-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="20317-105">Parameters</span></span>

<span data-ttu-id="20317-106">_picture_</span><span class="sxs-lookup"><span data-stu-id="20317-106">_picture_</span></span>
  
> <span data-ttu-id="20317-107">[out] Pointeur vers une structure qui spécifie un tableau d’octets qui représentent la ressource d’image d’une personne.</span><span class="sxs-lookup"><span data-stu-id="20317-107">[out] A pointer to a structure that specifies an array of bytes that represent the picture resource for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="20317-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="20317-108">Remarks</span></span>

<span data-ttu-id="20317-109">Les ressources d’image .bmp, .jpeg ou au format .png pris en charge.</span><span class="sxs-lookup"><span data-stu-id="20317-109">Supported picture resources are in .bmp, .jpeg, or .png format.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="20317-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20317-110">See also</span></span>

- [<span data-ttu-id="20317-111">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="20317-111">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

