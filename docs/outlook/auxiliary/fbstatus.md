---
title: FBStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f2d6a11e-847d-6bbe-cd77-e78ee961cb12
description: Une éumération pour l’état de libre/occupé des blocs de libre/occupé.
ms.openlocfilehash: 2a08ef142f9baddd453166c0ebcb989e69a51ceb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424090"
---
# <a name="fbstatus"></a><span data-ttu-id="fd425-103">FBStatus</span><span class="sxs-lookup"><span data-stu-id="fd425-103">FBStatus</span></span>

<span data-ttu-id="fd425-104">Une éumération pour l’état de libre/occupé des blocs de libre/occupé.</span><span class="sxs-lookup"><span data-stu-id="fd425-104">An enumeration for the free/busy status of free/busy blocks.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fd425-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="fd425-105">Quick info</span></span>

```cpp
enum  
    { 
      fbFree      = 0, 
      fbTentative = fbFree + 1, 
      fbBusy      = fbTentative + 1, 
      fbOutOfOffice = fbBusy + 1 
    }

```

## <a name="remarks"></a><span data-ttu-id="fd425-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="fd425-106">Remarks</span></span>

<span data-ttu-id="fd425-107">L’état de libre/occupé d’un bloc de temps détermine la façon dont il s’affiche dans un calendrier : **Libre,** **Occupé,** **Provisoire** ou **Hors** Office .</span><span class="sxs-lookup"><span data-stu-id="fd425-107">The free/busy status of a block of time determines how it is displayed on a calendar: **Free**, **Busy**, **Tentative**, or **Out of Office**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fd425-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd425-108">See also</span></span>

- [<span data-ttu-id="fd425-109">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="fd425-109">FBBlock_1</span></span>](fbblock_1.md)
- [<span data-ttu-id="fd425-110">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="fd425-110">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)

