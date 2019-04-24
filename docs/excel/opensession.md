---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3e4df0c5772f28ab4ab8d84eaddfe4409a88061b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301630"
---
# <a name="opensession"></a>OpenSession

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Crée une session dans laquelle des fonctions définies par l'utilisateur peuvent être exécutées.
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a>Paramètres

_Paramètres_
  
> Pointeur vers une chaîne UNICODE délimitée par des points-virgules de paramètres pour la session. Excel n'utilise pas cet argument.
    
## <a name="return-value"></a>Valeur renvoyée

Un ID de session à utiliser dans d'autres appels vers le connecteur de cluster, si la session a été correctement créée; sinon **xlHpcRetCallFailed**.
  
## <a name="see-also"></a>Voir aussi

- [Fonctions du connecteur de cluster Excel](excel-cluster-connector-functions.md)

