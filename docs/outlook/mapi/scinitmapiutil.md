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
ms.openlocfilehash: 090a73ed908d2a647d00de27b93538a77766c258
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351260"
---
# <a name="scinitmapiutil"></a><span data-ttu-id="96ad1-103">ScInitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="96ad1-103">ScInitMapiUtil</span></span>

  
  
<span data-ttu-id="96ad1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96ad1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96ad1-105">Remplace [MAPIInitialize](mapiinitialize.md) lorsque seules les fonctions utilitaires Select sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="96ad1-105">Replaces [MAPIInitialize](mapiinitialize.md) when only select utility functions are being used.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96ad1-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="96ad1-106">Header file:</span></span>  <br/> |<span data-ttu-id="96ad1-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="96ad1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="96ad1-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="96ad1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="96ad1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="96ad1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="96ad1-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="96ad1-110">Called by:</span></span>  <br/> |<span data-ttu-id="96ad1-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="96ad1-111">Client applications</span></span>  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="96ad1-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96ad1-112">Parameters</span></span>

 <span data-ttu-id="96ad1-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="96ad1-113">_ulFlags_</span></span>
  
> <span data-ttu-id="96ad1-114">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="96ad1-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="96ad1-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="96ad1-115">Return value</span></span>

<span data-ttu-id="96ad1-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="96ad1-116">S_OK</span></span> 
  
> <span data-ttu-id="96ad1-117">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="96ad1-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="96ad1-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="96ad1-118">Remarks</span></span>

<span data-ttu-id="96ad1-119">Les fonctions **ScInitMapiUtil** et [DeinitMapiUtil](deinitmapiutil.md) coopèrent pour appeler et libérer des fonctions utilitaires Select, par opposition à [MAPIInitialize](mapiinitialize.md), qui appelle Core ainsi que des fonctions utilitaires.</span><span class="sxs-lookup"><span data-stu-id="96ad1-119">The **ScInitMapiUtil** and [DeinitMapiUtil](deinitmapiutil.md) functions cooperate to call and release select utility functions, as opposed to [MAPIInitialize](mapiinitialize.md), which calls core as well as utility functions.</span></span> <span data-ttu-id="96ad1-120">Lorsque **ScInitMapiUtil** appelle les fonctions utilitaires, il initialise également la mémoire nécessaire.</span><span class="sxs-lookup"><span data-stu-id="96ad1-120">When **ScInitMapiUtil** calls utility functions, it also initializes the necessary memory.</span></span> 
  
<span data-ttu-id="96ad1-121">Lorsque l'utilisation des fonctions appelées par **ScInitMapiUtil** est terminée, **DeinitMapiUtil** doit être appelé explicitement pour les libérer.</span><span class="sxs-lookup"><span data-stu-id="96ad1-121">When use of the functions that **ScInitMapiUtil** has called is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="96ad1-122">En revanche, **MAPIInitialize** appelle implicitement **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="96ad1-122">In contrast, **MAPIInitialize** implicitly calls **DeinitMapiUtil**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="96ad1-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96ad1-123">See also</span></span>



[<span data-ttu-id="96ad1-124">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="96ad1-124">MAPIUninitialize</span></span>](mapiuninitialize.md)

