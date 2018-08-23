---
title: Vue d’ensemble du spouleur MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ec581e2170b92721410106eae00e2d36b3c775a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591337"
---
# <a name="mapi-spooler-overview"></a><span data-ttu-id="693f0-103">Vue d’ensemble du spouleur MAPI</span><span class="sxs-lookup"><span data-stu-id="693f0-103">MAPI spooler overview</span></span>
  
<span data-ttu-id="693f0-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="693f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="693f0-105">Spouleur MAPI est une fonction du processus de Microsoft Office Outlook qui est responsable de l’envoi des messages et réception de messages à partir d’un système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="693f0-105">MAPI spooler is a function of the Microsoft Office Outlook process that is responsible for sending messages to and receiving messages from a messaging system.</span></span> <span data-ttu-id="693f0-106">Spouleur MAPI joue un rôle essentiel dans la remise et de réception du message.</span><span class="sxs-lookup"><span data-stu-id="693f0-106">MAPI spooler plays a vital role in message receipt and delivery.</span></span> <span data-ttu-id="693f0-107">Lorsqu’un système de messagerie n’est pas disponible, spouleur MAPI stocke les messages et les transfère automatiquement à une date ultérieure.</span><span class="sxs-lookup"><span data-stu-id="693f0-107">When a messaging system is unavailable, MAPI spooler stores the messages and automatically forwards them at a later time.</span></span> <span data-ttu-id="693f0-108">Cette capacité d’envoyer des données lorsqu’il est nécessaire de façon permanente sur est appelée stocker et transférer, une fonctionnalité essentielle dans les environnements où les connexions à distance sont courants et le trafic réseau est élevé.</span><span class="sxs-lookup"><span data-stu-id="693f0-108">This ability to hold on to or send data when necessary is known as store and forward, a critical feature in environments where remote connections are common and network traffic is high.</span></span> <span data-ttu-id="693f0-109">Spouleur MAPI s’exécute comme un thread d’arrière-plan dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="693f0-109">MAPI spooler runs as a background thread within Outlook.</span></span>
  
<span data-ttu-id="693f0-110">Spouleur MAPI a des responsabilités supplémentaires liées à la distribution du message.</span><span class="sxs-lookup"><span data-stu-id="693f0-110">MAPI spooler has additional responsibilities related to message distribution.</span></span> <span data-ttu-id="693f0-111">Ces droits supplémentaires sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="693f0-111">These extra duties include the following:</span></span>
  
- <span data-ttu-id="693f0-112">Suivi des types de destinataires qui sont gérés par les fournisseurs de transport spécifique.</span><span class="sxs-lookup"><span data-stu-id="693f0-112">Keeping track of the recipient types that are handled by specific transport providers.</span></span>
    
- <span data-ttu-id="693f0-113">Informe une application cliente lorsqu’un nouveau message a été remis.</span><span class="sxs-lookup"><span data-stu-id="693f0-113">Informing a client application when a new message has been delivered.</span></span>
    
- <span data-ttu-id="693f0-114">Message d’appel de prétraitement et de post-traitement.</span><span class="sxs-lookup"><span data-stu-id="693f0-114">Invoking message preprocessing and postprocessing.</span></span>
    
- <span data-ttu-id="693f0-115">Génération de rapports qui indiquent que la remise des messages s’est produite.</span><span class="sxs-lookup"><span data-stu-id="693f0-115">Generating reports that indicate that message delivery has occurred.</span></span>
    
- <span data-ttu-id="693f0-116">Maintien du statut des destinataires traités.</span><span class="sxs-lookup"><span data-stu-id="693f0-116">Maintaining status on processed recipients.</span></span>
    
<span data-ttu-id="693f0-117">L’illustration suivante montre un haut niveau le flux d’un message à partir d’un client pour le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="693f0-117">The following illustration shows at a high level how a message flows from a client to the messaging system.</span></span>
  
<span data-ttu-id="693f0-118">**Flux de message sortant**</span><span class="sxs-lookup"><span data-stu-id="693f0-118">**Outgoing message flow**</span></span>
  
<span data-ttu-id="693f0-119">![Flux des messages de sortie] (media/amapi_46.gif "Flux des messages de sortie")</span><span class="sxs-lookup"><span data-stu-id="693f0-119">![Outgoing message flow](media/amapi_46.gif "Outgoing message flow")</span></span>
  
<span data-ttu-id="693f0-120">L’utilisateur d’une application cliente envoie un message à un ou plusieurs destinataires.</span><span class="sxs-lookup"><span data-stu-id="693f0-120">The user of a client application sends a message to one or more recipients.</span></span> <span data-ttu-id="693f0-121">La banque de messages fournisseur lance le processus d’envoi, le message de mise en forme avec des informations supplémentaires nécessaires pour la transmission.</span><span class="sxs-lookup"><span data-stu-id="693f0-121">The message store provider initiates the sending process, formatting the message with additional information needed for transmission.</span></span>
  
<span data-ttu-id="693f0-122">Spouleur MAPI reçoit le message à traiter si une des conditions suivantes se produisent :</span><span class="sxs-lookup"><span data-stu-id="693f0-122">MAPI spooler receives the message to process if any of the following conditions occur:</span></span>
  
- <span data-ttu-id="693f0-123">Le fournisseur de banque de messages n’est pas étroitement avec un fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="693f0-123">The message store provider is not tightly coupled with a transport provider.</span></span>
    
- <span data-ttu-id="693f0-124">Le message nécessite un prétraitement.</span><span class="sxs-lookup"><span data-stu-id="693f0-124">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="693f0-125">La banque de messages et de transport fournisseur sont étroitement, mais ils ne peuvent pas gérer tous les destinataires auxquels le message est adressé.</span><span class="sxs-lookup"><span data-stu-id="693f0-125">The message store and transport provider are tightly coupled, but they cannot handle all the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="693f0-126">Si le spouleur MAPI reçoit le message, il effectue tout prétraitement requis et remet le message au fournisseur de transport approprié.</span><span class="sxs-lookup"><span data-stu-id="693f0-126">If MAPI spooler receives the message, it performs any required preprocessing and delivers the message to the appropriate transport provider.</span></span> <span data-ttu-id="693f0-127">Le fournisseur de transport donne le message à son système de messagerie, qui envoie à son destinataire.</span><span class="sxs-lookup"><span data-stu-id="693f0-127">The transport provider gives the message to its messaging system, which sends it to its intended recipient.</span></span>
  
<span data-ttu-id="693f0-128">Avec les messages entrants, le flux est rétablie.</span><span class="sxs-lookup"><span data-stu-id="693f0-128">With incoming messages, the flow is reversed.</span></span> <span data-ttu-id="693f0-129">Le fournisseur de transport reçoit un message à partir de son système de messagerie et avertit spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="693f0-129">The transport provider receives a message from its messaging system and notifies MAPI spooler.</span></span> <span data-ttu-id="693f0-130">Spouleur effectue un post-traitement nécessaire et informe le fournisseur de banque de messages qu’un nouveau message est arrivé.</span><span class="sxs-lookup"><span data-stu-id="693f0-130">Spooler performs any necessary postprocessing and informs the message store provider that a new message has arrived.</span></span> <span data-ttu-id="693f0-131">Cette notification, le client actualiser son affichage du message, l’activation de l’utilisateur de lire le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="693f0-131">This notification causes the client to refresh its message display, enabling the user to read the new message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="693f0-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="693f0-132">See also</span></span>

- [<span data-ttu-id="693f0-133">Architecture et des fonctionnalités MAPI</span><span class="sxs-lookup"><span data-stu-id="693f0-133">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

