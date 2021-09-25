---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: 'Last modified: June 18, 2012'
ms.openlocfilehash: ad7323d02a8a3f080614f09b610175976cd4c01f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584037"
---
# <a name="mnls_lstrcpyw"></a>MNLS_lstrcpyW

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie une chaîne dans une mémoire tampon.
  
> [!CAUTION]
> Ne pas utiliser. Envisagez plutôt [d’utiliser StringCchCopy.](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a>Paramètres

lpString1
  
> [out] Mémoire tampon pour recevoir le contenu de la chaîne pointée par le paramètre lpString2.
    
lpString2
  
> [in] Chaîne terminée par null à copier.
    
## <a name="return-value"></a>Valeur renvoyée

Si la fonction réussit, la valeur de retour est un pointeur vers la mémoire tampon.
  
Si la fonction échoue, la valeur de retour est NULL et lpString1 peut ne pas être terminée par null.
  
## <a name="remarks"></a>Remarques

Cette fonction encapsule **la fonction lstrcpy.** Pour plus d’informations, voir [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).
  
## <a name="see-also"></a>Voir aussi



[lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

