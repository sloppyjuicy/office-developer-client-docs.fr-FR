---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8e8a6ac07e14af52337b6e280fa58274df453c65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412743"
---
# <a name="getdefcachedmode"></a><span data-ttu-id="1f715-103">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="1f715-103">GetDefCachedMode</span></span>

  
  
<span data-ttu-id="1f715-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f715-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f715-105">Indique si le mode Exchange mis en cache pour la Banque d'information privée est activé et s'il est appliqué par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="1f715-105">Indicates whether Cached Exchange Mode for the private Exchange store is enabled, and whether this is enforced by policy.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1f715-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="1f715-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f715-107">Exporté par:</span><span class="sxs-lookup"><span data-stu-id="1f715-107">Exported by:</span></span>  <br/> |<span data-ttu-id="1f715-108">msmapi32. dll</span><span class="sxs-lookup"><span data-stu-id="1f715-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="1f715-109">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="1f715-109">Called by:</span></span>  <br/> |<span data-ttu-id="1f715-110">Client</span><span class="sxs-lookup"><span data-stu-id="1f715-110">Client</span></span>  <br/> |
|<span data-ttu-id="1f715-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="1f715-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="1f715-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="1f715-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="1f715-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f715-113">Parameters</span></span>

 <span data-ttu-id="1f715-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="1f715-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="1f715-115">remarquer **true** si la valeur de retour est appliquée par stratégie, **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1f715-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="1f715-116">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="1f715-116">Return values</span></span>

 <span data-ttu-id="1f715-117">**a**</span><span class="sxs-lookup"><span data-stu-id="1f715-117">**true**</span></span>
  
- <span data-ttu-id="1f715-118">La mise en cache est activée.</span><span class="sxs-lookup"><span data-stu-id="1f715-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="1f715-119">**true**</span><span class="sxs-lookup"><span data-stu-id="1f715-119">**false**</span></span>
  
- <span data-ttu-id="1f715-120">La mise en cache est désactivée.</span><span class="sxs-lookup"><span data-stu-id="1f715-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f715-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f715-121">See also</span></span>



[<span data-ttu-id="1f715-122">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="1f715-122">GetDefCachedModeDownloadPubFoldFavs</span></span>](getdefcachedmodedownloadpubfoldfavs.md)

