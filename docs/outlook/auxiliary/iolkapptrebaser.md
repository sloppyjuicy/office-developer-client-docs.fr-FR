---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: Prend en charge la redéfinition des rendez-vous dans un dossier de calendrier.
ms.openlocfilehash: 57ca59121f74c7b64a84282c7493e4aed3179f7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782738"
---
# <a name="iolkapptrebaser"></a>IOlkApptRebaser

Prend en charge la redéfinition des rendez-vous dans un dossier de calendrier.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérite de :  <br/> |**IUnknown** <br/> |
|Fichier d’en-tête :  <br/> |tzmovelib.h  <br/> |
|Implémentée par :  <br/> |tzmovelib.dll  <br/> |
|Appelée par :  <br/> |Applications clientes MAPI  <br/> |
|Exposée sur :  <br/> |Objet redéfinition Outlook  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)** <br/> |Commence une tâche pour l'énumération de rendez-vous dans un dossier de calendrier pour rechercher les rendez-vous qui ont besoin de relocalisation.  <br/> |
|**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)** <br/> |Attend pour l'énumération de rendez-vous dans un dossier de calendrier pour terminer et renvoie une liste de rendez-vous à cette nécessité la relocalisation.  <br/> |
|**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)** <br/> |Commence une tâche pour une liste de rendez-vous, généralement obtenu à partir de **EndEnumerateAppointments**redéfinir des rendez-vous.  <br/> |
|**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)** <br/> |Attend des rendez-vous pour terminer la relocalisation et récupère les résultats.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

