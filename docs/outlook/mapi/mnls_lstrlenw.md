---
title: MNLS_lstrlenW
description: MNLS_lstrlenW détermine la longueur de la chaîne Unicode spécifiée, à l’exception du caractère null de fin.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
ms.openlocfilehash: af8b7e15a44a158e9a97150981282e1431b01a97
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65826889"
---
# <a name="mnls_lstrlenw"></a>MNLS_lstrlenW

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détermine la longueur de la chaîne Unicode spécifiée, à l’exception du caractère null de fin.
  
> [!TIP]
> Envisagez plutôt d’utiliser [StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) . 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a>Paramètres

 _lpsz_
  
> [in] Chaîne Unicode terminée par null à vérifier.
    
## <a name="return-value"></a>Valeur renvoyée

La fonction retourne un entier avec la longueur de la chaîne. Il s’agit d’un nombre de caractères dans la chaîne, à l’exclusion du caractère null de fin. Si  _lpsz_ a la valeur NULL, la fonction retourne zéro. 
  
## <a name="remarks"></a>Remarques

Cette fonction encapsule la fonction **lstrlen** . Pour plus d’informations, consultez [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).
  
## <a name="see-also"></a>Voir aussi



[lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)
  
[StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)

