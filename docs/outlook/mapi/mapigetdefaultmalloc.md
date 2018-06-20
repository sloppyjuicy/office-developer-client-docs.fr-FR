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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b236b24c10a241dbdecc28bf2e04de5f69e989e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784736"
---
# <a name="mapigetdefaultmalloc"></a><span data-ttu-id="bed3a-103">MAPIGetDefaultMalloc</span><span class="sxs-lookup"><span data-stu-id="bed3a-103">MAPIGetDefaultMalloc</span></span>

  
  
<span data-ttu-id="bed3a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bed3a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bed3a-105">Récupère l’adresse de la fonction d’allocation de mémoire par défaut MAPI.</span><span class="sxs-lookup"><span data-stu-id="bed3a-105">Retrieves the address of the default MAPI memory allocation function.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bed3a-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="bed3a-106">Header file:</span></span>  <br/> |<span data-ttu-id="bed3a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="bed3a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="bed3a-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="bed3a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="bed3a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="bed3a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="bed3a-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="bed3a-110">Called by:</span></span>  <br/> |<span data-ttu-id="bed3a-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="bed3a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPMALLOC MAPIGetDefaultMalloc( );
```

## <a name="parameters"></a><span data-ttu-id="bed3a-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bed3a-112">Parameters</span></span>

<span data-ttu-id="bed3a-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="bed3a-113">None.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="bed3a-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bed3a-114">Return value</span></span>

<span data-ttu-id="bed3a-115">La fonction **MAPIGetDefaultMalloc** renvoie un pointeur vers la fonction d’allocation de mémoire par défaut MAPI.</span><span class="sxs-lookup"><span data-stu-id="bed3a-115">The **MAPIGetDefaultMalloc** function returns a pointer to the default MAPI memory allocation function.</span></span> 
  

