---
title: Présentation du spouleur MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 162957ea17b5a82d4da68340e971d328c85cd9f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432715"
---
# <a name="mapi-spooler-overview"></a><span data-ttu-id="d5449-103">Présentation du spouleur MAPI</span><span class="sxs-lookup"><span data-stu-id="d5449-103">MAPI spooler overview</span></span>
  
<span data-ttu-id="d5449-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5449-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5449-105">Lepooler MAPI est une fonction du processus Microsoft Office Outlook qui est responsable de l’envoi et de la réception de messages à partir d’un système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="d5449-105">MAPI spooler is a function of the Microsoft Office Outlook process that is responsible for sending messages to and receiving messages from a messaging system.</span></span> <span data-ttu-id="d5449-106">Lepooler MAPI joue un rôle vital dans la réception et la remise des messages.</span><span class="sxs-lookup"><span data-stu-id="d5449-106">MAPI spooler plays a vital role in message receipt and delivery.</span></span> <span data-ttu-id="d5449-107">Lorsqu’un système de messagerie n’est pas disponible, lepooler MAPI stocke les messages et les a automatiquement transmis ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="d5449-107">When a messaging system is unavailable, MAPI spooler stores the messages and automatically forwards them at a later time.</span></span> <span data-ttu-id="d5449-108">Cette possibilité de conserver ou d’envoyer des données lorsque cela est nécessaire est appelée stocker et transmettre, une fonctionnalité essentielle dans les environnements où les connexions distantes sont courantes et où le trafic réseau est élevé.</span><span class="sxs-lookup"><span data-stu-id="d5449-108">This ability to hold on to or send data when necessary is known as store and forward, a critical feature in environments where remote connections are common and network traffic is high.</span></span> <span data-ttu-id="d5449-109">Lepooler MAPI s’exécute en tant que thread d’arrière-plan dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="d5449-109">MAPI spooler runs as a background thread within Outlook.</span></span>
  
<span data-ttu-id="d5449-110">Lepooler MAPI a des responsabilités supplémentaires liées à la distribution des messages.</span><span class="sxs-lookup"><span data-stu-id="d5449-110">MAPI spooler has additional responsibilities related to message distribution.</span></span> <span data-ttu-id="d5449-111">Ces tâches supplémentaires sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="d5449-111">These extra duties include the following:</span></span>
  
- <span data-ttu-id="d5449-112">Suivi des types de destinataires gérés par des fournisseurs de transport spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d5449-112">Keeping track of the recipient types that are handled by specific transport providers.</span></span>
    
- <span data-ttu-id="d5449-113">Informer une application cliente lorsqu’un nouveau message a été remis.</span><span class="sxs-lookup"><span data-stu-id="d5449-113">Informing a client application when a new message has been delivered.</span></span>
    
- <span data-ttu-id="d5449-114">L’facturation du prétraitment et du post-traitement des messages.</span><span class="sxs-lookup"><span data-stu-id="d5449-114">Invoking message preprocessing and postprocessing.</span></span>
    
- <span data-ttu-id="d5449-115">Génération de rapports qui indiquent que la remise du message s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d5449-115">Generating reports that indicate that message delivery has occurred.</span></span>
    
- <span data-ttu-id="d5449-116">Maintien de l’état sur les destinataires traitées.</span><span class="sxs-lookup"><span data-stu-id="d5449-116">Maintaining status on processed recipients.</span></span>
    
<span data-ttu-id="d5449-117">L’illustration suivante montre à un niveau élevé comment un message circule d’un client vers le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="d5449-117">The following illustration shows at a high level how a message flows from a client to the messaging system.</span></span>
  
<span data-ttu-id="d5449-118">**Flux de message sortant**</span><span class="sxs-lookup"><span data-stu-id="d5449-118">**Outgoing message flow**</span></span>
  
<span data-ttu-id="d5449-119">![Flux de messages sortants](media/amapi_46.gif "Flux de messages sortants")</span><span class="sxs-lookup"><span data-stu-id="d5449-119">![Outgoing message flow](media/amapi_46.gif "Outgoing message flow")</span></span>
  
<span data-ttu-id="d5449-120">L’utilisateur d’une application cliente envoie un message à un ou plusieurs destinataires.</span><span class="sxs-lookup"><span data-stu-id="d5449-120">The user of a client application sends a message to one or more recipients.</span></span> <span data-ttu-id="d5449-121">Le fournisseur de la boutique de messages lance le processus d’envoi, en formatant le message avec des informations supplémentaires nécessaires pour la transmission.</span><span class="sxs-lookup"><span data-stu-id="d5449-121">The message store provider initiates the sending process, formatting the message with additional information needed for transmission.</span></span>
  
<span data-ttu-id="d5449-122">Lepooler MAPI reçoit le message à traiter si l’une des conditions suivantes se produit :</span><span class="sxs-lookup"><span data-stu-id="d5449-122">MAPI spooler receives the message to process if any of the following conditions occur:</span></span>
  
- <span data-ttu-id="d5449-123">Le fournisseur de la boutique de messages n’est pas étroitement associé à un fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="d5449-123">The message store provider is not tightly coupled with a transport provider.</span></span>
    
- <span data-ttu-id="d5449-124">Le message nécessite un prétraitment.</span><span class="sxs-lookup"><span data-stu-id="d5449-124">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="d5449-125">La magasin de messages et le fournisseur de transport sont étroitement associés, mais ils ne peuvent pas gérer tous les destinataires auxquels le message est adressé.</span><span class="sxs-lookup"><span data-stu-id="d5449-125">The message store and transport provider are tightly coupled, but they cannot handle all the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="d5449-126">Si lepooler MAPI reçoit le message, il effectue les prétraitations requises et le remettre au fournisseur de transport approprié.</span><span class="sxs-lookup"><span data-stu-id="d5449-126">If MAPI spooler receives the message, it performs any required preprocessing and delivers the message to the appropriate transport provider.</span></span> <span data-ttu-id="d5449-127">Le fournisseur de transport envoie le message à son système de messagerie, qui l’envoie à son destinataire prévu.</span><span class="sxs-lookup"><span data-stu-id="d5449-127">The transport provider gives the message to its messaging system, which sends it to its intended recipient.</span></span>
  
<span data-ttu-id="d5449-128">Avec les messages entrants, le flux est inversé.</span><span class="sxs-lookup"><span data-stu-id="d5449-128">With incoming messages, the flow is reversed.</span></span> <span data-ttu-id="d5449-129">Le fournisseur de transport reçoit un message de son système de messagerie et avertit lepooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="d5449-129">The transport provider receives a message from its messaging system and notifies MAPI spooler.</span></span> <span data-ttu-id="d5449-130">Spooler effectue tout post-traitement nécessaire et informe le fournisseur de la boutique de messages qu’un nouveau message est arrivé.</span><span class="sxs-lookup"><span data-stu-id="d5449-130">Spooler performs any necessary postprocessing and informs the message store provider that a new message has arrived.</span></span> <span data-ttu-id="d5449-131">Cette notification entraîne l’actualisation de l’affichage du message par le client, ce qui permet à l’utilisateur de lire le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="d5449-131">This notification causes the client to refresh its message display, enabling the user to read the new message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d5449-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5449-132">See also</span></span>

- [<span data-ttu-id="d5449-133">Fonctionnalités et architecture MAPI</span><span class="sxs-lookup"><span data-stu-id="d5449-133">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

