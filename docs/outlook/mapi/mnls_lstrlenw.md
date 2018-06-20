---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: 'Dernière modification : 21 février 2012'
ms.openlocfilehash: 70c15970ce69e4bc075da6bf55320cb23116b7a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784920"
---
# <a name="mnlslstrlenw"></a>MNLS_lstrlenW

  
  
**S’applique à**: Outlook 
  
Détermine la longueur de la chaîne Unicode spécifiée, à l’exception du caractère de fin null.
  
> [!TIP]
> Utilisez plutôt [StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx) . 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a>Paramètres

 _lpsz_
  
> [in] La chaîne Unicode terminée par null à vérifier.
    
## <a name="return-value"></a>Valeur renvoy�e

La fonction retourne un entier avec la longueur de la chaîne. Il s’agit d’un nombre de caractères dans la chaîne, à l’exception du caractère de fin null. Si _lpsz_ est NULL, la fonction renvoie zéro. 
  
## <a name="remarks"></a>Remarques

Cette fonction à la ligne de la fonction **lstrlen** . Pour plus d’informations, voir [lstrlen](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx).
  
## <a name="see-also"></a>Voir aussi



[lstrlen](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx)
  
[StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx)

