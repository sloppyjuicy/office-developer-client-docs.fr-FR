---
title: Télécharger l'état de l'état de lecture
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e8ad2acf019df3f07060c8e8c71a62afd3fca03c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282662"
---
# <a name="upload-read-status-state"></a><span data-ttu-id="e0369-103">Télécharger l'état de l'état de lecture</span><span class="sxs-lookup"><span data-stu-id="e0369-103">Upload Read Status State</span></span>

  
  
<span data-ttu-id="e0369-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0369-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="e0369-105">Cette rubrique décrit ce qui se passe lors de l'état de lecture de téléchargement de l'ordinateur d'état de réplication.</span><span class="sxs-lookup"><span data-stu-id="e0369-105">This topic describes what happens during the upload read status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e0369-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="e0369-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0369-107">Identificateur d'État:</span><span class="sxs-lookup"><span data-stu-id="e0369-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="e0369-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span><span class="sxs-lookup"><span data-stu-id="e0369-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span></span> <br/> |
|<span data-ttu-id="e0369-109">Structure de données associée:</span><span class="sxs-lookup"><span data-stu-id="e0369-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="e0369-110">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="e0369-110">**[UPREAD](upread.md)**</span></span> <br/> |
|<span data-ttu-id="e0369-111">À partir de cet État:</span><span class="sxs-lookup"><span data-stu-id="e0369-111">From this state:</span></span>  <br/> |[<span data-ttu-id="e0369-112">Charger l'état de la table</span><span class="sxs-lookup"><span data-stu-id="e0369-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="e0369-113">À cet État:</span><span class="sxs-lookup"><span data-stu-id="e0369-113">To this state:</span></span>  <br/> |<span data-ttu-id="e0369-114">Charger l'état de la table</span><span class="sxs-lookup"><span data-stu-id="e0369-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="e0369-115">L'ordinateur d'état de réplication est un ordinateur d'État déterministe.</span><span class="sxs-lookup"><span data-stu-id="e0369-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="e0369-116">Un client qui se déplace d'un État à un autre doit finalement revenir au premier de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="e0369-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="e0369-117">Description</span><span class="sxs-lookup"><span data-stu-id="e0369-117">Description</span></span>

<span data-ttu-id="e0369-118">Cet État lance le téléchargement de l'état de lecture des éléments dans un dossier spécifié dans un état de tableau de téléchargement précédent.</span><span class="sxs-lookup"><span data-stu-id="e0369-118">This state initiates uploading the read status of items in a folder specified in a preceding upload table state.</span></span> <span data-ttu-id="e0369-119">Dans cet État, Outlook initialise la structure de données de la **lecture** associée avec les informations de ces éléments dans le dossier dont le statut de lecture a changé.</span><span class="sxs-lookup"><span data-stu-id="e0369-119">During this state, Outlook initializes the associated **UPREAD** data structure with information for those items in the folder whose read status has changed.</span></span> <span data-ttu-id="e0369-120">Le client met ensuite à jour l'état de lecture de ces éléments sur le serveur comme étant lus ou non lus.</span><span class="sxs-lookup"><span data-stu-id="e0369-120">The client then updates the read status of these items on the server as being read or unread.</span></span> 
  
<span data-ttu-id="e0369-121">Lorsque cet État est terminé, Outlook efface les informations internes relatives à l'état de lecture de l'élément, ce qui empêche le chargement de l'état de lecture de l'élément.</span><span class="sxs-lookup"><span data-stu-id="e0369-121">When this state ends, Outlook clears the internal information about the item's read status, preventing the item's read status from being uploaded again.</span></span> <span data-ttu-id="e0369-122">Le magasin local revient à l'état de la table de chargement.</span><span class="sxs-lookup"><span data-stu-id="e0369-122">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e0369-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0369-123">See also</span></span>



[<span data-ttu-id="e0369-124">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="e0369-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="e0369-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="e0369-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="e0369-126">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="e0369-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="e0369-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="e0369-127">SYNCSTATE</span></span>](syncstate.md)

