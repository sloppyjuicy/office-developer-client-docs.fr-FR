---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 65d4257037b18c8fa68cabe0c08091ec67343fa5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782011"
---
# <a name="canceloutstandingrequests"></a>CancelOutstandingRequests

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Informe le connecteur de cluster un calcul Excel a été annulé, et par conséquent, tout en attente d’appels de fonction au sein de cette session peut être annulée ainsi (et que Microsoft Excel n’attend pas de rappels avec leurs résultats).
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a>Paramètres

_ID de session_
  
> ID de la session utilisée par le calcul annulé. Cette valeur correspond à la valeur renvoyée par la [méthode OpenSession](opensession.md).
    
## <a name="return-value"></a>Valeur renvoy�e

**xlHpcRetSuccess** si l’argument _SessionId_ est valide ; **xlHpcRetInvalidSessionId** si l’argument _SessionId_ n’est pas valide ; **xlHpcRetCallFailed** sur les autres erreurs. 
  
## <a name="remarks"></a>Remarques

L’implémentation doit s’arrêter tous les processus pour la session pour améliorer les performances, en tant que les résultats reçus après que cet appel est ignoré par Excel.
  
## <a name="see-also"></a>Voir aussi

- [Fonctions du connecteur de Cluster Excel](excel-cluster-connector-functions.md)

