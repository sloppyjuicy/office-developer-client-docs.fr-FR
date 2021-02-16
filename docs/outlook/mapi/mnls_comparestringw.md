---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 'Last modified: February 20, 2012'
ms.openlocfilehash: dbb18ce712d7900106f2c8dd18404e47d8bdbdb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356846"
---
# <a name="mnls_comparestringw"></a>MNLS_CompareStringW

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Compare deux chaînes Unicode.
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a>Paramètres

 _lcid_
  
> [in] Identificateur de paramètres régionaux. Pour obtenir des définitions détaillées, voir le paramètre  _Locale_ de [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).
    
 _dwFlags_
  
> [in] Indicateurs pour ignorer la case et les signes diacritiques. Pour obtenir des définitions détaillées, voir le  _paramètre dwCmpFlags_ de [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).
    
 _pstr1_
  
> [in] Pointeur vers la première chaîne Unicode à comparer.
    
 _cch1_
  
> [in] Longueur en caractères de la première chaîne Unicode, à l’exclusion du caractère null de fin. L’application peut fournir une valeur négative si la chaîne est terminée par null. Dans ce cas, la **fonction MNLS_CompareStringW** détermine automatiquement la longueur. 
    
 _pstr2_
  
> [in] Pointeur vers la deuxième chaîne Unicode à comparer.
    
 _cch2_
  
> [in] Longueur en caractères de la deuxième chaîne Unicode, à l’exclusion du caractère null de fin. L’application peut fournir une valeur négative si la chaîne est terminée par null. Dans ce cas, la fonction détermine automatiquement la longueur.
    
## <a name="return-value"></a>Valeur renvoyée

Renvoie les valeurs décrites [pour CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).
  
## <a name="remarks"></a>Remarques

Cette fonction [encapsule CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx). **MNLS_CompareStringW** prend les mêmes paramètres et a le même comportement que [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).
  
## <a name="see-also"></a>Voir aussi



[CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

