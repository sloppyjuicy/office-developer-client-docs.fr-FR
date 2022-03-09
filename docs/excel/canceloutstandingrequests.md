---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
ms.openlocfilehash: f3c061014e31d131ccd5ab3b3a1398c2a389a51a
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62464830"
---
# <a name="canceloutstandingrequests"></a>CancelOutstandingRequests

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Informe le connecteur de cluster qu’un calcul Excel a été annulé et que tous les appels de fonction en attente au sein de cette session peuvent également être annulés (et que le Excel ne s’attend pas à des rappels avec leurs résultats).
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a>Paramètres

_SessionID_
  
> ID de la session utilisée par le calcul annulé. Cette valeur correspond à la valeur renvoyée par [OpenSession](opensession.md).
    
## <a name="return-value"></a>Valeur renvoyée

**xlHpcRetSuccess si** l’argument _SessionId_ est valide ; **xlHpcRetInvalidSessionId** si l’argument _SessionId_ n’est pas valide ; **xlHpcRetCallFailed sur** d’autres échecs. 
  
## <a name="remarks"></a>Remarques

Les implémenteurs doivent arrêter tous les processus de la session pour améliorer les performances, car tous les résultats reçus après cet appel seront ignorés par Excel.
  
## <a name="see-also"></a>Voir aussi

- [Fonctions du connecteur de cluster Excel](excel-cluster-connector-functions.md)

