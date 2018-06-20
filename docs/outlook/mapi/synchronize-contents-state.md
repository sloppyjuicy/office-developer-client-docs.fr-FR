---
title: Synchroniser le contenu d’un état
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 216691f2c1f94d658a5aa968d6a19148a9b3c06a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787311"
---
# <a name="synchronize-contents-state"></a><span data-ttu-id="c4631-103">Synchroniser le contenu d’un état</span><span class="sxs-lookup"><span data-stu-id="c4631-103">Synchronize Contents State</span></span>

  
  
<span data-ttu-id="c4631-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c4631-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="c4631-105">Cette rubrique décrit le déroulement de l’état du contenu de synchroniser de l’ordinateur d’état de réplication.</span><span class="sxs-lookup"><span data-stu-id="c4631-105">This topic describes what happens during the synchronize contents state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="c4631-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="c4631-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c4631-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="c4631-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="c4631-108">**LR_SYNC_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="c4631-108">**LR_SYNC_CONTENTS**</span></span> <br/> |
|<span data-ttu-id="c4631-109">Structure de données associées :</span><span class="sxs-lookup"><span data-stu-id="c4631-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="c4631-110">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="c4631-110">**[SYNCCONT](synccont.md)**</span></span> <br/> |
|<span data-ttu-id="c4631-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="c4631-111">From this state:</span></span>  <br/> |[<span data-ttu-id="c4631-112">État de synchronisation</span><span class="sxs-lookup"><span data-stu-id="c4631-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="c4631-113">Avec cet état :</span><span class="sxs-lookup"><span data-stu-id="c4631-113">To this state:</span></span>  <br/> |<span data-ttu-id="c4631-114">[Table état du téléchargement](download-table-state.md), [Téléchargez l’état de la table](upload-table-state.md), ou l’état de synchronisation</span><span class="sxs-lookup"><span data-stu-id="c4631-114">[Download table state](download-table-state.md), [upload table state](upload-table-state.md), or synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="c4631-115">L’ordinateur d’état de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="c4631-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="c4631-116">Un client au départ d’un état à l’autre doit renvoyer par la suite à l’ancienne à partir de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="c4631-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="c4631-117">Description</span><span class="sxs-lookup"><span data-stu-id="c4631-117">Description</span></span>

<span data-ttu-id="c4631-118">Cet état lance un des deux processus de réplication : télécharger le contenu de spécifiées dossiers dans un magasin local ou une synchronisation complète.</span><span class="sxs-lookup"><span data-stu-id="c4631-118">This state initiates one of the two replication processes: uploading the contents of specified folders on a local store, or a full synchronization.</span></span> <span data-ttu-id="c4631-119">Dans une synchronisation complète, pour chacun des dossiers spécifiés, le contenu est téléchargées en premier et puis téléchargé.</span><span class="sxs-lookup"><span data-stu-id="c4631-119">In a full synchronization, for each of the specified folders, contents are uploaded first and then downloaded.</span></span> <span data-ttu-id="c4631-120">Selon *ulFlags* définie dans la structure de **[synchronisation](sync.md)** correspondante dans le précédent synchroniser état, Outlook initialise [out] les membres de la structure **SYNCCONT** pour fournir des informations sur le contenu.</span><span class="sxs-lookup"><span data-stu-id="c4631-120">Depending on the  *ulFlags*  set in the corresponding **[SYNC](sync.md)** structure in the preceding synchronize state, Outlook initializes [out] members in the **SYNCCONT** structure to provide information about the contents.</span></span> 
  
<span data-ttu-id="c4631-121">Par le biais de la même structure **SYNCCONT** , le client obtient le nombre de dossiers dont le contenu téléchargé ou téléchargé.</span><span class="sxs-lookup"><span data-stu-id="c4631-121">Through the same **SYNCCONT** structure, the client obtains the count of the folders that have content to be uploaded or downloaded.</span></span> <span data-ttu-id="c4631-122">Le client parcourt en boucle chacun de ces dossiers par déplacement du magasin local à l’état de la table de téléchargement pour télécharger un dossier ou le déplacement du magasin local à l’état de table de téléchargement pour télécharger le dossier.</span><span class="sxs-lookup"><span data-stu-id="c4631-122">The client will loop through each of these folders by moving the local store to the upload table state to upload a folder, or moving the local store to the download table state to download the folder.</span></span> 
  
<span data-ttu-id="c4631-123">En outre, le client obtient les identificateurs d’entrée pour les dossiers nécessitant la réplication.</span><span class="sxs-lookup"><span data-stu-id="c4631-123">In addition, the client obtains entry IDs for the folders requiring replication.</span></span>
  
<span data-ttu-id="c4631-124">Lorsque cet état se termine, Outlook nettoie ses informations internes.</span><span class="sxs-lookup"><span data-stu-id="c4631-124">When this state ends, Outlook cleans up its internal information.</span></span> <span data-ttu-id="c4631-125">Le magasin local renvoie l’état de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="c4631-125">The local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c4631-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4631-126">See also</span></span>



[<span data-ttu-id="c4631-127">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="c4631-127">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="c4631-128">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="c4631-128">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="c4631-129">Sur l’ordinateur de l’état de réplication</span><span class="sxs-lookup"><span data-stu-id="c4631-129">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="c4631-130">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="c4631-130">SYNCSTATE</span></span>](syncstate.md)

