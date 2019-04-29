---
title: Gestion des notifications
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 451b71da-a888-4d8f-9814-12f9f846de05
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e261b71a8e94d9db3b1b17168d84798dfe18955d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429158"
---
# <a name="handling-notifications"></a>Gestion des notifications

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les notifications permettent à un objet d'informer un autre objet qu'il a subi une modification. Le type de modification est appelé un événement. MAPI définit plusieurs événements pour lesquels des notifications sont générées. 
  
Les clients s'inscrivent généralement pour un ou plusieurs événements avec un ou plusieurs objets. Ces objets sont appelés sources de notification. Les objets pouvant agir en tant que sources de notification incluent l'objet session, sous le contrôle de l'interface MAPI, ou un objet créé par un fournisseur de services, tel qu'un message. L'objet éclairé, appelé récepteur de notifications, contient une implémentation de l'interface [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) ou de l'interface [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) et se trouve dans une application cliente. 
  
Les objets source d'avis **** implémentent une méthode Advise, qui est appelée par les clients pour s'inscrire aux notifications, et une méthode Unadvise qui est appelée pour annuler une inscription. **** L'un des paramètres à **conseiller** est un pointeur vers une implémentation de **IMAPIAdviseSink** ou de * * IMAPIViewAdviseSink * *. La source de notification met en cache ce pointeur afin qu'il puisse appeler [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) ou l'une des méthodes dans **IMAPIViewAdviseSink** lorsqu'une modification se produit. 
  
Étant donné que la réception des notifications permet aux utilisateurs de visualiser les informations les plus à jour, il est recommandé que tous les clients s'inscrivent et gèrent les notifications. Toutefois, il est facultatif.
  
## <a name="in-this-section"></a>Dans cette section

- [Inscription pour une notification](registering-for-a-notification.md): décrit comment enregistrer un client pour les notifications dans le cadre de son processus d'initialisation.
    
- [Annulation d'une notification](canceling-a-notification.md): explique comment annuler un abonnement à une notification.
    
- [Gestion](handling-message-store-notification.md)des notifications de banque de messages: décrit comment s'inscrire pour les notifications de banque de messages.
    
- Gestion des notifications de [carnet](handing-address-book-notification.md)d'adresses: décrit comment inscrire et gérer les notifications de carnet d'adresses.
    
- [Gestion des notifications de table](handling-table-notification.md): décrit comment s'inscrire aux notifications à partir de la table de hiérarchie.
    
- [Implémentation d'un objet de récepteur](implementing-an-advise-sink-object.md)de notifications: décrit comment implémenter un objet récepteur de notifications.
    
- [Chronométrage d'une notification](timing-a-notification.md): décrit le calendrier des notifications client par les fournisseurs de services.
    
- [Vérification de la notification de thread-safe](ensuring-a-thread-safe-notification.md): décrit comment garantir la notification thread-safe avec MAPI.
    
- [Forcer une notification](forcing-a-notification.md): explique comment forcer une notification dans MAPI.
    

