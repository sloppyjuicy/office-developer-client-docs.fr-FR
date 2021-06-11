---
title: Télécharger État de lecture
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e8ad2acf019df3f07060c8e8c71a62afd3fca03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431539"
---
# <a name="upload-read-status-state"></a><span data-ttu-id="8f558-103">Télécharger État de lecture</span><span class="sxs-lookup"><span data-stu-id="8f558-103">Upload Read Status State</span></span>

  
  
<span data-ttu-id="8f558-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f558-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="8f558-105">Cette rubrique décrit ce qui se produit pendant l’état de lecture du chargement de la machine à états de réplication.</span><span class="sxs-lookup"><span data-stu-id="8f558-105">This topic describes what happens during the upload read status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="8f558-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="8f558-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8f558-107">Identificateur d’état :</span><span class="sxs-lookup"><span data-stu-id="8f558-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="8f558-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span><span class="sxs-lookup"><span data-stu-id="8f558-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span></span> <br/> |
|<span data-ttu-id="8f558-109">Structure de données associée :</span><span class="sxs-lookup"><span data-stu-id="8f558-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="8f558-110">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="8f558-110">**[UPREAD](upread.md)**</span></span> <br/> |
|<span data-ttu-id="8f558-111">À partir de cet état :</span><span class="sxs-lookup"><span data-stu-id="8f558-111">From this state:</span></span>  <br/> |[<span data-ttu-id="8f558-112">Télécharger table</span><span class="sxs-lookup"><span data-stu-id="8f558-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="8f558-113">À cet état :</span><span class="sxs-lookup"><span data-stu-id="8f558-113">To this state:</span></span>  <br/> |<span data-ttu-id="8f558-114">Télécharger table</span><span class="sxs-lookup"><span data-stu-id="8f558-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="8f558-115">La machine à états de réplication est une machine à états déterministe.</span><span class="sxs-lookup"><span data-stu-id="8f558-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="8f558-116">Un client s’écartant d’un état à un autre doit finalement revenir au premier à partir du second.</span><span class="sxs-lookup"><span data-stu-id="8f558-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="8f558-117">Description</span><span class="sxs-lookup"><span data-stu-id="8f558-117">Description</span></span>

<span data-ttu-id="8f558-118">Cet état initie le téléchargement de l’état de lecture des éléments dans un dossier spécifié dans un état de table de chargement précédent.</span><span class="sxs-lookup"><span data-stu-id="8f558-118">This state initiates uploading the read status of items in a folder specified in a preceding upload table state.</span></span> <span data-ttu-id="8f558-119">Au cours de cet état, Outlook initialise la structure de données **UPREAD** associée avec les informations pour les éléments du dossier dont l’état de lecture a changé.</span><span class="sxs-lookup"><span data-stu-id="8f558-119">During this state, Outlook initializes the associated **UPREAD** data structure with information for those items in the folder whose read status has changed.</span></span> <span data-ttu-id="8f558-120">Le client met ensuite à jour l’état de lecture de ces éléments sur le serveur comme étant lu ou non lu.</span><span class="sxs-lookup"><span data-stu-id="8f558-120">The client then updates the read status of these items on the server as being read or unread.</span></span> 
  
<span data-ttu-id="8f558-121">Lorsque cet état se termine, Outlook les informations internes sur l’état de lecture de l’élément, ce qui empêche le téléchargement de l’état de lecture de l’élément à nouveau.</span><span class="sxs-lookup"><span data-stu-id="8f558-121">When this state ends, Outlook clears the internal information about the item's read status, preventing the item's read status from being uploaded again.</span></span> <span data-ttu-id="8f558-122">La boutique locale revient à l’état de la table de chargement.</span><span class="sxs-lookup"><span data-stu-id="8f558-122">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8f558-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f558-123">See also</span></span>



[<span data-ttu-id="8f558-124">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="8f558-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="8f558-125">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="8f558-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="8f558-126">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="8f558-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="8f558-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="8f558-127">SYNCSTATE</span></span>](syncstate.md)

