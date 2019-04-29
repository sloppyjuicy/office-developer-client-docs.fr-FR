---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0fa5fe57e537a7b8c7d880b934809a6f68ce27a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408361"
---
# <a name="pingsession"></a>PingSession

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Vérifie si une session est valide. Cette fonction est généralement appelée lorsque Excel doit déterminer si un ID de session précédemment renvoyé est toujours actif et peut être utilisé.
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a>Paramètres

_SessionID_
  
> ID de la session à tester. Cette valeur doit correspondre à un ID renvoyé par un appel précédent à [OpenSession](opensession.md).
    
## <a name="return-value"></a>Valeur renvoyée

**xlHpcRetSuccess** si l'argument _SessionID_ est valide; sinon **xlHpcRetInvalidSessionId**.
  
## <a name="see-also"></a>Voir aussi

- [OpenSession](opensession.md)
- [Fonctions du connecteur de cluster Excel](excel-cluster-connector-functions.md)

