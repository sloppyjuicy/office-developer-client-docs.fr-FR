---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8e8a6ac07e14af52337b6e280fa58274df453c65
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299705"
---
# <a name="getdefcachedmode"></a><span data-ttu-id="e0abe-103">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="e0abe-103">GetDefCachedMode</span></span>

  
  
<span data-ttu-id="e0abe-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0abe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0abe-105">Indique si le mode Exchange mis en cache pour la Banque d'information privée est activé et s'il est appliqué par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="e0abe-105">Indicates whether Cached Exchange Mode for the private Exchange store is enabled, and whether this is enforced by policy.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e0abe-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="e0abe-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0abe-107">Exporté par:</span><span class="sxs-lookup"><span data-stu-id="e0abe-107">Exported by:</span></span>  <br/> |<span data-ttu-id="e0abe-108">msmapi32. dll</span><span class="sxs-lookup"><span data-stu-id="e0abe-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="e0abe-109">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="e0abe-109">Called by:</span></span>  <br/> |<span data-ttu-id="e0abe-110">Client</span><span class="sxs-lookup"><span data-stu-id="e0abe-110">Client</span></span>  <br/> |
|<span data-ttu-id="e0abe-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="e0abe-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="e0abe-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="e0abe-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="e0abe-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e0abe-113">Parameters</span></span>

 <span data-ttu-id="e0abe-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="e0abe-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="e0abe-115">remarquer **true** si la valeur de retour est appliquée par stratégie, **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e0abe-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="e0abe-116">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e0abe-116">Return values</span></span>

 <span data-ttu-id="e0abe-117">**true**</span><span class="sxs-lookup"><span data-stu-id="e0abe-117">**true**</span></span>
  
- <span data-ttu-id="e0abe-118">La mise en cache est activée.</span><span class="sxs-lookup"><span data-stu-id="e0abe-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="e0abe-119">**true**</span><span class="sxs-lookup"><span data-stu-id="e0abe-119">**false**</span></span>
  
- <span data-ttu-id="e0abe-120">La mise en cache est désactivée.</span><span class="sxs-lookup"><span data-stu-id="e0abe-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e0abe-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0abe-121">See also</span></span>



[<span data-ttu-id="e0abe-122">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="e0abe-122">GetDefCachedModeDownloadPubFoldFavs</span></span>](getdefcachedmodedownloadpubfoldfavs.md)

