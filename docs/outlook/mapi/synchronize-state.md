---
title: Synchroniser l'État
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7abbf049a848d417f640528e5030e37a954413e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414626"
---
# <a name="synchronize-state"></a><span data-ttu-id="3bcd2-103">Synchroniser l'État</span><span class="sxs-lookup"><span data-stu-id="3bcd2-103">Synchronize State</span></span>

  
  
<span data-ttu-id="3bcd2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3bcd2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="3bcd2-105">Cette rubrique décrit ce qui se passe lors de l'état de synchronisation de la machine à États de réplication.</span><span class="sxs-lookup"><span data-stu-id="3bcd2-105">This topic describes what happens during the synchronize state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="3bcd2-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="3bcd2-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3bcd2-107">Identificateur d'État:</span><span class="sxs-lookup"><span data-stu-id="3bcd2-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="3bcd2-108">**LR_SYNC**</span><span class="sxs-lookup"><span data-stu-id="3bcd2-108">**LR_SYNC**</span></span> <br/> |
|<span data-ttu-id="3bcd2-109">Structure de données associée:</span><span class="sxs-lookup"><span data-stu-id="3bcd2-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="3bcd2-110">**[SYNCHRONI](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="3bcd2-110">**[SYNC](sync.md)**</span></span> <br/> |
|<span data-ttu-id="3bcd2-111">À partir de cet État:</span><span class="sxs-lookup"><span data-stu-id="3bcd2-111">From this state:</span></span>  <br/> |[<span data-ttu-id="3bcd2-112">État inactif</span><span class="sxs-lookup"><span data-stu-id="3bcd2-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="3bcd2-113">À cet État:</span><span class="sxs-lookup"><span data-stu-id="3bcd2-113">To this state:</span></span>  <br/> |<span data-ttu-id="3bcd2-114">[Télécharger](download-hierarchy-state.md)l'état de la hiérarchie, synchroniser l'état du [contenu](synchronize-contents-state.md), [charger l'État](upload-hierarchy-state.md)de la hiérarchie ou état inactif</span><span class="sxs-lookup"><span data-stu-id="3bcd2-114">[Download hierarchy state](download-hierarchy-state.md), [synchronize contents state](synchronize-contents-state.md), [upload hierarchy state](upload-hierarchy-state.md), or idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="3bcd2-115">L'ordinateur d'état de réplication est un ordinateur d'État déterministe.</span><span class="sxs-lookup"><span data-stu-id="3bcd2-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="3bcd2-116">Un client qui se déplace d'un État à un autre doit finalement revenir au premier de ce dernier.</span><span class="sxs-lookup"><span data-stu-id="3bcd2-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="3bcd2-117">Description</span><span class="sxs-lookup"><span data-stu-id="3bcd2-117">Description</span></span>

<span data-ttu-id="3bcd2-118">Cet État lance la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="3bcd2-118">This state initiates synchronization.</span></span> <span data-ttu-id="3bcd2-119">Un magasin local peut effectuer une transition vers un état de téléchargement ou de téléchargement à partir de cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="3bcd2-119">A local store can transition to an upload or a download state from here.</span></span> <span data-ttu-id="3bcd2-120">Par exemple, un magasin local peut être déplacé vers l'état de la hiérarchie de téléchargement pour charger une hiérarchie de dossiers sur le serveur, ou il peut effectuer une synchronisation complète en téléchargeant d'abord la hiérarchie, puis en téléchargeant la hiérarchie à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="3bcd2-120">For example, a local store can move to the upload hierarchy state to upload a folder hierarchy to the server, or it can perform a full synchronization by first uploading the hierarchy and then downloading the hierarchy from the server.</span></span>
  
<span data-ttu-id="3bcd2-121">Dans cet État, Outlook initialise la structure de données de **synchronisation** associée avec le chemin d'accès au magasin local, afin qu'Outlook détecte les modifications dans les autres États.</span><span class="sxs-lookup"><span data-stu-id="3bcd2-121">During this state, Outlook initializes the associated **SYNC** data structure with the path to the local store, so that Outlook sees modifications during other states.</span></span> 
  
<span data-ttu-id="3bcd2-122">Le client définit les membres [in] de la **synchronisation**, ce qui indique à Outlook comment gérer d'autres États.</span><span class="sxs-lookup"><span data-stu-id="3bcd2-122">The client sets the [in] members of **SYNC**, which tells Outlook how to handle other states.</span></span> <span data-ttu-id="3bcd2-123">Par exemple, le client peut définir *ulFlags* sur **UPS_UPLOAD_ONLY** et **UPS_THESE_FOLDERS** et *PEL* sur une liste d'identificateurs d'entrée des dossiers pour indiquer à Outlook que seuls ces dossiers seront chargés.</span><span class="sxs-lookup"><span data-stu-id="3bcd2-123">For example, the client can set  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_THESE_FOLDERS** and  *pel*  to a list of entry identifiers of the folders to tell Outlook that only these folders will be uploaded.</span></span> <span data-ttu-id="3bcd2-124">Lorsque cet État se termine, le magasin local revient à l'état inactif.</span><span class="sxs-lookup"><span data-stu-id="3bcd2-124">When this state ends, the local store reverts to the idle state.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3bcd2-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bcd2-125">See also</span></span>



[<span data-ttu-id="3bcd2-126">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="3bcd2-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="3bcd2-127">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="3bcd2-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="3bcd2-128">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="3bcd2-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="3bcd2-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="3bcd2-129">SYNCSTATE</span></span>](syncstate.md)

