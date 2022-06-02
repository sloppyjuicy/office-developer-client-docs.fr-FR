---
title: MNLS_WideCharToMultiByte
description: MNLS_WideCharToMultiByte mappe une chaîne UTF-16 (caractère large) à une nouvelle chaîne de caractères, qui ne vient pas nécessairement d’un jeu de caractères multioctets.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
ms.openlocfilehash: e6b023c1d2b7d782f38f3be6d6bff5f40803a6b4
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828219"
---
# <a name="mnls_widechartomultibyte"></a>MNLS_WideCharToMultiByte

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette fonction est similaire à **WideCharToMultiByte**, qui mappe une chaîne UTF-16 (caractère large) à une nouvelle chaîne de caractères. La nouvelle chaîne de caractères ne vient pas nécessairement d’un jeu de caractères multioctets.
  
```cpp
int MNLS_WideCharToMultiByte(
  UINT uCodePage,
  DWORD dwFlags,
  LPCWSTR lpWideCharStr,
  int cchWideChar,
  LPSTR lpMultiByteStr,
  int cchMultiByte,
  LPCSTR lpDefaultChar,
  BOOL FAR *lpfUsedDefaultChar);
```

## <a name="parameters"></a>Paramètres

 _uCodePage_
  
> [in] Page de code à utiliser pour effectuer la conversion.
    
 _dwFlags_
  
> [in] Indicateurs indiquant le type de conversion.
    
 _lpWideCharStr_
  
> [in] Pointeur vers la chaîne Unicode à convertir.
    
 _cchWideChar_
  
> [in] Indicateurs indiquant le type de conversion.
    
 _lpMultiByteStr_
  
> [out] Facultatif. Pointeur vers une mémoire tampon qui reçoit la chaîne convertie.
    
 _cchMultiByte_
  
> [in] Taille, en octets, de la mémoire tampon indiquée par  _lpMultiByteStr_.
    
 _lpDefaultChar_
  
> [in] Facultatif. Pointeur vers le caractère à utiliser si un caractère ne peut pas être représenté dans la page de codes spécifiée.
    
 _lpfUsedDefaultChar_
  
> [out] Facultatif. Pointeur vers un indicateur qui indique si la fonction a utilisé un caractère par défaut dans la conversion.
    
## <a name="return-value"></a>Valeur renvoyée

Retourne le nombre d’octets écrits dans la mémoire tampon pointée par  _lpMultiByteStr_ en cas de réussite. 
  
## <a name="remarks"></a>Remarques

Cette fonction encapsule la fonction **WideCharToMultiByte** . Pour plus d’informations, consultez [WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).
  
## <a name="see-also"></a>Voir aussi



[WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)

