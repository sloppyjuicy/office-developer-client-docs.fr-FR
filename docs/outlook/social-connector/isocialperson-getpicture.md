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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406709"
---
# <a name="isocialpersongetpicture"></a>ISocialPerson::GetPicture

Obtient un tableau d'octets qui contient la ressource image de la personne. 
  
```cpp
HRESULT _stdcall GetPicture([out, retval] SAFEARRAY(unsigned char)* picture);
```

## <a name="parameters"></a>Paramètres

_ci_
  
> remarquer Pointeur vers une structure qui spécifie un tableau d'octets représentant la ressource image d'une personne.
    
## <a name="remarks"></a>Remarques

Les ressources d'images prises en charge sont au format. bmp,. jpeg ou. png.
  
## <a name="see-also"></a>Voir aussi

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

