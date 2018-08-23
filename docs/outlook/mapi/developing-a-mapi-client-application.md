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
ms.openlocfilehash: bffcfdd6d688c483655b97d61075b147430e3fcc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564975"
---
# <a name="developing-a-mapi-client-application"></a><span data-ttu-id="75405-103">Développement d’une application cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="75405-103">Developing a MAPI Client Application</span></span>

  
  
<span data-ttu-id="75405-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75405-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75405-105">Les applications clientes MAPI sont écrites avec l’interface de client orientée objet MAPI.</span><span class="sxs-lookup"><span data-stu-id="75405-105">MAPI client applications are written with the object oriented MAPI client interface.</span></span> <span data-ttu-id="75405-106">Clients MAPI interagissent avec un ou plusieurs systèmes de messagerie via le sous-système MAPI et les fournisseurs de services compatible MAPI.</span><span class="sxs-lookup"><span data-stu-id="75405-106">MAPI clients interact with one or more messaging systems through the MAPI subsystem and MAPI-compliant service providers.</span></span> <span data-ttu-id="75405-107">Cette interaction peut se produire de différentes façons ; Il existe une grande diversité de dans les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="75405-107">This interaction can occur in many different ways; there is an enormous variety in client applications.</span></span> <span data-ttu-id="75405-108">La plupart des clients sont des clients, l’intégration de messagerie dans leur ensemble de fonctionnalités établies ou l’exécution de messagerie en tant que leur fonctionnalité principale de messagerie.</span><span class="sxs-lookup"><span data-stu-id="75405-108">Most clients are messaging clients, either integrating messaging into their established feature set or performing messaging as their primary feature.</span></span> <span data-ttu-id="75405-109">Administration des profils sont les autres fonctionnalités qui peuvent fournir des clients MAPI ou stockent la gestion des messages et le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="75405-109">Other features that MAPI clients might provide include profile administration or address book and message store management.</span></span>
  
<span data-ttu-id="75405-110">Tous les clients de messagerie initialiser les bibliothèques MAPI et démarrer une **session** avec le sous-système MAPI.</span><span class="sxs-lookup"><span data-stu-id="75405-110">All messaging clients initialize the MAPI libraries and start a **session** with the MAPI subsystem.</span></span> <span data-ttu-id="75405-111">Pour plus d’informations, consultez [Accès à des objets à l’aide de la Session](accessing-objects-by-using-the-session.md).</span><span class="sxs-lookup"><span data-stu-id="75405-111">For more information, see [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md).</span></span> <span data-ttu-id="75405-112">Après l’établissement d’une session, un client peut :</span><span class="sxs-lookup"><span data-stu-id="75405-112">After a session has been established, a client can:</span></span>
  
- <span data-ttu-id="75405-113">Gérer les messages sortants, y compris les réponses, transférée des messages et retransmissions.</span><span class="sxs-lookup"><span data-stu-id="75405-113">Handle outgoing messages, including replies, forwarded messages, and retransmissions.</span></span>
    
- <span data-ttu-id="75405-114">Gérer les messages entrants.</span><span class="sxs-lookup"><span data-stu-id="75405-114">Handle incoming messages.</span></span>
    
- <span data-ttu-id="75405-115">Gérer la banque de messages par l’ouverture des dossiers et messages, création, modification, copie, envoyer des messages, le suivi des conversations et un ou plusieurs dossiers de recherche.</span><span class="sxs-lookup"><span data-stu-id="75405-115">Handle the message store by opening folders and messages, creating, modifying, copying, and sending messages, tracking conversations, and searching one or more folders.</span></span>
    
- <span data-ttu-id="75405-116">Gérer le carnet d’adresses en création et modification des destinataires, localiser les entrées et parcourir la hiérarchie des conteneurs.</span><span class="sxs-lookup"><span data-stu-id="75405-116">Handle the address book by creating and modifying recipients, locating entries, and traversing the container hierarchy.</span></span>
    
- <span data-ttu-id="75405-117">Gérer un fournisseur de transport en effectuant la reconfiguration, définition de l’ordre des options et de transport et envoyer des messages à la demande.</span><span class="sxs-lookup"><span data-stu-id="75405-117">Handle a transport provider by performing reconfiguration, setting options and transport order, and sending messages on demand.</span></span>
    
- <span data-ttu-id="75405-118">Gérer les notifications d’événement.</span><span class="sxs-lookup"><span data-stu-id="75405-118">Handle event notification.</span></span>
    
- <span data-ttu-id="75405-119">Gérer les formulaires.</span><span class="sxs-lookup"><span data-stu-id="75405-119">Handle forms.</span></span>
    
- <span data-ttu-id="75405-120">Gérer les profils et les services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="75405-120">Handle profiles and message services.</span></span>
    
<span data-ttu-id="75405-121">Utilisez les rubriques de cette section pour vous aider à implémenter ces tâches de base et les fonctionnalités spécifiques qui permette de rendre votre client MAPI unique.</span><span class="sxs-lookup"><span data-stu-id="75405-121">Use the topics in this section to help you implement these basic tasks and the specific features that will make your MAPI client unique.</span></span>
  

