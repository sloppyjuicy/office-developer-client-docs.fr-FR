---
title: Télécharger l'état de l'en-tête du message
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c8e83119d724f583d40583a6a5227bc467dc94da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338835"
---
# <a name="download-message-header-state"></a><span data-ttu-id="928f4-103">Télécharger l'état de l'en-tête du message</span><span class="sxs-lookup"><span data-stu-id="928f4-103">Download Message Header State</span></span>

  
  
<span data-ttu-id="928f4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="928f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="928f4-105">Cette rubrique décrit ce qui se passe pendant l'état de l'en-tête du message de téléchargement de la machine à États de réplication.</span><span class="sxs-lookup"><span data-stu-id="928f4-105">This topic describes what happens during the download message header state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="928f4-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="928f4-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="928f4-107">Identificateur d'État:</span><span class="sxs-lookup"><span data-stu-id="928f4-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="928f4-108">**LR_SYNC_DOWNLOAD_HEADER**</span><span class="sxs-lookup"><span data-stu-id="928f4-108">**LR_SYNC_DOWNLOAD_HEADER**</span></span> <br/> |
|<span data-ttu-id="928f4-109">Structure de données associée:</span><span class="sxs-lookup"><span data-stu-id="928f4-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="928f4-110">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="928f4-110">**[HDRSYNC](hdrsync.md)**</span></span> <br/> |
|<span data-ttu-id="928f4-111">À partir de cet État:</span><span class="sxs-lookup"><span data-stu-id="928f4-111">From this state:</span></span>  <br/> |[<span data-ttu-id="928f4-112">État inactif</span><span class="sxs-lookup"><span data-stu-id="928f4-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="928f4-113">À cet État:</span><span class="sxs-lookup"><span data-stu-id="928f4-113">To this state:</span></span>  <br/> |<span data-ttu-id="928f4-114">État inactif</span><span class="sxs-lookup"><span data-stu-id="928f4-114">Idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="928f4-115">L'ordinateur d'état de réplication est un ordinateur d'État déterministe.</span><span class="sxs-lookup"><span data-stu-id="928f4-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="928f4-116">Un client qui se déplace d'un État à un autre doit finalement revenir au premier de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="928f4-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="928f4-117">Description</span><span class="sxs-lookup"><span data-stu-id="928f4-117">Description</span></span>

<span data-ttu-id="928f4-118">Dans cet État, le client met à jour l'en-tête d'un message dans un magasin local.</span><span class="sxs-lookup"><span data-stu-id="928f4-118">During this state, the client updates the header of a message on a local store.</span></span> <span data-ttu-id="928f4-119">Le magasin local passe dans cet État sur **[IOSTX:: SyncHdrBeg](iostx-synchdrbeg.md)** et quitte lorsque **[IOSTX:: SyncHdrEnd](iostx-synchdrend.md)** est appelé.</span><span class="sxs-lookup"><span data-stu-id="928f4-119">The local store enters this state upon **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** and exits when **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** is called.</span></span> <span data-ttu-id="928f4-120">Dans cet État, Outlook initialise les membres de la structure de données **HDRSYNC** associée avec des informations sur l'en-tête d'un message.</span><span class="sxs-lookup"><span data-stu-id="928f4-120">During this state, Outlook initializes members of the associated **HDRSYNC** data structure with information about the header of a message.</span></span> <span data-ttu-id="928f4-121">Le client télécharge d'abord l'élément de message complet à partir du serveur, puis met à jour l'en-tête de l'élément de message localement.</span><span class="sxs-lookup"><span data-stu-id="928f4-121">The client first downloads the full message item from the server and then updates the header of the message item locally.</span></span> 
  
<span data-ttu-id="928f4-122">Lorsque synchronisation se termine, le client définit les résultats du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="928f4-122">When syncrhonization ends, the client sets the download results.</span></span> <span data-ttu-id="928f4-123">Le magasin local revient à l'état inactif.</span><span class="sxs-lookup"><span data-stu-id="928f4-123">The local store returns to the idle state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="928f4-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="928f4-124">See also</span></span>



[<span data-ttu-id="928f4-125">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="928f4-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="928f4-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="928f4-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="928f4-127">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="928f4-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="928f4-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="928f4-128">SYNCSTATE</span></span>](syncstate.md)

