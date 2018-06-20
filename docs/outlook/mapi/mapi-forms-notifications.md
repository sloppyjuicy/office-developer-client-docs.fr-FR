---
title: Notifications des formulaires MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 97ff2733-a2b1-4da0-b628-00850fc7925b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 7064aee2ccd35b6b372bc6f911c7508113c26162
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784626"
---
# <a name="mapi-forms-notifications"></a>Notifications des formulaires MAPI

  
  
**S’applique à**: Outlook 
  
Inscription pour et la gestion des notifications à partir des objets de formulaire sont un processus différent de pour d’autres objets MAPI. Récepteurs de notifications pour implémenter des notifications de formulaire soit **l’IMAPIViewAdviseSink** ou interface **IMAPIFormAdviseSink** plutôt que **IMAPIAdviseSink**. [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) et [IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md) chacun avoir plusieurs méthodes, un pour chacun des événements possibles correspondant de notification source est capable de générer. Par exemple, **IMAPIFormAdviseSink** dispose de deux méthodes : [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) pour gérer une modification apportée à l’état et [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md) pour afficher un nouveau message avec le formulaire correct de l’utilisateur du formulaire. 
  
Stratégie pour les formulaires de gestion d’événements sont similaire à la stratégie implémentée dans OLE de gestion d’événements. Clients n’enregistrent pas pour les types d’événements spécifiques, comme ils le font pour la plupart des objets MAPI. L’hypothèse est qu’inscription pour la notification leur permet de recevoir n’importe quel type d’événement qui peut être générée par la source advise particulier. Étant donné que **IMAPIAdviseSink::OnNotify** doit être écrite pour gérer tous les événements enregistrés, sa mise en œuvre peut être complexe pour les clients qui s’inscrire pour un grand nombre d’événements. Étant donné que les méthodes dans le formulaire cible d’objets de récepteur de notification un seul événement, l’implémentation de ces méthodes est plus simple. 
  

