---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: 'Last modified: June 18, 2012'
ms.openlocfilehash: da855762a601fdf28544cd75d50610f7964761c7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575434"
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

Renvoie les valeurs décrites pour un appel équivalent **à MNLS_CompareStringW** à l’exception de CSTR_EQUAL. 
  
## <a name="remarks"></a>Remarques

 _MNLS_lstrcmpW_ effectue une comparaison en appelant [MNLS_CompareStringW](mnls_comparestringw.md) avec les paramètres régionaux GetUserDefaultLCID, 0 pour les indicateurs et -1 pour cch1 et cch2. 
  
## <a name="see-also"></a>Voir aussi



[GetUserDefaultLCID](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

