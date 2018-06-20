---
title: Section MapiSvc.inf [Services]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 19031f6c02f3e8e925adfc8d2affa43fb6532fee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784777"
---
# <a name="mapisvcinf-services-section"></a>Section MapiSvc.inf [Services]

  
  
**S’applique à**: Outlook 
  
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
  

