---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 1d55f22de88b274d0403f81717d0fddefbea0219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782007"
---
# <a name="calludf"></a>CallUDF

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Appelle une fonction définie par l’utilisateur dans un environnement informatique hautes performances.
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a>Paramètres

_ID de session_
  
> ID de la session dans laquelle effectuer l’appel.
    
_XLLName_
  
> Le nom de la ressource XLL contenant la fonction définie par l’utilisateur.
    
_UDFName_
  
> Nom de la fonction définie par l’utilisateur.
    
_CallBackAddr_
  
> La fonction que le connecteur doit appeler lorsque la fonction définie par l’utilisateur est terminée.
    
_pxAsyncHandle_
  
> La poignée asynchrone utilisée par Excel et le connecteur pour effectuer le suivi de l’appel en attente de fonction définie par l’utilisateur. Le connecteur utilise plus tard lors de l’appel est terminé, lorsqu’il rappelle dans Excel à l’aide du pointeur de fonction passés dans l’argument _CallBackAddr_ . 
    
_ArgCount_
  
> Le nombre d’arguments à transmettre à la fonction définie par l’utilisateur. La valeur maximale autorisée est de 255.
    
_Parameter1_
  
> Une valeur à passer à la fonction définie par l’utilisateur. Répétez cet argument pour chaque paramètre indiqué par _ArgCount_.
    
## <a name="return-value"></a>Valeur renvoy�e

**xlHpcRetSuccess** si l’appel des UDF est démarré ; **xlHpcRetInvalidSessionId** si l’argument _SessionId_ n’est pas valide ; **xlHpcRetCallFailed** sur les autres erreurs, y compris le délai d’expiration. Si l’appel retourne un code d’erreur (n’est pas **xlHpcRetSuccess**), puis Excel considère que l’appel des UDF a échoué, invalide le _pxAsyncHandle_et n’attend pas un rappel se produise.
  
## <a name="remarks"></a>Remarques

Cette fonction s’exécute en mode asynchrone.
  
## <a name="see-also"></a>Voir aussi

- [Fonctions du connecteur de Cluster Excel](excel-cluster-connector-functions.md)

