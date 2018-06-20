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
ms.openlocfilehash: 7595fac4346a537eed86550432f56a761c27c0ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783436"
---
# <a name="getdefcachedmode"></a><span data-ttu-id="e5bd0-103">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="e5bd0-103">GetDefCachedMode</span></span>

  
  
<span data-ttu-id="e5bd0-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e5bd0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e5bd0-105">Indique si le Mode Exchange mis en cache pour la banque Exchange privée est activé, et si cela est appliqué par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="e5bd0-105">Indicates whether Cached Exchange Mode for the private Exchange store is enabled, and whether this is enforced by policy.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e5bd0-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="e5bd0-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5bd0-107">Exportés par :</span><span class="sxs-lookup"><span data-stu-id="e5bd0-107">Exported by:</span></span>  <br/> |<span data-ttu-id="e5bd0-108">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="e5bd0-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="e5bd0-109">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="e5bd0-109">Called by:</span></span>  <br/> |<span data-ttu-id="e5bd0-110">Client</span><span class="sxs-lookup"><span data-stu-id="e5bd0-110">Client</span></span>  <br/> |
|<span data-ttu-id="e5bd0-111">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="e5bd0-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="e5bd0-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="e5bd0-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="e5bd0-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5bd0-113">Parameters</span></span>

 <span data-ttu-id="e5bd0-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="e5bd0-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="e5bd0-115">[out] **true** si la valeur de retour est appliquée par la stratégie, **false** si elle n’est pas.</span><span class="sxs-lookup"><span data-stu-id="e5bd0-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="e5bd0-116">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="e5bd0-116">Return values</span></span>

 <span data-ttu-id="e5bd0-117">**valeur True**</span><span class="sxs-lookup"><span data-stu-id="e5bd0-117">**true**</span></span>
  
- <span data-ttu-id="e5bd0-118">La mise en cache est activé.</span><span class="sxs-lookup"><span data-stu-id="e5bd0-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="e5bd0-119">**False**</span><span class="sxs-lookup"><span data-stu-id="e5bd0-119">**false**</span></span>
  
- <span data-ttu-id="e5bd0-120">La mise en cache est désactivée.</span><span class="sxs-lookup"><span data-stu-id="e5bd0-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e5bd0-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5bd0-121">See also</span></span>



[<span data-ttu-id="e5bd0-122">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="e5bd0-122">GetDefCachedModeDownloadPubFoldFavs</span></span>](getdefcachedmodedownloadpubfoldfavs.md)

