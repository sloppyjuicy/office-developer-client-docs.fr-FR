---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 45ef7ce9291376ac020035f0bde6172caf6cc01b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359422"
---
# <a name="uphier"></a><span data-ttu-id="c9b7a-103">UPHIER</span><span class="sxs-lookup"><span data-stu-id="c9b7a-103">UPHIER</span></span>
 
<span data-ttu-id="c9b7a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9b7a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9b7a-105">Informations pour la synchronisation d'une hiérarchie de dossiers pendant l'état de la [hiérarchie de téléchargement](upload-hierarchy-state.md).</span><span class="sxs-lookup"><span data-stu-id="c9b7a-105">Information for synchronizing a folder hierarchy during the [upload hierarchy state](upload-hierarchy-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c9b7a-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="c9b7a-106">Quick info</span></span>

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="c9b7a-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c9b7a-107">Members</span></span>

<span data-ttu-id="c9b7a-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c9b7a-108">_ulFlags_</span></span>
  
> <span data-ttu-id="c9b7a-109">dans Indicateurs permettant de modifier le comportement lors de la synchronisation de la hiérarchie de dossiers.</span><span class="sxs-lookup"><span data-stu-id="c9b7a-109">[in] Flags to modify the behavior when synchronizing the folder hierarchy.</span></span>
    
  - <span data-ttu-id="c9b7a-110">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="c9b7a-110">UPH_OK</span></span>
    
    - <span data-ttu-id="c9b7a-111">dans Le chargement a réussi.</span><span class="sxs-lookup"><span data-stu-id="c9b7a-111">[in] Upload was successful.</span></span> <span data-ttu-id="c9b7a-112">Le client définit ceci après le chargement réussi des informations sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="c9b7a-112">The client sets this after successfully uploading information to the server.</span></span> <span data-ttu-id="c9b7a-113">À l'affichage de cet indicateur, Outlook efface toutes les informations de suivi internes qui indiquaient la hiérarchie de dossiers nécessaire à la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="c9b7a-113">Upon seeing this flag, Outlook clears any internal bookkeeping information that indicated the folder hierarchy needed updating.</span></span> 
    
    - <span data-ttu-id="c9b7a-114">Le client transmet le HRESULT si le chargement a échoué.</span><span class="sxs-lookup"><span data-stu-id="c9b7a-114">The client passes the HRESULT if the upload was not successful.</span></span>
    
<span data-ttu-id="c9b7a-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="c9b7a-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="c9b7a-116">remarquer Ce membre est réservé à un usage interne d'Outlook et n'est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c9b7a-116">[out] This member is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="c9b7a-117">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="c9b7a-117">_iEnt_</span></span>
  
> <span data-ttu-id="c9b7a-118">remarquer Index pour suivre la synchronisation du nombre de dossiers spécifiés par *cEnt* .</span><span class="sxs-lookup"><span data-stu-id="c9b7a-118">[out] Index to track synchronizing the number of folders specified by  *cEnt*  .</span></span> 
    
<span data-ttu-id="c9b7a-119">_Motivé_</span><span class="sxs-lookup"><span data-stu-id="c9b7a-119">_cEnt_</span></span>
  
> <span data-ttu-id="c9b7a-120">remarquer Nombre de dossiers désynchronisés.</span><span class="sxs-lookup"><span data-stu-id="c9b7a-120">[out] Number of folders that are out of sync.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9b7a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9b7a-121">See also</span></span>

- [<span data-ttu-id="c9b7a-122">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="c9b7a-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="c9b7a-123">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="c9b7a-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="c9b7a-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="c9b7a-124">MAPI Constants</span></span>](mapi-constants.md)

