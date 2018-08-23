---
title: UPFLD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6da9d6b6-a016-ccef-77da-3e037c30450d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 34d6eb0653c3eb550bf03242a2c1b2acc3330a13
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572290"
---
# <a name="upfld"></a><span data-ttu-id="c773f-103">UPFLD</span><span class="sxs-lookup"><span data-stu-id="c773f-103">UPFLD</span></span>

<span data-ttu-id="c773f-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c773f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c773f-105">Informations de téléchargement d’un dossier au cours de l' [état du dossier de téléchargement](upload-folder-state.md).</span><span class="sxs-lookup"><span data-stu-id="c773f-105">Information for uploading a folder during the [upload folder state](upload-folder-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c773f-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="c773f-106">Quick info</span></span>

```cpp
struct UPFLD 
{ 
    ULONG ulFlags; 
    LPMAPIFOLDER pfld; 
    FEID feid; 
}; 

```

## <a name="members"></a><span data-ttu-id="c773f-107">Members</span><span class="sxs-lookup"><span data-stu-id="c773f-107">Members</span></span>

<span data-ttu-id="c773f-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c773f-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="c773f-109">[out] / [in] indicateurs pour déterminer les actions appropriées pour l’uplaod.</span><span class="sxs-lookup"><span data-stu-id="c773f-109">[out]/[in] Flags to determine appropriate actions for the uplaod.</span></span> 
    
  - <span data-ttu-id="c773f-110">UPF_NEW</span><span class="sxs-lookup"><span data-stu-id="c773f-110">UPF_NEW</span></span>
    
    - <span data-ttu-id="c773f-111">[out] Dossier est nouveau.</span><span class="sxs-lookup"><span data-stu-id="c773f-111">[out] Folder is new.</span></span>
    
  - <span data-ttu-id="c773f-112">UPF_MOD_PARENT</span><span class="sxs-lookup"><span data-stu-id="c773f-112">UPF_MOD_PARENT</span></span>
    
    - <span data-ttu-id="c773f-113">[out] Dossier a été déplacé.</span><span class="sxs-lookup"><span data-stu-id="c773f-113">[out] Folder has been moved.</span></span>
    
  - <span data-ttu-id="c773f-114">UPF_MOD_PROPS</span><span class="sxs-lookup"><span data-stu-id="c773f-114">UPF_MOD_PROPS</span></span>
    
    - <span data-ttu-id="c773f-115">[out] Les propriétés de dossier ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="c773f-115">[out] Folder properties have been modified.</span></span>
    
  - <span data-ttu-id="c773f-116">UPF_DEL</span><span class="sxs-lookup"><span data-stu-id="c773f-116">UPF_DEL</span></span>
    
    - <span data-ttu-id="c773f-117">[out] Dossier a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="c773f-117">[out] Folder was deleted.</span></span>
    
  - <span data-ttu-id="c773f-118">UPF_OK</span><span class="sxs-lookup"><span data-stu-id="c773f-118">UPF_OK</span></span>
    
    - <span data-ttu-id="c773f-119">[in] Téléchargement a réussi.</span><span class="sxs-lookup"><span data-stu-id="c773f-119">[in] Upload was successful.</span></span> <span data-ttu-id="c773f-120">Le client définit après le téléchargement des informations sur les dossiers sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="c773f-120">The client sets this after uploading folder information to the server.</span></span>
    
<span data-ttu-id="c773f-121">_pfld_</span><span class="sxs-lookup"><span data-stu-id="c773f-121">_pfld_</span></span>
  
> <span data-ttu-id="c773f-122">[out] L’objet d’ouvrir le dossier à télécharger.</span><span class="sxs-lookup"><span data-stu-id="c773f-122">[out] The open folder object to upload.</span></span>
    
<span data-ttu-id="c773f-123">_feid_</span><span class="sxs-lookup"><span data-stu-id="c773f-123">_feid_</span></span>
  
> <span data-ttu-id="c773f-124">[out] ID d’entrée du dossier.</span><span class="sxs-lookup"><span data-stu-id="c773f-124">[out] Entry ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c773f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c773f-125">See also</span></span>

- [<span data-ttu-id="c773f-126">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="c773f-126">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="c773f-127">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="c773f-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="c773f-128">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="c773f-128">MAPI Constants</span></span>](mapi-constants.md)

