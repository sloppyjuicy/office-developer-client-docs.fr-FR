---
title: MNLS_CompareStringW
description: Décrit la syntaxe, les paramètres, la valeur de retour et les remarques pour MNLS_CompareStringW, qui compare deux chaînes Unicode.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
ms.openlocfilehash: 7316ff699ac9983a6c1c81b89cbe95ae09d5e13b
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828184"
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
  
> [in] Identificateur de paramètres régionaux. Pour obtenir des définitions détaillées, consultez le paramètre  _Paramètres régionaux_ de [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).
    
 _dwFlags_
  
> [in] Indicateurs pour ignorer la casse et les signes diacritiques. Pour obtenir des définitions détaillées, consultez le paramètre  _dwCmpFlags_ de [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).
    
 _pstr1_
  
> [in] Pointeur vers la première chaîne Unicode à comparer.
    
 _cch1_
  
> [in] Longueur en caractères de la première chaîne Unicode, à l’exception du caractère null de fin. L’application peut fournir une valeur négative si la chaîne est terminée par une valeur Null. Dans ce cas, la fonction **MNLS_CompareStringW** détermine automatiquement la longueur. 
    
 _pstr2_
  
> [in] Pointeur vers la deuxième chaîne Unicode à comparer.
    
 _cch2_
  
> [in] Longueur en caractères de la deuxième chaîne Unicode, à l’exception du caractère null de fin. L’application peut fournir une valeur négative si la chaîne est terminée par une valeur Null. Dans ce cas, la fonction détermine automatiquement la longueur.
    
## <a name="return-value"></a>Valeur renvoyée

Retourne les valeurs décrites pour [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).
  
## <a name="remarks"></a>Remarques

Cette fonction encapsule [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx). **MNLS_CompareStringW** prend les mêmes paramètres et a le même comportement que [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).
  
## <a name="see-also"></a>Voir aussi



[CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

