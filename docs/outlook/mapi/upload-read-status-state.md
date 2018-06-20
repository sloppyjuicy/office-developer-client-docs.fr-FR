---
title: État de la lecture de téléchargement
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 172eaf47d305cf6e4d1ba54ceb4ac4b4feab80e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787429"
---
# <a name="upload-read-status-state"></a><span data-ttu-id="03943-103">État de la lecture de téléchargement</span><span class="sxs-lookup"><span data-stu-id="03943-103">Upload Read Status State</span></span>

  
  
<span data-ttu-id="03943-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="03943-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="03943-105">Cette rubrique décrit ce qui se produit lors du téléchargement de lire l’état de l’ordinateur d’état de réplication.</span><span class="sxs-lookup"><span data-stu-id="03943-105">This topic describes what happens during the upload read status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="03943-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="03943-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="03943-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="03943-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="03943-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span><span class="sxs-lookup"><span data-stu-id="03943-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span></span> <br/> |
|<span data-ttu-id="03943-109">Structure de données associées :</span><span class="sxs-lookup"><span data-stu-id="03943-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="03943-110">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="03943-110">**[UPREAD](upread.md)**</span></span> <br/> |
|<span data-ttu-id="03943-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="03943-111">From this state:</span></span>  <br/> |[<span data-ttu-id="03943-112">Télécharger l’état de la table</span><span class="sxs-lookup"><span data-stu-id="03943-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="03943-113">Avec cet état :</span><span class="sxs-lookup"><span data-stu-id="03943-113">To this state:</span></span>  <br/> |<span data-ttu-id="03943-114">Télécharger l’état de la table</span><span class="sxs-lookup"><span data-stu-id="03943-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="03943-115">L’ordinateur d’état de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="03943-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="03943-116">Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="03943-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="03943-117">Description</span><span class="sxs-lookup"><span data-stu-id="03943-117">Description</span></span>

<span data-ttu-id="03943-118">Cet état lance le téléchargement de l’état de lecture d’éléments dans un dossier spécifié dans un état de table de téléchargement précédent.</span><span class="sxs-lookup"><span data-stu-id="03943-118">This state initiates uploading the read status of items in a folder specified in a preceding upload table state.</span></span> <span data-ttu-id="03943-119">Au cours de cet état, Outlook initialise la structure de données **UPREAD** associée avec des informations pour ces éléments dans le dossier dont l’état de lecture a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="03943-119">During this state, Outlook initializes the associated **UPREAD** data structure with information for those items in the folder whose read status has changed.</span></span> <span data-ttu-id="03943-120">Le client met à jour l’état de lecture de ces éléments sur le serveur comme étant lus ou non lus.</span><span class="sxs-lookup"><span data-stu-id="03943-120">The client then updates the read status of these items on the server as being read or unread.</span></span> 
  
<span data-ttu-id="03943-121">Lorsque cet état se termine, Outlook efface les informations internes sur l’état de la lecture, empêche le téléchargement à nouveau l’état de lecture.</span><span class="sxs-lookup"><span data-stu-id="03943-121">When this state ends, Outlook clears the internal information about the item's read status, preventing the item's read status from being uploaded again.</span></span> <span data-ttu-id="03943-122">Le magasin local renvoie l’état de la table de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="03943-122">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="03943-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03943-123">See also</span></span>



[<span data-ttu-id="03943-124">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="03943-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="03943-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="03943-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="03943-126">Sur l’ordinateur de l’état de réplication</span><span class="sxs-lookup"><span data-stu-id="03943-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="03943-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="03943-127">SYNCSTATE</span></span>](syncstate.md)

