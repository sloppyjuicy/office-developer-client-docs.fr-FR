---
title: Méthode OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 782843f11643e203488b313181d224443a1d36c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782184"
---
# <a name="opensession"></a>Méthode OpenSession

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Crée une session dans laquelle les fonctions définies par l’utilisateur peuvent être exécutées.
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a>Paramètres

_Paramètres_
  
> Pointeur vers une chaîne UNICODE délimitée par des paramètres pour la session. Excel n’utilise pas cet argument.
    
## <a name="return-value"></a>Valeur renvoy�e

Un ID de session à utiliser dans les autres appels vers le connecteur de cluster, si la session a été créée avec succès ; dans le cas contraire **xlHpcRetCallFailed**.
  
## <a name="see-also"></a>Voir aussi

- [Fonctions du connecteur de Cluster Excel](excel-cluster-connector-functions.md)

