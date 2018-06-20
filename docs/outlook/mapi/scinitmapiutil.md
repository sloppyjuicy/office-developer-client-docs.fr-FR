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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 771b466e58bf57a7eb4285c6f6ce94c815ec7288
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787070"
---
# <a name="scinitmapiutil"></a><span data-ttu-id="19583-103">ScInitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="19583-103">ScInitMapiUtil</span></span>

  
  
<span data-ttu-id="19583-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="19583-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="19583-105">Remplace les [exécuter MAPIInitialize](mapiinitialize.md) si uniquement les fonctions d’utilitaire select sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="19583-105">Replaces [MAPIInitialize](mapiinitialize.md) when only select utility functions are being used.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="19583-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="19583-106">Header file:</span></span>  <br/> |<span data-ttu-id="19583-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="19583-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="19583-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="19583-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="19583-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="19583-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="19583-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="19583-110">Called by:</span></span>  <br/> |<span data-ttu-id="19583-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="19583-111">Client applications</span></span>  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="19583-112">Param�tres</span><span class="sxs-lookup"><span data-stu-id="19583-112">Parameters</span></span>

 <span data-ttu-id="19583-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="19583-113">_ulFlags_</span></span>
  
> <span data-ttu-id="19583-114">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="19583-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="19583-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="19583-115">Return value</span></span>

<span data-ttu-id="19583-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="19583-116">S_OK</span></span> 
  
> <span data-ttu-id="19583-117">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="19583-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="19583-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="19583-118">Remarks</span></span>

<span data-ttu-id="19583-119">Les fonctions **ScInitMapiUtil** et [DeinitMapiUtil](deinitmapiutil.md) coopèrent pour appeler et sélectionnez utilitaire, par opposition à [exécuter MAPIInitialize](mapiinitialize.md)qui appelle principaux, ainsi que des utilitaires fonctions de publication.</span><span class="sxs-lookup"><span data-stu-id="19583-119">The **ScInitMapiUtil** and [DeinitMapiUtil](deinitmapiutil.md) functions cooperate to call and release select utility functions, as opposed to [MAPIInitialize](mapiinitialize.md), which calls core as well as utility functions.</span></span> <span data-ttu-id="19583-120">Lorsque **ScInitMapiUtil** appelle les fonctions utilitaires, il initialise également la mémoire nécessaire.</span><span class="sxs-lookup"><span data-stu-id="19583-120">When **ScInitMapiUtil** calls utility functions, it also initializes the necessary memory.</span></span> 
  
<span data-ttu-id="19583-121">Lors de l’utilisation des fonctions **ScInitMapiUtil** a appelée est terminée, **DeinitMapiUtil** doit être explicitement appelée pour libérer les.</span><span class="sxs-lookup"><span data-stu-id="19583-121">When use of the functions that **ScInitMapiUtil** has called is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="19583-122">En revanche, **exécuter MAPIInitialize** appelle implicitement **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="19583-122">In contrast, **MAPIInitialize** implicitly calls **DeinitMapiUtil**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="19583-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19583-123">See also</span></span>



[<span data-ttu-id="19583-124">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="19583-124">MAPIUninitialize</span></span>](mapiuninitialize.md)

