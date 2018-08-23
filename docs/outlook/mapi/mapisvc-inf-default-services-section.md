---
title: Section [services par défaut] MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a7270bce12f6d91dbb5632f739f4644df866924d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573144"
---
# <a name="mapisvcinf-default-services-section"></a>Section [services par défaut] MapiSvc.inf

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
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


