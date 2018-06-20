---
title: DeinitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeinitMapiUtil
api_type:
- HeaderDef
ms.assetid: e0b8dc9c-cc46-4d27-9497-7a55a0bfdff5
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ae6f7d7066638ef1b149d3e411443384d531184d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783128"
---
# <a name="deinitmapiutil"></a><span data-ttu-id="2a61e-103">DeinitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="2a61e-103">DeinitMapiUtil</span></span>

  
  
<span data-ttu-id="2a61e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2a61e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2a61e-105">Fonctions utilitaire appelées explicitement par la fonction [ScInitMapiUtil](scinitmapiutil.md) ou implicitement par la fonction [exécuter MAPIInitialize](mapiinitialize.md) le relâche.</span><span class="sxs-lookup"><span data-stu-id="2a61e-105">Releases utility functions called explicitly by the [ScInitMapiUtil](scinitmapiutil.md) function or implicitly by the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2a61e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="2a61e-106">Header file:</span></span>  <br/> |<span data-ttu-id="2a61e-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2a61e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2a61e-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="2a61e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2a61e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2a61e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2a61e-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="2a61e-110">Called by:</span></span>  <br/> |<span data-ttu-id="2a61e-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="2a61e-111">Client applications</span></span>  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a><span data-ttu-id="2a61e-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a61e-112">Parameters</span></span>

<span data-ttu-id="2a61e-113">Aucune</span><span class="sxs-lookup"><span data-stu-id="2a61e-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="2a61e-114">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="2a61e-114">Return value</span></span>

<span data-ttu-id="2a61e-115">Aucune</span><span class="sxs-lookup"><span data-stu-id="2a61e-115">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2a61e-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="2a61e-116">Remarks</span></span>

<span data-ttu-id="2a61e-117">La fonction **DeinitMapiUtil** release fonctions initialisées avec [ScInitMapiUtil](scinitmapiutil.md) ou [exécuter MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="2a61e-117">The **DeinitMapiUtil** function release functions initialized with [ScInitMapiUtil](scinitmapiutil.md) or [MAPIInitialize](mapiinitialize.md).</span></span> 
  
<span data-ttu-id="2a61e-118">Lors de l’utilisation des fonctions appelée par **ScInitMapiUtil** est terminée, **DeinitMapiUtil** doit être explicitement appelée pour libérer les.</span><span class="sxs-lookup"><span data-stu-id="2a61e-118">When use of the functions called by **ScInitMapiUtil** is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="2a61e-119">En revanche, [MAPIUninitialize](mapiuninitialize.md) appelle implicitement **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="2a61e-119">In contrast, [MAPIUninitialize](mapiuninitialize.md) implicitly calls **DeinitMapiUtil**.</span></span> 
  

