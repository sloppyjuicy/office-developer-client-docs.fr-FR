---
title: MAPIUninitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIUninitialize
api_type:
- HeaderDef
ms.assetid: 0f4e54dc-80e5-49a7-9703-0225d8133492
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f7339588bcc6815545e7341eafffe9cf001c1d76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408522"
---
# <a name="mapiuninitialize"></a><span data-ttu-id="b7b04-103">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="b7b04-103">MAPIUninitialize</span></span>

  
  
<span data-ttu-id="b7b04-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7b04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7b04-105">Décrémente le nombre de références, nettoie et supprime les données globales par instance pour la DLL MAPI.</span><span class="sxs-lookup"><span data-stu-id="b7b04-105">Decrements the reference count, cleans up, and deletes per-instance global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7b04-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b7b04-106">Header file:</span></span>  <br/> |<span data-ttu-id="b7b04-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="b7b04-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="b7b04-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="b7b04-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b7b04-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b7b04-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b7b04-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="b7b04-110">Called by:</span></span>  <br/> |<span data-ttu-id="b7b04-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="b7b04-111">Client applications</span></span>  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a><span data-ttu-id="b7b04-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7b04-112">Parameters</span></span>

<span data-ttu-id="b7b04-113">Aucun</span><span class="sxs-lookup"><span data-stu-id="b7b04-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="b7b04-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b7b04-114">Return value</span></span>

<span data-ttu-id="b7b04-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b7b04-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b7b04-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="b7b04-116">Remarks</span></span>

<span data-ttu-id="b7b04-117">Une application cliente appelle la **fonction MAPIUninitialize** pour mettre fin à son interaction avec MAPI, commencée par un appel à la fonction [MAPIInitialize.](mapiinitialize.md)</span><span class="sxs-lookup"><span data-stu-id="b7b04-117">A client application calls the **MAPIUninitialize** function to end its interaction with MAPI, begun with a call to the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="b7b04-118">Une **fois MAPIUninitialize** appelé, aucun autre appel MAPI ne peut être effectué par le client.</span><span class="sxs-lookup"><span data-stu-id="b7b04-118">After **MAPIUninitialize** is called, no other MAPI calls can be made by the client.</span></span> 
  
 <span data-ttu-id="b7b04-119">**MAPIUninitialize** décrémente le nombre de références et la fonction **MAPIInitialize** correspondante incrémente le nombre de références.</span><span class="sxs-lookup"><span data-stu-id="b7b04-119">**MAPIUninitialize** decrements the reference count, and the corresponding **MAPIInitialize** function increments the reference count.</span></span> <span data-ttu-id="b7b04-120">Par conséquent, le nombre d’appels à une fonction doit être égal au nombre d’appels à l’autre.</span><span class="sxs-lookup"><span data-stu-id="b7b04-120">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b7b04-121">Vous ne pouvez pas appeler **MAPIInitialize** ou **MAPIUninitialize** à partir d’une fonction **Win32 DllMain** ou toute autre fonction qui crée ou termine des threads.</span><span class="sxs-lookup"><span data-stu-id="b7b04-121">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="b7b04-122">Pour plus d’informations, [voir Using Thread-Safe Objects](using-thread-safe-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b7b04-122">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  

