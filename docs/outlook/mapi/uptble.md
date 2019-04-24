---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: d0b440f01aad7078ed76cd37d36c5ad506215438
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329707"
---
# <a name="uptble"></a><span data-ttu-id="54a42-103">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="54a42-103">UPTBLE</span></span>

<span data-ttu-id="54a42-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54a42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54a42-105">Informations étendues pour le téléchargement du contenu d'un dossier lors de l'état de la [table de chargement](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="54a42-105">Extended information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="54a42-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="54a42-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="54a42-107">Membres</span><span class="sxs-lookup"><span data-stu-id="54a42-107">Members</span></span>

 <span data-ttu-id="54a42-108">_iEntMod_</span><span class="sxs-lookup"><span data-stu-id="54a42-108">_iEntMod_</span></span>
  
>  <span data-ttu-id="54a42-109">remarquer Index permettant de suivre le téléchargement du nombre _cEntMod_ d'éléments nouveaux ou modifiés.</span><span class="sxs-lookup"><span data-stu-id="54a42-109">[out] Index to track uploading the  _cEntMod_ number of new or modified items.</span></span> 
    
 <span data-ttu-id="54a42-110">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="54a42-110">_cEntMod_</span></span>
  
>  <span data-ttu-id="54a42-111">remarquer Nombre d'éléments nouveaux ou modifiés dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="54a42-111">[out] Number of new or modified items in the folder.</span></span> 
    
 <span data-ttu-id="54a42-112">_iEntRead_</span><span class="sxs-lookup"><span data-stu-id="54a42-112">_iEntRead_</span></span>
  
>  <span data-ttu-id="54a42-113">remarquer Index permettant de suivre le téléchargement du nombre d'éléments de lecture _cEntRead_ .</span><span class="sxs-lookup"><span data-stu-id="54a42-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span></span> 
    
 <span data-ttu-id="54a42-114">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="54a42-114">_cEntRead_</span></span>
  
>  <span data-ttu-id="54a42-115">remarquer Nombre d'éléments lus dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="54a42-115">[out] Number of read items in the folder.</span></span> 
    
 <span data-ttu-id="54a42-116">_iEntDel_</span><span class="sxs-lookup"><span data-stu-id="54a42-116">_iEntDel_</span></span>
  
>  <span data-ttu-id="54a42-117">remarquer Index permettant de suivre le téléchargement du nombre d'éléments supprimés _cEntDel_ .</span><span class="sxs-lookup"><span data-stu-id="54a42-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span></span> 
    
 <span data-ttu-id="54a42-118">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="54a42-118">_cEntDel_</span></span>
  
>  <span data-ttu-id="54a42-119">remarquer Nombre d'éléments supprimés dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="54a42-119">[out] Number of deleted items in the folder.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="54a42-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54a42-120">See also</span></span>

- [<span data-ttu-id="54a42-121">À propos de l’API de réplication</span><span class="sxs-lookup"><span data-stu-id="54a42-121">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="54a42-122">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="54a42-122">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="54a42-123">UPTBL</span><span class="sxs-lookup"><span data-stu-id="54a42-123">UPTBL</span></span>](uptbl.md)

