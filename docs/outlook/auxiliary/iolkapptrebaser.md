---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: Prend en charge le rebasing des rendez-vous dans un dossier de calendrier.
ms.openlocfilehash: a673b9962c34db99b4aabba4cd7a682fc604200c
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63630433"
---
# <a name="iolkapptrebaser"></a>IOlkApptRebaser

Prend en charge le rebasing des rendez-vous dans un dossier de calendrier.
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Hérite de :  <br/> |**IUnknown** <br/> |
|Fichier d’en-tête :  <br/> |tzmovelib.h  <br/> |
|Implémenté par :  <br/> |tzmovelib.dll  <br/> |
|Appelé par :  <br/> |Applications clientes MAPI  <br/> |
|Exposé sur :  <br/> |Outlook de rebasing  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

||Valeur |
|:-----|:-----|
|**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)** <br/> |Commence une tâche pour l'énumération de rendez-vous dans un dossier de calendrier pour rechercher les rendez-vous qui ont besoin de relocalisation. |
|**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)** <br/> |Attend pour l'énumération de rendez-vous dans un dossier de calendrier pour terminer et renvoie une liste de rendez-vous à cette nécessité la relocalisation. |
|**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)** <br/> |Commence une tâche de rebasing de rendez-vous en fonction d’une liste de rendez-vous, généralement obtenue à partir de **EndEnumerateAppointments**. |
|**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)** <br/> |Attend des rendez-vous pour terminer la relocalisation et récupère les résultats. |
   
## <a name="see-also"></a>Consultez aussi

- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

