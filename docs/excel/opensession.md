---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
ms.openlocfilehash: 70d09d119fdeeaf357997d4f65131ff6b6d55768
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62198603"
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

