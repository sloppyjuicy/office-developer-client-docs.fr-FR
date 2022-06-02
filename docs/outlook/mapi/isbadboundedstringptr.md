---
title: IsBadBoundedStringPtr
description: IsBadBoundedStringPtr vérifie que le processus appelant dispose d’un accès en lecture à la plage de mémoire spécifiée.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
ms.openlocfilehash: 176857c2e67e2a00c20b72200588cd09b29c5b1b
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828524"
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
  
> [in] Pointeur vers une chaîne ASCII terminée par une valeur Null.
    
 _cchMax_
  
> [in] Taille maximale de la chaîne, en VALEURS CHAR. La fonction vérifie l’accès en lecture dans tous les caractères jusqu’au caractère null de fin de la chaîne, ou jusqu’au nombre de caractères spécifié par ce paramètre, selon la valeur la plus petite. Si ce paramètre est égal à zéro, la valeur de retour est zéro.
    
## <a name="return-value"></a>Valeur renvoyée

La valeur de retour est zéro lorsque le processus appelant dispose d’un accès en lecture à tous les caractères jusqu’au caractère null de fin de la chaîne, ou d’un accès en lecture jusqu’au nombre de caractères spécifié par  _cchMax_.
  
La valeur de retour n’est pas égale à zéro lorsque le processus appelant n’a pas accès en lecture à tous les caractères jusqu’au caractère null de fin de la chaîne, ou l’accès en lecture jusqu’au nombre de caractères spécifié par  _cchMax_.
  
## <a name="remarks"></a>Remarques

La fonction **IsBadBoundedStringPtr** équivaut à l’utilisation **d’IsBadStringPtr**.
  
## <a name="see-also"></a>Voir aussi



[IsBadStringPtr](https://msdn.microsoft.com/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

