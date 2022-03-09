---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
ms.openlocfilehash: f793ce0ca988069b00e0a19b6ae9488cd8857002
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62464537"
---
# <a name="pingsession"></a>PingSession

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Vérifie si une session est valide. Cette fonction est généralement appelée lorsque Excel doit déterminer si un ID de session précédemment renvoyé est toujours actif et peut être utilisé.
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a>Paramètres

_SessionID_
  
> ID de la session à ping. Cette valeur doit correspondre à un ID renvoyé par un appel précédent [à OpenSession](opensession.md).
    
## <a name="return-value"></a>Valeur renvoyée

**xlHpcRetSuccess si** l’argument _SessionId_ est valide ; sinon **xlHpcRetInvalidSessionId**.
  
## <a name="see-also"></a>Voir aussi

- [OpenSession](opensession.md)
- [Fonctions du connecteur de cluster Excel](excel-cluster-connector-functions.md)

