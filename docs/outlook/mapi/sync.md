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
ms.openlocfilehash: e856044a1b6345c4e495a75dfb7ca0defa52ceec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433807"
---
# <a name="sync"></a><span data-ttu-id="a8a37-103">SYNC</span><span class="sxs-lookup"><span data-stu-id="a8a37-103">SYNC</span></span>

  
  
<span data-ttu-id="a8a37-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8a37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8a37-105">Informations de démarrage de la synchronisation entre un magasin local et un serveur.</span><span class="sxs-lookup"><span data-stu-id="a8a37-105">Information for starting synchronization between a local store and a server.</span></span> <span data-ttu-id="a8a37-106">Ces informations sont utilisées pendant [l’état de synchronisation.](synchronize-state.md)</span><span class="sxs-lookup"><span data-stu-id="a8a37-106">This information is used during the [synchronize state](synchronize-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a8a37-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="a8a37-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="a8a37-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a8a37-108">Members</span></span>

 <span data-ttu-id="a8a37-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a8a37-109">_ulFlags_</span></span>
  
- <span data-ttu-id="a8a37-110">[out]/[in] Masque de bits des indicateurs suivants qui modifie le comportement lors de la synchronisation :</span><span class="sxs-lookup"><span data-stu-id="a8a37-110">[out]/[in] A bitmask of the following flags that modifies the behavior during synchronization:</span></span>
    
- <span data-ttu-id="a8a37-111">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="a8a37-111">UPS_UPLOAD_ONLY</span></span>
    
  - <span data-ttu-id="a8a37-112">[in] Le client effectue uniquement le chargement.</span><span class="sxs-lookup"><span data-stu-id="a8a37-112">[in] The client will be performing only upload.</span></span> <span data-ttu-id="a8a37-113">Outlook renvoie uniquement les dossiers modifiés localement.</span><span class="sxs-lookup"><span data-stu-id="a8a37-113">Outlook only returns locally modified folders.</span></span>
    
- <span data-ttu-id="a8a37-114">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="a8a37-114">UPS_DNLOAD_ONLY</span></span>
    
  - <span data-ttu-id="a8a37-115">[in] Le client effectue uniquement le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="a8a37-115">[in] The client will be performing only download.</span></span> <span data-ttu-id="a8a37-116">Outlook ne doit pas effacer les bits de chargement pour les dossiers.</span><span class="sxs-lookup"><span data-stu-id="a8a37-116">Outlook should not clear upload bits for folders.</span></span>
    
- <span data-ttu-id="a8a37-117">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="a8a37-117">UPS_THESE_FOLDERS</span></span>
    
  - <span data-ttu-id="a8a37-118">[in] Le client synchronisera un ensemble spécifié de dossiers avec les ID d’entrée fournis.</span><span class="sxs-lookup"><span data-stu-id="a8a37-118">[in] The client will be synchronizing a specified set of folders with the provided entry IDs.</span></span> <span data-ttu-id="a8a37-119">Cet indicateur peut être combiné avec **l’UPS_UPLOAD_ONLY** ou **UPS_DNLOAD_ONLY’indicateur.**</span><span class="sxs-lookup"><span data-stu-id="a8a37-119">This flag can be combined with either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> 
    
- <span data-ttu-id="a8a37-120">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="a8a37-120">UPS_OK</span></span>
    
  - <span data-ttu-id="a8a37-121">[out] La synchronisation a réussi.</span><span class="sxs-lookup"><span data-stu-id="a8a37-121">[out] Synchronization was successful.</span></span> <span data-ttu-id="a8a37-122">Le client définit cela une fois le téléchargement ou une synchronisation complète terminée.</span><span class="sxs-lookup"><span data-stu-id="a8a37-122">The client sets this after uploading or a full synchronization completes.</span></span>
    
- 
    
    > [!NOTE]
    > <span data-ttu-id="a8a37-123">Même si le client peut charger ou synchroniser entièrement (télécharger puis télécharger) des dossiers et des éléments avec l’API de réplication, le client spécifie les *ulFlags* avec un seul sens de la réplication à la fois ( l’indicateur **UPS_UPLOAD_ONLY** ou **UPS_DNLOAD_ONLY).**</span><span class="sxs-lookup"><span data-stu-id="a8a37-123">Even though the client can either upload or fully synchronize (upload then download) folders and items with the Replication API, the client specifies  *ulFlags*  with only one direction of the replication at a time — either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> <span data-ttu-id="a8a37-124">Dans le cas d’une synchronisation complète, le client fait d’abord un chargement avec l’indicateur **UPS_UPLOAD_ONLY,** puis un téléchargement avec **l’indicateur UPS_DNLOAD_ONLY.**</span><span class="sxs-lookup"><span data-stu-id="a8a37-124">In the case of a full synchronization, the client first does an upload with the **UPS_UPLOAD_ONLY** flag, and then a download with the **UPS_DNLOAD_ONLY** flag.</span></span> 
  
 <span data-ttu-id="a8a37-125">_pwzPath_</span><span class="sxs-lookup"><span data-stu-id="a8a37-125">_pwzPath_</span></span>
  
- <span data-ttu-id="a8a37-126">[out] Chemin d’accès au magasin local.</span><span class="sxs-lookup"><span data-stu-id="a8a37-126">[out] Path to the local store.</span></span>
    
 <span data-ttu-id="a8a37-127">_Reserved1_</span><span class="sxs-lookup"><span data-stu-id="a8a37-127">_Reserved1_</span></span>
  
- <span data-ttu-id="a8a37-128">Ce membre est réservé à l’utilisation interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a8a37-128">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="a8a37-129">_Reserved2_</span><span class="sxs-lookup"><span data-stu-id="a8a37-129">_Reserved2_</span></span>
  
- <span data-ttu-id="a8a37-130">Ce membre est réservé à l’utilisation interne d’Outlook et n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a8a37-130">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="a8a37-131">*pel*</span><span class="sxs-lookup"><span data-stu-id="a8a37-131">*pel*</span></span> 
  
- <span data-ttu-id="a8a37-132">[in] Il s’agit de la liste des ID d’entrée des dossiers à synchroniser si **UPS_THESE_FOLDERS** a été définie.</span><span class="sxs-lookup"><span data-stu-id="a8a37-132">[in] This is the list of entry IDs of the folders to synchronize if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="a8a37-133">Voir mapidefs.h pour la définition de type **de LPENTRYLIST**.</span><span class="sxs-lookup"><span data-stu-id="a8a37-133">See mapidefs.h for the type definition of **LPENTRYLIST**.</span></span> 
    
 <span data-ttu-id="a8a37-134">_ErrsFolderOptions_</span><span class="sxs-lookup"><span data-stu-id="a8a37-134">_pulFolderOptions_</span></span>
  
- <span data-ttu-id="a8a37-135">[in] Il s’agit d’un tableau d’options de dossier pour les dossiers correspondants dans  *pel* **si UPS_THESE_FOLDERS** a été définie.</span><span class="sxs-lookup"><span data-stu-id="a8a37-135">[in] This is an array of folder options for corresponding folders in  *pel*  if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="a8a37-136">Ces options de dossier sont utilisées lors du téléchargement de chacun des dossiers répertoriés dans *pel* pendant l’état [de chargement du dossier.](upload-folder-state.md)</span><span class="sxs-lookup"><span data-stu-id="a8a37-136">These folder options are used when uploading each of the folders listed in  *pel*  during the [upload folder state](upload-folder-state.md).</span></span> <span data-ttu-id="a8a37-137">Pour plus d’informations sur les options de dossier, **[voir UPFLD](upfld.md)**.</span><span class="sxs-lookup"><span data-stu-id="a8a37-137">For more information about folder options, see **[UPFLD](upfld.md)**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a8a37-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8a37-138">See also</span></span>



[<span data-ttu-id="a8a37-139">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="a8a37-139">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="a8a37-140">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="a8a37-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="a8a37-141">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="a8a37-141">MAPI Constants</span></span>](mapi-constants.md)

