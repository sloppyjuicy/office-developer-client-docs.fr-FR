---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: 'Dernière modification : 18 juin 2012'
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382707"
---
# <a name="mnlslstrcpyw"></a>MNLS_lstrcpyW

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Copie une chaîne dans une mémoire tampon.
  
> [!CAUTION]
> Ne pas utiliser. Utilisez plutôt [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) . 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a>Paramètres

lpString1
  
> [out] Mémoire tampon pour recevoir le contenu de la chaîne indiquée par le paramètre lpString2.
    
lpString2
  
> [in] La chaîne à copier.
    
## <a name="return-value"></a>Valeur renvoyée

Si la fonction réussit, la valeur de retour est un pointeur vers la mémoire tampon.
  
Si la fonction échoue, la valeur de retour est NULL et lpString1 ne peut pas être terminée.
  
## <a name="remarks"></a>Remarques

Cette fonction encapsule la fonction **lstrcpy** . Pour plus d’informations, voir [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx).
  
## <a name="see-also"></a>Voir aussi



[lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

