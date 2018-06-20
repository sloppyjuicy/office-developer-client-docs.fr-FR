---
title: En-tête d’état du Message de téléchargement
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7407b6606634ecc0151f582e4481ecbff5e7dc57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783197"
---
# <a name="download-message-header-state"></a><span data-ttu-id="d7379-103">En-tête d’état du Message de téléchargement</span><span class="sxs-lookup"><span data-stu-id="d7379-103">Download Message Header State</span></span>

  
  
<span data-ttu-id="d7379-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7379-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="d7379-105">Cette rubrique décrit le déroulement de l’état d’en-tête de message téléchargement de l’ordinateur d’état de réplication.</span><span class="sxs-lookup"><span data-stu-id="d7379-105">This topic describes what happens during the download message header state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="d7379-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="d7379-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d7379-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="d7379-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="d7379-108">**LR_SYNC_DOWNLOAD_HEADER**</span><span class="sxs-lookup"><span data-stu-id="d7379-108">**LR_SYNC_DOWNLOAD_HEADER**</span></span> <br/> |
|<span data-ttu-id="d7379-109">Structure de données associées :</span><span class="sxs-lookup"><span data-stu-id="d7379-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="d7379-110">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="d7379-110">**[HDRSYNC](hdrsync.md)**</span></span> <br/> |
|<span data-ttu-id="d7379-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="d7379-111">From this state:</span></span>  <br/> |[<span data-ttu-id="d7379-112">État inactif</span><span class="sxs-lookup"><span data-stu-id="d7379-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="d7379-113">Avec cet état :</span><span class="sxs-lookup"><span data-stu-id="d7379-113">To this state:</span></span>  <br/> |<span data-ttu-id="d7379-114">État inactif</span><span class="sxs-lookup"><span data-stu-id="d7379-114">Idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="d7379-115">L’ordinateur d’état de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="d7379-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="d7379-116">Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="d7379-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="d7379-117">Description</span><span class="sxs-lookup"><span data-stu-id="d7379-117">Description</span></span>

<span data-ttu-id="d7379-118">Au cours de cet état, le client met à jour l’en-tête d’un message sur un magasin local.</span><span class="sxs-lookup"><span data-stu-id="d7379-118">During this state, the client updates the header of a message on a local store.</span></span> <span data-ttu-id="d7379-119">Le magasin local passe à cet état lors de **[l’IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** et quitte lorsque **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** est appelée.</span><span class="sxs-lookup"><span data-stu-id="d7379-119">The local store enters this state upon **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** and exits when **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** is called.</span></span> <span data-ttu-id="d7379-120">Au cours de cet état, Outlook initialise les membres de la structure de données **HDRSYNC** associée avec des informations sur l’en-tête d’un message.</span><span class="sxs-lookup"><span data-stu-id="d7379-120">During this state, Outlook initializes members of the associated **HDRSYNC** data structure with information about the header of a message.</span></span> <span data-ttu-id="d7379-121">Le client télécharge d’abord l’élément de message complet à partir du serveur, puis met à jour l’en-tête de l’élément de message localement.</span><span class="sxs-lookup"><span data-stu-id="d7379-121">The client first downloads the full message item from the server and then updates the header of the message item locally.</span></span> 
  
<span data-ttu-id="d7379-122">Lors de la synchronisation se termine, le client définit les résultats de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="d7379-122">When syncrhonization ends, the client sets the download results.</span></span> <span data-ttu-id="d7379-123">Le magasin local renvoie l’état inactif.</span><span class="sxs-lookup"><span data-stu-id="d7379-123">The local store returns to the idle state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d7379-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7379-124">See also</span></span>



[<span data-ttu-id="d7379-125">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="d7379-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="d7379-126">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="d7379-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="d7379-127">Sur l’ordinateur de l’état de réplication</span><span class="sxs-lookup"><span data-stu-id="d7379-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="d7379-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="d7379-128">SYNCSTATE</span></span>](syncstate.md)

