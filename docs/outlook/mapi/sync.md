---
title: SYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f07fddf-4c42-6ea7-162d-57022166a83f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a40046a26efe118e48cdca4749d2e99212bb8bfe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579840"
---
# <a name="sync"></a><span data-ttu-id="2aea5-103">SYNC</span><span class="sxs-lookup"><span data-stu-id="2aea5-103">SYNC</span></span>

  
  
<span data-ttu-id="2aea5-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2aea5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2aea5-105">Informations de démarrage de la synchronisation entre un magasin local et un serveur.</span><span class="sxs-lookup"><span data-stu-id="2aea5-105">Information for starting synchronization between a local store and a server.</span></span> <span data-ttu-id="2aea5-106">Ces informations sont utilisées lors de l' [état de synchronisation](synchronize-state.md).</span><span class="sxs-lookup"><span data-stu-id="2aea5-106">This information is used during the [synchronize state](synchronize-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2aea5-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="2aea5-107">Quick info</span></span>

```cpp
struct SYNC 
{ 
    ULONG ulFlags; 
    LPWSTR pwzPath; 
    FEID Reserved1; 
    MEID Reserved2; 
    LPENTRYLIST pel; 
    ULONG const * pulFolderOptions; 
};
```

## <a name="members"></a><span data-ttu-id="2aea5-108">Members</span><span class="sxs-lookup"><span data-stu-id="2aea5-108">Members</span></span>

 <span data-ttu-id="2aea5-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2aea5-109">_ulFlags_</span></span>
  
- <span data-ttu-id="2aea5-110">[out] / [in] un masque de bits des indicateurs suivants qui modifie le comportement lors de la synchronisation :</span><span class="sxs-lookup"><span data-stu-id="2aea5-110">[out]/[in] A bitmask of the following flags that modifies the behavior during synchronization:</span></span>
    
- <span data-ttu-id="2aea5-111">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="2aea5-111">UPS_UPLOAD_ONLY</span></span>
    
  - <span data-ttu-id="2aea5-112">[in] Le client effectueront téléchargement uniquement.</span><span class="sxs-lookup"><span data-stu-id="2aea5-112">[in] The client will be performing only upload.</span></span> <span data-ttu-id="2aea5-113">Outlook ne renvoie que les dossiers modifiés localement.</span><span class="sxs-lookup"><span data-stu-id="2aea5-113">Outlook only returns locally modified folders.</span></span>
    
- <span data-ttu-id="2aea5-114">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="2aea5-114">UPS_DNLOAD_ONLY</span></span>
    
  - <span data-ttu-id="2aea5-115">[in] Le client effectueront téléchargement uniquement.</span><span class="sxs-lookup"><span data-stu-id="2aea5-115">[in] The client will be performing only download.</span></span> <span data-ttu-id="2aea5-116">Outlook ne doit pas effacer les bits de téléchargement des dossiers.</span><span class="sxs-lookup"><span data-stu-id="2aea5-116">Outlook should not clear upload bits for folders.</span></span>
    
- <span data-ttu-id="2aea5-117">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="2aea5-117">UPS_THESE_FOLDERS</span></span>
    
  - <span data-ttu-id="2aea5-118">[in] Le client sera synchroniser un ensemble spécifié de dossiers avec l’identificateur d’entrée fourni.</span><span class="sxs-lookup"><span data-stu-id="2aea5-118">[in] The client will be synchronizing a specified set of folders with the provided entry IDs.</span></span> <span data-ttu-id="2aea5-119">Cet indicateur peut être combiné avec indicateur le **UPS_UPLOAD_ONLY** ou **UPS_DNLOAD_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="2aea5-119">This flag can be combined with either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> 
    
- <span data-ttu-id="2aea5-120">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="2aea5-120">UPS_OK</span></span>
    
  - <span data-ttu-id="2aea5-121">[out] La synchronisation a réussi.</span><span class="sxs-lookup"><span data-stu-id="2aea5-121">[out] Synchronization was successful.</span></span> <span data-ttu-id="2aea5-122">Le client définit ce après avoir téléchargé ou une synchronisation complète est terminée.</span><span class="sxs-lookup"><span data-stu-id="2aea5-122">The client sets this after uploading or a full synchronization completes.</span></span>
    
- 
    
    > [!NOTE]
    > <span data-ttu-id="2aea5-123">Même si le client peut télécharger ou synchroniser entièrement (télécharger, puis téléchargez) des dossiers et des éléments avec l’API de réplication, le client spécifie *ulFlags* avec uniquement un sens de la réplication à la fois, **UPS_UPLOAD_ONLY** ou Indicateur **UPS_DNLOAD_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="2aea5-123">Even though the client can either upload or fully synchronize (upload then download) folders and items with the Replication API, the client specifies  *ulFlags*  with only one direction of the replication at a time — either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> <span data-ttu-id="2aea5-124">Dans le cas d’une synchronisation complète, le client effectue tout d’abord un téléchargement avec l’indicateur **UPS_UPLOAD_ONLY** , puis un téléchargement avec l’indicateur **UPS_DNLOAD_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="2aea5-124">In the case of a full synchronization, the client first does an upload with the **UPS_UPLOAD_ONLY** flag, and then a download with the **UPS_DNLOAD_ONLY** flag.</span></span> 
  
 <span data-ttu-id="2aea5-125">_pwzPath_</span><span class="sxs-lookup"><span data-stu-id="2aea5-125">_pwzPath_</span></span>
  
- <span data-ttu-id="2aea5-126">[out] Chemin d’accès dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="2aea5-126">[out] Path to the local store.</span></span>
    
 <span data-ttu-id="2aea5-127">_Reserved1_</span><span class="sxs-lookup"><span data-stu-id="2aea5-127">_Reserved1_</span></span>
  
- <span data-ttu-id="2aea5-128">Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2aea5-128">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="2aea5-129">_Reserved2_</span><span class="sxs-lookup"><span data-stu-id="2aea5-129">_Reserved2_</span></span>
  
- <span data-ttu-id="2aea5-130">Ce membre est réservé à un usage interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2aea5-130">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="2aea5-131">*PEL*</span><span class="sxs-lookup"><span data-stu-id="2aea5-131">*pel*</span></span> 
  
- <span data-ttu-id="2aea5-132">[in] Il s’agit de la liste des identificateurs d’entrée de dossiers à synchroniser si **UPS_THESE_FOLDERS** a été définie.</span><span class="sxs-lookup"><span data-stu-id="2aea5-132">[in] This is the list of entry IDs of the folders to synchronize if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="2aea5-133">Voir mapidefs.h pour la définition du type de **LPENTRYLIST**.</span><span class="sxs-lookup"><span data-stu-id="2aea5-133">See mapidefs.h for the type definition of **LPENTRYLIST**.</span></span> 
    
 <span data-ttu-id="2aea5-134">_pulFolderOptions_</span><span class="sxs-lookup"><span data-stu-id="2aea5-134">_pulFolderOptions_</span></span>
  
- <span data-ttu-id="2aea5-135">[in] Il s’agit d’un tableau des options de dossier pour les dossiers correspondants dans *pel* si **UPS_THESE_FOLDERS** a été définie.</span><span class="sxs-lookup"><span data-stu-id="2aea5-135">[in] This is an array of folder options for corresponding folders in  *pel*  if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="2aea5-136">Ces options de dossier sont utilisées lors du téléchargement de chacun des dossiers répertoriés dans *pel* au cours de l' [état du dossier de téléchargement](upload-folder-state.md).</span><span class="sxs-lookup"><span data-stu-id="2aea5-136">These folder options are used when uploading each of the folders listed in  *pel*  during the [upload folder state](upload-folder-state.md).</span></span> <span data-ttu-id="2aea5-137">Pour plus d’informations sur les options du dossier, voir **[UPFLD](upfld.md)**.</span><span class="sxs-lookup"><span data-stu-id="2aea5-137">For more information about folder options, see **[UPFLD](upfld.md)**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2aea5-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2aea5-138">See also</span></span>



[<span data-ttu-id="2aea5-139">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="2aea5-139">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="2aea5-140">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="2aea5-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="2aea5-141">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="2aea5-141">MAPI Constants</span></span>](mapi-constants.md)

