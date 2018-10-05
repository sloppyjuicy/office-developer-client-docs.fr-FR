---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: 'Dernière modification : 21 février 2012'
ms.openlocfilehash: ad41f9b6060e5cfbabecfd9bb29a47815929d6b5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385514"
---
# <a name="mnlswidechartomultibyte"></a>MNLS_WideCharToMultiByte

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette fonction est similaire à **WideCharToMultiByte**qui mappe la chaîne UTF-16 (caractères étendus) avec une nouvelle chaîne de caractères. La nouvelle chaîne de caractères est pas nécessairement à partir d’un caractère multi-octets définie.
  
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
  
> [in] Page de codes à utiliser lors de la conversion.
    
 _dwFlags_
  
> [in] Indicateurs indiquant le type de conversion.
    
 _lpWideCharStr_
  
> [in] Pointeur vers la chaîne Unicode à convertir.
    
 _cchWideChar_
  
> [in] Indicateurs indiquant le type de conversion.
    
 _lpMultiByteStr_
  
> [out] Facultatif. Pointeur vers un tampon qui reçoit la chaîne convertie.
    
 _cchMultiByte_
  
> [in] Taille, en octets, de la mémoire tampon indiquée par _lpMultiByteStr_.
    
 _lpDefaultChar_
  
> [in] Facultatif. Pointeur vers le caractère à utiliser si un caractère ne peut pas être représenté dans la page de code spécifié.
    
 _lpfUsedDefaultChar_
  
> [out] Facultatif. Pointeur vers un indicateur qui indique si la fonction a utilisé un caractère par défaut lors de la conversion.
    
## <a name="return-value"></a>Valeur renvoyée

Renvoie le nombre d’octets écrits dans la mémoire tampon vers laquelle pointée _lpMultiByteStr_ si l’opération réussit. 
  
## <a name="remarks"></a>Remarques

Cette fonction encapsule la fonction **WideCharToMultiByte** . Pour plus d’informations, voir [WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).
  
## <a name="see-also"></a>Voir aussi



[WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)

