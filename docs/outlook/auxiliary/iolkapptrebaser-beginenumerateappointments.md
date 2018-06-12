---
title: IOlkApptRebaserBeginEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8946703a-aaa8-6b3f-aa68-931365db620d
description: Commence une tâche pour l'énumération de rendez-vous dans un dossier de calendrier pour rechercher les rendez-vous qui ont besoin de relocalisation.
ms.openlocfilehash: 2ad26692483d87166a538ec2f04d3fc13b9ea930
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782731"
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
  
## <a name="remarks"></a>Note

Cette tâche s'exécute sur un nouveau thread.
  
## <a name="see-also"></a>Voir aussi

- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

