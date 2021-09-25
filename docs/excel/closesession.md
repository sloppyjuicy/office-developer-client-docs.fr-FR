---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cba9dbdbcab59dc178a5ae0573ff3e7f0009d72b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593011"
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

**xlHpcRetSuccess si** la session s’est fermée ; **xlHpcRetInvalidSessionId** si l’argument  _SessionId_ n’est pas valide ; **xlHpcRetCallFailed sur** d’autres échecs. 
  
## <a name="see-also"></a>Voir aussi

- [OpenSession](opensession.md)
- [Fonctions du connecteur de cluster Excel](excel-cluster-connector-functions.md)

