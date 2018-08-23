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
ms.openlocfilehash: 3e23fa9fcb074fabacf1a2dd9ac3f632cdce5b5c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576175"
---
# <a name="mnlscomparestringw"></a>MNLS_CompareStringW

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Identificateur de paramètres régionaux. Pour les définitions détaillées, voir le paramètre _Locale_ de [CompareString](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).
    
 _dwFlags_
  
> [in] Indicateurs à ignorer la casse et des signes diacritiques. Pour les définitions détaillées, voir le paramètre _dwCmpFlags_ de [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).
    
 _pstr1_
  
> [in] Pointeur vers la première chaîne Unicode à comparer.
    
 _cch1_
  
> [in] Longueur en caractères de la première chaîne Unicode, à l’exception du caractère de fin null. L’application peut fournir une valeur négative si la chaîne est terminée. Dans ce cas, la fonction **MNLS_CompareStringW** détermine automatiquement la longueur. 
    
 _pstr2_
  
> [in] Pointeur vers la deuxième chaîne Unicode à comparer.
    
 _cch2_
  
> [in] Longueur en caractères de la deuxième chaîne Unicode, à l’exception du caractère de fin null. L’application peut fournir une valeur négative si la chaîne est terminée. Dans ce cas, la fonction détermine automatiquement la longueur.
    
## <a name="return-value"></a>Valeur renvoy�e

Renvoie les valeurs indiquées pour [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).
  
## <a name="remarks"></a>Remarques

Cette fonction encapsule [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx). **MNLS_CompareStringW** accepte les mêmes paramètres et a le même comportement que [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).
  
## <a name="see-also"></a>Voir aussi



[CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)
  
[CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)

