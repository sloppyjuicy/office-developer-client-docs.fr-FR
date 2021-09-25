---
title: MapiSvc.inf [Default Services] Section
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e99fec901bac6f72ac1ded4934896fd3869e89b6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595755"
---
# <a name="mapisvcinf-default-services-section"></a>MapiSvc.inf [Default Services] Section

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La section **[Services par défaut]** répertorie tous les services de message sélectionnés comme services de message par défaut. Ces services de message par défaut sont un sous-ensemble des services de message répertoriés dans la section **[Services].** Lorsqu’un programme de configuration de profil crée un profil par défaut, les services de message de cette section sont automatiquement inclus. 
  
Les entrées utilisent le même format que les entrées de la section **[Services],** comme illustré ci-après : 
  
 **[Services par défaut]**
  
 _nom de la section_  =   message-service _nom du service de message_
  
Les entrées suivantes seraient incluses dans la section **[Default Services]** pour le mapisvc.inf illustré dans l’illustration précédente : 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


