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
# <a name="handling-notifications"></a><span data-ttu-id="4f73f-103">Gestion des notifications</span><span class="sxs-lookup"><span data-stu-id="4f73f-103">Handling notifications</span></span>

<span data-ttu-id="4f73f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f73f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f73f-105">Les notifications permettent à un objet d'informer un autre objet qu'il a subi une modification.</span><span class="sxs-lookup"><span data-stu-id="4f73f-105">Notifications enable one object to inform another object that it has undergone a change.</span></span> <span data-ttu-id="4f73f-106">Le type de modification est appelé un événement.</span><span class="sxs-lookup"><span data-stu-id="4f73f-106">The type of change is referred to as an event.</span></span> <span data-ttu-id="4f73f-107">MAPI définit plusieurs événements pour lesquels des notifications sont générées.</span><span class="sxs-lookup"><span data-stu-id="4f73f-107">MAPI defines several events for which notifications are generated.</span></span> 
  
<span data-ttu-id="4f73f-108">Les clients s'inscrivent généralement pour un ou plusieurs événements avec un ou plusieurs objets.</span><span class="sxs-lookup"><span data-stu-id="4f73f-108">Clients typically register for one or more events with one or more objects.</span></span> <span data-ttu-id="4f73f-109">Ces objets sont appelés sources de notification.</span><span class="sxs-lookup"><span data-stu-id="4f73f-109">These objects are referred to as advise sources.</span></span> <span data-ttu-id="4f73f-110">Les objets pouvant agir en tant que sources de notification incluent l'objet session, sous le contrôle de l'interface MAPI, ou un objet créé par un fournisseur de services, tel qu'un message.</span><span class="sxs-lookup"><span data-stu-id="4f73f-110">Objects that can act as advise sources include the session object, under MAPI's control, or an object created by a service provider, such as a message.</span></span> <span data-ttu-id="4f73f-111">L'objet éclairé, appelé récepteur de notifications, contient une implémentation de l'interface [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) ou de l'interface [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) et se trouve dans une application cliente.</span><span class="sxs-lookup"><span data-stu-id="4f73f-111">The informed object, referred to as the advise sink, contains either an implementation of the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface or the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and is within a client application.</span></span> 
  
<span data-ttu-id="4f73f-112">Les objets source d'avis \*\*\*\* implémentent une méthode Advise, qui est appelée par les clients pour s'inscrire aux notifications, et une méthode Unadvise qui est appelée pour annuler une inscription. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4f73f-112">Advise source objects implement an **Advise** method, which is called by clients to register for notifications, and an **Unadvise** method, which is called to cancel a registration.</span></span> <span data-ttu-id="4f73f-113">L'un des paramètres à **conseiller** est un pointeur vers une implémentation de **IMAPIAdviseSink** ou de \* \* IMAPIViewAdviseSink \* \*.</span><span class="sxs-lookup"><span data-stu-id="4f73f-113">One of the parameters to **Advise** is a pointer to an implementation of **IMAPIAdviseSink** or \*\* IMAPIViewAdviseSink \*\*.</span></span> <span data-ttu-id="4f73f-114">La source de notification met en cache ce pointeur afin qu'il puisse appeler [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) ou l'une des méthodes dans **IMAPIViewAdviseSink** lorsqu'une modification se produit.</span><span class="sxs-lookup"><span data-stu-id="4f73f-114">The advise source caches this pointer so that it can call [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) or one of the methods in **IMAPIViewAdviseSink** when a change occurs.</span></span> 
  
<span data-ttu-id="4f73f-115">Étant donné que la réception des notifications permet aux utilisateurs de visualiser les informations les plus à jour, il est recommandé que tous les clients s'inscrivent et gèrent les notifications.</span><span class="sxs-lookup"><span data-stu-id="4f73f-115">Because receiving notifications enables users to view the most up-to-date information, it is recommended that all clients register for and handle notifications.</span></span> <span data-ttu-id="4f73f-116">Toutefois, il est facultatif.</span><span class="sxs-lookup"><span data-stu-id="4f73f-116">However, it is optional.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="4f73f-117">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="4f73f-117">In this section</span></span>

- <span data-ttu-id="4f73f-118">[Inscription pour une notification](registering-for-a-notification.md): décrit comment enregistrer un client pour les notifications dans le cadre de son processus d'initialisation.</span><span class="sxs-lookup"><span data-stu-id="4f73f-118">[Registering for a Notification](registering-for-a-notification.md): Describes how to register a client for notifications as a part of its initialization process.</span></span>
    
- <span data-ttu-id="4f73f-119">[Annulation d'une notification](canceling-a-notification.md): explique comment annuler un abonnement à une notification.</span><span class="sxs-lookup"><span data-stu-id="4f73f-119">[Canceling a Notification](canceling-a-notification.md): Describes how to cancel a subscription to a notification.</span></span>
    
- <span data-ttu-id="4f73f-120">[Gestion](handling-message-store-notification.md)des notifications de banque de messages: décrit comment s'inscrire pour les notifications de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="4f73f-120">[Handling Message Store Notification](handling-message-store-notification.md): Describes how to register for message store notifications.</span></span>
    
- <span data-ttu-id="4f73f-121">Gestion des notifications de [carnet](handing-address-book-notification.md)d'adresses: décrit comment inscrire et gérer les notifications de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="4f73f-121">[Handing Address Book Notification](handing-address-book-notification.md): Describes how to register for and handle address book notifications.</span></span>
    
- <span data-ttu-id="4f73f-122">[Gestion des notifications de table](handling-table-notification.md): décrit comment s'inscrire aux notifications à partir de la table de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="4f73f-122">[Handling Table Notification](handling-table-notification.md): Describes how to register for notifications from the hierarchy table.</span></span>
    
- <span data-ttu-id="4f73f-123">[Implémentation d'un objet de récepteur](implementing-an-advise-sink-object.md)de notifications: décrit comment implémenter un objet récepteur de notifications.</span><span class="sxs-lookup"><span data-stu-id="4f73f-123">[Implementing an Advise Sink Object](implementing-an-advise-sink-object.md): Describes how to implement an advise sink object.</span></span>
    
- <span data-ttu-id="4f73f-124">[Chronométrage d'une notification](timing-a-notification.md): décrit le calendrier des notifications client par les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="4f73f-124">[Timing a Notification](timing-a-notification.md): Describes the timing of client notification by service providers.</span></span>
    
- <span data-ttu-id="4f73f-125">[Vérification de la notification de thread-safe](ensuring-a-thread-safe-notification.md): décrit comment garantir la notification thread-safe avec MAPI.</span><span class="sxs-lookup"><span data-stu-id="4f73f-125">[Ensuring a Thread-Safe Notification](ensuring-a-thread-safe-notification.md): Describes how to ensure thread-safe notification with MAPI.</span></span>
    
- <span data-ttu-id="4f73f-126">[Forcer une notification](forcing-a-notification.md): explique comment forcer une notification dans MAPI.</span><span class="sxs-lookup"><span data-stu-id="4f73f-126">[Forcing a Notification](forcing-a-notification.md): Describes how to force a notification in MAPI.</span></span>
    

