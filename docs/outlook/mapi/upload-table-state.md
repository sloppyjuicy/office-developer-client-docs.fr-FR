---
title: Télécharger l’état de la table
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: bd54c30e8701a13637235e28ddcfef4c21d10a2b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576980"
---
# <a name="upload-table-state"></a><span data-ttu-id="df9ff-103">Télécharger l’état de la table</span><span class="sxs-lookup"><span data-stu-id="df9ff-103">Upload Table State</span></span>

  
  
<span data-ttu-id="df9ff-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df9ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="df9ff-105">Cette rubrique décrit le déroulement de l’état du tableau de téléchargement de l’ordinateur d’état de réplication.</span><span class="sxs-lookup"><span data-stu-id="df9ff-105">This topic describes what happens during the upload table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="df9ff-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="df9ff-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df9ff-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="df9ff-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="df9ff-108">**LR_SYNC_UPLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="df9ff-108">**LR_SYNC_UPLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="df9ff-109">Structure de données associées :</span><span class="sxs-lookup"><span data-stu-id="df9ff-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="df9ff-110">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="df9ff-110">**[UPTBL](uptbl.md)**</span></span> <br/> |
|<span data-ttu-id="df9ff-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="df9ff-111">From this state:</span></span>  <br/> |[<span data-ttu-id="df9ff-112">Synchroniser le contenu d’un état</span><span class="sxs-lookup"><span data-stu-id="df9ff-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="df9ff-113">Avec cet état :</span><span class="sxs-lookup"><span data-stu-id="df9ff-113">To this state:</span></span>  <br/> |<span data-ttu-id="df9ff-114">[Télécharger l’état du message](upload-message-state.md), [téléchargement supprimer état](upload-delete-status-state.md), [lire l’état de téléchargement](upload-read-status-state.md), ou de synchroniser le contenu d’un état</span><span class="sxs-lookup"><span data-stu-id="df9ff-114">[Upload message state](upload-message-state.md), [upload delete status state](upload-delete-status-state.md), [upload read status state](upload-read-status-state.md), or synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="df9ff-115">L’ordinateur d’état de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="df9ff-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="df9ff-116">Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="df9ff-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="df9ff-117">Description</span><span class="sxs-lookup"><span data-stu-id="df9ff-117">Description</span></span>

<span data-ttu-id="df9ff-118">Cet état lance le téléchargement du contenu d’un dossier qui a été spécifié dans un état de contenu précédente synchroniser.</span><span class="sxs-lookup"><span data-stu-id="df9ff-118">This state initiates uploading the contents of a folder that has been specified in a preceding synchronize contents state.</span></span> <span data-ttu-id="df9ff-119">Le dossier peut être un dossier de courrier, calendrier, contacts, tâches, notes ou journal.</span><span class="sxs-lookup"><span data-stu-id="df9ff-119">The folder can be a mail, calendar, contacts, tasks, notes, or journal folder.</span></span> <span data-ttu-id="df9ff-120">Au cours de cet état, Outlook crée une liste d’éléments qui ont été ajoutées, modifiées, déplacé, supprimé ou marqués comme étant en lecture et prépare les informations appropriées internes de l’état du message de téléchargement correspondant, télécharger l’état de la suppression ou charger l’état de lecture état.</span><span class="sxs-lookup"><span data-stu-id="df9ff-120">During this state, Outlook creates a list of items that have been added, modified, moved, deleted, or marked as read, and prepares the appropriate internal information for the corresponding upload message state, upload delete status state, or upload read status state.</span></span>
  
<span data-ttu-id="df9ff-121">Lorsque cet état se termine, Outlook marque le dossier comme ayant son contenu synchronisées, afin que le contenu n’est téléchargé à nouveau jusqu'à ce qu’un autre est modifiée.</span><span class="sxs-lookup"><span data-stu-id="df9ff-121">When this state ends, Outlook marks the folder as having its contents synchronized, so that the contents will not be uploaded again until another modification is made.</span></span> <span data-ttu-id="df9ff-122">Le magasin local renvoie à l’état du contenu synchroniser.</span><span class="sxs-lookup"><span data-stu-id="df9ff-122">The local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="df9ff-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df9ff-123">See also</span></span>



[<span data-ttu-id="df9ff-124">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="df9ff-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="df9ff-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="df9ff-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="df9ff-126">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="df9ff-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="df9ff-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="df9ff-127">SYNCSTATE</span></span>](syncstate.md)

