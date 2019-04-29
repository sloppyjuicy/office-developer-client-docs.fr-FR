---
title: IOlkApptRebaserBeginEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8946703a-aaa8-6b3f-aa68-931365db620d
description: Commence une tâche pour l'énumération de rendez-vous dans un dossier de calendrier pour rechercher les rendez-vous qui ont besoin de relocalisation.
ms.openlocfilehash: cc89b3510f09bb98fd6720cb6d5ab3edeb13eac8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407269"
---
# <a name="iolkapptrebaserbeginenumerateappointments"></a>IOlkApptRebaser::BeginEnumerateAppointments

Commence une tâche pour l'énumération de rendez-vous dans un dossier de calendrier pour rechercher les rendez-vous qui ont besoin de relocalisation.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkApptRebaser](iolkapptrebaser.md).
  
```cpp
HRESULT BeginEnumerateAppointments( 
    PFNREBASETASKPROGRESS pfnProgress, 
    void **ppContext);
```

## <a name="parameters"></a>Paramètres

_pfnProgress_
  
> [in] Facultatif. Pointeur vers une fonction de la progression de tâche rebase pour recevoir les cours. **PFNREBASETASKPROGRESS** est défini dans tzmovelib.h. 
    
_ppContext_
  
> [out] Obligatoire. Pointeur vers un pointeur vers le contexte retourné. Ce contexte est passé à [IOlkApptRebaser::EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md).
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

Cette tâche s'exécute sur un nouveau thread.
  
## <a name="see-also"></a>Voir aussi

- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

