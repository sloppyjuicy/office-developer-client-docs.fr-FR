---
title: ISocialPersonGetPicture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 02fcaf25-42b5-4584-95c6-d44a3d035128
description: Obtient un tableau d’octets qui contient la ressource d’image de la personne.
ms.openlocfilehash: 090dae46f97c2b937155d61ec65b87f2c635da5d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629157"
---
# <a name="isocialpersongetpicture"></a>ISocialPerson::GetPicture

Obtient un tableau d’octets qui contient la ressource d’image de la personne. 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a>Paramètres

_picture_
  
> [out] Pointeur vers une structure qui spécifie un tableau d’octets qui représentent la ressource d’image d’une personne.
    
## <a name="remarks"></a>Remarques

Les ressources d’image .bmp, .jpeg ou au format .png pris en charge.
  
## <a name="see-also"></a>Voir aussi

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

