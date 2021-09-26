---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a9103430bf340837f22302d5ba76adcb197e8fdb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631495"
---
# <a name="opensession"></a>OpenSession

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Crée une session dans laquelle les fonctions définies par l’utilisateur peuvent être exécutées.
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a>Paramètres

_Paramètres_
  
> Pointeur vers une chaîne de paramètres UNICODE délimitée par des points-virgules pour la session. Excel n’utilise pas cet argument.
    
## <a name="return-value"></a>Valeur renvoyée

ID de session à utiliser dans d’autres appels au connecteur de cluster, si la session a été correctement créée ; sinon **xlHpcRetCallFailed**.
  
## <a name="see-also"></a>Voir aussi

- [Fonctions du connecteur de cluster Excel](excel-cluster-connector-functions.md)

