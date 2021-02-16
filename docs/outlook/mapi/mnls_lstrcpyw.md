---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: 'Last modified: June 18, 2012'
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341726"
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

Cette fonction encapsule **la fonction lstrcpy.** Pour plus d’informations, [voir lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).
  
## <a name="see-also"></a>Voir aussi



[lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

