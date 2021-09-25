---
title: Gestion des notifications
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 451b71da-a888-4d8f-9814-12f9f846de05
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1d87b4bc2ee33d4a9590f94af868a2d98ba7c7ac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576204"
---
# <a name="handling-notifications"></a>Gestion des notifications

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les notifications permettent à un objet d’informer un autre objet qu’il a subi une modification. Le type de modification est appelé « événement ». MAPI définit plusieurs événements pour lesquels des notifications sont générées. 
  
Les clients s’inscrivent généralement pour un ou plusieurs événements avec un ou plusieurs objets. Ces objets sont appelés sources de conseil. Les objets qui peuvent agir en tant que sources de conseil incluent l’objet de session, sous le contrôle de MAPI, ou un objet créé par un fournisseur de services, tel qu’un message. L’objet informé, appelé sink de conseil, contient soit une implémentation de l’interface [IMAPIAdviseSink : IUnknown,](imapiadvisesinkiunknown.md) soit l’interface [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) et se trouve dans une application cliente. 
  
Les objets source advise implémentent une méthode **Advise,** qui est appelée par les clients pour s’inscrire aux notifications, et une méthode **Unadvise,** qui est appelée pour annuler une inscription. L’un des paramètres de **Advise** est un pointeur vers une implémentation de **IMAPIAdviseSink** ou ** IMAPIViewAdviseSink **. La source de conseil met en cache ce pointeur afin qu’il puisse appeler [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) ou l’une des méthodes dans **IMAPIViewAdviseSink** lorsqu’une modification se produit. 
  
Étant donné que la réception de notifications permet aux utilisateurs d’afficher les informations les plus à jour, il est recommandé que tous les clients s’inscrivent et gèrent les notifications. Toutefois, il est facultatif.
  
## <a name="in-this-section"></a>Dans cette section

- [Inscription à une notification](registering-for-a-notification.md): décrit comment inscrire un client pour les notifications dans le cadre de son processus d’initialisation.
    
- [Annulation d’une notification](canceling-a-notification.md): décrit comment annuler un abonnement à une notification.
    
- [Gestion des notifications de la boutique](handling-message-store-notification.md)de messages : décrit comment s’inscrire aux notifications de la boutique de messages.
    
- [Notification de carnet d’adresses](handing-address-book-notification.md)de remise : décrit comment s’inscrire et gérer les notifications de carnet d’adresses.
    
- [Gestion des notifications de table](handling-table-notification.md): décrit comment s’inscrire aux notifications à partir de la table de hiérarchie.
    
- [Mise en œuvre d’un objet de sink de conseil](implementing-an-advise-sink-object.md): décrit comment implémenter un objet de sink de conseil.
    
- [Minutage d’une notification](timing-a-notification.md): décrit le minutage de la notification du client par les fournisseurs de services.
    
- [Garantie d’une notification Thread-Safe :](ensuring-a-thread-safe-notification.md)décrit comment garantir une notification thread-safe avec MAPI.
    
- [Forçage d’une notification](forcing-a-notification.md): décrit comment forcer une notification dans MAPI.
    

