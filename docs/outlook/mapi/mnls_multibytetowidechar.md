---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Dernière modification: 21 février 2012'
ms.openlocfilehash: 1f137aba40703fe84e5753ee6e370262f780f0a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338240"
---
# <a name="mnlsmultibytetowidechar"></a>MNLS_MultiByteToWideChar

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Semblable à **MultiByteToWideChar**, qui mappe une chaîne de caractères à une chaîne de caractères UTF-16 (caractères larges). La chaîne de caractères ne fait pas nécessairement partir d'un jeu de caractères codés sur plusieurs octets.
  
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
  
> dans Page de codes à utiliser lors de la conversion.
    
 _dwFlags_
  
> dans Indicateurs indiquant le type de conversion.
    
 _lpMultiByteStr_
  
> dans Pointeur vers la chaîne de caractères à convertir.
    
 _cchMultiByte_
  
> dans Taille, en octets, de la chaîne indiquée par le paramètre _lpMultiByteStr_ . 
    
 _lpWideCharStr_
  
> [out] Facultatif. Pointeur vers une mémoire tampon qui reçoit la chaîne convertie.
    
 _cchWideChar_
  
> dans Taille, en caractères, de la mémoire tampon indiquée par _lpWideCharStr_.
    
## <a name="return-value"></a>Valeur renvoyée

Renvoie le nombre de caractères écrits dans la mémoire tampon indiquée par _lpWideCharStr_ en cas de réussite. 
  
## <a name="remarks"></a>Remarques

Cette fonction encapsule la fonction **MultiByteToWideChar** . Pour plus d'informations, consultez la rubrique [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).
  

