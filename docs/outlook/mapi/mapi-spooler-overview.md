---
title: Présentation du spouleur MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5866b202-883e-454e-aeb1-61526c43dae9
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 162957ea17b5a82d4da68340e971d328c85cd9f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309578"
---
# <a name="mapi-spooler-overview"></a><span data-ttu-id="cc2c2-103">Présentation du spouleur MAPI</span><span class="sxs-lookup"><span data-stu-id="cc2c2-103">MAPI spooler overview</span></span>
  
<span data-ttu-id="cc2c2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc2c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc2c2-105">Le spouleur MAPI est une fonction du processus Microsoft Office Outlook responsable de l'envoi et de la réception de messages à partir d'un système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-105">MAPI spooler is a function of the Microsoft Office Outlook process that is responsible for sending messages to and receiving messages from a messaging system.</span></span> <span data-ttu-id="cc2c2-106">Le spouleur MAPI joue un rôle vital dans la réception et la remise des messages.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-106">MAPI spooler plays a vital role in message receipt and delivery.</span></span> <span data-ttu-id="cc2c2-107">Lorsqu'un système de messagerie est indisponible, le spouleur MAPI stocke les messages et les transfère automatiquement ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-107">When a messaging system is unavailable, MAPI spooler stores the messages and automatically forwards them at a later time.</span></span> <span data-ttu-id="cc2c2-108">Cette possibilité de conserver ou d'envoyer des données lorsque cela est nécessaire est appelée Store et Forward, une fonctionnalité essentielle dans les environnements où les connexions distantes sont courantes et où le trafic réseau est élevé.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-108">This ability to hold on to or send data when necessary is known as store and forward, a critical feature in environments where remote connections are common and network traffic is high.</span></span> <span data-ttu-id="cc2c2-109">Le spouleur MAPI s'exécute comme un thread d'arrière-plan dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-109">MAPI spooler runs as a background thread within Outlook.</span></span>
  
<span data-ttu-id="cc2c2-110">Le spouleur MAPI dispose de responsabilités supplémentaires liées à la distribution des messages.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-110">MAPI spooler has additional responsibilities related to message distribution.</span></span> <span data-ttu-id="cc2c2-111">Ces droits supplémentaires sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="cc2c2-111">These extra duties include the following:</span></span>
  
- <span data-ttu-id="cc2c2-112">Assurer le suivi des types de destinataires qui sont gérés par des fournisseurs de transport spécifiques.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-112">Keeping track of the recipient types that are handled by specific transport providers.</span></span>
    
- <span data-ttu-id="cc2c2-113">Informer une application cliente lorsqu'un nouveau message a été remis.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-113">Informing a client application when a new message has been delivered.</span></span>
    
- <span data-ttu-id="cc2c2-114">Appel du prétraitement des messages et du post-traitement.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-114">Invoking message preprocessing and postprocessing.</span></span>
    
- <span data-ttu-id="cc2c2-115">Génération de rapports indiquant que la remise des messages s'est produite.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-115">Generating reports that indicate that message delivery has occurred.</span></span>
    
- <span data-ttu-id="cc2c2-116">Gestion de l'état des destinataires traités.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-116">Maintaining status on processed recipients.</span></span>
    
<span data-ttu-id="cc2c2-117">L'illustration suivante montre à un niveau élevé le flux d'un message d'un client vers le système de messagerie.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-117">The following illustration shows at a high level how a message flows from a client to the messaging system.</span></span>
  
<span data-ttu-id="cc2c2-118">**Flux de message sortant**</span><span class="sxs-lookup"><span data-stu-id="cc2c2-118">**Outgoing message flow**</span></span>
  
<span data-ttu-id="cc2c2-119">![Flux de messages sortants] (media/amapi_46.gif "Flux de messages sortants")</span><span class="sxs-lookup"><span data-stu-id="cc2c2-119">![Outgoing message flow](media/amapi_46.gif "Outgoing message flow")</span></span>
  
<span data-ttu-id="cc2c2-120">L'utilisateur d'une application cliente envoie un message à un ou plusieurs destinataires.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-120">The user of a client application sends a message to one or more recipients.</span></span> <span data-ttu-id="cc2c2-121">Le fournisseur de banque de messages lance le processus d'envoi, en mettant en forme le message avec des informations supplémentaires nécessaires pour la transmission.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-121">The message store provider initiates the sending process, formatting the message with additional information needed for transmission.</span></span>
  
<span data-ttu-id="cc2c2-122">Le spouleur MAPI reçoit le message à traiter si l'une des conditions suivantes se produit:</span><span class="sxs-lookup"><span data-stu-id="cc2c2-122">MAPI spooler receives the message to process if any of the following conditions occur:</span></span>
  
- <span data-ttu-id="cc2c2-123">Le fournisseur de banque de messages n'est pas étroitement couplé à un fournisseur de transport.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-123">The message store provider is not tightly coupled with a transport provider.</span></span>
    
- <span data-ttu-id="cc2c2-124">Le message doit être prétraité.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-124">The message requires preprocessing.</span></span>
    
- <span data-ttu-id="cc2c2-125">La Banque de messages et le fournisseur de transport sont étroitement couplés, mais ils ne peuvent pas gérer tous les destinataires auxquels le message est adressé.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-125">The message store and transport provider are tightly coupled, but they cannot handle all the recipients to whom the message is addressed.</span></span>
    
<span data-ttu-id="cc2c2-126">Si le spouleur MAPI reçoit le message, il effectue tout prétraitement requis et remet le message au fournisseur de transport approprié.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-126">If MAPI spooler receives the message, it performs any required preprocessing and delivers the message to the appropriate transport provider.</span></span> <span data-ttu-id="cc2c2-127">Le fournisseur de transport transmet le message à son système de messagerie, qui l'envoie à son destinataire.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-127">The transport provider gives the message to its messaging system, which sends it to its intended recipient.</span></span>
  
<span data-ttu-id="cc2c2-128">Avec les messages entrants, le flux est inversé.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-128">With incoming messages, the flow is reversed.</span></span> <span data-ttu-id="cc2c2-129">Le fournisseur de transport reçoit un message de son système de messagerie et avertit le spouleur MAPI.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-129">The transport provider receives a message from its messaging system and notifies MAPI spooler.</span></span> <span data-ttu-id="cc2c2-130">Spooler effectue le post-traitement nécessaire et informe le fournisseur de banque de messages qu'un nouveau message est arrivé.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-130">Spooler performs any necessary postprocessing and informs the message store provider that a new message has arrived.</span></span> <span data-ttu-id="cc2c2-131">Cette notification fait en sorte que le client actualise son affichage de messages, ce qui permet à l'utilisateur de lire le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="cc2c2-131">This notification causes the client to refresh its message display, enabling the user to read the new message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cc2c2-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc2c2-132">See also</span></span>

- [<span data-ttu-id="cc2c2-133">Architecture et fonctionnalités MAPI</span><span class="sxs-lookup"><span data-stu-id="cc2c2-133">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

