---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9d5ebb0e16138c3cc65ff6fd7c635e5498c9c1ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278833"
---
# <a name="isbadboundedstringptr"></a>IsBadBoundedStringPtr

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Vérifie que le processus appelant dispose d’un accès en lecture à la plage de mémoire spécifiée.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |mapiwin.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services.  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a>Paramètres

 _lpsz_
  
> [in] Pointeur vers une chaîne ASCII terminée par null.
    
 _cchMax_
  
> [in] Taille maximale de la chaîne, en chars. La fonction vérifie l’accès en lecture dans tous les caractères jusqu’au caractère null de fin de la chaîne ou jusqu’au nombre de caractères spécifié par ce paramètre, selon la valeur la plus petite. Si ce paramètre est zéro, la valeur de retour est zéro.
    
## <a name="return-value"></a>Valeur renvoyée

La valeur de retour est zéro lorsque le processus appelant a un accès en lecture à tous les caractères jusqu’au caractère null de fin de la chaîne, ou un accès en lecture jusqu’au nombre de caractères spécifié par  _cchMax_.
  
La valeur de retour est non nulle lorsque le processus appelant n’a pas accès en lecture à tous les caractères jusqu’au caractère null de fin de la chaîne, ou l’accès en lecture jusqu’au nombre de caractères spécifié par  _cchMax_.
  
## <a name="remarks"></a>Remarques

La **fonction IsBadBoundedStringPtr** équivaut à utiliser **IsBadStringPtr**.
  
## <a name="see-also"></a>Voir aussi



[IsBadStringPtr](https://msdn.microsoft.com/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

