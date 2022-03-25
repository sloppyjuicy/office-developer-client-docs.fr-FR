---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 66158281661539681bef9d83ed1542565dcf191b
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63783167"
---
# <a name="isbadboundedstringptr"></a>IsBadBoundedStringPtr

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Vérifie que le processus appelant dispose d’un accès en lecture à la plage de mémoire spécifiée.
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |mapiwin.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services. |
   
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

La valeur de retour est zéro lorsque le processus appelant dispose d’un accès en lecture à tous les caractères jusqu’au caractère null de fin de la chaîne ou d’un accès en lecture jusqu’au nombre de caractères spécifié par  _cchMax_.
  
La valeur de retour n’est pas nulle lorsque le processus appelant n’a pas accès en lecture à tous les caractères jusqu’au caractère null de fin de la chaîne ou l’accès en lecture jusqu’au nombre de caractères spécifié par  _cchMax_.
  
## <a name="remarks"></a>Remarques

La **fonction IsBadBoundedStringPtr équivaut** à utiliser **IsBadStringPtr**.
  
## <a name="see-also"></a>Voir aussi



[IsBadStringPtr](https://msdn.microsoft.com/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

