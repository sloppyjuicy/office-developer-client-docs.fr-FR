---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 27ec919d720e1089d6e102f20485d936c9dc9808
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406345"
---
# <a name="ftmuldw"></a><span data-ttu-id="c1de3-103">FtMulDw</span><span class="sxs-lookup"><span data-stu-id="c1de3-103">FtMulDw</span></span>

  
  
<span data-ttu-id="c1de3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1de3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1de3-105">Multiplie un nombre integer 64 bits non signé par un nombre integer 32 bits non signé.</span><span class="sxs-lookup"><span data-stu-id="c1de3-105">Multiplies an unsigned 64-bit integer by an unsigned 32-bit integer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c1de3-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="c1de3-106">Header file:</span></span>  <br/> |<span data-ttu-id="c1de3-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c1de3-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c1de3-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="c1de3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c1de3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c1de3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c1de3-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="c1de3-110">Called by:</span></span>  <br/> |<span data-ttu-id="c1de3-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="c1de3-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a><span data-ttu-id="c1de3-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1de3-112">Parameters</span></span>

 <span data-ttu-id="c1de3-113">_Multiplicateur_</span><span class="sxs-lookup"><span data-stu-id="c1de3-113">_Multiplier_</span></span>
  
> <span data-ttu-id="c1de3-114">[in] Mot double qui contient le multiplicateur d’nombres integer 32 bits non signé.</span><span class="sxs-lookup"><span data-stu-id="c1de3-114">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span> 
    
 <span data-ttu-id="c1de3-115">_Multiplicand_</span><span class="sxs-lookup"><span data-stu-id="c1de3-115">_Multiplicand_</span></span>
  
> <span data-ttu-id="c1de3-116">[in] Structure [FILETIME](filetime.md) qui contient l’integer 64 bits non signé à multiplier par la valeur dans le paramètre Multiplicateur. </span><span class="sxs-lookup"><span data-stu-id="c1de3-116">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c1de3-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c1de3-117">Return value</span></span>

<span data-ttu-id="c1de3-118">La **fonction FtMulDw** renvoie une structure **FILETIME** qui contient le produit des deux nombres entières.</span><span class="sxs-lookup"><span data-stu-id="c1de3-118">The **FtMulDw** function returns a **FILETIME** structure that contains the product of the two integers.</span></span> <span data-ttu-id="c1de3-119">Les deux paramètres d’entrée restent inchangés.</span><span class="sxs-lookup"><span data-stu-id="c1de3-119">The two input parameters remain unchanged.</span></span> 
  

