---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
ms.openlocfilehash: f159b24e8a95fd41318e27d09bac1ae36ccb74b4
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62199730"
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

**xlHpcRetSuccess si** l’argument  _SessionId_ est valide ; sinon **xlHpcRetInvalidSessionId**.
  
## <a name="see-also"></a>Voir aussi

- [OpenSession](opensession.md)
- [Fonctions du connecteur de cluster Excel](excel-cluster-connector-functions.md)

