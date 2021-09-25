---
title: IOlkApptRebaserBeginRebaseAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ed50422e-9edf-4b73-1789-340b70532621
description: Commence une tâche pour la relocalisation de rendez-vous donné une liste de rendez-vous, généralement obtenu à partir de IOlkApptRebaser::EndEnumerateAppointments.
ms.openlocfilehash: e13bf4c738925ccb7994de5c68ddb97d9b70b95c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605378"
---
# <a name="iolkapptrebaserbeginrebaseappointments"></a>IOlkApptRebaser::BeginRebaseAppointments

Commence une tâche pour la relocalisation de rendez-vous donné une liste de rendez-vous, généralement obtenu à partir de [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkApptRebaser](iolkapptrebaser.md).
  
```cpp
HRESULT BeginRebaseAppointments( 
    const SRowSet *pRows, 
    PFNREBASETASKPROGRESS pfnProgress, 
    PFNREBASETASKCOMPLETE pfnComplete, 
    void **ppContext);
```

## <a name="parameters"></a>Paramètres

_pRows_
  
> [in] Obligatoire. Pointeur vers une structure [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) qui décrit les rendez-vous qui ont besoin de relocalisation. Cette structure est généralement obtenue à partir d'un appel antérieur à [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).
    
_pfnProgress_
  
> [in] Facultatif. Pointeur vers une fonction de la progression de tâche rebase pour recevoir les cours. **PFNREBASETASKPROGRESS** est défini dans tzmovelib.h. 
    
_pfnComplete_
  
> [out] Facultatif. Un pointeur vers une fonction de saisie semi-automatique de tâche rebase pour recevoir une notification d'achèvement rebase. **PFNREBASETASKCOMPLETE** est défini dans tzmovelib.h. 
    
_ppContext_
  
> [out] Obligatoire. Pointeur vers un pointeur vers le contexte retourné. Ce contexte sera généralement passé à [IOlkApptRebaser::EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md).
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

Cette tâche s'exécute sur un nouveau thread.
  
## <a name="see-also"></a>Voir aussi

- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

