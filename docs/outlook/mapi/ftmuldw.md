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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 27ec919d720e1089d6e102f20485d936c9dc9808
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327999"
---
# <a name="ftmuldw"></a><span data-ttu-id="86dac-103">FtMulDw</span><span class="sxs-lookup"><span data-stu-id="86dac-103">FtMulDw</span></span>

  
  
<span data-ttu-id="86dac-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86dac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86dac-105">Multiplie un entier non signé 64 bits par un entier non signé 32 bits.</span><span class="sxs-lookup"><span data-stu-id="86dac-105">Multiplies an unsigned 64-bit integer by an unsigned 32-bit integer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="86dac-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="86dac-106">Header file:</span></span>  <br/> |<span data-ttu-id="86dac-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="86dac-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="86dac-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="86dac-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="86dac-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="86dac-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="86dac-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="86dac-110">Called by:</span></span>  <br/> |<span data-ttu-id="86dac-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="86dac-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a><span data-ttu-id="86dac-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86dac-112">Parameters</span></span>

 <span data-ttu-id="86dac-113">_Multiplicateur_</span><span class="sxs-lookup"><span data-stu-id="86dac-113">_Multiplier_</span></span>
  
> <span data-ttu-id="86dac-114">dans Un double mot qui contient le multiplicateur de nombres entiers non signés 32 bits.</span><span class="sxs-lookup"><span data-stu-id="86dac-114">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span> 
    
 <span data-ttu-id="86dac-115">_Multiplicand_</span><span class="sxs-lookup"><span data-stu-id="86dac-115">_Multiplicand_</span></span>
  
> <span data-ttu-id="86dac-116">dans Une structure [fileTime](filetime.md) qui contient l'entier non signé 64 bits à multiplier par la valeur dans le paramètre _multiplicateur_ .</span><span class="sxs-lookup"><span data-stu-id="86dac-116">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="86dac-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="86dac-117">Return value</span></span>

<span data-ttu-id="86dac-118">La fonction **FtMulDw** renvoie une structure **fileTime** qui contient le produit des deux entiers.</span><span class="sxs-lookup"><span data-stu-id="86dac-118">The **FtMulDw** function returns a **FILETIME** structure that contains the product of the two integers.</span></span> <span data-ttu-id="86dac-119">Les deux paramètres d'entrée restent inchangés.</span><span class="sxs-lookup"><span data-stu-id="86dac-119">The two input parameters remain unchanged.</span></span> 
  

