---
title: ISocialPersonGetPicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: Obtient un tableau d'octets qui contient la ressource image de la personne.
ms.openlocfilehash: 755e2138378136a3c1d810a1957923f4e8db721d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331653"
---
# <a name="isocialpersongetpicture"></a><span data-ttu-id="d0c00-103">ISocialPerson::GetPicture</span><span class="sxs-lookup"><span data-stu-id="d0c00-103">ISocialPerson::GetPicture</span></span>

<span data-ttu-id="d0c00-104">Obtient un tableau d'octets qui contient la ressource image de la personne.</span><span class="sxs-lookup"><span data-stu-id="d0c00-104">Gets an array of bytes that contains the picture resource for the person.</span></span> 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a><span data-ttu-id="d0c00-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0c00-105">Parameters</span></span>

<span data-ttu-id="d0c00-106">_ci_</span><span class="sxs-lookup"><span data-stu-id="d0c00-106">_picture_</span></span>
  
> <span data-ttu-id="d0c00-107">remarquer Pointeur vers une structure qui spécifie un tableau d'octets représentant la ressource image d'une personne.</span><span class="sxs-lookup"><span data-stu-id="d0c00-107">[out] A pointer to a structure that specifies an array of bytes that represent the picture resource for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d0c00-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="d0c00-108">Remarks</span></span>

<span data-ttu-id="d0c00-109">Les ressources d'images prises en charge sont au format. bmp,. jpeg ou. png.</span><span class="sxs-lookup"><span data-stu-id="d0c00-109">Supported picture resources are in .bmp, .jpeg, or .png format.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d0c00-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0c00-110">See also</span></span>

- [<span data-ttu-id="d0c00-111">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d0c00-111">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

