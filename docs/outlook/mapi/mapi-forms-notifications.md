---
title: Notifications de formulaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 97ff2733-a2b1-4da0-b628-00850fc7925b
ms.openlocfilehash: 4a2875e62c197f38c219b51b88212f11c78489c8
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369097"
---
# <a name="mapi-forms-notifications"></a>Notifications de formulaires MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’inscription et la gestion des notifications à partir d’objets de formulaire sont un processus différent de celui des autres objets MAPI. Les réceptions de conseil pour les notifications de formulaire implémentent l’interface **IMAPIViewAdviseSink** ou **IMAPIFormAdviseSink** plutôt que **IMAPIAdviseSink**. [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) et [IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) ont chacune plusieurs méthodes, une pour chacun des événements possibles que la source de conseil correspondante est capable de générer. Par exemple, **IMAPIFormAdviseSink** dispose de deux méthodes : [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) pour gérer une modification de l’état de la visionneuse de formulaires et [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md) pour afficher un nouveau message avec le formulaire correct. 
  
La stratégie de gestion des événements pour les formulaires est similaire à la stratégie de gestion des événements implémentée dans OLE. Les clients ne s’inscrivent pas à des types d’événements spécifiques, comme ils le font pour la plupart des objets MAPI. L’hypothèse est que l’inscription aux notifications leur permet de recevoir tout type d’événement qui peut être généré par la source d’avis particulière. Étant **donné que IMAPIAdviseSink::OnNotify** doit être écrit de manière à gérer tous les événements inscrits, son implémentation peut être complexe pour les clients qui s’inscrivent à de nombreux événements différents. Étant donné que les méthodes dans le formulaire conseillent les objets de sink ciblent un événement unique, l’implémentation de ces méthodes est plus simple. 
  

