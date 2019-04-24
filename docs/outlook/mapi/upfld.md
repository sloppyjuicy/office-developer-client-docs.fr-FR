---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: c8f7bdc5864c049d8db6f38e92a69c97b6f9dc73
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360479"
---
# <a name="upfld"></a><span data-ttu-id="8f2eb-103">UPFLD</span><span class="sxs-lookup"><span data-stu-id="8f2eb-103">UPFLD</span></span>

<span data-ttu-id="8f2eb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f2eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f2eb-105">Informations pour le téléchargement d'un dossier lors de l' [État du dossier de chargement](upload-folder-state.md).</span><span class="sxs-lookup"><span data-stu-id="8f2eb-105">Information for uploading a folder during the [upload folder state](upload-folder-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8f2eb-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="8f2eb-106">Quick info</span></span>

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a><span data-ttu-id="8f2eb-107">Membres</span><span class="sxs-lookup"><span data-stu-id="8f2eb-107">Members</span></span>

<span data-ttu-id="8f2eb-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8f2eb-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="8f2eb-109">[out]/[in] indicateurs pour déterminer les actions appropriées pour le uplaod.</span><span class="sxs-lookup"><span data-stu-id="8f2eb-109">[out]/[in] Flags to determine appropriate actions for the uplaod.</span></span> 
    
  - <span data-ttu-id="8f2eb-110">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="8f2eb-110">UPF_NEW</span></span>
    
    - <span data-ttu-id="8f2eb-111">remarquer Le dossier est nouveau.</span><span class="sxs-lookup"><span data-stu-id="8f2eb-111">[out] Folder is new.</span></span>
    
  - <span data-ttu-id="8f2eb-112">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="8f2eb-112">UPF_MOD_PARENT</span></span>
    
    - <span data-ttu-id="8f2eb-113">remarquer Le dossier a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="8f2eb-113">[out] Folder has been moved.</span></span>
    
  - <span data-ttu-id="8f2eb-114">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="8f2eb-114">UPF_MOD_PROPS</span></span>
    
    - <span data-ttu-id="8f2eb-115">remarquer Les propriétés du dossier ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="8f2eb-115">[out] Folder properties have been modified.</span></span>
    
  - <span data-ttu-id="8f2eb-116">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="8f2eb-116">UPF_DEL</span></span>
    
    - <span data-ttu-id="8f2eb-117">remarquer Le dossier a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="8f2eb-117">[out] Folder was deleted.</span></span>
    
  - <span data-ttu-id="8f2eb-118">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="8f2eb-118">UPF_OK</span></span>
    
    - <span data-ttu-id="8f2eb-119">dans Le chargement a réussi.</span><span class="sxs-lookup"><span data-stu-id="8f2eb-119">[in] Upload was successful.</span></span> <span data-ttu-id="8f2eb-120">Le client le définit après avoir téléchargé les informations de dossier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="8f2eb-120">The client sets this after uploading folder information to the server.</span></span>
    
<span data-ttu-id="8f2eb-121">_pfld_</span><span class="sxs-lookup"><span data-stu-id="8f2eb-121">_pfld_</span></span>
  
> <span data-ttu-id="8f2eb-122">remarquer Objet Folder ouvert à télécharger.</span><span class="sxs-lookup"><span data-stu-id="8f2eb-122">[out] The open folder object to upload.</span></span>
    
<span data-ttu-id="8f2eb-123">_feid_</span><span class="sxs-lookup"><span data-stu-id="8f2eb-123">_feid_</span></span>
  
> <span data-ttu-id="8f2eb-124">[sortant] ID d’entrée du dossier.</span><span class="sxs-lookup"><span data-stu-id="8f2eb-124">[out] Entry ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8f2eb-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f2eb-125">See also</span></span>

- [<span data-ttu-id="8f2eb-126">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="8f2eb-126">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="8f2eb-127">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="8f2eb-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="8f2eb-128">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="8f2eb-128">MAPI Constants</span></span>](mapi-constants.md)

