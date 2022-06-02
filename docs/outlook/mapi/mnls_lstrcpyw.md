---
title: MNLS_lstrcpyW
description: Décrit la syntaxe, les paramètres, la valeur de retour et les remarques pour NLS_lstrcpyW, qui copie une chaîne dans une mémoire tampon.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
ms.openlocfilehash: 27d77e3044b75d1102cb379fbf11163af920b7ad
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827981"
---
# <a name="mnls_lstrcpyw"></a>MNLS_lstrcpyW

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie une chaîne dans une mémoire tampon.
  
> [!CAUTION]
> Ne pas utiliser. Envisagez plutôt d’utiliser [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) . 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a>Paramètres

lpString1
  
> [out] Mémoire tampon pour recevoir le contenu de la chaîne pointée par le paramètre lpString2.
    
lpString2
  
> [in] Chaîne terminée par une valeur Null à copier.
    
## <a name="return-value"></a>Valeur renvoyée

Si la fonction réussit, la valeur de retour est un pointeur vers la mémoire tampon.
  
Si la fonction échoue, la valeur de retour est NULL et lpString1 peut ne pas être terminé par null.
  
## <a name="remarks"></a>Remarques

Cette fonction encapsule la fonction **lstrcpy** . Pour plus d’informations, consultez [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).
  
## <a name="see-also"></a>Voir aussi



[lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

