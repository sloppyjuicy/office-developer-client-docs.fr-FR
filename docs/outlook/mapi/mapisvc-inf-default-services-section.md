---
title: MapiSvc.inf [Default Services] Section
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
ms.openlocfilehash: ae94a98895b616c977fffbe5f6eeaf487a987621
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376573"
---
# <a name="mapisvcinf-default-services-section"></a>MapiSvc.inf [Default Services] Section

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La section **[Services par défaut]** répertorie tous les services de message sélectionnés comme services de message par défaut. Ces services de message par défaut sont un sous-ensemble des services de messages répertoriés dans la section **[Services** ]. Lorsqu’un programme de configuration de profil crée un profil par défaut, les services de message de cette section sont automatiquement inclus. 
  
Les entrées utilisent le même format que les entrées de la section **[Services],** comme illustré ci-après : 
  
 **[Services par défaut]**
  
 _nom de la section_ =   message-service _nom du service de message_
  
Les entrées suivantes seraient incluses dans la section **[Services** par défaut] pour le mapisvc.inf illustré dans l’illustration précédente : 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


