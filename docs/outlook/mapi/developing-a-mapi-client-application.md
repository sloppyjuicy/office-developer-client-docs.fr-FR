---
title: Développement d'une application cliente MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bcb59b08-e6d7-4739-8cb5-e545bd0d478f
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 7f66d2e4d46519dd186a676a0d0fbb836322893b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316687"
---
# <a name="developing-a-mapi-client-application"></a><span data-ttu-id="ae976-103">Développement d'une application cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="ae976-103">Developing a MAPI Client Application</span></span>

  
  
<span data-ttu-id="ae976-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae976-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae976-105">Les applications clientes MAPI sont écrites avec l'interface client MAPI orientée objet.</span><span class="sxs-lookup"><span data-stu-id="ae976-105">MAPI client applications are written with the object oriented MAPI client interface.</span></span> <span data-ttu-id="ae976-106">Les clients MAPI interagissent avec un ou plusieurs systèmes de messagerie via le sous-système MAPI et les fournisseurs de services compatibles MAPI.</span><span class="sxs-lookup"><span data-stu-id="ae976-106">MAPI clients interact with one or more messaging systems through the MAPI subsystem and MAPI-compliant service providers.</span></span> <span data-ttu-id="ae976-107">Cette interaction peut se produire de plusieurs façons différentes; Il existe une variété énorme dans les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="ae976-107">This interaction can occur in many different ways; there is an enormous variety in client applications.</span></span> <span data-ttu-id="ae976-108">La plupart des clients sont des clients de messagerie, soit l'intégration de la messagerie dans l'ensemble des fonctionnalités établies, soit l'exécution de la messagerie comme fonctionnalité principale.</span><span class="sxs-lookup"><span data-stu-id="ae976-108">Most clients are messaging clients, either integrating messaging into their established feature set or performing messaging as their primary feature.</span></span> <span data-ttu-id="ae976-109">Les autres fonctionnalités que les clients MAPI peuvent fournir incluent l'administration des profils, la gestion des carnets d'adresses et de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="ae976-109">Other features that MAPI clients might provide include profile administration or address book and message store management.</span></span>
  
<span data-ttu-id="ae976-110">Tous les clients de messagerie initialisent les bibliothèques MAPI et démarrent une **session** avec le sous-système MAPI.</span><span class="sxs-lookup"><span data-stu-id="ae976-110">All messaging clients initialize the MAPI libraries and start a **session** with the MAPI subsystem.</span></span> <span data-ttu-id="ae976-111">Pour plus d'informations, consultez [la rubrique accès aux objets à l'aide de la session](accessing-objects-by-using-the-session.md).</span><span class="sxs-lookup"><span data-stu-id="ae976-111">For more information, see [Accessing Objects by Using the Session](accessing-objects-by-using-the-session.md).</span></span> <span data-ttu-id="ae976-112">Une fois qu'une session a été établie, un client peut:</span><span class="sxs-lookup"><span data-stu-id="ae976-112">After a session has been established, a client can:</span></span>
  
- <span data-ttu-id="ae976-113">Gérer les messages sortants, y compris les réponses, les messages transférés et les retransmissions.</span><span class="sxs-lookup"><span data-stu-id="ae976-113">Handle outgoing messages, including replies, forwarded messages, and retransmissions.</span></span>
    
- <span data-ttu-id="ae976-114">Gérer les messages entrants.</span><span class="sxs-lookup"><span data-stu-id="ae976-114">Handle incoming messages.</span></span>
    
- <span data-ttu-id="ae976-115">Gérez la Banque de messages en ouvrant des dossiers et des messages, en créant, modifiant, copiant et envoyant des messages, en suivi des conversations et en recherchant dans un ou plusieurs dossiers.</span><span class="sxs-lookup"><span data-stu-id="ae976-115">Handle the message store by opening folders and messages, creating, modifying, copying, and sending messages, tracking conversations, and searching one or more folders.</span></span>
    
- <span data-ttu-id="ae976-116">Gérez le carnet d'adresses en créant et en modifiant des destinataires, en localisant des entrées et en parcourant la hiérarchie de conteneurs.</span><span class="sxs-lookup"><span data-stu-id="ae976-116">Handle the address book by creating and modifying recipients, locating entries, and traversing the container hierarchy.</span></span>
    
- <span data-ttu-id="ae976-117">Gérez un fournisseur de transport en effectuant une reconfiguration, en définissant les options et l'ordre de transport, et en envoyant des messages à la demande.</span><span class="sxs-lookup"><span data-stu-id="ae976-117">Handle a transport provider by performing reconfiguration, setting options and transport order, and sending messages on demand.</span></span>
    
- <span data-ttu-id="ae976-118">Gérer la notification d'événement.</span><span class="sxs-lookup"><span data-stu-id="ae976-118">Handle event notification.</span></span>
    
- <span data-ttu-id="ae976-119">Gérer les formulaires.</span><span class="sxs-lookup"><span data-stu-id="ae976-119">Handle forms.</span></span>
    
- <span data-ttu-id="ae976-120">Gérer les profils et les services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="ae976-120">Handle profiles and message services.</span></span>
    
<span data-ttu-id="ae976-121">Utilisez les rubriques de cette section pour vous aider à implémenter ces tâches de base et les fonctionnalités spécifiques qui feront de votre client MAPI un usage unique.</span><span class="sxs-lookup"><span data-stu-id="ae976-121">Use the topics in this section to help you implement these basic tasks and the specific features that will make your MAPI client unique.</span></span>
  

