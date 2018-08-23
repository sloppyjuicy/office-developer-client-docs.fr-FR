---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ced6f2c6540e04a0bb4945ff98c4fda520322f03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581726"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a><span data-ttu-id="bee25-103">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="bee25-103">GetDefCachedModeDownloadPubFoldFavs</span></span>

  
  
<span data-ttu-id="bee25-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bee25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bee25-105">Indique si le Mode Exchange mis en cache pour le dossier **Favoris des dossiers publics** est activé, et si cela est appliqué par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="bee25-105">Indicates whether Cached Exchange Mode for the **Public Folder Favorites** folder is enabled, and whether this is enforced by policy.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="bee25-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="bee25-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bee25-107">Exportés par :</span><span class="sxs-lookup"><span data-stu-id="bee25-107">Exported by:</span></span>  <br/> |<span data-ttu-id="bee25-108">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="bee25-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="bee25-109">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="bee25-109">Called by:</span></span>  <br/> |<span data-ttu-id="bee25-110">Client</span><span class="sxs-lookup"><span data-stu-id="bee25-110">Client</span></span>  <br/> |
|<span data-ttu-id="bee25-111">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="bee25-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="bee25-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="bee25-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="bee25-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bee25-113">Parameters</span></span>

 <span data-ttu-id="bee25-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="bee25-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="bee25-115">[out] **true** si la valeur de retour est appliquée par la stratégie, **false** si elle n’est pas.</span><span class="sxs-lookup"><span data-stu-id="bee25-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="bee25-116">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="bee25-116">Return values</span></span>

 <span data-ttu-id="bee25-117">**valeur True**</span><span class="sxs-lookup"><span data-stu-id="bee25-117">**true**</span></span>
  
- <span data-ttu-id="bee25-118">La mise en cache est activé.</span><span class="sxs-lookup"><span data-stu-id="bee25-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="bee25-119">**False**</span><span class="sxs-lookup"><span data-stu-id="bee25-119">**false**</span></span>
  
- <span data-ttu-id="bee25-120">La mise en cache est désactivée.</span><span class="sxs-lookup"><span data-stu-id="bee25-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bee25-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bee25-121">See also</span></span>



[<span data-ttu-id="bee25-122">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="bee25-122">GetDefCachedMode</span></span>](getdefcachedmode.md)

