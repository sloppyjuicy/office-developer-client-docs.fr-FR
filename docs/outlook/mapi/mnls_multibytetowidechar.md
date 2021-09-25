---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Last modified: February 21, 2012'
ms.openlocfilehash: a5f0d0d3e209ec1bb1b87b822badcb581a540a35
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583967"
---
# <a name="mnls_multibytetowidechar"></a>MNLS_MultiByteToWideChar

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Similaire à **MultiByteToWideChar**, qui mappé une chaîne de caractères à une chaîne UTF-16 (caractère large). La chaîne de caractères n’est pas nécessairement un jeu de caractères multioctets.
  
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
  
> [in] Page de code à utiliser lors de la conversion.
    
 _dwFlags_
  
> [in] Indicateurs indiquant le type de conversion.
    
 _lpMultiByteStr_
  
> [in] Pointeur vers la chaîne de caractères à convertir.
    
 _cchMultiByte_
  
> [in] Taille, en octets, de la chaîne indiquée par le paramètre _lpMultiByteStr._ 
    
 _lpWideCharStr_
  
> [out] Facultatif. Pointeur vers une mémoire tampon qui reçoit la chaîne convertie.
    
 _cchWideChar_
  
> [in] Taille, en caractères, de la mémoire tampon indiquée par  _lpWideCharStr_.
    
## <a name="return-value"></a>Valeur renvoyée

Renvoie le nombre de caractères écrits dans la mémoire tampon indiquée par  _lpWideCharStr_ en cas de réussite. 
  
## <a name="remarks"></a>Remarques

Cette fonction encapsule **la fonction MultiByteToWideChar.** Pour plus d’informations, [voir MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).
  

