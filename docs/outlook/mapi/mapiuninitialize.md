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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f95c86a137e7253f3445123c23f2dc0d76b6d87a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567390"
---
# <a name="mapiuninitialize"></a><span data-ttu-id="9611a-103">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="9611a-103">MAPIUninitialize</span></span>

  
  
<span data-ttu-id="9611a-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9611a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9611a-105">Décrémente le décompte de références, nettoie et supprime par instance globale des données pour la DLL MAPI.</span><span class="sxs-lookup"><span data-stu-id="9611a-105">Decrements the reference count, cleans up, and deletes per-instance global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9611a-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="9611a-106">Header file:</span></span>  <br/> |<span data-ttu-id="9611a-107">MAPIX.h</span><span class="sxs-lookup"><span data-stu-id="9611a-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="9611a-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="9611a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9611a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9611a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9611a-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="9611a-110">Called by:</span></span>  <br/> |<span data-ttu-id="9611a-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="9611a-111">Client applications</span></span>  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a><span data-ttu-id="9611a-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9611a-112">Parameters</span></span>

<span data-ttu-id="9611a-113">Aucune</span><span class="sxs-lookup"><span data-stu-id="9611a-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="9611a-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9611a-114">Return value</span></span>

<span data-ttu-id="9611a-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9611a-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9611a-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="9611a-116">Remarks</span></span>

<span data-ttu-id="9611a-117">Une application cliente appelle la fonction **MAPIUninitialize** pour mettre fin à son interaction avec l’interface MAPI, commencé avec un appel à la fonction [exécuter MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="9611a-117">A client application calls the **MAPIUninitialize** function to end its interaction with MAPI, begun with a call to the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="9611a-118">Après avoir appelé **MAPIUninitialize** , aucun autre appel MAPI ne peut être effectuées par le client.</span><span class="sxs-lookup"><span data-stu-id="9611a-118">After **MAPIUninitialize** is called, no other MAPI calls can be made by the client.</span></span> 
  
 <span data-ttu-id="9611a-119">**MAPIUninitialize** décrémente le nombre et la fonction **exécuter MAPIInitialize** correspondante incrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="9611a-119">**MAPIUninitialize** decrements the reference count, and the corresponding **MAPIInitialize** function increments the reference count.</span></span> <span data-ttu-id="9611a-120">Par conséquent, le nombre d’appels à une fonction doit correspondre au nombre d’appels à l’autre.</span><span class="sxs-lookup"><span data-stu-id="9611a-120">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9611a-121">Impossible d’appeler **exécuter MAPIInitialize** ou **MAPIUninitialize** au sein d’une fonction Win32 **DllMain** ou toute autre fonction qui crée ou met fin à des threads.</span><span class="sxs-lookup"><span data-stu-id="9611a-121">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="9611a-122">Pour plus d’informations, voir [Utilisation des objets Thread-Safe](using-thread-safe-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9611a-122">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  

