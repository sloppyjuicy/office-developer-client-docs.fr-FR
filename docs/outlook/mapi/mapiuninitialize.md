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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c1a78889ea98133af46089fdc93b0c1c4bb24226
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784792"
---
# <a name="mapiuninitialize"></a><span data-ttu-id="651bd-103">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="651bd-103">MAPIUninitialize</span></span>

  
  
<span data-ttu-id="651bd-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="651bd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="651bd-105">Décrémente le décompte de références, nettoie et supprime par instance globale des données pour la DLL MAPI.</span><span class="sxs-lookup"><span data-stu-id="651bd-105">Decrements the reference count, cleans up, and deletes per-instance global data for the MAPI DLL.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="651bd-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="651bd-106">Header file:</span></span>  <br/> |<span data-ttu-id="651bd-107">MAPIX.h</span><span class="sxs-lookup"><span data-stu-id="651bd-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="651bd-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="651bd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="651bd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="651bd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="651bd-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="651bd-110">Called by:</span></span>  <br/> |<span data-ttu-id="651bd-111">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="651bd-111">Client applications</span></span>  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a><span data-ttu-id="651bd-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="651bd-112">Parameters</span></span>

<span data-ttu-id="651bd-113">Aucune</span><span class="sxs-lookup"><span data-stu-id="651bd-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="651bd-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="651bd-114">Return value</span></span>

<span data-ttu-id="651bd-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="651bd-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="651bd-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="651bd-116">Remarks</span></span>

<span data-ttu-id="651bd-117">Une application cliente appelle la fonction **MAPIUninitialize** pour mettre fin à son interaction avec l’interface MAPI, commencé avec un appel à la fonction [exécuter MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="651bd-117">A client application calls the **MAPIUninitialize** function to end its interaction with MAPI, begun with a call to the [MAPIInitialize](mapiinitialize.md) function.</span></span> <span data-ttu-id="651bd-118">Après avoir appelé **MAPIUninitialize** , aucun autre appel MAPI ne peut être effectuées par le client.</span><span class="sxs-lookup"><span data-stu-id="651bd-118">After **MAPIUninitialize** is called, no other MAPI calls can be made by the client.</span></span> 
  
 <span data-ttu-id="651bd-119">**MAPIUninitialize** décrémente le nombre et la fonction **exécuter MAPIInitialize** correspondante incrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="651bd-119">**MAPIUninitialize** decrements the reference count, and the corresponding **MAPIInitialize** function increments the reference count.</span></span> <span data-ttu-id="651bd-120">Par conséquent, le nombre d’appels à une fonction doit correspondre au nombre d’appels à l’autre.</span><span class="sxs-lookup"><span data-stu-id="651bd-120">Thus, the number of calls to one function must equal the number of calls to the other.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="651bd-121">Impossible d’appeler **exécuter MAPIInitialize** ou **MAPIUninitialize** au sein d’une fonction Win32 **DllMain** ou toute autre fonction qui crée ou met fin à des threads.</span><span class="sxs-lookup"><span data-stu-id="651bd-121">You cannot call **MAPIInitialize** or **MAPIUninitialize** from within a Win32 **DllMain** function or any other function that creates or terminates threads.</span></span> <span data-ttu-id="651bd-122">Pour plus d’informations, voir [Utilisation des objets Thread-Safe](using-thread-safe-objects.md).</span><span class="sxs-lookup"><span data-stu-id="651bd-122">For more information, see [Using Thread-Safe Objects](using-thread-safe-objects.md).</span></span> 
  

