---
title: Section MapiSvc.inf [Services par défaut]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 5d860135d846df8ef1ea0784d7430c71ad0fe64e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784772"
---
# <a name="mapisvcinf-default-services-section"></a>Section MapiSvc.inf [Services par défaut]

  
  
**S’applique à**: Outlook 
  
La section **[Services par défaut]** répertorie tous les services de message sont sélectionnés en tant que services de messagerie par défaut. Ces services de messagerie par défaut sont un sous-ensemble des services message répertorié dans la section **[Services]** . Lorsqu’un programme de configuration du profil crée un profil par défaut, les services de message dans cette section sont inclus automatiquement. 
  
Les entrées utilisent le même format comme des entrées dans la section **[Services]** , comme illustré suivantes : 
  
 **[Services par défaut]**
  
 _nom de la section service de message_ =  _nom de service de message_
  
Les entrées suivantes doivent figurer dans la section **[Services par défaut]** pour le fichier mapisvc.inf indiqué dans l’illustration précédente : 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


