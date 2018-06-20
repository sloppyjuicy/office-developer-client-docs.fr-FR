---
title: Méthode CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: af8f7398ed9d5edfbf1615930874a800d8835487
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782021"
---
# <a name="closesession"></a>Méthode CloseSession

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Ferme une session avec un cluster.
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a>Paramètres

_ID de session_
  
> ID de la session pour fermer. Cette valeur doit correspondre à la valeur renvoyée par la [méthode OpenSession](opensession.md).
    
## <a name="return-value"></a>Valeur renvoy�e

**xlHpcRetSuccess** si la session est fermée ; **xlHpcRetInvalidSessionId** si l’argument _SessionId_ n’est pas valide ; **xlHpcRetCallFailed** sur les autres erreurs. 
  
## <a name="see-also"></a>Voir aussi

- [Méthode OpenSession](opensession.md)
- [Fonctions du connecteur de Cluster Excel](excel-cluster-connector-functions.md)

