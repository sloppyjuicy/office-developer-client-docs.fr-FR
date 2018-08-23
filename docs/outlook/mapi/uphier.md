---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a1ec71d7120eab220ee3b11d2a751fba51cee48e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592093"
---
# <a name="uphier"></a><span data-ttu-id="af847-103">UPHIER</span><span class="sxs-lookup"><span data-stu-id="af847-103">UPHIER</span></span>
 
<span data-ttu-id="af847-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af847-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af847-105">Informations pour la synchronisation d’une hiérarchie de dossiers au cours de l' [état de la hiérarchie de télécharger](upload-hierarchy-state.md).</span><span class="sxs-lookup"><span data-stu-id="af847-105">Information for synchronizing a folder hierarchy during the [upload hierarchy state](upload-hierarchy-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="af847-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="af847-106">Quick info</span></span>

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="af847-107">Members</span><span class="sxs-lookup"><span data-stu-id="af847-107">Members</span></span>

<span data-ttu-id="af847-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="af847-108">_ulFlags_</span></span>
  
> <span data-ttu-id="af847-109">[in] Indicateurs pour modifier le comportement lors de la synchronisation de la hiérarchie de dossiers.</span><span class="sxs-lookup"><span data-stu-id="af847-109">[in] Flags to modify the behavior when synchronizing the folder hierarchy.</span></span>
    
  - <span data-ttu-id="af847-110">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="af847-110">UPH_OK</span></span>
    
    - <span data-ttu-id="af847-111">[in] Téléchargement a réussi.</span><span class="sxs-lookup"><span data-stu-id="af847-111">[in] Upload was successful.</span></span> <span data-ttu-id="af847-112">Le client définit après avoir téléchargé correctement les informations sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="af847-112">The client sets this after successfully uploading information to the server.</span></span> <span data-ttu-id="af847-113">À l’affichage de cet indicateur, Outlook efface toutes les informations de référence interne qui indique la hiérarchie de dossiers nécessaire de mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="af847-113">Upon seeing this flag, Outlook clears any internal bookkeeping information that indicated the folder hierarchy needed updating.</span></span> 
    
    - <span data-ttu-id="af847-114">Le client transmet le HRESULT si le transfert n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="af847-114">The client passes the HRESULT if the upload was not successful.</span></span>
    
<span data-ttu-id="af847-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="af847-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="af847-116">[out] Ce membre est réservé à un usage interne Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="af847-116">[out] This member is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="af847-117">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="af847-117">_iEnt_</span></span>
  
> <span data-ttu-id="af847-118">[out] Index pour effectuer le suivi de la synchronisation du nombre de dossiers spécifiée par *cEnt* .</span><span class="sxs-lookup"><span data-stu-id="af847-118">[out] Index to track synchronizing the number of folders specified by  *cEnt*  .</span></span> 
    
<span data-ttu-id="af847-119">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="af847-119">_cEnt_</span></span>
  
> <span data-ttu-id="af847-120">[out] Nombre de dossiers qui ne sont pas synchronisés.</span><span class="sxs-lookup"><span data-stu-id="af847-120">[out] Number of folders that are out of sync.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af847-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af847-121">See also</span></span>

- [<span data-ttu-id="af847-122">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="af847-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="af847-123">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="af847-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="af847-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="af847-124">MAPI Constants</span></span>](mapi-constants.md)

