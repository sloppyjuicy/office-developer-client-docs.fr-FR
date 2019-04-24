---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 882458ab096cbced8e0635dab65fe0b1d680388f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310996"
---
# <a name="canceloutstandingrequests"></a>CancelOutstandingRequests

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Informe le connecteur de cluster qu'un calcul Excel a été annulé et, par conséquent, tous les appels de fonction en attente au sein de cette session peuvent être annulés également (et qu'Excel n'attend pas les rappels avec leurs résultats).
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a>Paramètres

_SessionID_
  
> ID de la session utilisée par le calcul annulé. Cette valeur correspond à la valeur renvoyée par [OpenSession](opensession.md).
    
## <a name="return-value"></a>Valeur renvoyée

**xlHpcRetSuccess** si l'argument _SessionID_ est valide; **xlHpcRetInvalidSessionId** si l'argument _SessionID_ n'est pas valide; **xlHpcRetCallFailed** sur d'autres défaillances. 
  
## <a name="remarks"></a>Remarques

Les responsables de l'implémentation doivent arrêter tous les processus de la session pour améliorer les performances, comme tout résultat reçu après que cet appel sera ignoré par Excel.
  
## <a name="see-also"></a>Voir aussi

- [Fonctions du connecteur de cluster Excel](excel-cluster-connector-functions.md)

