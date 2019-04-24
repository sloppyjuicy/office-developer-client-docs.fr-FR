---
title: Charger l'état de la table
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a2a9b3f214c76b8ec965c84c4731e0dc57e83352
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342839"
---
# <a name="upload-table-state"></a><span data-ttu-id="4694b-103">Charger l'état de la table</span><span class="sxs-lookup"><span data-stu-id="4694b-103">Upload Table State</span></span>

  
  
<span data-ttu-id="4694b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4694b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="4694b-105">Cette rubrique décrit ce qui se passe lors de l'état de la table de chargement de la machine à États de réplication.</span><span class="sxs-lookup"><span data-stu-id="4694b-105">This topic describes what happens during the upload table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4694b-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="4694b-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4694b-107">Identificateur d'État:</span><span class="sxs-lookup"><span data-stu-id="4694b-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="4694b-108">**LR_SYNC_UPLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="4694b-108">**LR_SYNC_UPLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="4694b-109">Structure de données associée:</span><span class="sxs-lookup"><span data-stu-id="4694b-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="4694b-110">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="4694b-110">**[UPTBL](uptbl.md)**</span></span> <br/> |
|<span data-ttu-id="4694b-111">À partir de cet État:</span><span class="sxs-lookup"><span data-stu-id="4694b-111">From this state:</span></span>  <br/> |[<span data-ttu-id="4694b-112">Synchroniser l'état du contenu</span><span class="sxs-lookup"><span data-stu-id="4694b-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="4694b-113">À cet État:</span><span class="sxs-lookup"><span data-stu-id="4694b-113">To this state:</span></span>  <br/> |<span data-ttu-id="4694b-114">[Télécharger](upload-message-state.md)l'état du message, télécharger l'état de l'état de la [suppression](upload-delete-status-state.md), télécharger l'état de l'état de [lecture](upload-read-status-state.md)ou synchroniser l'état du contenu</span><span class="sxs-lookup"><span data-stu-id="4694b-114">[Upload message state](upload-message-state.md), [upload delete status state](upload-delete-status-state.md), [upload read status state](upload-read-status-state.md), or synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="4694b-115">L'ordinateur d'état de réplication est un ordinateur d'État déterministe.</span><span class="sxs-lookup"><span data-stu-id="4694b-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="4694b-116">Un client qui se déplace d'un État à un autre doit finalement revenir au premier de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="4694b-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="4694b-117">Description</span><span class="sxs-lookup"><span data-stu-id="4694b-117">Description</span></span>

<span data-ttu-id="4694b-118">Cet État lance le téléchargement du contenu d'un dossier qui a été spécifié dans un état de contenu de synchronisation précédent.</span><span class="sxs-lookup"><span data-stu-id="4694b-118">This state initiates uploading the contents of a folder that has been specified in a preceding synchronize contents state.</span></span> <span data-ttu-id="4694b-119">Le dossier peut être un dossier courrier, calendrier, contacts, tâches, notes ou journal.</span><span class="sxs-lookup"><span data-stu-id="4694b-119">The folder can be a mail, calendar, contacts, tasks, notes, or journal folder.</span></span> <span data-ttu-id="4694b-120">Dans cet État, Outlook crée une liste des éléments qui ont été ajoutés, modifiés, déplacés, supprimés ou marqués comme lus, et prépare les informations internes appropriées pour l'état du message de téléchargement correspondant, l'état de la suppression du téléchargement ou le statut de lecture du téléchargement. Etat.</span><span class="sxs-lookup"><span data-stu-id="4694b-120">During this state, Outlook creates a list of items that have been added, modified, moved, deleted, or marked as read, and prepares the appropriate internal information for the corresponding upload message state, upload delete status state, or upload read status state.</span></span>
  
<span data-ttu-id="4694b-121">Lorsque cet État est terminé, Outlook marque le dossier comme étant synchronisé, de sorte que le contenu ne soit pas téléchargé à nouveau tant qu'une autre modification n'est pas effectuée.</span><span class="sxs-lookup"><span data-stu-id="4694b-121">When this state ends, Outlook marks the folder as having its contents synchronized, so that the contents will not be uploaded again until another modification is made.</span></span> <span data-ttu-id="4694b-122">Le magasin local revient à l'État Synchronize content.</span><span class="sxs-lookup"><span data-stu-id="4694b-122">The local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4694b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4694b-123">See also</span></span>



[<span data-ttu-id="4694b-124">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="4694b-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="4694b-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="4694b-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="4694b-126">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="4694b-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="4694b-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="4694b-127">SYNCSTATE</span></span>](syncstate.md)

