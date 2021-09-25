---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f02b20c5a8355f68a937ad96cf4106c37f3a767a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614618"
---
# <a name="calludf"></a>CallUDF

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Appelle une fonction définie par l’utilisateur dans un environnement informatique hautes performances.
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a>Paramètres

_SessionId_
  
> ID de la session dans laquelle effectuer l’appel.
    
_XLLName_
  
> Nom du XLL qui contient la fonction définie par l’utilisateur.
    
_UDFName_
  
> Nom de la fonction définie par l’utilisateur.
    
_CallBackAddr_
  
> Fonction que le connecteur doit appeler lorsque la fonction définie par l’utilisateur est terminée.
    
_pxAsyncHandle_
  
> Handle asynchrone utilisé par Excel et le connecteur pour suivre l’appel de fonction définie par l’utilisateur en attente. Le connecteur l’utilise ultérieurement lorsque l’appel est terminé, lorsqu’il rappelle Excel à l’aide du pointeur de fonction transmis dans l’argument _CallBackAddr._ 
    
_ArgCount_
  
> Nombre d’arguments à transmettre à la fonction définie par l’utilisateur. La valeur maximale autorisée est 255.
    
_Parameter1_
  
> Valeur à transmettre à la fonction définie par l’utilisateur. Répétez cet argument pour chaque paramètre indiqué par  _ArgCount_.
    
## <a name="return-value"></a>Valeur renvoyée

**xlHpcRetSuccess si** l’appel UDF est correctement initié ; **xlHpcRetInvalidSessionId** si l’argument _SessionId_ n’est pas valide ; **xlHpcRetCallFailed sur** d’autres échecs, y compris le délai d’arrêt. Si l’appel renvoie un code d’erreur (sauf **xlHpcRetSuccess),** alors Excel considère que l’appel UDF a échoué, invalide _pxAsyncHandle_ et ne s’attend pas à ce qu’un rappel se produise.
  
## <a name="remarks"></a>Remarques

Cette fonction s’exécute de manière asynchrone.
  
## <a name="see-also"></a>Voir aussi

- [Fonctions du connecteur de cluster Excel](excel-cluster-connector-functions.md)

