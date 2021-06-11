---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5e623c9d40ffd2dd276bd9601676244644bb3402
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417706"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a><span data-ttu-id="2a722-103">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="2a722-103">GetDefCachedModeDownloadPubFoldFavs</span></span>

  
  
<span data-ttu-id="2a722-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a722-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a722-105">Indique si le mode Exchange mis en cache pour le dossier Favoris des **dossiers** publics est activé et si cela est appliqué par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="2a722-105">Indicates whether Cached Exchange Mode for the **Public Folder Favorites** folder is enabled, and whether this is enforced by policy.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="2a722-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="2a722-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a722-107">Exporté par :</span><span class="sxs-lookup"><span data-stu-id="2a722-107">Exported by:</span></span>  <br/> |<span data-ttu-id="2a722-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="2a722-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="2a722-109">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="2a722-109">Called by:</span></span>  <br/> |<span data-ttu-id="2a722-110">Client</span><span class="sxs-lookup"><span data-stu-id="2a722-110">Client</span></span>  <br/> |
|<span data-ttu-id="2a722-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="2a722-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="2a722-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="2a722-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="2a722-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="2a722-113">Parameters</span></span>

 <span data-ttu-id="2a722-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="2a722-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="2a722-115">[out] **true** si la valeur de retour est appliquée par la stratégie, **false** si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="2a722-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="2a722-116">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="2a722-116">Return values</span></span>

 <span data-ttu-id="2a722-117">**true**</span><span class="sxs-lookup"><span data-stu-id="2a722-117">**true**</span></span>
  
- <span data-ttu-id="2a722-118">La mise en cache est activée.</span><span class="sxs-lookup"><span data-stu-id="2a722-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="2a722-119">**false**</span><span class="sxs-lookup"><span data-stu-id="2a722-119">**false**</span></span>
  
- <span data-ttu-id="2a722-120">La mise en cache est désactivée.</span><span class="sxs-lookup"><span data-stu-id="2a722-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2a722-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a722-121">See also</span></span>



[<span data-ttu-id="2a722-122">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="2a722-122">GetDefCachedMode</span></span>](getdefcachedmode.md)

