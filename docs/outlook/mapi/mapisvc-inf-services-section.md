---
title: Section [services] MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 520478061e192f9fec97c6b13edde7833a13a3d6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571394"
---
# <a name="mapisvcinf-services-section"></a>Section [services] MapiSvc.inf

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
La section **[Services]** répertorie les services de message qui sont installés sur un ordinateur. Entrées de cette section utilisent le format suivant : 
  
 **[Services]**
  
 _nom de la section service de message_ =  _nom de service de message_
  
Le nom de la section service de message est qu'une chaîne définie par le service de message qui se lie cette entrée à la section correspondante pour le service ailleurs dans le fichier mapisvc.inf. Le nom de service de message est le nom du service installé. La section suivante montre les trois services du message : le Service de banque de messages, My Service propre et le carnet d’adresses par défaut. Ces services sont fictives, à des fins d’illustration uniquement. Chaque implémentation de service de message doit substituer l’entrée appropriée pour son service de message dans cette section.
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

Chaque entrée de cette section comporte une section correspondante qui lui est propre stockant des informations pour le service de message. Par exemple, la section correspondante pour le carnet d’adresses par défaut est appelée [AB].
  

