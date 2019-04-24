---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5e623c9d40ffd2dd276bd9601676244644bb3402
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299887"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a><span data-ttu-id="19dc5-103">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="19dc5-103">GetDefCachedModeDownloadPubFoldFavs</span></span>

  
  
<span data-ttu-id="19dc5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19dc5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19dc5-105">Indique si le mode Exchange mis en cache pour le dossier **public favoris** est activé, et s'il est appliqué par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="19dc5-105">Indicates whether Cached Exchange Mode for the **Public Folder Favorites** folder is enabled, and whether this is enforced by policy.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="19dc5-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="19dc5-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19dc5-107">Exporté par:</span><span class="sxs-lookup"><span data-stu-id="19dc5-107">Exported by:</span></span>  <br/> |<span data-ttu-id="19dc5-108">msmapi32. dll</span><span class="sxs-lookup"><span data-stu-id="19dc5-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="19dc5-109">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="19dc5-109">Called by:</span></span>  <br/> |<span data-ttu-id="19dc5-110">Client</span><span class="sxs-lookup"><span data-stu-id="19dc5-110">Client</span></span>  <br/> |
|<span data-ttu-id="19dc5-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="19dc5-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="19dc5-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="19dc5-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="19dc5-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19dc5-113">Parameters</span></span>

 <span data-ttu-id="19dc5-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="19dc5-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="19dc5-115">remarquer **true** si la valeur de retour est appliquée par stratégie, **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="19dc5-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="19dc5-116">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="19dc5-116">Return values</span></span>

 <span data-ttu-id="19dc5-117">**true**</span><span class="sxs-lookup"><span data-stu-id="19dc5-117">**true**</span></span>
  
- <span data-ttu-id="19dc5-118">La mise en cache est activée.</span><span class="sxs-lookup"><span data-stu-id="19dc5-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="19dc5-119">**true**</span><span class="sxs-lookup"><span data-stu-id="19dc5-119">**false**</span></span>
  
- <span data-ttu-id="19dc5-120">La mise en cache est désactivée.</span><span class="sxs-lookup"><span data-stu-id="19dc5-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="19dc5-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19dc5-121">See also</span></span>



[<span data-ttu-id="19dc5-122">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="19dc5-122">GetDefCachedMode</span></span>](getdefcachedmode.md)

