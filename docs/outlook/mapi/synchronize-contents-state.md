---
title: Synchroniser l'état du contenu
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3ebe1f5f48f9becdf01ea184c2b76fa2c8fa21e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349566"
---
# <a name="synchronize-contents-state"></a><span data-ttu-id="16380-103">Synchroniser l'état du contenu</span><span class="sxs-lookup"><span data-stu-id="16380-103">Synchronize Contents State</span></span>

  
  
<span data-ttu-id="16380-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16380-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="16380-105">Cette rubrique décrit ce qui se passe lors de l'État synchroniser le contenu de la machine à États de réplication.</span><span class="sxs-lookup"><span data-stu-id="16380-105">This topic describes what happens during the synchronize contents state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="16380-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="16380-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="16380-107">Identificateur d'État:</span><span class="sxs-lookup"><span data-stu-id="16380-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="16380-108">**LR_SYNC_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="16380-108">**LR_SYNC_CONTENTS**</span></span> <br/> |
|<span data-ttu-id="16380-109">Structure de données associée:</span><span class="sxs-lookup"><span data-stu-id="16380-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="16380-110">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="16380-110">**[SYNCCONT](synccont.md)**</span></span> <br/> |
|<span data-ttu-id="16380-111">À partir de cet État:</span><span class="sxs-lookup"><span data-stu-id="16380-111">From this state:</span></span>  <br/> |[<span data-ttu-id="16380-112">Synchronisation de l’état</span><span class="sxs-lookup"><span data-stu-id="16380-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="16380-113">À cet État:</span><span class="sxs-lookup"><span data-stu-id="16380-113">To this state:</span></span>  <br/> |<span data-ttu-id="16380-114">[Télécharger](download-table-state.md)l'état de la table, charger l'état de la [table](upload-table-state.md)ou synchroniser l'État</span><span class="sxs-lookup"><span data-stu-id="16380-114">[Download table state](download-table-state.md), [upload table state](upload-table-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="16380-115">L'ordinateur d'état de réplication est un ordinateur d'État déterministe.</span><span class="sxs-lookup"><span data-stu-id="16380-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="16380-116">Un client qui se déplace d'un État à un autre doit finalement revenir au premier de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="16380-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="16380-117">Description</span><span class="sxs-lookup"><span data-stu-id="16380-117">Description</span></span>

<span data-ttu-id="16380-118">Cet État lance l'un des deux processus de réplication suivants: le téléchargement du contenu de dossiers spécifiés dans un magasin local ou une synchronisation complète.</span><span class="sxs-lookup"><span data-stu-id="16380-118">This state initiates one of the two replication processes: uploading the contents of specified folders on a local store, or a full synchronization.</span></span> <span data-ttu-id="16380-119">Dans une synchronisation complète, le contenu des dossiers spécifiés est chargé en premier, puis téléchargé.</span><span class="sxs-lookup"><span data-stu-id="16380-119">In a full synchronization, for each of the specified folders, contents are uploaded first and then downloaded.</span></span> <span data-ttu-id="16380-120">Selon le *ulFlags* défini dans la structure de **[synchronisation](sync.md)** correspondante dans l'état de synchronisation précédent, Outlook initialise les membres [out] dans la structure **SYNCCONT** pour fournir des informations sur le contenu.</span><span class="sxs-lookup"><span data-stu-id="16380-120">Depending on the  *ulFlags*  set in the corresponding **[SYNC](sync.md)** structure in the preceding synchronize state, Outlook initializes [out] members in the **SYNCCONT** structure to provide information about the contents.</span></span> 
  
<span data-ttu-id="16380-121">Par le biais de la même structure **SYNCCONT** , le client obtient le nombre de dossiers dont le contenu doit être chargé ou téléchargé.</span><span class="sxs-lookup"><span data-stu-id="16380-121">Through the same **SYNCCONT** structure, the client obtains the count of the folders that have content to be uploaded or downloaded.</span></span> <span data-ttu-id="16380-122">Le client parcourt chacun de ces dossiers en déplacant le magasin local vers l'état de la table de chargement pour télécharger un dossier ou en déplacant le magasin local vers l'état de téléchargement de la table pour télécharger le dossier.</span><span class="sxs-lookup"><span data-stu-id="16380-122">The client will loop through each of these folders by moving the local store to the upload table state to upload a folder, or moving the local store to the download table state to download the folder.</span></span> 
  
<span data-ttu-id="16380-123">En outre, le client obtient des ID d'entrée pour les dossiers qui nécessitent une réplication.</span><span class="sxs-lookup"><span data-stu-id="16380-123">In addition, the client obtains entry IDs for the folders requiring replication.</span></span>
  
<span data-ttu-id="16380-124">Lorsque cet État prend fin, Outlook nettoie ses informations internes.</span><span class="sxs-lookup"><span data-stu-id="16380-124">When this state ends, Outlook cleans up its internal information.</span></span> <span data-ttu-id="16380-125">Le magasin local revient à l'État Synchronize.</span><span class="sxs-lookup"><span data-stu-id="16380-125">The local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="16380-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16380-126">See also</span></span>



[<span data-ttu-id="16380-127">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="16380-127">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="16380-128">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="16380-128">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="16380-129">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="16380-129">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="16380-130">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="16380-130">SYNCSTATE</span></span>](syncstate.md)

