---
title: Développement d’une application cliente MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 7f66d2e4d46519dd186a676a0d0fbb836322893b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410034"
---
# <a name="developing-a-mapi-client-application"></a><span data-ttu-id="e5ba5-103">Développement d’une application cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="e5ba5-103">Developing a MAPI Client Application</span></span>

  
  
<span data-ttu-id="e5ba5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5ba5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5ba5-105">Les applications clientes MAPI sont écrites avec l’interface cliente MAPI orientée objet.</span><span class="sxs-lookup"><span data-stu-id="e5ba5-105">MAPI client applications are written with the object oriented MAPI client interface.</span></span> <span data-ttu-id="e5ba5-106">Les clients MAPI interagissent avec un ou plusieurs systèmes de messagerie via le sous-système MAPI et les fournisseurs de services conformes MAPI.</span><span class="sxs-lookup"><span data-stu-id="e5ba5-106">MAPI clients interact with one or more messaging systems through the MAPI subsystem and MAPI-compliant service providers.</span></span> <span data-ttu-id="e5ba5-107">Cette interaction peut se produire de nombreuses manières différentes . il existe une grande variété dans les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="e5ba5-107">This interaction can occur in many different ways; there is an enormous variety in client applications.</span></span> <span data-ttu-id="e5ba5-108">La plupart des clients sont des clients de messagerie, soit en intégrant la messagerie dans leur ensemble de fonctionnalités établi, soit en les intégrant comme fonctionnalité principale.</span><span class="sxs-lookup"><span data-stu-id="e5ba5-108">Most clients are messaging clients, either integrating messaging into their established feature set or performing messaging as their primary feature.</span></span> <span data-ttu-id="e5ba5-109">Les clients MAPI peuvent également fournir d’autres fonctionnalités, notamment l’administration des profils, le carnet d’adresses et la gestion des magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="e5ba5-109">Other features that MAPI clients might provide include profile administration or address book and message store management.</span></span>
  
<span data-ttu-id="e5ba5-110">Tous les clients de messagerie initialisent les bibliothèques MAPI et démarrent une **session** avec le sous-système MAPI.</span><span class="sxs-lookup"><span data-stu-id="e5ba5-110">All messaging clients initialize the MAPI libraries and start a **session** with the MAPI subsystem.</span></span> <span data-ttu-id="e5ba5-111">Pour plus d’informations, [voir Accès aux objets à l’aide de la session.](accessing-objects-by-using-the-session.md)</span><span class="sxs-lookup"><span data-stu-id="e5ba5-111">For more information, see [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md).</span></span> <span data-ttu-id="e5ba5-112">Une fois qu’une session a été établie, un client peut :</span><span class="sxs-lookup"><span data-stu-id="e5ba5-112">After a session has been established, a client can:</span></span>
  
- <span data-ttu-id="e5ba5-113">Gérer les messages sortants, y compris les réponses, les messages transmis et les retransmissions.</span><span class="sxs-lookup"><span data-stu-id="e5ba5-113">Handle outgoing messages, including replies, forwarded messages, and retransmissions.</span></span>
    
- <span data-ttu-id="e5ba5-114">Gérer les messages entrants.</span><span class="sxs-lookup"><span data-stu-id="e5ba5-114">Handle incoming messages.</span></span>
    
- <span data-ttu-id="e5ba5-115">Gérer la magasin de messages en ouvrant des dossiers et des messages, en créant, modifiant, copiant et envoyant des messages, en suivant les conversations et en recherchant un ou plusieurs dossiers.</span><span class="sxs-lookup"><span data-stu-id="e5ba5-115">Handle the message store by opening folders and messages, creating, modifying, copying, and sending messages, tracking conversations, and searching one or more folders.</span></span>
    
- <span data-ttu-id="e5ba5-116">Gérer le carnet d’adresses en créant et en modifiant des destinataires, en localisant des entrées et en parcourant la hiérarchie des conteneurs.</span><span class="sxs-lookup"><span data-stu-id="e5ba5-116">Handle the address book by creating and modifying recipients, locating entries, and traversing the container hierarchy.</span></span>
    
- <span data-ttu-id="e5ba5-117">Gérer un fournisseur de transport en effectuer la reconfiguration, définir des options et un ordre de transport et envoyer des messages à la demande.</span><span class="sxs-lookup"><span data-stu-id="e5ba5-117">Handle a transport provider by performing reconfiguration, setting options and transport order, and sending messages on demand.</span></span>
    
- <span data-ttu-id="e5ba5-118">Gérer les notifications d’événement.</span><span class="sxs-lookup"><span data-stu-id="e5ba5-118">Handle event notification.</span></span>
    
- <span data-ttu-id="e5ba5-119">Gérer les formulaires.</span><span class="sxs-lookup"><span data-stu-id="e5ba5-119">Handle forms.</span></span>
    
- <span data-ttu-id="e5ba5-120">Gérer les profils et les services de message.</span><span class="sxs-lookup"><span data-stu-id="e5ba5-120">Handle profiles and message services.</span></span>
    
<span data-ttu-id="e5ba5-121">Utilisez les rubriques de cette section pour vous aider à implémenter ces tâches de base et les fonctionnalités spécifiques qui rendent votre client MAPI unique.</span><span class="sxs-lookup"><span data-stu-id="e5ba5-121">Use the topics in this section to help you implement these basic tasks and the specific features that will make your MAPI client unique.</span></span>
  

