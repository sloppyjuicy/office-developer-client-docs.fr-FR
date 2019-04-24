---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 096f57335572c3788fdf129dd3bcf4a76cf62b01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304164"
---
# <a name="calludf"></a>CallUDF

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Appelle une fonction définie par l'utilisateur dans un environnement informatique à hautes performances.
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a>Paramètres

_Session_
  
> ID de la session dans laquelle effectuer l'appel.
    
_XLLName_
  
> Nom de la XLL qui contient la fonction définie par l'utilisateur.
    
_UDFName_
  
> Nom de la fonction définie par l'utilisateur.
    
_CallBackAddr_
  
> Fonction que le connecteur doit appeler lorsque la fonction définie par l'utilisateur est terminée.
    
_pxAsyncHandle_
  
> Le handle asynchrone utilisé par Excel et le connecteur pour effectuer le suivi de l'appel de fonction défini par l'utilisateur en attente. Le connecteur l'utilise ultérieurement lorsque l'appel est terminé, lorsqu'il rappelle dans Excel à l'aide du pointeur de fonction transmis dans l'argument _CallBackAddr_ . 
    
_ArgCount_
  
> Nombre d'arguments à transmettre à la fonction définie par l'utilisateur. La valeur maximale autorisée est 255.
    
_Paramètre1_
  
> Valeur à transmettre à la fonction définie par l'utilisateur. Répétez cet argument pour chaque paramètre indiqué par _ArgCount_.
    
## <a name="return-value"></a>Valeur renvoyée

**xlHpcRetSuccess** si l'appel de la FDU est initié avec succès; **xlHpcRetInvalidSessionId** si l'argument _SessionID_ n'est pas valide; **xlHpcRetCallFailed** sur d'autres défaillances, y compris le délai d'expiration. Si l'appel renvoie tout code d'erreur (à l'exception de **xlHpcRetSuccess**), Excel considère que l'appel de la FDU a échoué, annule la _pxAsyncHandle_et ne s'attend pas à un rappel.
  
## <a name="remarks"></a>Remarques

Cette fonction s'exécute de façon asynchrone.
  
## <a name="see-also"></a>Voir aussi

- [Fonctions du connecteur de cluster Excel](excel-cluster-connector-functions.md)

