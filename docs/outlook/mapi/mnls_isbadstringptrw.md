---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: 'Dernière modification : 20 février 2012'
ms.openlocfilehash: 0052d0bd6b485340a92cca9f22ca65c9e2442df6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589566"
---
# <a name="mnlsisbadstringptrw"></a>MNLS_IsBadStringPtrW

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Vérifie qu’un pointeur vers une chaîne large est valide.
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a>Paramètres

 _lpsz_
  
> [in] Pointeur vers la chaîne de caractères large.
    
 _ucchMax_
  
> [in] La longueur maximale de la chaîne de caractères, y compris la marque de fin.
    
## <a name="return-value"></a>Valeur renvoy�e

Renvoie une valeur Boolean qui a la valeur true si la chaîne est incorrecte.
  
## <a name="remarks"></a>Remarques

Cette fonction encapsule [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx). Pour plus d’informations, voir [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx).
  

