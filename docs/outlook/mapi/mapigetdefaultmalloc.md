---
title: MAPIGetDefaultMalloc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIGetDefaultMalloc
api_type:
- HeaderDef
ms.assetid: 148695dd-d886-4a06-9cfe-749059ae91ed
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: cb0630ba30f8d3d7ae38c165c5da60bbc12077c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592331"
---
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="5a2d9-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="5a2d9-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="5a2d9-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a2d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a2d9-105">Récupère l’adresse de la fonction d’allocation de mémoire par défaut MAPI.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5a2d9-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="5a2d9-106">Header file:</span></span>  <br/> |<span data-ttu-id="5a2d9-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5a2d9-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5a2d9-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="5a2d9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5a2d9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5a2d9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5a2d9-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="5a2d9-110">Called by:</span></span>  <br/> |<span data-ttu-id="5a2d9-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="5a2d9-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="5a2d9-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a2d9-112">Parameters</span></span>

<span data-ttu-id="5a2d9-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="5a2d9-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5a2d9-114">Return value</span></span>

<span data-ttu-id="5a2d9-115">La fonction **MAPIGetDefaultMalloc** renvoie un pointeur vers la fonction d’allocation de mémoire par défaut MAPI.</span><span class="sxs-lookup"><span data-stu-id="5a2d9-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

