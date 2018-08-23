---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b2523c149d98dacf9ad321a4a443382a39753fd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592338"
---
# <a name="uptble"></a><span data-ttu-id="67665-103">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="67665-103">UPTBLE</span></span>

<span data-ttu-id="67665-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67665-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67665-105">Informations de téléchargement du contenu d’un dossier pendant la [Télécharger l’état de la table](upload-table-state.md)d’étendues.</span><span class="sxs-lookup"><span data-stu-id="67665-105">Extended information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="67665-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="67665-106">Quick info</span></span>

```cpp
struct UPTBLE 
{ 
    UINTiEntMod; 
    UINTcEntMod; 
    UINTiEntRead; 
    UINTcEntRead; 
    UINTiEntDel; 
    UINTcEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="67665-107">Members</span><span class="sxs-lookup"><span data-stu-id="67665-107">Members</span></span>

 <span data-ttu-id="67665-108">_iEntMod_</span><span class="sxs-lookup"><span data-stu-id="67665-108">_iEntMod_</span></span>
  
>  <span data-ttu-id="67665-109">[out] Index pour effectuer le suivi de téléchargement le nombre de _cEntMod_ d’éléments nouveaux ou modifiés.</span><span class="sxs-lookup"><span data-stu-id="67665-109">[out] Index to track uploading the  _cEntMod_ number of new or modified items.</span></span> 
    
 <span data-ttu-id="67665-110">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="67665-110">_cEntMod_</span></span>
  
>  <span data-ttu-id="67665-111">[out] Nombre d’éléments nouveaux ou modifiés dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="67665-111">[out] Number of new or modified items in the folder.</span></span> 
    
 <span data-ttu-id="67665-112">_iEntRead_</span><span class="sxs-lookup"><span data-stu-id="67665-112">_iEntRead_</span></span>
  
>  <span data-ttu-id="67665-113">[out] Pour effectuer le suivi de téléchargement le nombre de _cEntRead_ lire des éléments d’index.</span><span class="sxs-lookup"><span data-stu-id="67665-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span></span> 
    
 <span data-ttu-id="67665-114">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="67665-114">_cEntRead_</span></span>
  
>  <span data-ttu-id="67665-115">[out] Nombre d’éléments lus dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="67665-115">[out] Number of read items in the folder.</span></span> 
    
 <span data-ttu-id="67665-116">_iEntDel_</span><span class="sxs-lookup"><span data-stu-id="67665-116">_iEntDel_</span></span>
  
>  <span data-ttu-id="67665-117">[out] Index pour effectuer le suivi de téléchargement le nombre de _cEntDel_ les éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="67665-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span></span> 
    
 <span data-ttu-id="67665-118">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="67665-118">_cEntDel_</span></span>
  
>  <span data-ttu-id="67665-119">[out] Nombre d’éléments supprimés dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="67665-119">[out] Number of deleted items in the folder.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="67665-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67665-120">See also</span></span>

- [<span data-ttu-id="67665-121">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="67665-121">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="67665-122">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="67665-122">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="67665-123">UPTBL</span><span class="sxs-lookup"><span data-stu-id="67665-123">UPTBL</span></span>](uptbl.md)

