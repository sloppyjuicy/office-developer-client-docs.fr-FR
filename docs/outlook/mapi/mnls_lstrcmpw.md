---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: 'Dernière modification: 18 juin 2012'
ms.openlocfilehash: 03b0eb794b07bc56ec6dce4a567d89294b2c908a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356839"
---
# <a name="mnlslstrcmpw"></a>MNLS_lstrcmpW

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux chaînes Unicode.
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a>Paramètres

 _lpString1_
  
> dans Pointeur vers la première chaîne Unicode à comparer.
    
 _lpString2_
  
> dans Pointeur vers la deuxième chaîne Unicode à comparer.
    
## <a name="return-value"></a>Valeur renvoyée

Renvoie les valeurs décrites pour un appel équivalent à **MNLS_CompareStringW** à l'exception de CSTR_EQUAL. 
  
## <a name="remarks"></a>Remarques

 _MNLS_lstrcmpW_ effectue une comparaison en appelant [MNLS_CompareStringW](mnls_comparestringw.md) avec les paramètres régionaux GetUserDefaultLCID, 0 pour les indicateurs et-1 pour cch1 et cch2. 
  
## <a name="see-also"></a>Voir aussi



[GetUserDefaultLCID](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

