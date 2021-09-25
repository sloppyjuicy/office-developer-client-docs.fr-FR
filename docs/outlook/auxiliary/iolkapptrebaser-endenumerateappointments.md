---
title: IOlkApptRebaserEndEnumerateAppointments
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: bc4506c7-7a4f-940d-d0a6-e0fab4561a88
description: Attend pour l'énumération de rendez-vous dans un dossier de calendrier pour terminer et renvoie une liste de rendez-vous à cette nécessité la relocalisation.
ms.openlocfilehash: 9472f9b1da9db435b8deba12c4468c02311098ee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605371"
---
# <a name="iolkapptrebaserendenumerateappointments"></a>IOlkApptRebaser::EndEnumerateAppointments

Attend pour l'énumération de rendez-vous dans un dossier de calendrier pour terminer et renvoie une liste de rendez-vous à cette nécessité la relocalisation.
  
## <a name="quick-info"></a>Informations rapides

Voir [IOlkApptRebaser](iolkapptrebaser.md).
  
```cpp
HRESULT EndEnumerateAppointments( 
    void *pContext, 
    HRESULT *phResult, 
    MAPIERROR **ppError, 
    SRowSet **ppRows);
```

## <a name="parameters"></a>Paramètres

_pContext_
  
> [in] Obligatoire. Pointeur vers le contexte obtenu par un appel préalable à [IOlkApptRebaser::BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md).
    
_phResult_
  
> [out] Obligatoire. Pointeur vers **HRESULT** pour récupérer les résultats de l'opération d'énumération. 
    
_ppError_
  
> [out] Facultatif. Pointeur vers un pointeur vers une structure **MAPIERROR** pour extraire des informations d'erreur étendues. 
    
_ppRows_
  
> [out] Obligatoire. Pointeur vers un pointeur vers une structure [SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx) qui décrit les rendez-vous qui ont besoin de relocalisation. Cette structure sera généralement passée à [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="see-also"></a>Voir aussi

- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

