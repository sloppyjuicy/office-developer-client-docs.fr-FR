---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: 'Derni�re modification�: jeudi 5 juillet 2012'
ms.openlocfilehash: 41a61bd05bd511888aeab756166016813f4dceb8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391947"
---
# <a name="dntble"></a><span data-ttu-id="ec52c-103">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="ec52c-103">DNTBLE</span></span>

  
  
<span data-ttu-id="ec52c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec52c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec52c-105">Informations pour le téléchargement du contenu d’un dossier à partir du serveur au cours de l' [état de la table du téléchargement](download-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="ec52c-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md).</span></span> <span data-ttu-id="ec52c-106">Ce processus de téléchargement utilise la synchronisation modification incrémentielle (ICS) de Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="ec52c-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="ec52c-107">Pour plus d’informations sur le partage de connexion Internet, voir [Critères d’évaluation de partage de connexion Internet](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ec52c-107">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ec52c-108">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="ec52c-108">Quick info</span></span>

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="ec52c-109">Members</span><span class="sxs-lookup"><span data-stu-id="ec52c-109">Members</span></span>

 <span data-ttu-id="ec52c-110">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="ec52c-110">_cEntNew_</span></span>
  
> <span data-ttu-id="ec52c-111">[out] Nombre d’éléments ajoutés dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="ec52c-111">[out] Number of items added to the local store.</span></span> <span data-ttu-id="ec52c-112">Outlook remplit cette valeur pendant le téléchargement lors de l’utilisation du partage de connexion Internet.</span><span class="sxs-lookup"><span data-stu-id="ec52c-112">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="ec52c-113">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="ec52c-113">_cEntMod_</span></span>
  
> <span data-ttu-id="ec52c-114">[out] Nombre d’éléments modifiés sur le magasin local.</span><span class="sxs-lookup"><span data-stu-id="ec52c-114">[out] Number of items modified on the local store.</span></span> <span data-ttu-id="ec52c-115">Outlook remplit cette valeur pendant le téléchargement lors de l’utilisation du partage de connexion Internet.</span><span class="sxs-lookup"><span data-stu-id="ec52c-115">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="ec52c-116">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="ec52c-116">_cEntRead_</span></span>
  
> <span data-ttu-id="ec52c-117">[out] Nombre d’éléments de lire ou marqués comme non lu dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="ec52c-117">[out] Number of items read or marked unread on the local store.</span></span> <span data-ttu-id="ec52c-118">Outlook remplit cette valeur pendant le téléchargement lors de l’utilisation du partage de connexion Internet.</span><span class="sxs-lookup"><span data-stu-id="ec52c-118">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="ec52c-119">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="ec52c-119">_cEntDel_</span></span>
  
> <span data-ttu-id="ec52c-120">[out] Nombre d’éléments supprimés dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="ec52c-120">[out] Number of items deleted on the local store.</span></span> <span data-ttu-id="ec52c-121">Outlook remplit cette valeur pendant le téléchargement lors de l’utilisation du partage de connexion Internet.</span><span class="sxs-lookup"><span data-stu-id="ec52c-121">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ec52c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec52c-122">See also</span></span>



[<span data-ttu-id="ec52c-123">À propos de la machine à états de réplication</span><span class="sxs-lookup"><span data-stu-id="ec52c-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="ec52c-124">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="ec52c-124">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="ec52c-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="ec52c-125">DNTBL</span></span>](dntbl.md)

