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
# <a name="handling-notifications"></a><span data-ttu-id="de37e-103">Gérer les notifications</span><span class="sxs-lookup"><span data-stu-id="de37e-103">Handling notifications</span></span>

<span data-ttu-id="de37e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de37e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de37e-105">Notifications d’activer un seul objet informer un autre objet qu’il a subi une modification.</span><span class="sxs-lookup"><span data-stu-id="de37e-105">Notifications enable one object to inform another object that it has undergone a change.</span></span> <span data-ttu-id="de37e-106">Le type de modification correspond à un événement.</span><span class="sxs-lookup"><span data-stu-id="de37e-106">The type of change is referred to as an event.</span></span> <span data-ttu-id="de37e-107">MAPI définit plusieurs événements pour lequel les notifications sont générées.</span><span class="sxs-lookup"><span data-stu-id="de37e-107">MAPI defines several events for which notifications are generated.</span></span> 
  
<span data-ttu-id="de37e-108">Généralement, les clients enregistrent pour un ou plusieurs des événements avec un ou plusieurs objets.</span><span class="sxs-lookup"><span data-stu-id="de37e-108">Clients typically register for one or more events with one or more objects.</span></span> <span data-ttu-id="de37e-109">Ces objets sont appelés des sources de notification.</span><span class="sxs-lookup"><span data-stu-id="de37e-109">These objects are referred to as advise sources.</span></span> <span data-ttu-id="de37e-110">Les objets qui peuvent être utilisés comme sources de notification comprennent l’objet de session, sous contrôle de MAPI, ou un objet créé par un fournisseur de services, comme un message.</span><span class="sxs-lookup"><span data-stu-id="de37e-110">Objects that can act as advise sources include the session object, under MAPI's control, or an object created by a service provider, such as a message.</span></span> <span data-ttu-id="de37e-111">L’objet informé, appelé le récepteur de notifications contient une mise en œuvre de la [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface ou la [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) de l’interface et se trouve dans une application cliente.</span><span class="sxs-lookup"><span data-stu-id="de37e-111">The informed object, referred to as the advise sink, contains either an implementation of the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface or the [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) interface and is within a client application.</span></span> 
  
<span data-ttu-id="de37e-112">Les objets source Advise implémentent une méthode **Advise** , qui est appelée par les clients pour s’inscrire pour les notifications et une méthode **Unadvise** , qui est appelée pour annuler l’inscription d’une.</span><span class="sxs-lookup"><span data-stu-id="de37e-112">Advise source objects implement an **Advise** method, which is called by clients to register for notifications, and an **Unadvise** method, which is called to cancel a registration.</span></span> <span data-ttu-id="de37e-113">L’un des paramètres à **Advise** est un pointeur vers une implémentation de **IMAPIAdviseSink** ou ** IMAPIViewAdviseSink **.</span><span class="sxs-lookup"><span data-stu-id="de37e-113">One of the parameters to **Advise** is a pointer to an implementation of **IMAPIAdviseSink** or ** IMAPIViewAdviseSink **.</span></span> <span data-ttu-id="de37e-114">La source advise met en cache ce pointeur afin qu’il peut appeler [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) ou une des méthodes dans **IMAPIViewAdviseSink** lorsqu’une modification se produit.</span><span class="sxs-lookup"><span data-stu-id="de37e-114">The advise source caches this pointer so that it can call [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) or one of the methods in **IMAPIViewAdviseSink** when a change occurs.</span></span> 
  
<span data-ttu-id="de37e-115">Recevoir des notifications permet aux utilisateurs d’afficher les informations les plus récentes, il est recommandé que tous les clients s’inscrire pour et gérer les notifications.</span><span class="sxs-lookup"><span data-stu-id="de37e-115">Because receiving notifications enables users to view the most up-to-date information, it is recommended that all clients register for and handle notifications.</span></span> <span data-ttu-id="de37e-116">Toutefois, il est facultatif.</span><span class="sxs-lookup"><span data-stu-id="de37e-116">However, it is optional.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="de37e-117">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="de37e-117">In this section</span></span>

- <span data-ttu-id="de37e-118">[Inscription pour une Notification](registering-for-a-notification.md): explique comment inscrire un client pour les notifications dans le cadre du processus d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="de37e-118">[Registering for a Notification](registering-for-a-notification.md): Describes how to register a client for notifications as a part of its initialization process.</span></span>
    
- <span data-ttu-id="de37e-119">[Annulation d’une Notification](canceling-a-notification.md): explique comment annuler un abonnement à une notification.</span><span class="sxs-lookup"><span data-stu-id="de37e-119">[Canceling a Notification](canceling-a-notification.md): Describes how to cancel a subscription to a notification.</span></span>
    
- <span data-ttu-id="de37e-120">[Gestion des notifications de stocker Message](handling-message-store-notification.md): décrit comment s’inscrire pour les notifications de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="de37e-120">[Handling Message Store Notification](handling-message-store-notification.md): Describes how to register for message store notifications.</span></span>
    
- <span data-ttu-id="de37e-121">[Remise de Notification de carnet d’adresses](handing-address-book-notification.md): explique comment inscrire et gérer les notifications de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="de37e-121">[Handing Address Book Notification](handing-address-book-notification.md): Describes how to register for and handle address book notifications.</span></span>
    
- <span data-ttu-id="de37e-122">[Gestion de la Notification de Table](handling-table-notification.md): décrit comment s’inscrire pour les notifications de la table de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="de37e-122">[Handling Table Notification](handling-table-notification.md): Describes how to register for notifications from the hierarchy table.</span></span>
    
- <span data-ttu-id="de37e-123">[L’implémentation d’un objet récepteur de notification](implementing-an-advise-sink-object.md): explique comment implémenter un objet de réception de notifications.</span><span class="sxs-lookup"><span data-stu-id="de37e-123">[Implementing an Advise Sink Object](implementing-an-advise-sink-object.md): Describes how to implement an advise sink object.</span></span>
    
- <span data-ttu-id="de37e-124">[Une Notification de minutage](timing-a-notification.md): décrit la planification de notification du client par les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="de37e-124">[Timing a Notification](timing-a-notification.md): Describes the timing of client notification by service providers.</span></span>
    
- <span data-ttu-id="de37e-125">[Assurer une Notification de Thread-Safe](ensuring-a-thread-safe-notification.md): décrit comment s’assurer de notification de thread-safe MAPI.</span><span class="sxs-lookup"><span data-stu-id="de37e-125">[Ensuring a Thread-Safe Notification](ensuring-a-thread-safe-notification.md): Describes how to ensure thread-safe notification with MAPI.</span></span>
    
- <span data-ttu-id="de37e-126">[Forcer une Notification](forcing-a-notification.md): décrit comment forcer une notification MAPI.</span><span class="sxs-lookup"><span data-stu-id="de37e-126">[Forcing a Notification](forcing-a-notification.md): Describes how to force a notification in MAPI.</span></span>
    

