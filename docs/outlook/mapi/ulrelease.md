---
title: UlRelease
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlRelease
api_type:
- COM
ms.assetid: 95db96ef-f95f-41da-b216-f717c23bffd2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 288e34a159db48b1344524b87f02b045259f1565
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415844"
---
# <a name="ulrelease"></a><span data-ttu-id="b6b01-103">UlRelease</span><span class="sxs-lookup"><span data-stu-id="b6b01-103">UlRelease</span></span>

  
  
<span data-ttu-id="b6b01-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6b01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6b01-105">Fournit une autre méthode pour appeler la méthode OLE **IUnknown::Release**.</span><span class="sxs-lookup"><span data-stu-id="b6b01-105">Provides an alternative way to invoke the OLE method **IUnknown::Release**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b6b01-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b6b01-106">Header file:</span></span>  <br/> |<span data-ttu-id="b6b01-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b6b01-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b6b01-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="b6b01-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b6b01-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b6b01-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b6b01-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="b6b01-110">Called by:</span></span>  <br/> |<span data-ttu-id="b6b01-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="b6b01-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="b6b01-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6b01-112">Parameters</span></span>

 <span data-ttu-id="b6b01-113">_sous-président_</span><span class="sxs-lookup"><span data-stu-id="b6b01-113">_punk_</span></span>
  
> <span data-ttu-id="b6b01-114">[in] Pointeur vers une interface dérivée de l’interface **IUnknown,** en d’autres termes toute interface MAPI.</span><span class="sxs-lookup"><span data-stu-id="b6b01-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b6b01-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b6b01-115">Return value</span></span>

<span data-ttu-id="b6b01-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b6b01-116">S_OK</span></span> 
  
> <span data-ttu-id="b6b01-117">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="b6b01-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="b6b01-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="b6b01-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="b6b01-119">Une erreur d’origine inattendue ou inconnue a empêché l’exécution de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b6b01-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b6b01-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="b6b01-120">Remarks</span></span>

<span data-ttu-id="b6b01-121">Le nombre de références est le nombre de pointeurs existants vers l’objet à libérer.</span><span class="sxs-lookup"><span data-stu-id="b6b01-121">The reference count is the number of existing pointers to the object to be released.</span></span> 
  
<span data-ttu-id="b6b01-122">Si le  _paramètre de contrôle_ est NULL, la fonction renvoie immédiatement sans appeler **IUnknown::Release**</span><span class="sxs-lookup"><span data-stu-id="b6b01-122">If the  _punk_ parameter is NULL, the function returns immediately without calling **IUnknown::Release**</span></span>
  
 <span data-ttu-id="b6b01-123">**UlRelease renvoie** la valeur renvoyée par la méthode **IUnknown::Release,** qui peut être égale au nombre de références de l’objet à libérer.</span><span class="sxs-lookup"><span data-stu-id="b6b01-123">**UlRelease** returns the value returned by the **IUnknown::Release** method, which can be equal to the reference count for the object to be released.</span></span> 
  
<span data-ttu-id="b6b01-124">Pour plus d’informations **sur IUnknown::Release,** voir [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span><span class="sxs-lookup"><span data-stu-id="b6b01-124">For more information about **IUnknown::Release**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

