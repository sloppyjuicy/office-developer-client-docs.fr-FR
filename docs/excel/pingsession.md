---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 165be9eada54b2030471fc10e7a0bf0c7dcc7c8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782197"
---
# <a name="pingsession"></a>PingSession

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Vérifie si une session est valide. Cette fonction est généralement appelée lorsque Excel doit déterminer si un ID de session précédemment retourné est toujours actif et peut être utilisé.
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a>Paramètres

_ID de session_
  
> ID de la session Ping. Cette valeur doit correspondre à un ID renvoyé par un appel précédent à la [méthode OpenSession](opensession.md).
    
## <a name="return-value"></a>Valeur renvoy�e

**xlHpcRetSuccess** si l’argument _SessionId_ est valide ; dans le cas contraire **xlHpcRetInvalidSessionId**.
  
## <a name="see-also"></a>Voir aussi

- [Méthode OpenSession](opensession.md)
- [Fonctions du connecteur de Cluster Excel](excel-cluster-connector-functions.md)

