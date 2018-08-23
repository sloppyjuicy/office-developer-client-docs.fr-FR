---
title: FtNegFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtNegFt
api_type:
- COM
ms.assetid: 639a408c-aed1-456b-9f75-9d6fb8dcb33b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 37dc92a40043657cb791359d543ef52c77dbd8ce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589237"
---
# <a name="ftnegft"></a><span data-ttu-id="9c83d-103">FtNegFt</span><span class="sxs-lookup"><span data-stu-id="9c83d-103">FtNegFt</span></span>

  
  
<span data-ttu-id="9c83d-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c83d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9c83d-105">Calcule des deux complément d’un nombre entier non signé 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9c83d-105">Computes the two's complement of an unsigned 64-bit integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c83d-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="9c83d-106">Header file:</span></span>  <br/> |<span data-ttu-id="9c83d-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9c83d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9c83d-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="9c83d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9c83d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9c83d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9c83d-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="9c83d-110">Called by:</span></span>  <br/> |<span data-ttu-id="9c83d-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="9c83d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a><span data-ttu-id="9c83d-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c83d-112">Parameters</span></span>

 <span data-ttu-id="9c83d-113">_FT_</span><span class="sxs-lookup"><span data-stu-id="9c83d-113">_ft_</span></span>
  
> <span data-ttu-id="9c83d-114">[in] Une structure [FILETIME](filetime.md) qui contient l’entier non signé de 64 bits pour lequel calculer les compléments des deux.</span><span class="sxs-lookup"><span data-stu-id="9c83d-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer for which to compute the two's complement.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9c83d-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="9c83d-115">Return value</span></span>

<span data-ttu-id="9c83d-116">La fonction **FtNegFt** renvoie une structure **FILETIME** qui contient des deux complément de l’entier.</span><span class="sxs-lookup"><span data-stu-id="9c83d-116">The **FtNegFt** function returns a **FILETIME** structure that contains the two's complement of the integer.</span></span> <span data-ttu-id="9c83d-117">Le paramètre d’entrée reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="9c83d-117">The input parameter remains unchanged.</span></span> 
  

