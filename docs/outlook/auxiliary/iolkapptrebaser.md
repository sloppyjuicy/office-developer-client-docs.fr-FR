---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: Prend en charge le rebasing des rendez-vous dans un dossier de calendrier.
ms.openlocfilehash: 28ebe305548127f384dbbd28bd5f29a1de526859
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564497"
---
# <a name="iolkapptrebaser"></a>IOlkApptRebaser

Prend en charge le rebasing des rendez-vous dans un dossier de calendrier.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérite de :  <br/> |**IUnknown** <br/> |
|Fichier d’en-tête :  <br/> |tzmovelib.h  <br/> |
|Implémenté par :  <br/> |tzmovelib.dll  <br/> |
|Appelé par :  <br/> |Applications clientes MAPI  <br/> |
|Exposé sur :  <br/> |Outlook de rebasing  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)** <br/> |Commence une tâche pour l'énumération de rendez-vous dans un dossier de calendrier pour rechercher les rendez-vous qui ont besoin de relocalisation.  <br/> |
|**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)** <br/> |Attend pour l'énumération de rendez-vous dans un dossier de calendrier pour terminer et renvoie une liste de rendez-vous à cette nécessité la relocalisation.  <br/> |
|**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)** <br/> |Commence une tâche pour le rebasing de rendez-vous, en fonction d’une liste de rendez-vous, généralement obtenue à partir de **EndEnumerateAppointments**.  <br/> |
|**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)** <br/> |Attend des rendez-vous pour terminer la relocalisation et récupère les résultats.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

