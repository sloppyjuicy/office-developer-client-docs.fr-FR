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
ms.openlocfilehash: a9654efc34280941cdbc727bce9912a0a39d0fb9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427345"
---
# <a name="deinitmapiutil"></a><span data-ttu-id="28634-103">DeinitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="28634-103">DeinitMapiUtil</span></span>

  
  
<span data-ttu-id="28634-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28634-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28634-105">Libère les fonctions utilitaires appelées explicitement par la [fonction ScInitMapiUtil](scinitmapiutil.md) ou implicitement par la [fonction MAPIInitialize.](mapiinitialize.md)</span><span class="sxs-lookup"><span data-stu-id="28634-105">Releases utility functions called explicitly by the [ScInitMapiUtil](scinitmapiutil.md) function or implicitly by the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="28634-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="28634-106">Header file:</span></span>  <br/> |<span data-ttu-id="28634-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="28634-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="28634-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="28634-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="28634-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="28634-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="28634-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="28634-110">Called by:</span></span>  <br/> |<span data-ttu-id="28634-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="28634-111">Client applications</span></span>  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a><span data-ttu-id="28634-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28634-112">Parameters</span></span>

<span data-ttu-id="28634-113">Aucun</span><span class="sxs-lookup"><span data-stu-id="28634-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="28634-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="28634-114">Return value</span></span>

<span data-ttu-id="28634-115">Aucun</span><span class="sxs-lookup"><span data-stu-id="28634-115">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="28634-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="28634-116">Remarks</span></span>

<span data-ttu-id="28634-117">Fonctions de publication de la fonction **DeinitMapiUtil** initialisées avec [ScInitMapiUtil](scinitmapiutil.md) ou [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="28634-117">The **DeinitMapiUtil** function release functions initialized with [ScInitMapiUtil](scinitmapiutil.md) or [MAPIInitialize](mapiinitialize.md).</span></span> 
  
<span data-ttu-id="28634-118">Lorsque l’utilisation des fonctions appelées par **ScInitMapiUtil** est terminée, **DeinitMapiUtil** doit être explicitement appelée pour les libérer.</span><span class="sxs-lookup"><span data-stu-id="28634-118">When use of the functions called by **ScInitMapiUtil** is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="28634-119">En revanche, [MAPIUninitialize](mapiuninitialize.md) appelle implicitement **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="28634-119">In contrast, [MAPIUninitialize](mapiuninitialize.md) implicitly calls **DeinitMapiUtil**.</span></span> 
  

