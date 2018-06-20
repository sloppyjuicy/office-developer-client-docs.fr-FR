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
# <a name="isocialpersongetpicture"></a>ISocialPerson::GetPicture

Obtient un tableau d’octets qui contient la ressource image de la personne. 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a>Paramètres

_image_
  
> [out] Pointeur vers une structure qui spécifie un tableau d’octets qui représentent la ressource image d’une personne.
    
## <a name="remarks"></a>Remarques

Prise en charge d’image ressources sont au format .bmp, .jpeg ou .png.
  
## <a name="see-also"></a>Voir aussi

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

