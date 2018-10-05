---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 'Dernière modification : 20 février 2012'
ms.openlocfilehash: dbb18ce712d7900106f2c8dd18404e47d8bdbdb7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396210"
---
# <a name="mnlscomparestringw"></a>MNLS_CompareStringW

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
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

 _LCID_
  
> [in] Identificateur de paramètres régionaux. Pour les définitions détaillées, voir le paramètre _Locale_ de [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).
    
 _dwFlags_
  
> [in] Indicateurs à ignorer la casse et des signes diacritiques. Pour les définitions détaillées, voir le paramètre _dwCmpFlags_ de [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).
    
 _pstr1_
  
> [in] Pointeur vers la première chaîne Unicode à comparer.
    
 _cch1_
  
> [in] Longueur en caractères de la première chaîne Unicode, à l’exception du caractère de fin null. L’application peut fournir une valeur négative si la chaîne est terminée. Dans ce cas, la fonction **MNLS_CompareStringW** détermine automatiquement la longueur. 
    
 _pstr2_
  
> [in] Pointeur vers la deuxième chaîne Unicode à comparer.
    
 _cch2_
  
> [in] Longueur en caractères de la deuxième chaîne Unicode, à l’exception du caractère de fin null. L’application peut fournir une valeur négative si la chaîne est terminée. Dans ce cas, la fonction détermine automatiquement la longueur.
    
## <a name="return-value"></a>Valeur renvoyée

Renvoie les valeurs indiquées pour [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).
  
## <a name="remarks"></a>Remarques

Cette fonction encapsule [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx). **MNLS_CompareStringW** accepte les mêmes paramètres et a le même comportement que [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).
  
## <a name="see-also"></a>Voir aussi



[CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

