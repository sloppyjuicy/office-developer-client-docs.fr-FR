---
title: Notifications de formulaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97ff2733-a2b1-4da0-b628-00850fc7925b
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: e9c10f78af6dff2e0d0c59d0bfe59be07dccd4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351477"
---
# <a name="mapi-forms-notifications"></a>Notifications de formulaires MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'inscription et la gestion des notifications à partir des objets de formulaire constituent un processus différent de celui des autres objets MAPI. Les récepteurs de notification pour les notifications de formulaire implémentent l'interface **IMAPIViewAdviseSink** ou **IMAPIFormAdviseSink** au lieu de **IMAPIAdviseSink**. [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) et [IMAPIFormAdviseSink: IUnknown](imapiformadvisesinkiunknown.md) chacune d'elles ont plusieurs méthodes, une pour chacun des événements possibles que la source de notification correspondante est capable de générer. Par exemple, **IMAPIFormAdviseSink** comporte deux méthodes: [IMAPIFormAdviseSink:: OnChange](imapiformadvisesink-onchange.md) pour gérer une modification apportée à l'état de la visionneuse de formulaires et [IMAPIFormAdviseSink:: OnActivateNext](imapiformadvisesink-onactivatenext.md) pour afficher un nouveau message avec le bon format. 
  
La stratégie de gestion des événements pour les formulaires est similaire à la stratégie de gestion des événements implémentée dans OLE. Les clients ne s'inscrivent pas pour des types d'événements spécifiques, car ils le font pour la plupart des objets MAPI. Il est supposé que l'enregistrement de la notification leur permet de recevoir tous les types d'événements pouvant être générés par la source de notification particulière. Étant donné que **IMAPIAdviseSink:: OnNotify** doit être écrit de manière à gérer tous les événements inscrits, son implémentation peut être complexe pour les clients qui s'inscrivent pour un grand nombre d'événements. Étant donné que les méthodes dans les objets de récepteur de formulaire conseillent un seul événement, l'implémentation de ces méthodes est plus simple. 
  

