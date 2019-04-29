---
title: ScInitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ScInitMapiUtil
api_type:
- HeaderDef
ms.assetid: d83b8ea8-a3b8-4038-a226-de1869c5d722
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 090a73ed908d2a647d00de27b93538a77766c258
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420590"
---
# <a name="scinitmapiutil"></a><span data-ttu-id="ca6ad-103">ScInitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="ca6ad-103">ScInitMapiUtil</span></span>

  
  
<span data-ttu-id="ca6ad-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca6ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca6ad-105">Remplace [MAPIInitialize](mapiinitialize.md) lorsque seules les fonctions utilitaires Select sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="ca6ad-105">Replaces [MAPIInitialize](mapiinitialize.md) when only select utility functions are being used.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca6ad-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="ca6ad-106">Header file:</span></span>  <br/> |<span data-ttu-id="ca6ad-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="ca6ad-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ca6ad-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="ca6ad-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ca6ad-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ca6ad-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ca6ad-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="ca6ad-110">Called by:</span></span>  <br/> |<span data-ttu-id="ca6ad-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="ca6ad-111">Client applications</span></span>  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ca6ad-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca6ad-112">Parameters</span></span>

 <span data-ttu-id="ca6ad-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ca6ad-113">_ulFlags_</span></span>
  
> <span data-ttu-id="ca6ad-114">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="ca6ad-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ca6ad-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ca6ad-115">Return value</span></span>

<span data-ttu-id="ca6ad-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca6ad-116">S_OK</span></span> 
  
> <span data-ttu-id="ca6ad-117">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="ca6ad-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ca6ad-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="ca6ad-118">Remarks</span></span>

<span data-ttu-id="ca6ad-119">Les fonctions **ScInitMapiUtil** et [DeinitMapiUtil](deinitmapiutil.md) coopèrent pour appeler et libérer des fonctions utilitaires Select, par opposition à [MAPIInitialize](mapiinitialize.md), qui appelle Core ainsi que des fonctions utilitaires.</span><span class="sxs-lookup"><span data-stu-id="ca6ad-119">The **ScInitMapiUtil** and [DeinitMapiUtil](deinitmapiutil.md) functions cooperate to call and release select utility functions, as opposed to [MAPIInitialize](mapiinitialize.md), which calls core as well as utility functions.</span></span> <span data-ttu-id="ca6ad-120">Lorsque **ScInitMapiUtil** appelle les fonctions utilitaires, il initialise également la mémoire nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ca6ad-120">When **ScInitMapiUtil** calls utility functions, it also initializes the necessary memory.</span></span> 
  
<span data-ttu-id="ca6ad-121">Lorsque l'utilisation des fonctions appelées par **ScInitMapiUtil** est terminée, **DeinitMapiUtil** doit être appelé explicitement pour les libérer.</span><span class="sxs-lookup"><span data-stu-id="ca6ad-121">When use of the functions that **ScInitMapiUtil** has called is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="ca6ad-122">En revanche, **MAPIInitialize** appelle implicitement **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="ca6ad-122">In contrast, **MAPIInitialize** implicitly calls **DeinitMapiUtil**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ca6ad-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca6ad-123">See also</span></span>



[<span data-ttu-id="ca6ad-124">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="ca6ad-124">MAPIUninitialize</span></span>](mapiuninitialize.md)

