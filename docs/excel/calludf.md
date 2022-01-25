---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
ms.openlocfilehash: 52b099afc779562af88c4b348225144c43621043
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198561"
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

**xlHpcRetSuccess si** l’appel UDF est correctement lancé ; **xlHpcRetInvalidSessionId** si l’argument _SessionId_ n’est pas valide ; **xlHpcRetCallFailed sur** d’autres échecs, y compris le délai d’arrêt. Si l’appel renvoie un code d’erreur (sauf **xlHpcRetSuccess),** alors Excel considère que l’appel UDF a échoué, invalide _pxAsyncHandle_ et ne s’attend pas à ce qu’un rappel se produise.
  
## <a name="remarks"></a>Remarques

Cette fonction s’exécute de manière asynchrone.
  
## <a name="see-also"></a>Voir aussi

- [Fonctions du connecteur de cluster Excel](excel-cluster-connector-functions.md)

