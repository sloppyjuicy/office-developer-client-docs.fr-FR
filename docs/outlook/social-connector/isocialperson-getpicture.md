---
title: ISocialPersonGetPicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: Obtient un tableau d’octets qui contient la ressource image de la personne.
ms.openlocfilehash: dcb0da5bc36c2166d569c770d1f182cd21339435
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787587"
---
# <a name="isocialpersongetpicture"></a><span data-ttu-id="c6a0c-103">ISocialPerson::GetPicture</span><span class="sxs-lookup"><span data-stu-id="c6a0c-103">ISocialPerson::GetPicture</span></span>

<span data-ttu-id="c6a0c-104">Obtient un tableau d’octets qui contient la ressource image de la personne.</span><span class="sxs-lookup"><span data-stu-id="c6a0c-104">Gets an array of bytes that contains the picture resource for the person.</span></span> 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a><span data-ttu-id="c6a0c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6a0c-105">Parameters</span></span>

<span data-ttu-id="c6a0c-106">_image_</span><span class="sxs-lookup"><span data-stu-id="c6a0c-106">_picture_</span></span>
  
> <span data-ttu-id="c6a0c-107">[out] Pointeur vers une structure qui spécifie un tableau d’octets qui représentent la ressource image d’une personne.</span><span class="sxs-lookup"><span data-stu-id="c6a0c-107">[out] A pointer to a structure that specifies an array of bytes that represent the picture resource for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c6a0c-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="c6a0c-108">Remarks</span></span>

<span data-ttu-id="c6a0c-109">Prise en charge d’image ressources sont au format .bmp, .jpeg ou .png.</span><span class="sxs-lookup"><span data-stu-id="c6a0c-109">Supported picture resources are in .bmp, .jpeg, or .png format.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c6a0c-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6a0c-110">See also</span></span>

- [<span data-ttu-id="c6a0c-111">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c6a0c-111">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

