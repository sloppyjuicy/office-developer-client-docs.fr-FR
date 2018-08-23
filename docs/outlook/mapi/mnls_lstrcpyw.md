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
ms.openlocfilehash: 4d3210c098d0a7c83721798c8c32ffd9f1e5ebb4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575461"
---
# <a name="mnlslstrcpyw"></a>MNLS_lstrcpyW

 
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Copie une chaîne dans une mémoire tampon.
  
> [!CAUTION]
> Ne pas utiliser. Utilisez plutôt [StringCchCopy](http://msdn.microsoft.com/en-us/library/ms647527%28VS.85%29.aspx) . 
  
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
    
## <a name="return-value"></a>Valeur renvoy�e

Si la fonction réussit, la valeur de retour est un pointeur vers la mémoire tampon.
  
Si la fonction échoue, la valeur de retour est NULL et lpString1 ne peut pas être terminée.
  
## <a name="remarks"></a>Remarques

Cette fonction encapsule la fonction **lstrcpy** . Pour plus d’informations, voir [lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx).
  
## <a name="see-also"></a>Voir aussi



[lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx)

