---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: 'Dernière modification : 18 juin 2012'
ms.openlocfilehash: 36e22c60b32242425335b122b66c2c77e376848b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580116"
---
# <a name="mnlslstrcmpw"></a>MNLS_lstrcmpW

 
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="return-value"></a>Valeur renvoy�e

Renvoie les valeurs décrites pour un appel à **MNLS_CompareStringW** à l’exception de CSTR_EQUAL équivalent. 
  
## <a name="remarks"></a>Remarques

 _MNLS_lstrcmpW_ effectue une comparaison en appelant [MNLS_CompareStringW](mnls_comparestringw.md) avec les paramètres régionaux de GetUserDefaultLCID, 0 pour les indicateurs et -1 pour cch1 et cch2. 
  
## <a name="see-also"></a>Voir aussi



[GetUserDefaultLCID](http://msdn.microsoft.com/en-us/library/dd318135%28VS.85%29.aspx)

