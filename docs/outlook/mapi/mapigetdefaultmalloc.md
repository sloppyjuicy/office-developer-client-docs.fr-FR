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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 635f22c97ed27889245becbebb990ab3995b70b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438203"
---
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="58ef9-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="58ef9-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="58ef9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58ef9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58ef9-105">Récupère l’adresse de la fonction d’allocation de mémoire MAPI par défaut.</span><span class="sxs-lookup"><span data-stu-id="58ef9-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="58ef9-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="58ef9-106">Header file:</span></span>  <br/> |<span data-ttu-id="58ef9-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="58ef9-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="58ef9-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="58ef9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="58ef9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="58ef9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="58ef9-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="58ef9-110">Called by:</span></span>  <br/> |<span data-ttu-id="58ef9-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="58ef9-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="58ef9-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58ef9-112">Parameters</span></span>

<span data-ttu-id="58ef9-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="58ef9-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="58ef9-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="58ef9-114">Return value</span></span>

<span data-ttu-id="58ef9-115">La **fonction MAPIGetDefaultMalloc** renvoie un pointeur vers la fonction d’allocation de mémoire MAPI par défaut.</span><span class="sxs-lookup"><span data-stu-id="58ef9-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

