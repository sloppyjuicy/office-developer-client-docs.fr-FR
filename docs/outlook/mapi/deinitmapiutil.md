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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e84dbc0976f5c438a7e0b5fd7cddcbf1c0659f40
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574796"
---
# <a name="deinitmapiutil"></a><span data-ttu-id="32725-103">DeinitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="32725-103">DeinitMapiUtil</span></span>

  
  
<span data-ttu-id="32725-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32725-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32725-105">Fonctions utilitaire appelées explicitement par la fonction [ScInitMapiUtil](scinitmapiutil.md) ou implicitement par la fonction [exécuter MAPIInitialize](mapiinitialize.md) le relâche.</span><span class="sxs-lookup"><span data-stu-id="32725-105">Releases utility functions called explicitly by the [ScInitMapiUtil](scinitmapiutil.md) function or implicitly by the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="32725-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="32725-106">Header file:</span></span>  <br/> |<span data-ttu-id="32725-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="32725-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="32725-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="32725-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="32725-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="32725-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="32725-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="32725-110">Called by:</span></span>  <br/> |<span data-ttu-id="32725-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="32725-111">Client applications</span></span>  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a><span data-ttu-id="32725-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32725-112">Parameters</span></span>

<span data-ttu-id="32725-113">Aucune</span><span class="sxs-lookup"><span data-stu-id="32725-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="32725-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="32725-114">Return value</span></span>

<span data-ttu-id="32725-115">Aucune</span><span class="sxs-lookup"><span data-stu-id="32725-115">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="32725-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="32725-116">Remarks</span></span>

<span data-ttu-id="32725-117">La fonction **DeinitMapiUtil** release fonctions initialisées avec [ScInitMapiUtil](scinitmapiutil.md) ou [exécuter MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="32725-117">The **DeinitMapiUtil** function release functions initialized with [ScInitMapiUtil](scinitmapiutil.md) or [MAPIInitialize](mapiinitialize.md).</span></span> 
  
<span data-ttu-id="32725-118">Lors de l’utilisation des fonctions appelée par **ScInitMapiUtil** est terminée, **DeinitMapiUtil** doit être explicitement appelée pour libérer les.</span><span class="sxs-lookup"><span data-stu-id="32725-118">When use of the functions called by **ScInitMapiUtil** is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="32725-119">En revanche, [MAPIUninitialize](mapiuninitialize.md) appelle implicitement **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="32725-119">In contrast, [MAPIUninitialize](mapiuninitialize.md) implicitly calls **DeinitMapiUtil**.</span></span> 
  

