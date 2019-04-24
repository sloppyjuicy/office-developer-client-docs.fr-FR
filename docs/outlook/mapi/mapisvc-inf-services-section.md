---
title: Section [services] MapiSvc. inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: e5bf5242ef673976ebda928d6ce4862e3e7dd072
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270020"
---
# <a name="mapisvcinf-services-section"></a>Section [services] MapiSvc. inf

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La section **[services]** répertorie les services de messagerie installés sur un ordinateur. Les entrées de cette section utilisent le format suivant: 
  
 **Services**
  
 _message-nom_ =  de la section du service de_messagerie nom du service_
  
Le nom de section du service de message est une chaîne définie par le service de messagerie qui lie cette entrée à une section correspondante pour le service ailleurs dans MAPISVC. inf. Le nom du service de messagerie est le nom du service installé. La section suivante présente trois services de messagerie: le carnet d'adresses par défaut, mon propre service et le service de banque de messages. Ces services sont fictifs, à des fins d'illustration uniquement. Chaque implémenteur de service de messagerie substitue l'entrée appropriée pour son service de messagerie dans cette section.
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

Chaque entrée de cette section a une section correspondante de son propre emplacement de stockage des informations sur le service de messagerie. Par exemple, la section correspondante pour le carnet d'adresses par défaut est appelée [AB].
  

