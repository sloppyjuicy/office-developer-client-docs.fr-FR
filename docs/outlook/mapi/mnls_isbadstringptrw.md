---
title: MNLS_IsBadStringPtrW
description: Décrit la syntaxe, les paramètres, la valeur de retour et les remarques pour MNLS_IsBadStringPtrW, qui vérifie qu’un pointeur vers une chaîne large est valide.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
ms.openlocfilehash: 1e2c90fefffa2112efc0e67bce7341a0605828ea
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828473"
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
  
> [in] Pointeur vers la chaîne de caractères larges.
    
 _ucchMax_
  
> [in] Longueur maximale de la chaîne en caractères, y compris le terminateur.
    
## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur booléenne qui est true si la chaîne est incorrecte.
  
## <a name="remarks"></a>Remarques

Cette fonction encapsule [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx). Pour plus d’informations, consultez [IsBadStringPtr](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx).
  

