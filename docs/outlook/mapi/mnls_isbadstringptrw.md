---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: 'Last modified: February 20, 2012'
ms.openlocfilehash: 56c2d84cf883f2452e6aa9a2904478eb8e3ec190
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571401"
---
# <a name="mnls_isbadstringptrw"></a>MNLS_IsBadStringPtrW

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Vérifie qu’un pointeur vers une chaîne large est valide.
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a>Paramètres

 _lpsz_
  
> [in] Pointeur vers la chaîne de caractères large.
    
 _ucchMax_
  
> [in] Longueur maximale de la chaîne en caractères, y compris terminateur.
    
## <a name="return-value"></a>Valeur renvoyée

Renvoie un booléen qui est true si la chaîne est mauvaise.
  
## <a name="remarks"></a>Remarques

Cette fonction [encapsule IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx). Pour plus d’informations, [voir IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).
  

