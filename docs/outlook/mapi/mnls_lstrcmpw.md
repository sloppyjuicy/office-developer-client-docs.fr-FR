---
title: MNLS_lstrcmpW
description: Décrit la syntaxe, les paramètres, la valeur de retour et les remarques pour MNLS_lstrcmpW, qui compare deux chaînes Unicode.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
ms.openlocfilehash: 04b0ae87c3bd8694d9d7e4ff065362357a489b8d
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828177"
---
# <a name="mnls_lstrcmpw"></a>MNLS_lstrcmpW

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux chaînes Unicode.
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a>Paramètres

 _lpString1_
  
> [in] Pointeur vers la première chaîne Unicode à comparer.
    
 _lpString2_
  
> [in] Pointeur vers la deuxième chaîne Unicode à comparer.
    
## <a name="return-value"></a>Valeur renvoyée

Retourne les valeurs décrites pour un appel équivalent à **MNLS_CompareStringW** à l’exception de CSTR_EQUAL. 
  
## <a name="remarks"></a>Remarques

 _MNLS_lstrcmpW_ effectue une comparaison en appelant [MNLS_CompareStringW](mnls_comparestringw.md) avec les paramètres régionaux GetUserDefaultLCID, 0 pour les indicateurs et -1 pour cch1 et cch2. 
  
## <a name="see-also"></a>Voir aussi



[GetUserDefaultLCID](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

