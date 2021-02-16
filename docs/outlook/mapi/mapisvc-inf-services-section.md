---
title: MapiSvc.inf [Services] Section
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e5bf5242ef673976ebda928d6ce4862e3e7dd072
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434780"
---
# <a name="mapisvcinf-services-section"></a>MapiSvc.inf [Services] Section

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La section **[Services]** répertorie les services de message installés sur un ordinateur. Les entrées de cette section utilisent le format suivant : 
  
 **[Services]**
  
 _nom de la section_  =   message-service _nom du service de message_
  
Le nom de la section de service de message est une chaîne définie par le service de message qui lie cette entrée à une section correspondante pour le service ailleurs dans mapisvc.inf. Le nom du service de message est le nom du service installé. La section suivante présente trois services de message : le carnet d’adresses par défaut, mon propre service et le service de magasin de messages. Ces services sont fictifs, à des fins d’illustration uniquement. Chaque implémenteur de service de message remplacerait l’entrée appropriée pour son service de message dans cette section.
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

Chaque entrée de cette section possède une section correspondante dans laquelle les informations du service de message sont stockées. Par exemple, la section correspondante du carnet d’adresses par défaut est appelée [AB].
  

