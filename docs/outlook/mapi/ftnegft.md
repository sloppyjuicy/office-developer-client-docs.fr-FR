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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: db208dad8697060e394b3ee037ea658cefbab669
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327971"
---
# <a name="ftnegft"></a><span data-ttu-id="5329e-103">FtNegFt</span><span class="sxs-lookup"><span data-stu-id="5329e-103">FtNegFt</span></span>

  
  
<span data-ttu-id="5329e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5329e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5329e-105">Calcule le complément à deux d'un entier non signé 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5329e-105">Computes the two's complement of an unsigned 64-bit integer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5329e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="5329e-106">Header file:</span></span>  <br/> |<span data-ttu-id="5329e-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="5329e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5329e-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="5329e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5329e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5329e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5329e-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="5329e-110">Called by:</span></span>  <br/> |<span data-ttu-id="5329e-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="5329e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a><span data-ttu-id="5329e-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5329e-112">Parameters</span></span>

 <span data-ttu-id="5329e-113">_pied_</span><span class="sxs-lookup"><span data-stu-id="5329e-113">_ft_</span></span>
  
> <span data-ttu-id="5329e-114">dans Une structure [fileTime](filetime.md) qui contient l'entier non signé 64 bits pour lequel calculer le complément à deux.</span><span class="sxs-lookup"><span data-stu-id="5329e-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer for which to compute the two's complement.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5329e-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5329e-115">Return value</span></span>

<span data-ttu-id="5329e-116">La fonction **FtNegFt** renvoie une structure **fileTime** qui contient le complément à deux de l'entier.</span><span class="sxs-lookup"><span data-stu-id="5329e-116">The **FtNegFt** function returns a **FILETIME** structure that contains the two's complement of the integer.</span></span> <span data-ttu-id="5329e-117">Le paramètre d'entrée reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="5329e-117">The input parameter remains unchanged.</span></span> 
  

