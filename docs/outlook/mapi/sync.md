---
title: SYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f07fddf-4c42-6ea7-162d-57022166a83f
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: e856044a1b6345c4e495a75dfb7ca0defa52ceec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349594"
---
# <a name="sync"></a><span data-ttu-id="d261e-103">SYNC</span><span class="sxs-lookup"><span data-stu-id="d261e-103">SYNC</span></span>

  
  
<span data-ttu-id="d261e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d261e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d261e-105">Informations pour le démarrage de la synchronisation entre un magasin local et un serveur.</span><span class="sxs-lookup"><span data-stu-id="d261e-105">Information for starting synchronization between a local store and a server.</span></span> <span data-ttu-id="d261e-106">Ces informations sont utilisées lors de l' [État Synchronize](synchronize-state.md).</span><span class="sxs-lookup"><span data-stu-id="d261e-106">This information is used during the [synchronize state](synchronize-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d261e-107">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="d261e-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="d261e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d261e-108">Members</span></span>

 <span data-ttu-id="d261e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d261e-109">_ulFlags_</span></span>
  
- <span data-ttu-id="d261e-110">[out]/[in] masque de masque des indicateurs suivants qui modifie le comportement lors de la synchronisation:</span><span class="sxs-lookup"><span data-stu-id="d261e-110">[out]/[in] A bitmask of the following flags that modifies the behavior during synchronization:</span></span>
    
- <span data-ttu-id="d261e-111">UPS_UPLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="d261e-111">UPS_UPLOAD_ONLY</span></span>
    
  - <span data-ttu-id="d261e-112">dans Le client effectuera uniquement le chargement.</span><span class="sxs-lookup"><span data-stu-id="d261e-112">[in] The client will be performing only upload.</span></span> <span data-ttu-id="d261e-113">Outlook retourne uniquement les dossiers modifiés localement.</span><span class="sxs-lookup"><span data-stu-id="d261e-113">Outlook only returns locally modified folders.</span></span>
    
- <span data-ttu-id="d261e-114">UPS_DNLOAD_ONLY</span><span class="sxs-lookup"><span data-stu-id="d261e-114">UPS_DNLOAD_ONLY</span></span>
    
  - <span data-ttu-id="d261e-115">dans Le client effectue uniquement un téléchargement.</span><span class="sxs-lookup"><span data-stu-id="d261e-115">[in] The client will be performing only download.</span></span> <span data-ttu-id="d261e-116">Outlook ne doit pas effacer les bits de téléchargement pour les dossiers.</span><span class="sxs-lookup"><span data-stu-id="d261e-116">Outlook should not clear upload bits for folders.</span></span>
    
- <span data-ttu-id="d261e-117">UPS_THESE_FOLDERS</span><span class="sxs-lookup"><span data-stu-id="d261e-117">UPS_THESE_FOLDERS</span></span>
    
  - <span data-ttu-id="d261e-118">dans Le client synchronise un ensemble spécifié de dossiers avec les ID d'entrée fournis.</span><span class="sxs-lookup"><span data-stu-id="d261e-118">[in] The client will be synchronizing a specified set of folders with the provided entry IDs.</span></span> <span data-ttu-id="d261e-119">Cet indicateur peut être combiné avec l'indicateur **UPS_UPLOAD_ONLY** ou **UPS_DNLOAD_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="d261e-119">This flag can be combined with either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> 
    
- <span data-ttu-id="d261e-120">UPS_OK</span><span class="sxs-lookup"><span data-stu-id="d261e-120">UPS_OK</span></span>
    
  - <span data-ttu-id="d261e-121">remarquer La synchronisation a réussi.</span><span class="sxs-lookup"><span data-stu-id="d261e-121">[out] Synchronization was successful.</span></span> <span data-ttu-id="d261e-122">Le client définit ceci après le téléchargement ou une synchronisation complète.</span><span class="sxs-lookup"><span data-stu-id="d261e-122">The client sets this after uploading or a full synchronization completes.</span></span>
    
- 
    
    > [!NOTE]
    > <span data-ttu-id="d261e-123">Même si le client peut télécharger des dossiers et des éléments avec l'API de réPlication ou les synchroniser entièrement (télécharger et télécharger), le client spécifie *ulFlags* avec une seule direction de la réplication à la fois, à savoir le **UPS_UPLOAD_ONLY** ou Indicateur **UPS_DNLOAD_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="d261e-123">Even though the client can either upload or fully synchronize (upload then download) folders and items with the Replication API, the client specifies  *ulFlags*  with only one direction of the replication at a time — either the **UPS_UPLOAD_ONLY** or **UPS_DNLOAD_ONLY** flag.</span></span> <span data-ttu-id="d261e-124">Dans le cas d'une synchronisation complète, le client effectue d'abord un chargement avec l'indicateur **UPS_UPLOAD_ONLY** , puis un téléchargement avec l'indicateur **UPS_DNLOAD_ONLY** .</span><span class="sxs-lookup"><span data-stu-id="d261e-124">In the case of a full synchronization, the client first does an upload with the **UPS_UPLOAD_ONLY** flag, and then a download with the **UPS_DNLOAD_ONLY** flag.</span></span> 
  
 <span data-ttu-id="d261e-125">_pwzPath_</span><span class="sxs-lookup"><span data-stu-id="d261e-125">_pwzPath_</span></span>
  
- <span data-ttu-id="d261e-126">remarquer Chemin d'accès au magasin local.</span><span class="sxs-lookup"><span data-stu-id="d261e-126">[out] Path to the local store.</span></span>
    
 <span data-ttu-id="d261e-127">_Reserved1_</span><span class="sxs-lookup"><span data-stu-id="d261e-127">_Reserved1_</span></span>
  
- <span data-ttu-id="d261e-128">Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d261e-128">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="d261e-129">_Reserved2_</span><span class="sxs-lookup"><span data-stu-id="d261e-129">_Reserved2_</span></span>
  
- <span data-ttu-id="d261e-130">Ce membre est réservé à l'usage interne d'Outlook et n'est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d261e-130">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="d261e-131">*PEL*</span><span class="sxs-lookup"><span data-stu-id="d261e-131">*pel*</span></span> 
  
- <span data-ttu-id="d261e-132">dans Il s'agit de la liste des identificateurs d'entrée des dossiers à synchroniser si **UPS_THESE_FOLDERS** a été défini.</span><span class="sxs-lookup"><span data-stu-id="d261e-132">[in] This is the list of entry IDs of the folders to synchronize if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="d261e-133">Voir mapidefs. h pour la définition de type de **LPENTRYLIST**.</span><span class="sxs-lookup"><span data-stu-id="d261e-133">See mapidefs.h for the type definition of **LPENTRYLIST**.</span></span> 
    
 <span data-ttu-id="d261e-134">_pulFolderOptions_</span><span class="sxs-lookup"><span data-stu-id="d261e-134">_pulFolderOptions_</span></span>
  
- <span data-ttu-id="d261e-135">dans Il s'agit d'un tableau d'options de dossier pour les dossiers correspondants dans *PEL* si **UPS_THESE_FOLDERS** a été défini.</span><span class="sxs-lookup"><span data-stu-id="d261e-135">[in] This is an array of folder options for corresponding folders in  *pel*  if **UPS_THESE_FOLDERS** has been set.</span></span> <span data-ttu-id="d261e-136">Ces options de dossiers sont utilisées lors du téléchargement de chaque dossier répertorié dans *PEL* lors de l' [État du dossier de chargement](upload-folder-state.md).</span><span class="sxs-lookup"><span data-stu-id="d261e-136">These folder options are used when uploading each of the folders listed in  *pel*  during the [upload folder state](upload-folder-state.md).</span></span> <span data-ttu-id="d261e-137">Pour plus d'informations sur les options des dossiers, voir **[UPFLD](upfld.md)**.</span><span class="sxs-lookup"><span data-stu-id="d261e-137">For more information about folder options, see **[UPFLD](upfld.md)**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d261e-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d261e-138">See also</span></span>



[<span data-ttu-id="d261e-139">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="d261e-139">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="d261e-140">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="d261e-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="d261e-141">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="d261e-141">MAPI Constants</span></span>](mapi-constants.md)

