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
ms.openlocfilehash: 46c37dbcf1aa3b0469281b8db99f210bda0918be
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582300"
---
# <a name="ulrelease"></a><span data-ttu-id="f82b5-103">UlRelease</span><span class="sxs-lookup"><span data-stu-id="f82b5-103">UlRelease</span></span>

  
  
<span data-ttu-id="f82b5-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f82b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f82b5-105">Permet également d’appeler la méthode OLE **IUnknown::Release**.</span><span class="sxs-lookup"><span data-stu-id="f82b5-105">Provides an alternative way to invoke the OLE method **IUnknown::Release**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f82b5-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="f82b5-106">Header file:</span></span>  <br/> |<span data-ttu-id="f82b5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f82b5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f82b5-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="f82b5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f82b5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f82b5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f82b5-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="f82b5-110">Called by:</span></span>  <br/> |<span data-ttu-id="f82b5-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="f82b5-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG UlRelease(
  LPVOID punk
);
```

## <a name="parameters"></a><span data-ttu-id="f82b5-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f82b5-112">Parameters</span></span>

 <span data-ttu-id="f82b5-113">_pUnk_</span><span class="sxs-lookup"><span data-stu-id="f82b5-113">_punk_</span></span>
  
> <span data-ttu-id="f82b5-114">[in] Pointeur vers une interface dérivé de l’interface **IUnknown** , en d’autres termes n’importe quelle interface MAPI.</span><span class="sxs-lookup"><span data-stu-id="f82b5-114">[in] Pointer to an interface derived from the **IUnknown** interface, in other words any MAPI interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f82b5-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f82b5-115">Return value</span></span>

<span data-ttu-id="f82b5-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="f82b5-116">S_OK</span></span> 
  
> <span data-ttu-id="f82b5-117">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="f82b5-117">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="f82b5-118">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="f82b5-118">MAPI_E_CALL_FAILED</span></span> 
  
> <span data-ttu-id="f82b5-119">Une erreur d’origine inattendu ou inconnu a empêché l’opération de se terminer.</span><span class="sxs-lookup"><span data-stu-id="f82b5-119">An error of unexpected or unknown origin prevented the operation from completing.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f82b5-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="f82b5-120">Remarks</span></span>

<span data-ttu-id="f82b5-121">Le décompte de références est le nombre de pointeurs existants à l’objet doit être publié.</span><span class="sxs-lookup"><span data-stu-id="f82b5-121">The reference count is the number of existing pointers to the object to be released.</span></span> 
  
<span data-ttu-id="f82b5-122">Si le paramètre _punk_ est NULL, la fonction retourne immédiatement sans appeler **IUnknown::Release**</span><span class="sxs-lookup"><span data-stu-id="f82b5-122">If the  _punk_ parameter is NULL, the function returns immediately without calling **IUnknown::Release**</span></span>
  
 <span data-ttu-id="f82b5-123">**UlRelease** renvoie la valeur renvoyée par la méthode **IUnknown::Release** , qui peut être égale au nombre de références de l’objet doit être publié.</span><span class="sxs-lookup"><span data-stu-id="f82b5-123">**UlRelease** returns the value returned by the **IUnknown::Release** method, which can be equal to the reference count for the object to be released.</span></span> 
  
<span data-ttu-id="f82b5-124">Pour plus d’informations sur **IUnknown::Release**, voir [implémentation de l’IUnknown Interface](implementing-the-iunknown-interface.md).</span><span class="sxs-lookup"><span data-stu-id="f82b5-124">For more information about **IUnknown::Release**, see [Implementing the IUnknown Interface](implementing-the-iunknown-interface.md).</span></span> 
  

