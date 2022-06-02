---
title: MNLS_MultiByteToWideChar
description: MNLS_MultiByteToWideChar mappe une chaîne de caractères à une chaîne UTF-16 (caractère large), qui n’est pas nécessairement d’un jeu de caractères multioctets.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
ms.openlocfilehash: 4e27d1aab19194e36d6283dd87d57ff7954be252
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828324"
---
# <a name="mnls_multibytetowidechar"></a>MNLS_MultiByteToWideChar

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Similaire à **MultiByteToWideChar**, qui mappe une chaîne de caractères à une chaîne UTF-16 (caractère large). La chaîne de caractères ne vient pas nécessairement d’un jeu de caractères multioctets.
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a>Paramètres

 _uCodePage_
  
> [in] Page de code à utiliser pour effectuer la conversion.
    
 _dwFlags_
  
> [in] Indicateurs indiquant le type de conversion.
    
 _lpMultiByteStr_
  
> [in] Pointeur vers la chaîne de caractères à convertir.
    
 _cchMultiByte_
  
> [in] Taille, en octets, de la chaîne indiquée par le paramètre  _lpMultiByteStr_ . 
    
 _lpWideCharStr_
  
> [out] Facultatif. Pointeur vers une mémoire tampon qui reçoit la chaîne convertie.
    
 _cchWideChar_
  
> [in] Taille, en caractères, de la mémoire tampon indiquée par  _lpWideCharStr_.
    
## <a name="return-value"></a>Valeur renvoyée

Retourne le nombre de caractères écrits dans la mémoire tampon indiquée par  _lpWideCharStr_ en cas de réussite. 
  
## <a name="remarks"></a>Remarques

Cette fonction encapsule la fonction **MultiByteToWideChar** . Pour plus d’informations, consultez [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).
  

