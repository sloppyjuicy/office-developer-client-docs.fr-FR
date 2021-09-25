---
title: Notifications de formulaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 97ff2733-a2b1-4da0-b628-00850fc7925b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b0d5ffeb6aee30966f12e13a82ef7e345a86ab3f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556174"
---
# <a name="mapi-forms-notifications"></a>Notifications de formulaires MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’inscription et la gestion des notifications à partir d’objets de formulaire sont un processus différent de celui des autres objets MAPI. Les réceptions de conseil pour les notifications de formulaire implémentent l’interface **IMAPIViewAdviseSink** ou **IMAPIFormAdviseSink** plutôt que **IMAPIAdviseSink**. [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) et [IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) ont chacune plusieurs méthodes, une pour chacun des événements possibles que la source de conseil correspondante est capable de générer. Par exemple, **IMAPIFormAdviseSink** dispose de deux méthodes : [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) pour gérer une modification de l’état de la visionneuse de formulaires et [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md) pour afficher un nouveau message avec le formulaire correct. 
  
La stratégie de gestion des événements pour les formulaires est similaire à la stratégie de gestion des événements implémentée dans OLE. Les clients ne s’inscrivent pas à des types d’événements spécifiques, comme c’est le cas pour la plupart des objets MAPI. L’hypothèse est que l’inscription à la notification leur permet de recevoir tout type d’événement qui peut être généré par la source de notification particulière. Étant donné que **IMAPIAdviseSink::OnNotify** doit être écrit de manière à gérer tous les événements inscrits, son exécution peut être complexe pour les clients qui s’inscrivent à de nombreux événements différents. Étant donné que les méthodes dans le formulaire conseillent les objets de sink ciblent un événement unique, l’implémentation de ces méthodes est plus simple. 
  

