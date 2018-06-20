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
ms.openlocfilehash: cb93d9ae4e6660c208d74e43bb26be4dbd55f4e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783435"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a><span data-ttu-id="01024-103">GetDefCachedModeDownloadPubFoldFavs</span><span class="sxs-lookup"><span data-stu-id="01024-103">GetDefCachedModeDownloadPubFoldFavs</span></span>

  
  
<span data-ttu-id="01024-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="01024-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="01024-105">Indique si le Mode Exchange mis en cache pour le dossier **Favoris des dossiers publics** est activé, et si cela est appliqué par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="01024-105">Indicates whether Cached Exchange Mode for the **Public Folder Favorites** folder is enabled, and whether this is enforced by policy.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="01024-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="01024-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01024-107">Exportés par :</span><span class="sxs-lookup"><span data-stu-id="01024-107">Exported by:</span></span>  <br/> |<span data-ttu-id="01024-108">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="01024-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="01024-109">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="01024-109">Called by:</span></span>  <br/> |<span data-ttu-id="01024-110">Client</span><span class="sxs-lookup"><span data-stu-id="01024-110">Client</span></span>  <br/> |
|<span data-ttu-id="01024-111">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="01024-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="01024-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="01024-112">Outlook</span></span>  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a><span data-ttu-id="01024-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01024-113">Parameters</span></span>

 <span data-ttu-id="01024-114">_pfPolicy_</span><span class="sxs-lookup"><span data-stu-id="01024-114">_pfPolicy_</span></span>
  
> <span data-ttu-id="01024-115">[out] **true** si la valeur de retour est appliquée par la stratégie, **false** si elle n’est pas.</span><span class="sxs-lookup"><span data-stu-id="01024-115">[out] **true** if the return value is enforced by policy, **false** if it is not.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="01024-116">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="01024-116">Return values</span></span>

 <span data-ttu-id="01024-117">**valeur True**</span><span class="sxs-lookup"><span data-stu-id="01024-117">**true**</span></span>
  
- <span data-ttu-id="01024-118">La mise en cache est activé.</span><span class="sxs-lookup"><span data-stu-id="01024-118">Caching is enabled.</span></span>
    
 <span data-ttu-id="01024-119">**False**</span><span class="sxs-lookup"><span data-stu-id="01024-119">**false**</span></span>
  
- <span data-ttu-id="01024-120">La mise en cache est désactivée.</span><span class="sxs-lookup"><span data-stu-id="01024-120">Caching is disabled.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="01024-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01024-121">See also</span></span>



[<span data-ttu-id="01024-122">GetDefCachedMode</span><span class="sxs-lookup"><span data-stu-id="01024-122">GetDefCachedMode</span></span>](getdefcachedmode.md)

