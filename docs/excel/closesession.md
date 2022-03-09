---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
ms.openlocfilehash: 304acc3b80d0bdf4eae7d101514d9c1c9334b871
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62463169"
---
# <a name="closesession"></a>CloseSession

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Met fin à une session avec un cluster.
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a>Paramètres

_SessionId_
  
> ID de la session à fermer. Cette valeur doit correspondre à la valeur renvoyée [par OpenSession](opensession.md).
    
## <a name="return-value"></a>Valeur renvoyée

**xlHpcRetSuccess si** la session s’est fermée ; **xlHpcRetInvalidSessionId** si l’argument _SessionId_ n’est pas valide ; **xlHpcRetCallFailed sur** d’autres échecs. 
  
## <a name="see-also"></a>Voir aussi

- [OpenSession](opensession.md)
- [Fonctions du connecteur de cluster Excel](excel-cluster-connector-functions.md)

