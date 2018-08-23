---
title: Gérer les notifications
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 451b71da-a888-4d8f-9814-12f9f846de05
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4c19e88ac1cfb29a9841ec78516410e23b3e5403
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567579"
---
# <a name="handling-notifications"></a>Gérer les notifications

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Notifications d’activer un seul objet informer un autre objet qu’il a subi une modification. Le type de modification correspond à un événement. MAPI définit plusieurs événements pour lequel les notifications sont générées. 
  
Généralement, les clients enregistrent pour un ou plusieurs des événements avec un ou plusieurs objets. Ces objets sont appelés des sources de notification. Les objets qui peuvent être utilisés comme sources de notification comprennent l’objet de session, sous contrôle de MAPI, ou un objet créé par un fournisseur de services, comme un message. L’objet informé, appelé le récepteur de notifications contient une mise en œuvre de la [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface ou la [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) de l’interface et se trouve dans une application cliente. 
  
Les objets source Advise implémentent une méthode **Advise** , qui est appelée par les clients pour s’inscrire pour les notifications et une méthode **Unadvise** , qui est appelée pour annuler l’inscription d’une. L’un des paramètres à **Advise** est un pointeur vers une implémentation de **IMAPIAdviseSink** ou ** IMAPIViewAdviseSink **. La source advise met en cache ce pointeur afin qu’il peut appeler [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) ou une des méthodes dans **IMAPIViewAdviseSink** lorsqu’une modification se produit. 
  
Recevoir des notifications permet aux utilisateurs d’afficher les informations les plus récentes, il est recommandé que tous les clients s’inscrire pour et gérer les notifications. Toutefois, il est facultatif.
  
## <a name="in-this-section"></a>Dans cette section

- [Inscription pour une Notification](registering-for-a-notification.md): explique comment inscrire un client pour les notifications dans le cadre du processus d’initialisation.
    
- [Annulation d’une Notification](canceling-a-notification.md): explique comment annuler un abonnement à une notification.
    
- [Gestion des notifications de stocker Message](handling-message-store-notification.md): décrit comment s’inscrire pour les notifications de banque de messages.
    
- [Remise de Notification de carnet d’adresses](handing-address-book-notification.md): explique comment inscrire et gérer les notifications de carnet d’adresses.
    
- [Gestion de la Notification de Table](handling-table-notification.md): décrit comment s’inscrire pour les notifications de la table de hiérarchie.
    
- [L’implémentation d’un objet récepteur de notification](implementing-an-advise-sink-object.md): explique comment implémenter un objet de réception de notifications.
    
- [Une Notification de minutage](timing-a-notification.md): décrit la planification de notification du client par les fournisseurs de services.
    
- [Assurer une Notification de Thread-Safe](ensuring-a-thread-safe-notification.md): décrit comment s’assurer de notification de thread-safe MAPI.
    
- [Forcer une Notification](forcing-a-notification.md): décrit comment forcer une notification MAPI.
    

