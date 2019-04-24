---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: 'Dernière modification: 21 février 2012'
ms.openlocfilehash: 31f699d1193e55a88e57a0f491658e0d537ef75d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338464"
---
# <a name="mnlslstrlenw"></a>MNLS_lstrlenW

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détermine la longueur de la chaîne Unicode spécifiée, à l'exception du caractère null de fin.
  
> [!TIP]
> EnVisagez d'utiliser [StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) à la place. 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a>Paramètres

 _lpsz_
  
> dans Chaîne Unicode terminée par un caractère null à vérifier.
    
## <a name="return-value"></a>Valeur renvoyée

La fonction renvoie un entier avec la longueur de la chaîne. Il s'agit d'un décompte de caractères dans la chaîne, à l'exclusion du caractère null de fin. Si _lpsz_ est null, la fonction renvoie zéro. 
  
## <a name="remarks"></a>Remarques

Cette fonction encapsule la fonction **lstrlen** . Pour plus d'informations, consultez la rubrique [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx).
  
## <a name="see-also"></a>Voir aussi



[lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)
  
[StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)

