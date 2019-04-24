---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: 'Dernière modification: 21 février 2012'
ms.openlocfilehash: ad41f9b6060e5cfbabecfd9bb29a47815929d6b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338730"
---
# <a name="mnlswidechartomultibyte"></a>MNLS_WideCharToMultiByte

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette fonction est similaire à **WideCharToMultiByte**, qui mappe une chaîne UTF-16 (caractères larges) à une nouvelle chaîne de caractères. La nouvelle chaîne de caractères n'est pas nécessairement à partir d'un jeu de caractères codé sur plusieurs octets.
  
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
  
> dans Page de codes à utiliser lors de la conversion.
    
 _dwFlags_
  
> dans Indicateurs indiquant le type de conversion.
    
 _lpWideCharStr_
  
> dans Pointeur vers la chaîne Unicode à convertir.
    
 _cchWideChar_
  
> dans Indicateurs indiquant le type de conversion.
    
 _lpMultiByteStr_
  
> [out] Facultatif. Pointeur vers une mémoire tampon qui reçoit la chaîne convertie.
    
 _cchMultiByte_
  
> dans Taille, en octets, de la mémoire tampon indiquée par _lpMultiByteStr_.
    
 _lpDefaultChar_
  
> [in] Facultatif. Pointeur vers le caractère à utiliser si un caractère ne peut pas être représenté dans la page de codes spécifiée.
    
 _lpfUsedDefaultChar_
  
> [out] Facultatif. Pointeur vers un indicateur qui indique si la fonction a utilisé un caractère par défaut dans la conversion.
    
## <a name="return-value"></a>Valeur renvoyée

Renvoie le nombre d'octets écrits dans la mémoire tampon vers laquelle pointe _lpMultiByteStr_ en cas de réussite. 
  
## <a name="remarks"></a>Remarques

Cette fonction encapsule la fonction **WideCharToMultiByte** . Pour plus d'informations, consultez la rubrique [WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).
  
## <a name="see-also"></a>Voir aussi



[WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)

